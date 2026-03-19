# PrecoGibis

Projeto de coleta, processamento e análise de preços de gibis utilizando web scraping e Python.

## Overview

O **PrecoGibis** é um projeto de engenharia de dados aplicado ao mercado de quadrinhos, com foco na extração automatizada de informações do site Guia dos Quadrinhos.

O objetivo é construir uma base estruturada que permita analisar:

- Evolução de preços ao longo do tempo
- Distribuição de valores por editora/série

## Tecnologias utilizadas

- Python 3.x
- Pandas
- Requests
- BeautifulSoup
- Regex
- Time / Random (controle de scraping)

## Arquitetura do Projeto

O pipeline segue três etapas principais:

### 1. Coleta de dados (Web Scraping)
- Requisições HTTP para páginas do Guia dos Quadrinhos
- Parsing do HTML com BeautifulSoup
- Extração de:
  - Nome do gibi
  - Edição
  - Data de publicação
  - Preço
  - Número de páginas

### 2. Tratamento de dados
- Normalização de strings (acentuação, encoding)
- Conversão de datas (PT-BR → padrão)
- Limpeza de inconsistências
- Tratamento de valores ausentes

### 3. Armazenamento e análise
- Estruturação em DataFrame (Pandas)
- Exportação para CSV
- Base pronta para análises exploratórias

## Principais Insights (até agora)

Mesmo em estágio inicial, já é possível observar:

Quadrinhos no Brasil até os anos 1970 representavam menos de 1% do salário mínimo, época em que as tiragens passavam da casa das centenas de milhares e eram febre entre as crianças. Com os anos 80, veio a era Abril e a famigerada "década perdida", que culminou na inflação galopante. É nítido nos gráficos o aumento no período dos anos 80 e 90. Os gibis do Pato Donald mantiveram uma constancia no número de páginas, então a média do preço possui uma menor variação, enquanto que para o Batman, tem uma relação com o número variável de páginas. No período da pandemia do COVID-19, o preço dos quadrinhos Marvel/DC duplicaram no Brasil, representando 2% do salário mínimo no Brasil.

## Possíveis evoluções

- Dashboard interativo (Plotly / Dash)
- Modelos de machine learning para previsão de preços
- Análise do Pato Donald após o fim da Editora Abril em 2018 e continuidade dada pela Editora Culturama
