# real_estate_price_predicion

# Real Estate Price Prediction 
This project, developed during the university course in Data Mining and Text Analytics, aims to predict house prices in the city of Milan. The objective is to provide a data-driven approach to pricing newly listed properties, avoiding reliance solely on heuristics.

## 🚀 About Me
I am a student passionate about Data Science and Machine Learning. This project represents a practical application of my knowledge, with the goal of building reproducible and adaptable predictive models for real estate pricing.

## 📚 Appendix
This section provides additional details to ensure a step-by-step understanding and adaptability of the code. Below is the structured approach followed in the project:

### **1. Dataset Exploration and Cleaning**
- The code starts by displaying the columns and structure of the dataset.
- A preprocessing step was performed to clean verbose column names.
- An initial **Linear Regression** model was executed after encoding specific categorical variables:
  - One-hot encoding: `['condition', 'heating']`
  - Frequency encoding: `['neighborhood', 'street']`
- The initial set of features considered for prediction:
  ```python
  features = ['number_rooms', 'area_m2', 'bathrooms', 'floor_number', 'condominium fees',
              'year of construction', 'heating', 'condition_Excellent / Refurbished',
              'condition_Good condition / Liveable', 'condition_New / Under construction',
              'condition_Not open to participation', 'condition_Open to participate',
              'condition_To be refurbished']
  target = 'price_euro'
  ```

### **2. Feature Selection and Model Optimization**
- A second regression model was built with a **reduced number of features** and fewer categorical encodings:
  - One-hot encoding: `['heating']`
  - Frequency encoding: `['Energy Efficiency', 'neighborhood']`
- Updated feature set:
  ```python
  features = ['number_rooms', 'area_m2', 'bathrooms', 'floor_number', 'condominium fees', 'year of construction', 'Energy Efficiency']
  ```

### **3. Geospatial Feature Engineering**
- Extracted **property coordinates** and performed manual encoding on:
  - `Energy Efficiency`
  - `grid_cell` (coordinates categorized into numbered cells from 1 to 49)
  - `heating`
  - `condition`
- This approach ensures that newly entered data can be easily assigned the necessary characteristics for model predictions.

### **4. Feature Correlation and Mutual Information Analysis**
- A **correlation matrix** was generated to analyze relationships between variables.
- **Mutual information** was computed to determine the influence of features on the target price.

### **5. Grid-Based Model Enhancement**
- The city of Milan was divided into numbered grid cells based on extracted coordinates.
- **Regression models (Linear Regression & Random Forest) were retrained** using the new spatially categorized features.
- Initial models performed poorly, prompting further optimization.

### **6. Data Augmentation and Final Model Training**
- Focused on **grid cells 30 and 31**, which had high data density and similar characteristics.
- Extracted rows from these zones and **used ChatGPT to generate 20,000 synthetic records** that matched the existing data.
- Merged the synthetic data with the original subset, creating a dataset with **20,115 rows**.
- Trained final models on this enriched dataset:
  - **Linear Regression**
  - **Random Forest**

## ⚙️ Installation
### 1. Clone the repository
```bash
git clone <[repository_link](https://github.com/AleBragato/house_price_prediction.git)>
cd real_estate_price_prediction
```

### 2. Prerequisites
Ensure you have the following installed:
- Python (version 3.x or later)
- A code editor (e.g., VS Code, PyCharm)

### 3. Create a Virtual Environment
Creating a virtual environment prevents dependency conflicts:
```bash
python -m venv venv
source venv/bin/activate  # On Mac/Linux
venv\Scripts\activate  # On Windows
```

### 4. Install Required Libraries
```bash
pip install pandas scikit-learn matplotlib numpy geopandas shapely geopy seaborn
```

This project serves as both an academic exploration and a practical tool for real estate price prediction in Milan. 🌟

# 👥 acknowlegments

Alessandro Bragato

ChatGPT

GitHub Copilot

The dataset was obtained via web scraping by Amro Askar (Data Scientist & Machine Learning Engineer) and sourced from Kaggle. It is licensed under Apache 2.0.

# 📄 License
This project is licensed under the MIT License.

Copyright (c) 2025 Alessandro Bragato

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
