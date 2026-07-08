# Versão de Negócio — Synthesis

**Versão:** 1.0  
**Data:** 2026-07-07  
**Responsável:** Karen Martins

---

## Tema do Startup: 
Sistema de personas sintéticas: Plataforma de simulação de personas baseados em dados de consumidores da própria empresa para testar produtos, rodar experimentos e medir adesão/engajamento a determinada campanha de marketing ou ação.


## Sugestões de nomes para o produto

1. Plataforma de Simulação de Consumidores baseada em IA 
2. Plataforma Data-Driven de Simulação de Consumidores 
3. “Simule AI”, “Teste AI”

## Contexto de negócio

As empresas acumulam grandes volumes de dados provenientes de sistemas transacionais, plataformas digitais e canais de relacionamento com clientes. Apesar desse volume de informações, transformar esses dados em conhecimento para apoiar decisões estratégicas, ainda representa um grande desafio no dia-a-dia. 

## Objetivo de negócio

Disponibilizar um ambiente de experimentação baseado em dados históricos e Inteligência Artificial, permitindo que empresas avaliem possíveis impactos de campanhas, estratégias comerciais e lançamentos de produtos antes de sua execução. 
Transformar dados históricos em consumidores sintéticos capazes de apoiar decisões estratégicas com menor risco, menor custo e maior velocidade. 

## Problema 

Hoje, as empresas tomam decisões importantes sobre campanhas de marketing, lançamento de produtos e estratégias comerciais com informações limitadas.As alternativas existentes apresentam limitações:

- Pesquisas de mercado são caras e demoradas.
- Focus groups possuem amostras pequenas.
- Testes A/B só podem ser realizados após o lançamento.
- Entrevistas dependem da disponibilidade dos consumidores.
- Muitas empresas acabam decidindo com base na experiência ou na intuição.

Como consequência, campanhas podem não atingir o público esperado, produtos podem ter baixa aceitação e recursos financeiros são desperdiçados em iniciativas com alto risco.

## O que queremos resolver

Permitir que empresas simulem o comportamento dos seus próprios consumidores antes de tomar decisões de negócio.

Em vez de perguntar: "Vamos lançar e ver no que dá."
A empresa passa a perguntar:  "O que nossos consumidores provavelmente fariam diante deste cenário?"

Nosso objetivo é reduzir a incerteza na tomada de decisão utilizando dados históricos e inteligência artificial.

## Nossa solução

Uma Plataforma de Simulação de Consumidores baseada em IA que utiliza dados históricos da própria empresa para criar consumidores sintéticos capazes de representar diferentes perfis de clientes.

Esses consumidores sintéticos permitem simular cenários como:

- lançamento de novos produto
- campanhas de marketing
- alterações de preço
- promoções
- programas de fidelidade
- estratégias de comunicação

A plataforma apresenta previsões e indicadores que apoiam a tomada de decisão antes da execução das ações no mercado.

*Importante:* Nossa plataforma não substitui pesquisas de mercado nem garante previsões. Ela funciona como um ambiente de experimentação que permite às empresas simularem cenários antes da execução de campanhas, lançamentos e estratégias comerciais, utilizando consumidores sintéticos construídos a partir de seus próprios dados. 


## Diferencial

- utilizar dados históricos da própria empresa
- preservar a privacidade por meio da geração de consumidores sintéticos
- reduzir a necessidade de pesquisas tradicionais em etapas iniciais
- permitir testar múltiplos cenários antes da tomada de decisão
- integrar Engenharia de Dados, IA Generativa e Analytics em uma única plataforma.

## Fluxo de Negócio

Fluxo de negócio e possíveis tecnologias. 

1. Fontes de Dados: Salesforce CRM, SAP ERP, Google Analytics 4
2. Ingestão: Apache Kafka, Apache Airbyte, APIs REST
3. Lakehouse - Camada Bronze (dados brutos): Amazon S3, Apache Iceberg, MinIO
4. Processamento: Apache Spark, dbt, Databricks
5. Lakehouse - Camada Silver (dados tratados): Amazon S3, Apache Iceberg, Delta Lake
6. Tratamento: Apache Spark, SQL, dbt
7 . Lakehouse - Camada Gold (dados analíticos): Amazon S3, Apache Iceberg, Apache Parquet
8. Motor de IA: OpenAI GPT-5, LangChain, pgvector
9. Motor de Simulação: CrewAI, LangGraph, FastAPI
10. Resultados da Simulação: Amazon S3, Apache Iceberg, Apache Parquet
11. Dashboard: Power BI, Tableau, Apache Superset

