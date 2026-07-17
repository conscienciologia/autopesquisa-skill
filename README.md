# Skills de Autopesquisa Conscienciológica

Skills de IA para autopesquisa — **conhecer-se** a partir dos próprios registros.

Quem faz autopesquisa acumula anos de registros: pensenes, fatos, parafatos, sonhos, tenepes. Esse material quase sempre fica parado, porque relê-lo dá trabalho e a memória é seletiva e complacente. Estas skills ensinam um agente de IA a trabalhar com esses registros do jeito certo — respeitando o método, o vocabulário e o confor da Conscienciologia.

## Instalação

Dentro do [Claude Code](https://claude.com/claude-code), dois comandos:

```
/plugin marketplace add conscienciologia/autopesquisa-skill
/plugin install autopesquisa@conscienciologia
```

Pronto. Depois é só conversar:

```
/autopesquisa:fatuistica
```

Ou simplesmente pedir em linguagem natural — *"registra esse pensene"*, *"quais padrões aparecem nos meus registros dos últimos 3 meses?"* — que o Claude carrega a skill sozinho.

Para atualizar (marketplaces de terceiros não atualizam automaticamente):

```
/plugin marketplace update conscienciologia
```

## O que vem junto

| Skill | Para quê |
|---|---|
| **`fatuistica`** | Registrar pensenes, fatos e parafatos; analisar a série acumulada em busca de recorrências, concentrações e padrões; compor a Divisão II de verbetes. |
| **`verbete`** | Estrutura e confor dos verbetes — o formato da Enciclopédia da Conscienciologia / Encyclossapiens e o do Dicionário de Consciencioterapeuticologia (OIC). Redigir, revisar, checar estrutura. |
| **`tornieri-sinaletica`** | Base de conhecimento do livro *Mapeamento da Sinalética Energética Parapsíquica* ([Sandra Tornieri, 2018](https://editares.org/mapeamento-da-sinaletica/)): taxologia dos 44 sinais, protocolo de mapeamento, técnicas e frameworks da Sinaleticologia. 56 capítulos sob demanda. |

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
