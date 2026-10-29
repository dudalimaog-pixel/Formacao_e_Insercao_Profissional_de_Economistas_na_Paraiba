# Inventário de fontes


## 1. Fontes

| Base | Instituição/link | Cobertura | Formato | Acesso | Licença | Data de acesso |
|---|---|---|---|---|---|---|
| RAIS | MTE — [Microdados RAIS e Caged](https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/estatisticas-trabalho/microdados-rais-e-caged) | Brasil, vínculos por ano; recorte PB e ocupação de economista (CBO) | texto delimitado compactado | aberto | Domínio Público | 26/10/2026 |
| Novo CAGED (CAGEDMOV) | MTE — mesma página acima | Brasil, movimentações mensais (admissões e desligamentos); recorte PB e CBO | `.txt.gz` (`;` como separador) | aberto | Domínio Público | 26/10/2026 |
| Censo da Educação Superior | INEP — página de microdados (colar link) | Brasil, anual; cursos, matrículas, ingressantes e concluintes | CSV | aberto | Domínio Público | 26/10/2026 |
| PNAD Contínua | IBGE — página de microdados (colar link) | Brasil e UFs, trimestral; contexto do mercado de trabalho da PB | microdados em texto + dicionário | aberto | Domínio Público | 26/10/2026 |
| DTB (tabela auxiliar) | IBGE — Divisão Territorial Brasileira 2025 (colar link) | municípios do Brasil e regiões geográficas imediatas | `.xlsx` | aberto | Domínio Público | 26/10/2026 |
| Corecon-PB | Corecon-PB (solicitação feita na escuta) | inscrições ativas e novos registros por ano | A definir | **ainda não obtida** | A definir | — |

## 2. Unidade, chave, periodicidade e junções

| Tabela | Cada linha é... | Chave natural | Periodicidade | Junta com |
|---|---|---|---|---|
| RAIS | um vínculo de trabalho no ano | município (6 dígitos) + ano + CBO | anual | DTB (município); INEP (município + ano) |
| CAGEDMOV | uma movimentação (admissão ou desligamento) | município (6 dígitos) + competência (mês/ano) + CBO | mensal | DTB (município); RAIS |
| INEP (cursos) | um curso de graduação de uma instituição, no ano | código do curso + ano; município de oferta | anual | DTB (município) |
| PNAD Contínua | um domicílio/pessoa na amostra | UF + trimestre | trimestral | só contexto (nível UF) |
| DTB | um município | código do município | ano de referência 2025 | RAIS, CAGED, INEP |
| Corecon-PB | A definir | A definir | anual | A definir |

**Atenção à chave de município:** RAIS e CAGED usam código de 6 dígitos; o INEP e a DTB trazem o código IBGE de 7 dígitos. Padronizar nos 6 primeiros dígitos (mesmo procedimento da Aula 08/09: `str[:6]`).

## 3. Tabela principal da análise

- **Cada linha:** um par (região geográfica imediata da Paraíba, ano).
- **Colunas-chave:** `rgi_nome` e `ano`.
- **Variáveis:** concluintes de Economia (INEP), vínculos, admissões, desligamentos e saldo de economistas (RAIS/CAGED).
- **Por quê:** o Conselho decide onde concentrar esforço, ou seja, por região; a região imediata é o nível em que as duas bases se juntam.
- **Segunda tabela possível:** concluintes por instituição e ano (só INEP), se a decisão do Conselho for por instituição, pois a RAIS não traz a instituição de formação.

## 4. Riscos de compatibilização

- INEP conta concluinte por curso; RAIS conta vínculo por ocupação.
- Nem todo formado aparece registrado como economista.
- A comparação concluintes × vínculos é um indicador, não uma taxa de absorção.
