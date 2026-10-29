# Dicionário preliminar de variáveis

Apenas as variáveis essenciais. Os nomes exatos das colunas nos arquivos originais devem ser conferidos no dicionário oficial de cada base (marcados **confirmar**).

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
| `município` | código do município (6 dígitos) | texto | código IBGE | RAIS e CAGED (confirmar nome da coluna na RAIS) |
| `CO_MUNICIPIO` | código do município do curso (7 dígitos) | texto | código IBGE | INEP (confirmar) |
| `NU_ANO_CENSO` | ano do Censo | inteiro | ano | INEP (confirmar) |
| `NO_CURSO` | nome do curso | texto | — | INEP (confirmar) |
| `QT_CONC` | quantidade de concluintes do curso | inteiro | pessoas | INEP (confirmar) |
| CBO da ocupação | código da ocupação (CBO 2002) | texto | código | RAIS e CAGED (confirmar nome da coluna e códigos de economista) |
| `saldomovimentação` | 1 = admissão, −1 = desligamento | inteiro | — | CAGEDMOV |
| `uf` | código da UF (Paraíba = 25) | texto | código IBGE | CAGEDMOV e RAIS |
