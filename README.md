# Formação e inserção dos economistas na Paraíba

Projeto aplicado de extensão — **PSAE00320 Técnicas de Pesquisa e Análise Econômica II** · Turma 01 · 2026.2 · UFPB

**Organização de referência (demandante):** Corecon-PB, Conselho Regional de Economia da Paraíba.

## Equipe

| Nome | Responsabilidade |
|---|---|
| A PREENCHER | A PREENCHER |
| A PREENCHER | A PREENCHER |

## Problema

- **Tema:** formação e inserção dos economistas no mercado de trabalho formal da Paraíba.
- **Pergunta:** o que acontece com quem se forma em Ciências Econômicas no estado?
- **Hipótese (ainda não confirmada):** possível descompasso entre o número de concluintes e a quantidade absorvida pelo mercado formal.
- **Decisão que o trabalho pode apoiar:** onde o Conselho concentra esforço junto a estudantes e recém-formados.

## Fontes de dados

| Base | O que traz | Lado |
|---|---|---|
| RAIS e Novo CAGED (MTE) | vínculos e movimentações por ocupação (CBO) e município | inserção |
| Censo da Educação Superior (INEP) | matrículas, ingressantes e concluintes por curso e instituição | formação |
| PNAD Contínua (IBGE) | contexto do mercado de trabalho paraibano | contexto |
| Corecon-PB | inscrições ativas e novos registros por ano | ainda não obtida (pedida na escuta) |

Detalhes em [`docs/inventario_fontes.md`](docs/inventario_fontes.md).

## Estrutura do repositório

```
README.md
.gitignore
data/raw/          # dados originais permitidos (não versionados se grandes)
data/processed/    # dados tratados
notebooks/         # aquisição, tratamento e análise
docs/              # planos, memórias e relatórios
outputs/           # tabelas, gráficos e produtos
```

Documentos principais em `docs/`:
- [`inventario_fontes.md`](docs/inventario_fontes.md): fontes, unidades, chaves e junções
- [`dicionario_variaveis.md`](docs/dicionario_variaveis.md): variáveis essenciais
- [`plano_aquisicao.md`](docs/plano_aquisicao.md): como obter cada base

## Como reproduzir

1. Ler o [`plano_aquisicao.md`](docs/plano_aquisicao.md) e baixar cada base nos links indicados.
2. Colocar os arquivos baixados em `data/raw/` (essa pasta não é versionada).
3. Rodar os notebooks de `notebooks/` na ordem numérica.
4. Os dados tratados saem em `data/processed/` e os produtos em `outputs/`.

## Segurança

Este repositório não contém senhas, tokens, chaves, dados pessoais, documentos internos nem bases restritas. Arquivos grandes ou não redistribuíveis ficam fora do Git e são substituídos por instruções de obtenção.

## Limitações conhecidas

- Nem todo formado em Economia aparece registrado como economista na RAIS/CAGED.
- O INEP conta concluintes por curso; a RAIS conta vínculos por ocupação. As bases precisam ser compatibilizadas.
- Os dados do Corecon-PB ainda não foram obtidos.

## Tarefas

Acompanhadas na aba **Issues** do repositório, com responsável e prazo.
