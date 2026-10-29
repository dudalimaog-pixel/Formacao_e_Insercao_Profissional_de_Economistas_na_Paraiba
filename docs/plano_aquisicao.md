# Plano de aquisição

Os dados originais **não são versionados** no Git. Cada fonte abaixo tem o passo a passo para obtê-la de novo.

| Fonte | Método de obtenção | Arquivo/endpoint | Frequência | Parâmetros | Responsável | Data prevista | Atualização |
|---|---|---|---|---|---|---|---|
| RAIS | download manual na página de microdados do MTE | arquivo da RAIS do ano (A PREENCHER) | anual | UF = 25 (Paraíba); filtrar CBO de economista | A PREENCHER | 05/11/2026 | baixar o novo ano quando publicado |
| Novo CAGED | download manual na página de microdados do MTE | `CAGEDMOV<AAAAMM>.txt.gz` | mensal | `uf` = 25; filtrar CBO de economista; `sep=";"`, `decimal=","` | A PREENCHER |05/11/2026| baixar os meses novos |
| Censo da Educação Superior | download manual na página de microdados do INEP | arquivo de cursos do Censo (A PREENCHER) | anual | UF/município da Paraíba; curso de Ciências Econômicas | A PREENCHER | 05/11/2026 | baixar o novo Censo quando publicado |
| PNAD Contínua | download na página de microdados do IBGE | arquivo do trimestre + dicionário | trimestral | UF = Paraíba | A PREENCHER | 05/11/2026 | novo trimestre |
| DTB | download na página da Divisão Territorial Brasileira (IBGE) | `RELATORIO_DTB_BRASIL_2025_MUNICIPIOS.xlsx` | anual | `skiprows=6` na leitura | A PREENCHER | 05/11/2026 | nova edição |
| Corecon-PB | solicitação ao Conselho (sem acesso a dados em nome da UFPB) | 05/11/2026 | anual | inscrições ativas e novos registros por ano | A PREENCHER | 05/11/2026 | depende do Conselho |

## Procedimento de reprodução

1. Baixar cada arquivo no link da página oficial indicado em `inventario_fontes.md`.
2. Salvar em `data/raw/` mantendo o nome original do arquivo.
3. Registrar a **data de acesso** no inventário.
4. Rodar `notebooks/` na ordem numérica (aquisição → tratamento → análise).

## Segurança

Não versionar senhas, tokens, chaves, dados pessoais, documentos internos ou bases restritas. Se uma base for grande ou não puder ser redistribuída, ela fica fora do repositório e este plano descreve como obtê-la.
