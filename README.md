# README - Relatório de Vendas com Power BI

## Visão Geral

Este projeto tem como objetivo a criação de um relatório de vendas utilizando dados armazenados em um banco de dados MySQL, conectados ao Power BI para visualização e análise.

A imagem apresenta um dashboard de vendas com múltiplas métricas e visualizações gráficas que permitem uma análise detalhada do desempenho das vendas em diferentes perspectivas.

## Etapas do Projeto

### 1. Criação do Banco de Dados MySQL

Foi criado um banco de dados MySQL para armazenar as informações de vendas, com tabelas contendo dados de:

- **Vendas** (quantidade, valor, data, região, segmento, etc.)
- **Clientes** (nome, país, segmento, etc.)
- **Produtos** (categoria, preço, estoque, etc.)

### 2. Conexão com o Power BI

A conexão com o Power BI foi estabelecida por meio do conector nativo MySQL, permitindo a importação e a transformação dos dados.

### 3. Criação da Tabela Calendário com DAX

Foi criada uma tabela de datas utilizando a linguagem DAX no Power BI para permitir análises temporais mais detalhadas. A tabela inclui colunas como:

- Data completa
- Ano
- Trimestre
- Mês
- Dia da semana

Exemplo de código DAX para a tabela calendário:

```dax
CalendarTable = ADDCOLUMNS (
    CALENDAR (DATE(2013,1,1), DATE(2024,12,31)),
    "Ano", YEAR([Date]),
    "Mês", FORMAT([Date], "MMMM"),
    "Trimestre", "Q" & FORMAT([Date], "Q")
```
## Métricas Apresentadas
O dashboard apresenta as seguintes métricas principais:

* **Soma de Vendas**: 118,73 Milhões
* **Soma de Lucro**: 16,89 Milhões
* **Média de Vendas**: 169,61 Mil

## Visualizações
Evolução das Vendas ao Longo do Tempo

* Gráfico de linha mostrando o crescimento das vendas entre 2013 e 2014.
* Vendas por País e Trimestre
* Gráfico de colunas agrupadas mostrando vendas por país (Canadá, França, Alemanha, México, EUA) ao longo dos trimestres.
* Vendas por Segmento
* Gráfico de barras mostrando a distribuição de vendas nos segmentos: Governo, Pequenas Empresas, Empresas, Mercado Médio e Parceiros de Canal.

## Tecnologias Utilizadas
* **Banco de Dados**: MySQL
* **Ferramenta de BI**: Power BI
* **Linguagem de Código**: DAX para cálculos personalizados

## Conclusão
Este projeto demonstra como integrar MySQL com Power BI para criar relatórios de vendas eficazes, proporcionando insights valiosos através de dashboards interativos e intuitivos.

