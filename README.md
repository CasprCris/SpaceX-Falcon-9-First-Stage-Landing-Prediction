# SpaceX-Falcon-9-First-Stage-Recovery
#### Disclaimer
This is a guided project and part of the IBM Data Science Professional Certificate: https://www.coursera.org/professional-certificates/ibm-data-science. It is the final step of a 10 course Certification route and a demonstration of all aquired skills e.g.:
1. Data Collection using API calls and Webscraping
2. Data Wrangling
3. Exploratory Data Analysis using Pandas, Matplotlib and Seaborn
4. Exploratory Data Analysis using SQL Magic
5. Interactive Visual Analytics with Plotly Dash and Folium Maps
6. Machine Learing Predictions using four different Models and comparing their performance: Logisitc Regression, SVM, Decision Tree and KNN.

## Project Overview
This repository contains the culmination of the 10-course IBM Data Science Professional Certificate. The goal of this capstone project is to predict the success of SpaceX Falcon 9 first-stage landings, helping competitor aerospace companies estimate launch costs more accurately.
---
## Business Case
SpaceX can reuse the first stage of its Falcon 9 rockets, allowing them to advertise launch costs of around $62 million, whereas other providers cost upwards of $165 million. To help a competing commercial launch provider compete on price, this project builds four predictive models to determine if the first stage will land successfully, allowing the company to accurately estimate launch costs and bid effectively against SpaceX.
---
## 🛠️ Tech Stack & Skills
* **Data Wrangling & API Integration:** Python, Requests, Beautiful Soup, Pandas, NumPy
* **Exploratory Data Analysis (EDA):** SQL (IBM DB2 / SQLite), Pandas, Matplotlib, Seaborn
* **Interactive Data Visualization:** Folium (Geospatial maps), Plotly Dash (Interactive dashboards)
* **Machine Learning:** Scikit-Learn (Logistic Regression, SVM, Decision Trees, K-Nearest Neighbors)
---
## 🚀 Data Pipeline & Methodology
### 1. Data Collection & API Integration
* Gathered data from the SpaceX API regarding rocket launches, payloads, and landing outcomes.
* Supplemented dataset via web scraping Wikipedia for Falcon 9 launch records using BeautifulSoup.

### 2. Exploratory Data Analysis (EDA) & SQL
* Handled missing values (e.g., imputing payload mass averages).
* Executed SQL queries to analyze launch site success rates, total payload mass variations, and correlation between orbit types and landing success.

### 3. Interactive Visual Analytics
* **Folium:** Built geospatial maps to pinpoint launch site proximity to coastlines and railways, analyzing safety buffer zones.
* **Plotly Dash:** Developed a live dashboard featuring dropdown menus and range sliders to filter landing success rates by payload mass and launch site.

### 4. Predictive Modeling & Evaluation
* Standardized features using `StandardScaler`.
* Tuned hyperparameters for four algorithms using `GridSearchCV`:
  * Logistic Regression
  * Support Vector Machine (SVM)
  * Decision Tree Classifier
  * K-Nearest Neighbors (KNN)
 ---
 ## 📈 Key Insights & Results
### Model Performance Comparison

| Model | Accuracy (Train Set) | Accuracy (Test Set) | Best Hyperparameters |
| :--- | :---: | :---: | :--- |
| **Decision Tree** | 86.1% | **83.3%** | `criterion: gini`, `max_depth: 4` |
| **SVM** | 84.8% | **83.3%** | `C: 1.0`, `kernel: rbf` |
| **Logistic Regression** | 84.6% | **83.3%** | `C: 0.1`, `penalty: l2` |
| **KNN** | 84.8% | **83.3%** | `n_neighbors: 10`, `algorithm: auto` |

> While all models achieved a solid **83.3% test accuracy**, the **Decision Tree Classifier** slightly outperformed the others during training phase tuning. The primary features driving successful landings were **Payload Mass** and proximity to specific **Launch Sites** (e.g., KSC LC-39A - Kennedy Space Center - showing higher success rates).
---
#### Remarks
1. The Data collected via webscarping contains Falcon 9 AND Falcon 9 heavy launch data. The "Data Collection" approach collects Falcon 9 only.
2. Sometimes there are large cell outputs, which are really unconvenient to read, but unfortunately were required for the individual tasks.
3. To view Interactive Visualizations (Folium) copy link to https://nbviewer.org/
4. Dashboard Screenshots (Plotly Dash) below:
<img width="1897" height="701" alt="allsites" src="https://github.com/user-attachments/assets/ca01050f-1471-4d07-8702-2ba321b06bf0" />
<img width="1892" height="668" alt="Payload all sites" src="https://github.com/user-attachments/assets/9d303176-053a-40d6-809b-aeb581b6dfc6" />
<img width="1876" height="751" alt="ccafs2" src="https://github.com/user-attachments/assets/1180c0fd-6085-43f3-a130-12034d935d83" />
<img width="1897" height="726" alt="KSC" src="https://github.com/user-attachments/assets/bcdb231a-c0fa-40cc-9ad8-2e91acdea698" />
<img width="1885" height="763" alt="VAFB" src="https://github.com/user-attachments/assets/6edd6730-8c49-4365-be38-8e8ef15585d9" />
<img width="1883" height="701" alt="ccafs1" src="https://github.com/user-attachments/assets/86fa8b4e-9cd7-4d28-a1bc-21d673addc7b" />
<img width="1886" height="672" alt="Payload ccafs2" src="https://github.com/user-attachments/assets/15ca7c17-829d-46d0-92d4-a5fe98f193ef" />
<img width="1893" height="676" alt="Payload KSC" src="https://github.com/user-attachments/assets/38d46a63-b002-492c-93c5-f5172cb83e36" />
<img width="1890" height="671" alt="Payload vafb" src="https://github.com/user-attachments/assets/22ed8478-f063-4514-9b7e-979525993e40" />
<img width="1894" height="682" alt="Payload ccafs1" src="https://github.com/user-attachments/assets/41a9b747-2365-4623-ad04-077a167cda51" />
