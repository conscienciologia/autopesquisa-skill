# Adaptador: Obsidian com frontmatter YAML

Uma nota por registro, o campo do frontmatter nomeia a categoria. Formato de captura em uso real, verificado num vault com 274 registros. **Os exemplos abaixo são registros reais, publicados com autorização do pesquisador.**

## Como reconhecer

Arquivos `.md` cujo frontmatter tem **`pensene:`, `fato:` ou `parafato:`** como chave. Costumam viver numa pasta dedicada (`data/fatuistica/`, por exemplo) e ter nome no padrão Zettelkasten `YYYYMMDDHHMM.md`.

## Mapeamento

| Campo YAML | Destino |
|---|---|
| `pensene` | `pensene[]` |
| `fato` | `fato[]` |
| `parafato` | `parafato[]` |
| `date`, `horario` | data/hora do registro |
| `pessoas` | pessoas envolvidas |
| `lugar` | lugar |
| `tags` | categoria + área do CPC + avaliação cosmoética (ver abaixo) |
| `sinal` | **localização no corpo** onde a sinalética parapsíquica foi percebida |
| corpo da nota | contexto adicional; o wikilink `[[YYYY-MM-DD]]` aponta para a daily note |

**A mesma nota pode trazer mais de uma categoria** — é o caso mais informativo, porque o parafato ganha contexto pelo fato simultâneo. Ao normalizar, emita uma entrada por categoria, preservando o vínculo entre elas.

## Tags

Tag hierárquica com barras. O **último segmento é a avaliação cosmoética**: `/ok` (cosmoético), `/no` (anticosmoético), `/neutro` — conferida pelo pesquisador contra as cláusulas do próprio Código Pessoal de Cosmoética (CPC), no momento da captura.

- `pensene/no` — pensene anticosmoético
- `fato/ok` — fato cosmoético
- `cpc/work/no` — área do CPC (trabalho) + avaliação
- `cpc/familia/ok` — área do CPC (família) + avaliação
- `ecp2/261/pre` — contexto de curso; **não é avaliação**, embora o último segmento pareça uma

Áreas de CPC observadas: `posi`, `prof`, `work`, `dupla`, `soma`, `pri`, `familia`, `social`, `verbete`.

Nem toda tag termina em avaliação. Quando não terminar, **não infira** — o registro simplesmente não foi avaliado. Num corpus real, 59% dos registros não tinham avaliação; é o caso normal, não erro.

Preserve o segmento de área: é o que permite ver depois que um padrão se concentra numa cláusula do CPC e não em outra.

## Exemplos

**Pensene anticosmoético, com área do CPC e contexto no corpo:**

```yaml
---
tags:
  - pensene/no
  - cpc/work/no
pensene: Estou sendo irresponsável com o trabalho
---
[[2026-05-27]]

Eu estava utilizando o tempo do trabalho para realizar outras atividades. Anticosmoético
```

**O caso rico — fato e parafato no mesmo momento, com sinalética localizada:**

```yaml
---
date: 2026-05-28
horario: 11:59
tags:
  - fato/ok
  - parafato/ok
  - ecp2/261/pre
parafato: Ativação nas costas, ao organizar arquivos e saindo para comprar sopa
fato: Organizando atalhos e sai para comprar sopa
sinal:
  - costas
---
[[2026-05-28]]
```

Normalize para uma entrada em `fato[]` e uma em `parafato[]`, mantendo a ligação — é exatamente o material do cruzamento pensene–fato–parafato. `sinal: costas` diz **onde no corpo** a sinalética foi percebida.

**Pensene e fato juntos, ambos cosmoéticos:**

```yaml
---
tags:
  - fato/ok
  - pensene/ok
fato: Academia em casa e assistindo tertulia Opção pela Cosmoética
pensene: Vou incluir opção pela cosmoética fatuística no projeto do posicionamento
---
[[2026-05-28]]
```

**Registro mínimo, com campos de template em branco:**

```yaml
---
date: 2026-06-03
horario: 10:34
tags:
  - cpc/posi/ok
  - ecp2/261/pos
fato: "Cortando cabelo 💇‍♂️ "
pessoas:
  - 
lugar: casa
---
[[2026-06-03|fato]]
```

**Com pessoa nomeada:**

```yaml
---
date: 2026-07-16
horario: 09:24
tags:
  - cpc/familia/ok
fato: "Estou conversando com paty durante café da manhã"
pessoas:
  - Paty
lugar: casa
---
[[2026-07-16]]
```

## Armadilhas

- **Frontmatter incompleto é normal.** Muitos registros não têm `date`/`horario` (a data está no nome do arquivo) nem `pessoas`/`lugar`. Não trate como erro.
- `tags:` vazio existe. Significa não avaliado.
- **Caixa inconsistente nas tags.** Num corpus real conviviam `cpc/pri/` e `cpc/PRI/` — normalize a caixa antes de agrupar, ou a análise por área do CPC se fragmenta.
- `pessoas:` com item em branco (`- `) é resíduo de template, não pessoa anônima.
- Chaves residuais como `evento` e `ev` aparecem raramente — vêm de um dropdown de template com mais opções. `ev` é estado vibracional, não fatuística.
- A linguagem é coloquial, com erros de digitação e emoji. **Preserve como está** na captura e na análise; nominalize só ao compor verbete.

## Template de captura (Obsidian, plugin Templater)

```yaml
---
date: {{date}}
horario: {{time}}
tags:
  - cpc
{{VALUE:pensene,fato,parafato,evento,ev}}: "{{VALUE:descrição|label:Insira a descrição da fatuística}}"
pessoas:
  - 
lugar: casa
---
[[{{date}}]]
```
