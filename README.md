# Dashboard com Indicadores de Preço de Combustíveis Ofertados nos Postos Brasileiros

Este projeto consiste em um dashboard que reúne indicadores dos preços de combustíveis praticados em postos brasileiros, utilizando dados oficiais publicados pela ANP (Agência Nacional do Petróleo, Gás Natural e Biocombustíveis).

### Tecnologias

A aplicação utiliza um stack moderno focado em engenharia e visualização de dados.

| Componente | Tecnologia | Versão | Descrição |
| :--- | :--- | :--- | :--- |
| **Plataforma BI** | **Power BI** | `-` | Plataforma de BI utilizada para o desenvolvimento do dashboard |
| **Banco de Dados** | **PostgreSQL** | `13+` | SGBD para armazenamento dos dados. |
| **Orquestração/ETL** | **KNIME** | `4.7.x` | Plataforma para gerenciamento e agendamento de pipelines |
| **Linguagem** | **Python** | `3.10+` |Linguagem de programação base para o desenvolvimento dos scripts |

### Fontes de Dados

O fluxo de dados consome a série histórica oficial do portal de [dados abertos da ANP](https://www.gov.br/anp/pt-br/centrais-de-conteudo/dados-abertos/serie-historica-de-precos-de-combustiveis), integrando anos de registros da ANP em um ambiente otimizado para análise.

### Deploy

O dashboard está disponível via Power BI Service.

Link para o dashboard: https://app.powerbi.com/view?r=eyJrIjoiNGJlOTY3ZmYtZjZlMS00ZTEzLWJiMmMtMWRjYjJiZTBlYTAzIiwidCI6IjFmZTA1YTY2LWNhMjYtNGJmZC1hZDlkLWQzMDRhZGViMjIwNSJ9
