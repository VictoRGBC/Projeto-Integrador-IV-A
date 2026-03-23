# 📊 Identificação de "Zonas de Risco" para Evasão Escolar
**Projeto Integrador IV-A | [cite_start]Big Data e Inteligência Artificial - PUC Goiás** [cite: 1, 4, 5]

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Apache Spark](https://img.shields.io/badge/apache%20spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=Databricks&logoColor=white)

## 📌 Sobre o Projeto
[cite_start]Este projeto foi desenvolvido no contexto da extensão universitária[cite: 13], visando resolver um problema social e operacional latente: a **Evasão Escolar no Brasil**. 

[cite_start]Utilizando infraestrutura em nuvem e técnicas de processamento paralelo e distribuído[cite: 12, 31], o objetivo desta solução é analisar grandes volumes de dados de rendimento escolar (INEP) para identificar padrões, ranquear municípios e mapear as "zonas de risco" mais críticas. [cite_start]Os insights gerados servem como ferramenta de apoio à tomada de decisão para organizações públicas, privadas ou do terceiro setor que atuam na educação[cite: 12, 13, 29].

## 🏗️ Arquitetura em Nuvem e Tecnologias
[cite_start]A solução foi construída utilizando o modelo **PaaS (Platform as a Service)**[cite: 33], baseada nas seguintes tecnologias:

* **Databricks Community Edition:** Ambiente de nuvem utilizado para orquestração e execução dos notebooks[cite: 48].
* [cite_start]**Apache Spark (PySpark):** Motor de processamento paralelo e distribuído em memória, essencial para lidar com a volumetria e aplicar transformações nos dados de forma escalável[cite: 38, 44].
* [cite_start]**DBFS (Databricks File System):** Sistema de arquivos distribuído atuando como *Data Lake* para armazenamento dos arquivos brutos e processados[cite: 34].
* **Databricks Dashboards:** Ferramenta nativa para a geração de relatórios e visualizações interativas[cite: 46, 48].

## 🗄️ Origem dos Dados
Os dados utilizados são provenientes do **Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP)**, especificamente o dataset de Taxas de Rendimento Escolar de 2024 (`tx_rend_escolas_2024.csv`).

## ⚙️ Pipeline de Dados (Metodologia)
O fluxo de processamento seguiu as melhores práticas de Engenharia de Dados:
1.  **Ingestão (Bronze):** Coleta dos dados brutos em formato CSV e armazenamento distribuído[cite: 43].
2.  **Limpeza e Transformação (Silver):** Uso de PySpark para padronização de nomes de colunas, tratamento de valores nulos (ausência de dados representados por `--`) e conversão de tipagem de *strings* para *floats*[cite: 44].
3.  **Processamento Analítico (Gold):** Agrupamento e geração de métricas focadas na Taxa de Abandono (Evasão), analisando os dados sob quatro óticas principais[cite: 45]:
    * Média de evasão por Município (Zonas de Risco).
    * Comparativo entre localização Urbana e Rural.
    * Impacto por Dependência Administrativa (Municipal, Estadual, Federal, Privada).
    * Ranqueamento das escolas mais críticas em estados específicos.
4.  **Disponibilização:** Criação de um dashboard visual para consumo da organização parceira[cite: 46].

## 🚀 Como Executar o Projeto
1. Faça o clone deste repositório:
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)