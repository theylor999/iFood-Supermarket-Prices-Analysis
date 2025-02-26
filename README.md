# iFood-Supermarket-Prices---Data-Science-Project
This project collects and analyzes supermarkets data from iFood across all regions in Brazil.

# 🛒 iFood Price Analysis - Data Science Project  

Este repositório documenta meu projeto de análise de preços de supermercados no iFood. Desde a coleta e processamento dos dados até a análise e visualização, utilizei técnicas de web scraping, ETL, banco de dados e data visualization.  

This repository documents my project on analyzing supermarket prices on iFood. From data collection and processing to analysis and visualization, I used web scraping, ETL techniques, databases, and data visualization tools.  

---

## 📌 1. Introdução | Introduction  

### 🎯 Objetivo | Goal  
O objetivo deste projeto foi analisar os preços de produtos vendidos em supermercados pelo iFood, o maior aplicativo de delivery do Brasil. Para isso, utilizei técnicas de web scraping para coletar os dados diretamente da plataforma, além de realizar tratamento e visualização das informações.  

The goal of this project was to analyze the prices of supermarket products sold through iFood, Brazil’s largest food delivery app. To achieve this, I used web scraping techniques to collect data directly from the platform, performed data processing, and created insightful visualizations.  

### 🚀 Tecnologias | Technologies  
- **Python** (requests, pandas, BeautifulSoup, SQLAlchemy, etc.)  
- **MySQL** (armazenamento de dados | data storage)  
- **AWS** (banco de dados na nuvem | cloud database)  
- **Tableau** (visualização de dados | data visualization)  

---

## 🔍 2. Coleta de Dados | Data Collection  

### 🕵️‍♂️ 2.1. Como funciona o iFood? | How iFood Works  

Para entender como o iFood exibe mercados e produtos, utilizei o **Inspecionar Elemento** no navegador (aba **Network**) para encontrar as APIs utilizadas pelo site.  

To understand how iFood displays supermarkets and products, I used the **Inspect Element** tool in the browser (**Network** tab) to find the APIs used by the site.  

✅ **Descobertas | Discoveries:**  
- O iFood usa **Google Maps** para converter endereços em coordenadas.  
- O site exibe mercados com base na distância do cliente.  
- Cada mercado tem uma **ID única**, usada para buscar os produtos vendidos.  

🖼️ **Print: Inspecionando o site do iFood**  
![Screenshot](./img/inspecionar_elemento.png)  

---

### 🌎 2.2. Obtendo Coordenadas | Getting Coordinates  

Para acessar mercados em todo o Brasil, precisei de coordenadas de todas as cidades. Cidades grandes precisaram de múltiplas coordenadas.  

To access supermarkets throughout Brazil, I needed coordinates for all cities. Larger cities required multiple coordinates.  

📂 **Resultado | Result:**  
- Um arquivo CSV com **X linhas**, cobrindo grande parte do Brasil.  

🖼️ **Print: CSV de coordenadas gerado**  
![Screenshot](./img/csv_coordenadas.png)  

---

## ⚙️ 3. Extração e Processamento | Extraction & Processing  

Após enviar coordenadas para o iFood, recebi listas de mercados e coletei os produtos vendidos em cada um.  

After sending coordinates to iFood, I retrieved lists of supermarkets and collected the products they sold.  

❗ **Desafios | Challenges:**  
- A resposta da API tinha **tags desatualizadas e irrelevantes**.  
- Usei técnicas de **data mining e ETL** para limpar os dados.  

✅ **Resultado | Result:**  
- Dados organizados com:  
  - Nome do produto | Product name  
  - Categoria (corredor) | Category (aisle)  
  - Preço | Price  
  - ID do mercado | Supermarket ID  

🖼️ **Print: Exemplo de dados brutos vs. dados processados**  
![Screenshot](./img/dados_processados.png)  

---

## 🗄️ 4. Armazenamento | Database Storage  

Armazenei os dados no **MySQL**, tanto localmente quanto na **AWS**.  

I stored the data in **MySQL**, both locally and in **AWS**.  

📊 **Estatísticas do banco de dados | Database Stats:**  
- **15M+ linhas | 15M+ rows** de dados coletados.  
- Queries SQL para:  
  - Calcular **preço médio por estado | average price per state**.  
  - Comparar **preços entre mercados | prices between supermarkets**.  
  - Obter **distribuição de preços por categorias | price distribution by category**.  

🖼️ **Print: Estrutura do banco de dados**  
![Screenshot](./img/banco_dados.png)  

---

## 📊 5. Visualização de Dados | Data Visualization  

Usei **Python e Tableau** para criar gráficos e entender a distribuição dos preços.  

I used **Python and Tableau** to create charts and understand the price distribution.  

📈 **Visualizações criadas | Visualizations:**  
- **Mapa de calor | Heatmap** de preços médios por estado.  
- **Comparação de preços | Price comparison** entre mercados.  
- **Evolução de preços | Price trends over time**.  

🖼️ **Print: Exemplo de visualização no Tableau**  
![Screenshot](./img/visualizacao_tableau.png)  

---

## 🎯 6. Conclusão | Conclusion  

Este projeto demonstrou técnicas de **web scraping, ETL, bancos de dados e visualização de dados** para analisar preços no iFood.  

This project demonstrated **web scraping, ETL, database management, and data visualization** techniques to analyze iFood prices.  

🚀 **Futuras melhorias | Future improvements:**  
- Automatizar a atualização dos dados | Automate data updates.  
- Aplicar machine learning para prever preços | Apply machine learning for price prediction.  
