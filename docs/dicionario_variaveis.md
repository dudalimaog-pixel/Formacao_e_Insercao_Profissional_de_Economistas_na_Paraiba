# Dicionário preliminar de variáveis


## Tabela principal (região imediata × ano)

| Variável | Descrição | Tipo | Unidade | Fonte/cobertura |
|---|---|---|---|---|
| `rgi_nome` | nome da região geográfica imediata | texto | — | IBGE, DTB 2025; Paraíba |
| `ano` | ano de referência | inteiro | ano | RAIS e INEP; períodos a definir |
| `concluintes_econ` | concluintes dos cursos de Ciências Econômicas na região | inteiro | pessoas | INEP, Censo da Educação Superior |
| `vinculos_econ` | vínculos formais com ocupação de economista (CBO) em 31/12 | inteiro | vínculos | MTE, RAIS |
| `admissoes_econ` | admissões de economistas no ano | inteiro | movimentações | MTE, Novo CAGED |
| `desligamentos_econ` | desligamentos de economistas no ano | inteiro | movimentações | MTE, Novo CAGED |
| `saldo_econ` | admissões menos desligamentos | inteiro | movimentações | calculada |

## Variáveis de origem (antes do tratamento)

| Variável | Descrição | Tipo | Unidade | Fonte/cobertura |
|---|---|---|---|---|
| `município` | código do município (6 dígitos) | texto | código IBGE | RAIS e CAGED  |
| `CO_MUNICIPIO` | código do município do curso (7 dígitos) | texto | código IBGE | INEP|
| `NU_ANO_CENSO` | ano do Censo | inteiro | ano | INEP |
| `NO_CURSO` | nome do curso | texto | — | INEP |
| `QT_CONC` | quantidade de concluintes do curso | inteiro | pessoas | INEP |
| CBO da ocupação | código da ocupação (CBO 2002) | texto | código | RAIS e CAGED |
| `saldomovimentação` | 1 = admissão, −1 = desligamento | inteiro | — | CAGEDMOV |
| `uf` | código da UF (Paraíba = 25) | texto | código IBGE | CAGEDMOV e RAIS |
