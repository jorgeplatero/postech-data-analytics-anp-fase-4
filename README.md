# Dashboard com Indicadores de Preço de Combustíveis Ofertados nos Postos Brasileiros

Este projeto consiste em um dashboard que reune indicadores referentes ao preço dos combutíveis praticado em postos brasileiros e publicados pela ANP (Agência Nacional do Petróleo, Gás Natural e Biocombustíveis).

### Arquitetura do Projeto

<img src='https://github.com/jorgeplatero/postech_fase_4_anp/blob/b1addcdd199384a9c5869115ee81e90fa8f17571/img/arquitetura_anp.png' width='500'/> 

#### Banco de Dados

A tabela abaixo foi criada para comportar os dados:

```sql
CREATE TABLE anp.preco_combustivel(
	regiao 				varchar(255)
	,estado				varchar(255)
	,municipio			varchar(255)
	,revenda			varchar(255)
	,cnpj				varchar(255)
	,nome_rua			varchar(255)	
	,numero_rua			varchar(255)
	,complemento		        varchar(255)
	,bairro				varchar(255)
	,cep				varchar(255)
	,produto			varchar(255)
	,data_coleta		        date
	,valor_venda		        float
	,unidade_medida		        varchar(255)
	,bandeira			varchar(255)
)
```

#### ETL dos Dados

Os dados foram inseridos no banco de dados por meio da ferramenta de ETL KNIME. O fluxo do ETL foi construído na aplicação conforme ilustrado abaixo:

![etl knime](https://github.com/jorgeplatero/postech_fase_4_anp/blob/c4769c12a8050c4f7ccb68ebf8bf9d74cd2de788/img/etl_knime.png)

### Tecnologias

Abaixo estão listadas as tecnologias utilizadas no desenvolvimento da solução:

| Componente | Tecnologia | Descrição |
| :--- | :--- | :--- |
| **Frontend/App** | **Power BI** | Ferramenta utilizada para a criação e publicação do dashboard. |
| **Ambiente** | **Python** | Linguagem utilizada para processamento e suporte ao projeto. |
| **Banco de Dados** | **PostgreSQL** | Sistema gerenciador de banco de dados relacional para armazenamento dos dados. |
| **Orquestração/ETL** | **KNIME** | Plataforma utilizada para a construção do fluxo de extração, transformação e carga. |

### Fontes de Dados

Link para a base de dados: <a style='text-decoration:none;' href='https://www.gov.br/anp/pt-br/centrais-de-conteudo/dados-abertos/serie-historica-de-precos-de-combustiveis'>link</a>.

Utilizou-se os dados de 2018 a 2022.

### Link para a Aplicação

Dashboard Power BI: <a style='text-decoration:none;' href='https://app.powerbi.com/view?r=eyJrIjoiNGJlOTY3ZmYtZjZlMS00ZTEzLWJiMmMtMWRjYjJiZTBlYTAzIiwidCI6IjFmZTA1YTY2LWNhMjYtNGJmZC1hZDlkLWQzMDRhZGViMjIwNSJ9' target='_blank'>Acesse aqui</a>.
