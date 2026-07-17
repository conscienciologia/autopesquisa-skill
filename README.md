# Skills de Autopesquisa Conscienciológica

Skills de IA para autopesquisa — **conhecer-se** a partir dos próprios registros.

Quem faz autopesquisa acumula anos de registros: pensenes, fatos, parafatos, sonhos, tenepes. Esse material quase sempre fica parado, porque relê-lo dá trabalho e a memória é seletiva e complacente. Estas skills ensinam um agente de IA a trabalhar com esses registros do jeito certo — respeitando o método, o vocabulário e o confor da Conscienciologia.

## Instalação

Dentro do [Claude Code](https://claude.com/claude-code), a instalação tem **dois passos distintos**:

**1. Adicionar o marketplace.** Registra este repositório como uma *fonte* de plugins no seu Claude Code. Ainda não instala nada — só ensina o Claude onde encontrar o plugin.

```
/plugin marketplace add conscienciologia/autopesquisa-skill
```

**2. Instalar o plugin.** Baixa e ativa o plugin `autopesquisa` (com todas as suas skills) a partir do marketplace que você acabou de adicionar. A sintaxe é `plugin@marketplace`.

```
/plugin install autopesquisa@conscienciologia
```

Feito isso, **reinicie a sessão** do Claude Code e as skills estão disponíveis.

### Atualizar (é manual)

Marketplaces de terceiros **não se atualizam sozinhos**. Sempre que novas skills ou conteúdos são publicados (por exemplo, a versão `0.2.0`, que adicionou a `tornieri-sinaletica`), **cada usuário precisa puxar a atualização manualmente** — não há aviso nem push automático.

**1. Atualizar o marketplace** (puxa as novidades do repositório):

```
/plugin marketplace update conscienciologia
```

**2. Reiniciar a sessão** do Claude Code para carregar as skills novas.

Se, em algum ambiente, o plugin não refletir a nova versão só com o passo 1, reforce com:

```
/plugin update autopesquisa@conscienciologia
```

**Pode atualizar sem medo.** Atualizar é sempre seguro — não é preciso consultar nada antes. O [**CHANGELOG.md**](CHANGELOG.md) e as [**releases do GitHub**](https://github.com/conscienciologia/autopesquisa-skill/releases) existem apenas para comunicar o progresso: o que cada versão trouxe de skills novas, conteúdos e correções. Dê uma olhada se tiver curiosidade sobre as novidades.

## O que vem junto

| Skill | Para quê |
|---|---|
| **`fatuistica`** | Registrar pensenes, fatos e parafatos; analisar a série acumulada em busca de recorrências, concentrações e padrões; compor a Divisão II de verbetes. |
| **`verbete`** | Estrutura e confor dos verbetes — o formato da Enciclopédia da Conscienciologia / Encyclossapiens e o do Dicionário de Consciencioterapeuticologia (OIC). Redigir, revisar, checar estrutura. |
| **`tornieri-sinaletica`** | Base de conhecimento do livro *Mapeamento da Sinalética Energética Parapsíquica* ([Sandra Tornieri, 2018](https://editares.org/mapeamento-da-sinaletica/)): taxologia dos 44 sinais, protocolo de mapeamento, técnicas e frameworks da Sinaleticologia. 56 capítulos sob demanda. |

## Como usar cada skill

Você aciona uma skill de duas formas: pelo **comando** (`/autopesquisa:<skill>`) ou simplesmente **perguntando em linguagem natural** — o Claude reconhece o assunto e carrega a skill certa sozinho.

### Exemplo guiado: "Como posso mapear a minha sinalética?"

Basta digitar a pergunta:

```
Como posso mapear a minha sinalética?
```

O Claude carrega a `tornieri-sinaletica` e responde com o método do livro:

1. **Estabeleça seu padrão homeostático de referência** — como você se sente em equilíbrio, veículo a veículo (soma, energossoma, psicossoma, mentalsoma). É o "zero do termômetro".
2. **Aprenda a taxologia** — os 44 sinais organizados por veículo, para ter vocabulário ao registrar.
3. **Registre pelo protocolo de 15 variáveis** — data, hora, contexto, sinal, veículo, recorrência, decodificação, etc.
4. **Pratique as técnicas de mapeamento** (Seção IV) — comece pelo Estado Vibracional (EV), o acelerador universal.
5. **Avalie a recorrência** — só o que se repete no mesmo contexto vira sinalética confirmada.

E, seguindo a convenção do projeto, ele aponta para o livro original: <https://editares.org/mapeamento-da-sinaletica/> (PDF gratuito ou impresso).

### `tornieri-sinaletica`

Base de conhecimento do livro de Sandra Tornieri. Bom para identificar e interpretar sinais energéticos e parapsíquicos, aplicar o protocolo de mapeamento e estudar capítulos específicos.

```
/autopesquisa:tornieri-sinaletica
```

Exemplos em linguagem natural:
- *"o que pode significar um arrepio nas costas durante a tenepes?"*
- *"quais são as 44 sinaléticas da taxologia?"*
- *"como diferencio uma sinalética de amparo de uma de assédio?"*
- *"me mostra o capítulo do Estado Vibracional"* → carrega `ch45`

### `fatuistica`

Registra e analisa pensenes, fatos e parafatos, e compõe a Divisão II (Fatuística) de verbetes. Lê seus registros em Obsidian, planilha, Notion ou texto colado.

```
/autopesquisa:fatuistica
```

Exemplos em linguagem natural:
- *"registra esse pensene: [...]"*
- *"quais padrões aparecem nos meus registros dos últimos 3 meses?"*
- *"transforma estes registros na Fatuística de um verbete sobre autodisciplina"*

### `verbete`

Estrutura e confor dos verbetes da Conscienciologia (formato Encyclossapiens, 6 divisões; e o do Dicionário da OIC, 3 divisões). Bom para redigir, revisar e checar estrutura.

```
/autopesquisa:verbete
```

Exemplos em linguagem natural:
- *"quais seções faltam neste verbete?"*
- *"este verbete está no confor da Enciclopédia?"*
- *"qual formato devo usar: Encyclossapiens ou OIC?"*

## Funciona com os seus registros, no seu formato

Cada pesquisador captura no seu meio: Obsidian, planilha, Notion, caderno. As skills leem o formato que você já usa — hoje há adaptador pronto para **Obsidian com frontmatter YAML**, e para os demais formatos o agente infere o mapeamento a partir dos seus próprios dados e confirma com você antes de analisar.

Se você usa um formato ainda não documentado, [escrever o adaptador](CONTRIBUTING.md) é a melhor forma de contribuir — e é markdown, não código.

## O que estas skills não são

Não são fonte doutrinária de Conscienciologia. Em questão conceitual, elas remetem às obras e à comunidade em vez de improvisar definição. A referência normativa do formato Encyclossapiens é o *Manual de Verbetografia da Enciclopédia da Conscienciologia* (Rosa Nader, org.; Editares, 2012).

Autopesquisa é **conhecer-se**. Não é terapia. Diagnóstico, enfrentamento e remissão de patologias e parapatologias conscienciais são objeto da **Autoconsciencioterapia**, campo com propósito e método próprios, fora do escopo deste projeto.

A avaliação cosmoética dos próprios registros é sempre do pesquisador. As skills não a atribuem.

## Contribuir

Contribuições da comunidade são o ponto deste projeto — veja [CONTRIBUTING.md](CONTRIBUTING.md). **Não é preciso saber programar:** skills são arquivos de texto.

## Licença

[MIT](LICENSE).
