# real_estate_price_predicion

# Real Estate Price Prediction 
This project, developed during the university course in Data Mining and Text Analytics, aims to predict house prices in the city of Milan. The objective is to provide a data-driven approach to pricing newly listed properties, avoiding reliance solely on heuristics.

## 🚀 About Me
I am a student passionate about Data Science and Machine Learning. This project represents a practical application of my knowledge, with the goal of building reproducible and adaptable predictive models for real estate pricing.

## 📚 Appendix
Real Estate Price Prediction Project Description
The project aims to analyze and predict real estate prices in Milan using Machine Learning models. Data cleaning, feature engineering, and predictive modeling processes are performed.
Key Steps
1. Data Loading and Cleaning
    * Import the dataset containing Milan real estate prices.
    * Remove columns with more than 25% missing values to ensure data quality.
    * Standardize column names to lowercase.
    * Save the cleaned dataset for future use.
2. Feature Engineering
    * Create new features derived from existing ones (e.g., total_features).
    * Correct and normalize numerical values (e.g., area_m2, condominium fees).
    * Extract coordinates of properties to create a heatmap to visualize the distribution of properties and divide the city into a spatial grid for geographic data representation.
3. Dataset Splitting
    * Separate independent features (X) from the target variable (y).
    * Split the dataset into a training set (80%) and a test set (20%).
    * Standardize features to ensure consistency across models.
4. Model Training
    * Random Forest Regressor: A model based on decision trees for price prediction.
    * Linear Regression: A linear regression model to compare performance.
    * Train the models on the training data.
5. Performance Evaluation
    * Calculate error metrics for each model:
        * Mean Squared Error (MSE)
        * Mean Absolute Error (MAE)
        * Coefficient of Determination (R²)
    * Compare actual and predicted values using scatter plots.
6. Result Visualization
    * Generate comparison graphs between actual and predicted prices.
    * Add annotations with evaluation metrics to the graphs.
    * Divide the city into grids for better geographic analysis of prices.


# Requirements
* Python 3.x (or later version)
* A code editor (e.g., VS Code, PyCharm, jupyter notebook)

* # Project Execution
1 Create a Virtual Environment

Creating a virtual environment prevents dependency conflicts:
```bash
python -m venv venv
source venv/bin/activate  # On Mac/Linux
venv\Scripts\activate  # On Windows
#i've created the venv using anaconda navigator like so:
"conda create -n realestate" 
"conda activate realestate"
```
2. Load and clean the data.
3. Create new features and normalize values.
4. Split the dataset into training and test sets.
5. Train Machine Learning models.
6. Evaluate performance and visualize results.

The project provides a data-driven approach to predicting real estate prices, combining Machine Learning techniques and geographic analysis.


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
```
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
```
