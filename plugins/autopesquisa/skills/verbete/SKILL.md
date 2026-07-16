---
name: verbete
description: "Estrutura e confor dos verbetes da Conscienciologia — o formato da Enciclopédia da Conscienciologia / Encyclossapiens (6 divisões: Conformática, Fatuística, Detalhismo, Perfilologia, Argumentologia, Acabativa) e o do Dicionário de Consciencioterapeuticologia da OIC (Conformática, Consciencioterapeuticologia, Holoprescriciologia). Use ao redigir, revisar ou checar a estrutura de um verbete, identificar seções faltantes, ou entender qual formato se aplica."
---

# Verbete

Um verbete é uma peça de estrutura fixa e linguagem regrada. A maior parte do trabalho de revisão consiste em **conferir estrutura e confor**, não em julgar conteúdo — e é aí que esta skill ajuda.

**Existem dois formatos em uso na comunidade, e eles não se misturam.** Antes de qualquer coisa, identifique qual está em jogo; aplicar o confor errado é o erro mais comum e o mais custoso.

| | **Enciclopédia da Conscienciologia / Encyclossapiens** | **Dicionário de Consciencioterapeuticologia** (OIC) |
|---|---|---|
| Status | **Formato principal** | O equivalente da OIC, no domínio da Consciencioterapia |
| Divisões | 6 fixas, ~70 Seções | 3 fixas, subseções variáveis |
| Linguagem | **Denotativa** — frases nominais, sem verbo | **Prosa** — frases verbais completas |
| Fatuística | Divisão II | **Não existe** |
| Marcador YAML usual | `tipo: verbete` | `tipo: verbete-oic` |

Na dúvida, olhe a linguagem: se as seções são listas de expressões com artigo separadas por ponto e vírgula, é Encyclossapiens; se são parágrafos com sujeito e predicado, é OIC.

Estrutura completa das duas, com todas as Seções: `references/estrutura.md`.

## Formato Encyclossapiens

Cabeçalho: `Título: Especialidade; Categoria`, onde a Categoria é **Homeostático**, **Neutro** ou **Nosográfico**. A categoria governa a carga dos itens ao longo do verbete — um verbete Nosográfico tem itens predominantemente negativos, e isso é correto, não defeito.

As 6 divisões, na ordem:

1. **Conformática** — Definologia, Tematologia, Etimologia, Sinonimologia, Cognatologia, Neologia, Antonimologia, Estrangeirismologia, Atributologia, Megapensenologia, Coloquiologia, Citaciologia.
2. **Fatuística** — Pensenologia, Fatologia, Parafatologia. Todas fixas.
3. **Detalhismo** — a maior divisão: Sinergismologia, Principiologia, Codigologia, Teoriologia, Tecnologia, Voluntariologia, Laboratoriologia, Colegiologia, Efeitologia, Neossinapsologia, Ciclologia, Enumerologia, Binomiologia, Interaciologia, Crescendologia, Trinomiologia, Polinomiologia, Antagonismologia, Paradoxologia, Politicologia, Legislogia, Filiologia, Fobiologia, Sindromologia, Maniologia, Mitologia, Holotecologia, Interdisciplinologia.
4. **Perfilologia** — Elencologia, Masculinologia, Femininologia, Hominologia.
5. **Argumentologia** — Exemplologia, Culturologia, Taxologia, Caracterologia, Tipologia, Terapeuticologia, Tabelologia.
6. **Acabativa** — Remissiologia, Frase Enfática, Questionologia, Filmografia Específica, Bibliografia Específica.

**O confor que atravessa o verbete inteiro:** os itens das Seções são **frases nominais ou simples denominações, sem verbo**. Lista separada por ponto e vírgula, **cada item precedido de artigo**, ponto final em negrito.

```
Fatologia: o megaenfoque; o enfoque-chave; a logística do enfoque técnico.
```

Frases verbais existem em raríssimas exceções na Enciclopédia, e o Manual manda o neoverbetógrafo evitá-las. **Ao revisar, frase verbal numa Seção denotativa é achado — reporte.**

Outras regras de confor recorrentes:

- **Título factual como primeiro item** da Seção, quando couber ao tema.
- Natureza sintética e denotativa; sequenciamento lógico dos itens.
- Siglas entre parênteses: *o estado vibracional (EV)*.
- Conta-se **máximo** numa Seção quando a listagem ocupa ao menos 20 linhas.
- **Pensenologia** tem composição própria: abre com *o holopensene pessoal do(a)* + a especificidade do tema, e pareia tipicamente substantivo plural com característico singular — *os cosmopensenes; a cosmopensenidade*.

Para compor a Divisão II a partir de registros de autopesquisa, use a skill `fatuistica` — ela cobre a nominalização dos registros e o confor das três Seções.

## Formato do Dicionário de Consciencioterapeuticologia (OIC)

Os verbetes do **Dicionário de Consciencioterapeuticologia**, da Organização Internacional de Consciencioterapia (OIC), são o equivalente da OIC aos verbetes da Encyclossapiens — mesmo papel, estrutura e linguagem próprias. Três divisões:

1. **Conformática** — Definologia, Sinonimologia, Neologia Multilíngue (com as formas em alemão, inglês, espanhol e francês).
2. **Consciencioterapeuticologia** — o corpo do verbete. As subseções **variam por verbete**, escolhidas de um repertório: Parafisiologia, Experimentologia, Objetivologia, Parassemiologia, Paraterapeuticologia, Paraclinicologia, Procedimentologia, Indicaciologia, Discernimentologia, Parafisiopatologia, Taxologia, Evitaciologia, Paraetiologia, Paratecnologia, Parapatologia, entre outras. **Não cobre ausência de subseção como se fosse lacuna** — aqui a variação é a regra.
3. **Holoprescriciologia** — Remissiologia (lista numerada de verbetes correlatos, cada um com sua especialidade entre parênteses) e Bibliografia Específica.

**A linguagem é prosa, não enumeração denotativa.** Cada subseção é um parágrafo com frases verbais completas. Não aplique aqui o confor da Encyclossapiens: nominalizar um verbete da OIC é estragá-lo.

## Revisar

Ao revisar, trabalhe nesta ordem e reporte achados sem reescrever por conta própria:

1. **Formato** — Encyclossapiens ou OIC? Todo o resto depende disso.
2. **Estrutura** — Seções fixas ausentes ou fora de ordem. Confira contra `references/estrutura.md`.
3. **Confor** — no Encyclossapiens: frases verbais onde deveria haver nominais; itens sem artigo; separador que não é ponto e vírgula; sigla sem parênteses.
4. **Coerência de categoria** — a carga dos itens condiz com Homeostático / Neutro / Nosográfico?
5. **Conteúdo** — só então, e com parcimônia.

Distinga sempre **erro de confor** (objetivo, verificável contra a regra) de **sugestão de conteúdo** (opinião sua). Marque cada achado como um ou outro. O verbetógrafo decide o conteúdo; a regra decide o confor.

## Limites

A referência normativa do formato Encyclossapiens é o *Manual de Verbetografia da Enciclopédia da Conscienciologia* (Rosa Nader, org.; Editares, 2012). Esta skill descreve a **estrutura**; para a doutrina, os exemplos comentados e os verbetes-chave, consulte o Manual — não o reproduza.

Esta skill não é fonte doutrinária de Conscienciologia. Em questão conceitual, remeta às obras e à comunidade em vez de improvisar definição. Verbete é gênero de autoria: a redação é do verbetógrafo, e o papel aqui é de apoio ao método e ao confor.
