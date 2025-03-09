# 🛒 iFood Supermarket Prices Analysis - Data Science Project  

This repository documents my project on analyzing supermarket prices on iFood. From data collection and processing to analysis and visualization, I used web scraping, ETL techniques, databases, and data visualization tools.  

---

## 📌 1. Introduction  

### 🎯 Goal  
The goal of this project was to analyze the prices of supermarket products sold through iFood, Brazil’s largest food delivery app. To achieve this, I used web scraping techniques to collect data directly from the platform, performed data processing, and created insightful visualizations.  

### 🚀 Technologies Used  
- **Python** (requests, pandas, matplotlib, SQLAlchemy, etc.)  
- **MySQL** (data storage)  
- **AWS** (cloud database)  
- **Tableau** (data visualization)  

---

## 🔍 2. Data Collection  

### 🕵️‍♂️ 2.1. How iFood Works  

To understand how iFood displays supermarkets and products, I used the **Inspect Element** tool in the browser (**Network** tab) to find the APIs used by the site.  

✅ **Key Discoveries:**  
- iFood uses **Google Maps** to convert addresses into coordinates.  
- The website displays available supermarkets based on customer distance and supermarket choices.  
- Each supermarket has a **unique ID**.  

🖼️ **Inspecting iFood’s website**  
![Screenshot](./img/inspect.png)  

---

### 🌎 2.2. Getting Coordinates  

To access supermarkets throughout Brazil, I needed coordinates for all cities. Larger cities required multiple coordinates.  

📂 **Result:**  
- A CSV file with **7267 rows**, covering a large part of Brazil.  

🖼️ **Generated coordinates CSV**  
![Screenshot](./img/coordenadas.png)  

---

## ⚙️ 3. Data Extraction & Processing  

After sending coordinates to iFood, I retrieved lists of supermarkets and collected the products they sold.  

❗ **Challenges:**  
- The API response contained **outdated and irrelevant tags**.  
- I used **data mining and ETL** techniques to clean the data.  

✅ **Result:**  
- Organized data including:  
  - **Product name**  
  - **Category (aisle)**  
  - **Price**  
  - **Supermarket ID**  

🖼️ **Raw vs. processed data**  
![Screenshot](./img/datas_comparison.png)  

---

## 🗄️ 4. Database Storage  

I stored the data in **MySQL**, both locally and in **AWS**.  

📊 **Database Stats:**  
- **15M+ rows** collected.
- **3791 Supermarkets** collected.

🖼️ **Database**
![Screenshot](./img/mysql_example.png)
<img src="./img/database_info.png" width="800">

---

## 📊 5. Data Visualization  

I used **Python and Tableau** to create charts and understand price distribution.  

🖼️ **Examples of visualizations I created**  
![Screenshot](./img/distribuição_corredor.png)  
![Screenshot](./img/distribuicao_precos.png)  
![Screenshot](./img/preco_medio_sp.png)  
![Screenshot](./img/quantidade_mercados_estado.png) 

---

## 🎯 6. Conclusion  

I believe iFood could invest more in expanding its network of supermarkets by adding establishments from different states. Currently, there are regions with only 1, 3, or even 0 supermarkets registered, which limits the options for consumers. Additionally, the product registration could be better organized. Many items appear in unexpected categories, such as combos that are placed in the wrong sections, making it harder for users to search and navigate. These improvements could provide a smoother and more comprehensive experience for consumers.

The most expensive section is the alcoholic beverages section, which was expected since there are very high-price drinks. There are several outliers in all sections, which may be due to the fact that many supermarkets place bulk products, such as combo packs, outside the designated combo aisle. However, soon I will be able to filter this using machine learning. We can see that most products are priced between R$ 8.00 and R$ 20.00. I'm curious to see how these charts will look different in a few months.

As we can see in the last chart, several states have very few supermarkets available on iFood, making it impossible to accurately analyze the true average prices in these markets using only iFood data. Therefore, I am developing a method to gather more supermarket data from these states, most likely by utilizing the official websites of the supermarkets. This will also allow me to compare their prices with those available on iFood.

This project demonstrated **web scraping, ETL, database management, and data visualization** techniques to analyze iFood prices.  

🚀 **Future improvements:**  
- Automate data updates.
- Find a new data source for more supermarkets.
- Apply machine learning for price prediction.  
