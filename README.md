# Tupã — Coleta e Previsão de Dados Ambientais

Prova de conceito desenvolvida para a disciplina de Projetos de Engenharia 2 com o objetivo de explorar a integração entre coleta de dados ambientais, Internet das Coisas (IoT) e modelagem preditiva de séries temporais.

## Sobre o projeto

O projeto consistiu na concepção de uma pequena startup acadêmica voltada à coleta, tratamento e previsão de dados ambientais.

A solução combinava dados ambientais históricos com dados coletados localmente por meio de um microcontrolador equipado com um sensor DHT11. Os dados eram utilizados em uma cadeia de processamento que envolvia coleta, transmissão, tratamento e modelagem preditiva.

A proposta também explorou a utilização do ThingsBoard e do protocolo MQTT para comunicação dos dados provenientes do dispositivo, além da utilização de modelos de previsão para estimar valores futuros de variáveis ambientais.

O projeto foi desenvolvido academicamente em 2022 e representou uma das primeiras experiências práticas do autor com análise de dados, ciência de dados, Internet das Coisas, APIs, microcontroladores, Python e Machine Learning.

## Objetivo

Explorar, de forma prática, a construção de uma solução integrada capaz de:

* coletar e tratar dados ambientais;
* utilizar dados históricos para modelagem preditiva;
* realizar previsões de variáveis ambientais;
* coletar dados localmente por meio de um sensor DHT11;
* transmitir dados de um microcontrolador utilizando Wi-Fi e MQTT;
* integrar conceitos de IoT, análise de dados e Machine Learning em uma única prova de conceito.

## Dados

O projeto trabalhou com dados ambientais organizados em séries temporais, incluindo variáveis como:

* Temperatura;
* Umidade;
* Radiação global.

Os notebooks preservados no projeto realizam etapas de preparação dos dados, seleção das variáveis, separação entre períodos de treinamento e teste e preparação das séries para utilização nos modelos de previsão.

Os dados originais utilizados durante o desenvolvimento não estão incluídos neste repositório.

## Modelagem Preditiva

Foram desenvolvidos notebooks independentes para realizar previsões de diferentes variáveis ambientais:

* Temperatura;
* Umidade;
* Radiação global.

A modelagem foi realizada utilizando o Prophet, com avaliação das previsões por meio de métricas como MAE e erro percentual.

De forma simplificada, o fluxo da modelagem pode ser representado como:

```text
Dados ambientais históricos
          │
          ▼
Tratamento dos dados
          │
          ▼
Preparação da série temporal
          │
          ▼
Treinamento do modelo
          │
          ▼
Previsão
          │
          ▼
Avaliação dos resultados
```

## IoT e Coleta Local

Paralelamente à etapa de modelagem, foi desenvolvido um protótipo de coleta local utilizando um sensor DHT11 conectado a um microcontrolador.

O sensor era utilizado para obter:

* Temperatura;
* Umidade.

Uma das implementações realiza a leitura local dos dados e outra utiliza conexão Wi-Fi e MQTT para transmitir as informações para o ThingsBoard.

O fluxo de comunicação pode ser representado como:

```text
Sensor DHT11
     │
     ▼
Microcontrolador
     │
     ▼
Wi-Fi
     │
     ▼
MQTT
     │
     ▼
ThingsBoard
```

## Tecnologias

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Prophet
* Jupyter Notebook
* Arduino/C++
* ESP
* DHT11
* MQTT
* ThingsBoard
* APIs e integração de dados

## Estrutura do projeto

```text
.
├── embedded/
│   ├── sensor_dht11.ino
│   └── thingsboard_mqtt.ino
├── notebooks/
│   ├── humidity_forecasting.ipynb
│   ├── radiation_forecasting.ipynb
│   └── temperature_forecasting.ipynb 
└── README.md
```

## Execução

Os experimentos de modelagem estão organizados nos notebooks disponíveis no diretório:

```text
notebooks/
```

Os códigos relacionados à coleta de dados por sensores e comunicação com o ThingsBoard estão disponíveis em:

```text
embedded/
```

Os notebooks originais dependiam de arquivos de dados que não estão incluídos neste repositório. Portanto, a execução integral dos experimentos originais depende da disponibilidade dos dados utilizados durante o desenvolvimento.

## Limitações

Este projeto deve ser entendido como uma prova de conceito acadêmica desenvolvida em 2022 e não como uma plataforma de monitoramento ou previsão pronta para produção.

Os dados originais utilizados nos experimentos não estão incluídos neste repositório, e algumas informações sobre o ambiente original de execução, configurações de treinamento e infraestrutura utilizada durante o desenvolvimento não foram preservadas.

Os modelos e resultados apresentados representam o estado do projeto no período de seu desenvolvimento e não foram posteriormente reavaliados em um ambiente de produção.

## Possíveis melhorias

Entre as possibilidades de evolução do projeto estão:

* reconstrução e documentação do pipeline completo de dados;
* integração automatizada com fontes de dados ambientais;
* criação de um pipeline ETL/ELT;
* armazenamento estruturado dos dados coletados;
* implementação de APIs para disponibilização dos dados;
* monitoramento da qualidade dos dados;
* comparação entre diferentes modelos de previsão;
* utilização de métricas adicionais para avaliação;
* realização de validação temporal mais robusta;
* criação de dashboards para visualização dos dados;
* integração mais estruturada entre os dados históricos e os dados coletados pelo sensor;
* implementação de uma arquitetura IoT mais escalável.

## Contexto acadêmico

Projeto desenvolvido em 2022 para a disciplina de Projetos de Engenharia 2.

A proposta consistia na criação de uma pequena startup acadêmica voltada à coleta, tratamento e previsão de dados ambientais, combinando conceitos de análise de dados, ciência de dados, IoT, microcontroladores e Machine Learning.
