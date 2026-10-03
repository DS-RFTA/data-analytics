# Análise de Vendas | VarejoMax Distribuidora

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-2563EB?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power%20Query-0EA5E9?style=for-the-badge)
![Modelagem Estrela](https://img.shields.io/badge/Star%20Schema-7C3AED?style=for-the-badge)

## Projeto de Business Intelligence para Análise Comercial

Dashboard gerencial desenvolvido para transformar dados transacionais em indicadores estratégicos de vendas.

---

## Contexto do projeto

A **VarejoMax Distribuidora** é uma empresa fictícia criada para simular um cenário real de Business Intelligence. O objetivo foi transformar uma base transacional de vendas em um modelo analítico capaz de apoiar decisões gerenciais, permitindo acompanhar faturamento, volume de vendas, ticket médio, desempenho comercial, filiais e canais de venda.

Este projeto demonstra competências valorizadas para vagas de **Analista de Dados**, **Analista de BI** e **Power BI Developer**, aplicando todo o fluxo de desenvolvimento de um dashboard profissional: ETL, modelagem dimensional, DAX e visualização executiva.

---

## Objetivo

Converter dados operacionais em informações estratégicas por meio de um dashboard interativo para responder perguntas de negócio como:

- Qual o faturamento total e sua evolução mensal?
- Quais vendedores geram maior receita?
- Qual filial apresenta melhor desempenho?
- Qual canal possui maior participação nas vendas?
- Como evolui o ticket médio ao longo do tempo?

---

## Tecnologias utilizadas

- Power BI
- Power Query
- DAX
- Modelagem Dimensional (Star Schema)

---

## Tratamento dos dados (Power Query)

A base passou por um processo completo de ETL para garantir qualidade, consistência e desempenho.

### Etapas realizadas

- Importação da base transacional
- Correção dos tipos de dados
- Padronização de textos e categorias
- Remoção de duplicidades
- Tratamento de valores nulos
- Criação de colunas auxiliares de data
- Organização da base para modelo estrela

**Resultado:** dados limpos, padronizados e preparados para análises gerenciais.

---

## Modelagem de dados

Foi utilizada uma **Modelagem Estrela (Star Schema)**.

### Tabela Fato

**Fato_Vendas**

Contém as métricas transacionais:

- Valor da venda
- Quantidade
- Data
- Chaves de Filial, Vendedor e Canal

### Tabelas Dimensão

| Dimensão | Finalidade |
|----------|------------|
| Dim_Data | Inteligência temporal |
| Dim_Filial | Análise geográfica |
| Dim_Vendedor | Performance comercial |
| Dim_Canal | Comparação entre canais |

Os relacionamentos foram configurados em **1:N**, das dimensões para a tabela fato.

---

## Medidas DAX

```DAX
Faturamento = SUM(Fato_Vendas[ValorVenda])

Qtd Vendas =
COUNTROWS(Fato_Vendas)

Ticket Médio =
DIVIDE([Faturamento], [Qtd Vendas])

Fat. Mês Anterior =
CALCULATE(
    [Faturamento],
    DATEADD(Dim_Data[Data],-1,MONTH)
)

Variação Mensal =
[Faturamento] - [Fat. Mês Anterior]
```

### KPIs desenvolvidos

- Faturamento Total
- Quantidade de Vendas Concluídas
- Ticket Médio
- Faturamento do Mês Anterior
- Variação Mensal
- Participação por Filial
- Participação por Canal
- Ranking de Vendedores
- Canal Destaque

---

## Dashboard

### Página 1 — Visão Geral

Painel executivo com os principais indicadores do negócio, evolução do faturamento e KPIs consolidados.

### Página 2 — Performance de Vendedores

Análise individual dos vendedores, ranking, participação no faturamento e comparação de desempenho.

### Página 3 — Canais de Venda

Comparação entre canais comerciais, participação percentual e comportamento das vendas.

### Página 4 — Detalhamento

Tabela analítica com filtros dinâmicos por período, filial, vendedor e canal para análises aprofundadas.

---

## Principais insights

A análise permitiu identificar:

- Concentração do faturamento em poucas filiais.
- Vendedores responsáveis pela maior parcela da receita.
- Canais com maior participação nas vendas.
- Evolução mensal do faturamento e sazonalidade.
- Diferenças de desempenho entre unidades comerciais.

Esses indicadores fornecem suporte para decisões estratégicas relacionadas à gestão comercial e performance de vendas.

---

## Competências demonstradas

| Área | Competência |
|------|-------------|
| ETL | Power Query |
| Modelagem | Star Schema |
| DAX | KPIs e Inteligência Temporal |
| BI | Dashboards Executivos |
| Analytics | Análise de Negócio |
| Visualização | Storytelling com Dados |

---

## Estrutura do repositório

```text
Analise-VarejoMax-Distribuidora/
│
├── Base/
│   └── VarejoMax_Vendas.xlsx
│
├── Dashboard/
│   └── Analise_VarejoMax.pbix
│
├── Imagens/
│   ├── visao-geral.png
│   ├── vendedores.png
│   ├── canais.png
│   └── detalhamento.png
│
└── README.md
```

---



**Projeto de Business Intelligence | Power BI**

Desenvolvimento de dashboard executivo utilizando **Power Query, modelagem dimensional (Star Schema) e DAX** para análise de faturamento, ticket médio, desempenho de vendedores, filiais e canais de venda. Implementação de métricas com inteligência temporal, ETL e visualizações interativas voltadas ao suporte à tomada de decisão.

### Palavras-chave 

`Power BI` • `DAX` • `Power Query` • `ETL` • `Star Schema` • `Business Intelligence` • `Dashboard` • `Data Analysis` • `KPI` • `Modelagem de Dados`

