# Como lançar uma versão (release)

Guia para o mantenedor. Contribuidores não precisam disto — basta registrar a mudança em **[Não lançado]** no [CHANGELOG.md](CHANGELOG.md) (veja [CONTRIBUTING.md](CONTRIBUTING.md)).

## Padrão de versão

As releases usam data e hora do lançamento no formato:

```
yyyy.mm.dd.HHMM
```

Exemplo: um lançamento em 16/07/2026 às 14h32 → **`2026.07.16.1432`**.

- Vale para a **tag git**, o **título da release** no GitHub e o campo **`version`** dos dois manifestos (`marketplace.json` e `plugin.json`) — que devem ficar **iguais**.
- As versões `0.1.0` e `0.2.0` são anteriores a esta convenção e permanecem como estão.

## Passo a passo

Defina a versão uma vez e reutilize:

```bash
VERSION=$(date +%Y.%m.%d.%H%M)   # ex.: 2026.07.16.1432
echo "$VERSION"
```

**1. Fechar o CHANGELOG.** Mova o conteúdo de `## [Não lançado]` para uma nova seção `## [$VERSION] — yyyy-mm-dd`, deixando `[Não lançado]` vazia (_Nada ainda._). Atualize os links de comparação no rodapé do arquivo.

**2. Atualizar a versão nos dois manifestos** (têm de ser idênticos):

```bash
sed -i "s/\"version\": \"[^\"]*\"/\"version\": \"$VERSION\"/" .claude-plugin/marketplace.json
sed -i "s/\"version\": \"[^\"]*\"/\"version\": \"$VERSION\"/" plugins/autopesquisa/.claude-plugin/plugin.json
```

**3. Validar:**

```bash
claude plugin validate .
```

Deve passar sem warnings de versão (os dois manifestos batem).

**4. Commitar** (use o e-mail do mantenedor do projeto):

```bash
git add -A
git commit -m "Release $VERSION"
git push origin main
```

**5. Criar a tag e a release** com as notas da versão:

```bash
git tag "$VERSION" && git push origin "$VERSION"

gh release create "$VERSION" \
  --repo conscienciologia/autopesquisa-skill \
  --title "$VERSION" \
  --notes-file release-notes.md
```

Escreva `release-notes.md` a partir da seção correspondente do CHANGELOG.

## Modelo de notas de release (`release-notes.md`)

```markdown
## Novidades

### Adicionado
- ...

### Alterado
- ...

### Corrigido
- ...

## Como atualizar

Marketplaces de terceiros não atualizam sozinhos. Rode:

    /plugin marketplace update conscienciologia

E reinicie a sessão do Claude Code. Atualizar é sempre seguro.
```

Omita as subseções (_Adicionado_/_Alterado_/_Corrigido_) que não tiverem itens.
