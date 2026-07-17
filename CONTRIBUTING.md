# Como contribuir

**Não é preciso saber programar.** Uma skill é um arquivo de texto que ensina a IA a fazer uma coisa bem. Quem entende de autopesquisa, verbetografia ou de um método conscienciológico já tem o que é mais difícil — o conhecimento. O resto é escrever.

## Três formas de contribuir, da mais fácil para a mais difícil

### 1. Um adaptador para o seu formato de captura

**A contribuição mais útil hoje.** As skills sabem ler Obsidian com YAML porque alguém documentou esse formato. Se você registra em planilha, Notion, Evernote, caderno digitalizado ou qualquer outra coisa, documente e todos passam a ler.

Copie [`obsidian-yaml.md`](plugins/autopesquisa/skills/fatuistica/references/adaptadores/obsidian-yaml.md) para um arquivo novo na mesma pasta e adapte. Um bom adaptador responde:

- **Como reconhecer** este formato?
- **O mapeamento** — o que vira `pensene`, `fato`, `parafato`? E data, pessoas, lugar, avaliação cosmoética?
- **Exemplos reais** — dois ou três, de verdade, não inventados. É a parte que mais ajuda.
- **Armadilhas** — o que costuma faltar ou confundir.

Anonimize seus exemplos se forem pessoais.

### 2. Melhorar uma skill existente

Se a `fatuistica` classificou mal um registro seu, ou a `verbete` deixou passar um erro de confor, isso é um bug — e o relato já é contribuição. Abra uma issue com o caso concreto: o que você deu, o que ela respondeu, o que deveria ter respondido.

Melhor ainda: corrija o `SKILL.md` e explique no PR **por que** a regra nova está certa, citando a fonte.

### 3. Uma skill nova

Tem um método de autopesquisa que você pratica e sabe explicar? Sonhos, projeções, tenepes, sinalética, conscienciograma, CPC, consolidação semanal. Abra uma issue antes de escrever — vale conversar sobre o escopo primeiro.

## O que faz uma skill boa

- **Uma responsabilidade.** Skill que faz tudo não é usada para nada.
- **A `description` é o que a faz existir.** É por ela que a IA decide carregar a skill. Escreva com as palavras que uma pessoa realmente usaria ao pedir aquilo — não com o nome técnico que só você usa.
- **Instrução permanente, não roteiro.** O conteúdo entra na conversa de uma vez e fica. Escreva "ao analisar X, faça Y", não "passo 1, passo 2".
- **Enxuta.** Mire 1.500–2.000 palavras no `SKILL.md`. O que for consulta ocasional vai para `references/`, que só carrega quando precisa.
- **Concreta.** Exemplo real vale mais que parágrafo de teoria.

## Regras do domínio

Estas valem para tudo neste repositório, e não são negociáveis:

1. **Não somos fonte doutrinária.** Em questão conceitual, remeta às obras e à comunidade. Skill não inventa definição de Conscienciologia.
2. **Referenciar, nunca copiar — salvo obras disponibilizadas publicamente.** O *Manual de Verbetografia*, a *Enciclopédia*, o *Dicionário de Argumentos* e os verbetes da OIC são obras protegidas: descreva estrutura e método, cite a fonte, e não reproduza o texto. **Exceção:** para livros que o autor ou a editora disponibilizou publicamente (leitura livre e autorizada), é permitido extrair e sistematizar o conteúdo — frameworks, taxologias, técnicas — como base de conhecimento numa skill, sempre citando a fonte de forma clara. É o caso da skill `tornieri-sinaletica` e de outras skills de livros abertos. Na dúvida sobre o status de uma obra, trate-a como protegida.
3. **A avaliação cosmoética é do pesquisador.** Nenhuma skill atribui `/ok` ou `/no` por conta própria. Julgar a cosmoética alheia não é o nosso papel.
4. **Autopesquisa não é terapia.** Autoconsciencioterapia tem propósito e método próprios e está fora do escopo. Skill que se aproximar disso deve dizer que é outro campo.
5. **Os dois formatos de verbete não se misturam.** Encyclossapiens é denotativo; OIC é prosa. Aplicar o confor de um no outro estraga o verbete.
6. **Skill de livro sempre informa onde adquirir a obra.** Toda skill derivada de um livro deve trazer, no `SKILL.md`, o URL oficial onde o livro pode ser adquirido ou baixado, e orientar o agente a compartilhá-lo quando o usuário quiser aprofundar, conferir o original ou obter a obra. A skill é ponteiro para o livro, não substituto: recomende sempre a leitura do original. Exemplo: a `tornieri-sinaletica` aponta para <https://editares.org/mapeamento-da-sinaletica/>.

## Testar antes de abrir o PR

```bash
git clone https://github.com/conscienciologia/autopesquisa-skill
cd autopesquisa-skill
claude plugin validate .
claude --plugin-dir ./plugins/autopesquisa
```

Dentro do Claude Code, `/help` mostra se sua skill apareceu. Depois **use-a nos seus próprios registros** — é o único teste que importa. Se ela não disser nada que você já não soubesse, ainda não está pronta.

## Abrir o PR

Descreva o que muda e **em qual caso real você testou**. Se for adaptador, diga com quantos registros e de que fonte.

Dúvida sobre o que fazer? Abra uma issue e pergunte. Perguntar já é participar.
