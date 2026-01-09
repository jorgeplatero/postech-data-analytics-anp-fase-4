# Dashboard com Indicadores de Preço de Combustíveis Ofertados nos Postos Brasileiros

Este projeto consiste em um dashboard que reúne indicadores dos preços de combustíveis praticados em postos brasileiros, utilizando dados oficiais publicados pela ANP (Agência Nacional do Petróleo, Gás Natural e Biocombustíveis).

### Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas:

*   PostgreSQL
*   KNIME Analytics Platform
*   Power BI Desktop
*   Python 3.10+

### Instalação

Siga os passos abaixo para preparar o ambiente:

1. Banco de Dados:

Execute o script DDL no seu PostgreSQL para criar a tabela que receberá os dados:

```sql
CREATE TABLE anp.preco_combustivel(
    regiao          varchar(255),
    estado          varchar(255),
    municipio       varchar(255),
    revenda         varchar(255),
    cnpj            varchar(255),
    nome_rua        varchar(255),
    numero_rua      varchar(255),
    complemento     varchar(255),
    bairro          varchar(255),
    cep             varchar(255),
    produto         varchar(255),
    data_coleta     date,
    valor_venda     float,
    unidade_medida  varchar(255),
    bandeira        varchar(255)
);
```

2. Orquestração:
   
Abra o KNIME e importe o workflow contido na pasta `/etl` deste repositório e configure o nó **DB Connector** com suas credenciais do PostgreSQL.

### Como Rodar a Aplicação

Para atualizar e visualizar os indicadores, execute o workflow no KNIME, que irá realizar a extração dos dados da ANP, limpeza e carga no PostgreSQL. Abra o arquivo `.pbix` no Power BI Desktop, conecte co ma tabela criada no PostgreSQL e atualize os dados.


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
