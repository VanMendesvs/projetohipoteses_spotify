# Projeto de Análise de Hipóteses: Sucesso Musical no Spotify para Gravadoras

## 📄 Ficha Técnica do Projeto

Este `README.md` detalha o projeto de análise de dados focado em identificar e validar fatores de sucesso musical no Spotify, com insights estratégicos para gravadoras e artistas.

---

### **Objetivo Geral**

Transformar dados brutos de streaming em insights acionáveis para otimizar estratégias de negócios e potencializar o desempenho de músicas e artistas no mercado musical digital.

### **Problema de Negócio / Hipóteses Centrais**

O projeto buscou responder a perguntas-chave e validar hipóteses sobre o sucesso de músicas e artistas no Spotify, incluindo:
* A relação entre a presença em playlists e o volume de streams.
* O impacto do tamanho do catálogo de músicas de um artista no total de streams.
* A correlação entre o sucesso no Spotify e em outras plataformas de streaming (Deezer, Apple Music).
* A influência de características musicais (BPM, danceability, energy, etc.) no número de streams.

### **Tecnologias e Ferramentas Utilizadas**

* **Google BigQuery:** Utilizado para armazenamento, manipulação e tratamento inicial dos dados (ETL - Extração, Transformação e Carga).
* **Power BI:** Ferramenta principal para:
    * Modelagem de dados.
    * Validação de hipóteses através de análises e gráficos exploratórios.
    * Construção de um dashboard interativo.
    * Geração de insights e recomendações.
* **SQL:** Linguagem utilizada para consultas e manipulação de dados no BigQuery.
* **Google Slides:** Para a criação da apresentação executiva dos resultados.

### **Fontes de Dados**

O projeto utilizou um dataset que combina informações de:
* `track_in_spotify`: Dados de faixas no Spotify, incluindo streams.
* `track_in_competition`: Dados de faixas em outras plataformas (Deezer, Apple Music, Shazam).
* `track_technical_info`: Informações técnicas e características musicais das faixas (BPM, energia, etc.).

### **Estrutura do Projeto**

O projeto seguiu as seguintes etapas principais:

1.  **Coleta e Importação de Dados:**
    * Conexão e importação das 3 tabelas para o Google BigQuery.
2.  **Tratamento de Dados (BigQuery):**
    * Identificação e tratamento de valores nulos (ex: `in_shazam_charts`, `key`).
    * Identificação e tratamento de valores duplicados.
    * Padronização e limpeza de dados (ex: coluna `streams_limpo` para streams numéricos).
    * Conversão de tipos de dados (ex: datas).
3.  **Modelagem de Dados (Power BI):**
    * Unificação das tabelas em um modelo relacional para análise conjunta.
    * Criação de novas colunas calculadas (DAX) para métricas e categorias (ex: `participacao_total_playlist`, `categoria_participacao`).
4.  **Análise de Hipóteses e Visualização (Power BI):**
    * **KPIs Gerais:** Scorecards com `Soma de Streams (489 Bi)`, `Total Músicas (953)`, `Qtdade de Artistas (645)`, `Participação em Playlist (5,65 Mil)`.
    * **Hipóteses Validadas:**
        * **Participação em Playlists x Streams:** Correlação positiva forte. Músicas com maior participação em playlists geram mais streams.
        * **Total de Músicas por Artista x Streams:** Correlação positiva. Artistas com mais músicas tendem a ter mais streams.
        * **Sucesso Multiplataforma:** Correlação positiva entre ranking no Spotify e presença/rankings em Deezer e Apple Music.
    * **Hipóteses Não Suportadas:**
        * **BPM x Streams:** Não houve correlação significativa.
        * **Características Musicais x Streams:** Características como `energy`, `danceability`, `valence` não mostraram influência direta no volume de streams.
5.  **Geração de Conclusões e Recomendações:**
    * Baseado nos insights validados, foram elaboradas recomendações estratégicas para gravadoras e artistas.
6.  **Apresentação dos Resultados:**
    * Criação de slides executivos no Google Slides.
    * Gravação de vídeo individual apresentando as conclusões e recomendações do projeto.

### **Como Acessar o Projeto**

* **Dashboard Power BI:** [Incluso no repositorio]
* **Apresentação:** [https://docs.google.com/presentation/d/1qtvKDhojUo7fP1rrm3FbjyHRUsFtdOzZ8F9M4-ApZy0/edit?usp=drive_link]
* **Vídeo da Apresentação:** [https://www.loom.com/share/9881ed4619d541f094e24e88e6140014?sid=2aa4e0ca-b124-4ce9-b299-57aa330f588c]
* **Código/Arquivos:**
    * `[Incluso no Repositorio]` - Arquivo do Power BI Desktop.
    * `[https://console.cloud.google.com/bigquery?hl=pt-br&inv=1&invt=Ab3JMw&project=projeto2laboratoria&ws=!1m5!1m4!1m3!1sprojeto2laboratoria!2sbquxjob_579bbb01_197c8e78a0e!3sUS]` - Scripts SQL utilizados no BigQuery.
    

### **Feito por**

* **Vanessa Mendes da Silva**
* **Ariana Avelino**


---
