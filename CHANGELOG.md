# Changelog

Todas as mudanças relevantes deste projeto são registradas aqui.

O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/). As releases seguem o padrão de data **`yyyy.mm.dd.HHMM`** (ex.: `2026.07.16.1432`) — as versões `0.1.0` e `0.2.0` são anteriores a essa convenção. As versões também estão disponíveis como [releases no GitHub](https://github.com/conscienciologia/autopesquisa-skill/releases). O processo de lançamento está em [RELEASING.md](RELEASING.md).

> **Como atualizar:** marketplaces de terceiros não atualizam sozinhos. Rode `/plugin marketplace update conscienciologia` e reinicie a sessão do Claude Code. Veja [detalhes no README](README.md#atualizar-é-manual).

## [Não lançado]

_Nada ainda._

## [0.2.0] — 2026-07-16

### Adicionado
- **Skill `tornieri-sinaletica`** — base de conhecimento do livro _Mapeamento da Sinalética Energética Parapsíquica_ (Sandra Tornieri, Editares, 2ª ed. 2018): taxologia dos 44 sinais por veículo do holossoma, protocolo de mapeamento de 15 variáveis, 12 técnicas de mapeamento, glossário, patterns, cheatsheet e 56 capítulos carregados sob demanda. Fonte: <https://editares.org/mapeamento-da-sinaletica/>.
- **CONTRIBUTING regra 6** — toda skill derivada de um livro deve informar, no `SKILL.md`, o URL oficial de aquisição/download da obra e recomendar a leitura do original.
- **README** — seção "Como usar cada skill" com exemplos por skill, começando pelo exemplo guiado "Como posso mapear a minha sinalética?".

### Alterado
- **CONTRIBUTING regra 2** — abre exceção à norma "referenciar, nunca copiar" para livros disponibilizados publicamente pelo autor ou editora (leitura livre e autorizada).
- **README** — instalação reescrita em dois passos explicados (`marketplace add` vs `plugin install`) e nova seção sobre atualização manual.
- Versão do plugin `autopesquisa`: `0.1.0` → `0.2.0`.

## [0.1.0] — 2026-07-16

### Adicionado
- Lançamento inicial do plugin `autopesquisa`.
- **Skill `fatuistica`** — registro e análise de pensenes, fatos e parafatos; composição da Divisão II (Fatuística) de verbetes; adaptador para Obsidian com frontmatter YAML.
- **Skill `verbete`** — estrutura e confor dos verbetes (formato Encyclossapiens e Dicionário da OIC).

[Não lançado]: https://github.com/conscienciologia/autopesquisa-skill/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/conscienciologia/autopesquisa-skill/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/conscienciologia/autopesquisa-skill/releases/tag/v0.1.0
