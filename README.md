# Retail Sales Behavior Prediction  
**Data Science Institute – Cohort 8 – Group 6**

---

# Team Members
- Aram Dezfuli  
- Junaid Ghani  
- Nicole Latendresse  
- Mary Randle  
- Pavi Chandrasegaram  

---

# Project Overview

This project analyzes customer retail transaction data to explore whether customer demographics and purchasing behavior can be used to predict the **product category** a customer is most likely to purchase.

Using a retail dataset containing demographic information and transaction details, we applied exploratory analysis, visualization techniques, and machine learning classification models to evaluate whether meaningful predictive patterns exist.

The goal is to better understand customer purchasing behavior and assess whether such insights could support **targeted marketing strategies, product recommendations, and customer segmentation** in a retail environment.

---

# Business Objective

Retailers frequently seek to understand how customer characteristics influence purchasing decisions. If businesses can anticipate what type of products customers are most likely to buy, they can improve marketing campaigns, optimize product recommendations, and enhance personalized shopping experiences.

The primary business question addressed in this project is:

**Can we predict the product category a customer is likely to purchase based on demographic attributes and transaction-related features?**

Although the dataset is simplified, the project demonstrates how data science methods can be used to investigate customer purchasing patterns.

---

# Stakeholders

Potential stakeholders for this analysis include:

- Marketing teams seeking to improve targeted campaigns  
- Product managers responsible for category performance  
- Customer analytics teams studying purchasing behavior  
- Retail strategists looking to improve personalization  

Insights from this analysis could help stakeholders better understand how customer characteristics relate to purchasing patterns.

---

# Dataset

The dataset used in this project is the **Retail Sales Dataset** available on Kaggle.

Source:  
https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset

### Dataset Characteristics
- 1000 retail transactions
- Each transaction represents a unique customer
- Product categories include:
  - Beauty
  - Clothing
  - Electronics

### Key Features
- Customer ID
- Age
- Gender
- Product Category
- Quantity
- Price per Unit
- Total Amount

### Dataset Limitations

Several characteristics of the dataset limit real-world generalization:

- Each customer appears only once (no repeat purchase history)
- Only three product categories are represented
- The dataset contains no missing values or failed transactions
- Age range is limited (18–64)
- Pricing structure appears simplified

These constraints reduce the behavioral depth available for modeling and may impact predictive performance.

---

# Techniques and Technologies

The project was implemented using the following tools and libraries:

### Programming Language
- Python

### Libraries
- **Pandas** – data manipulation and preprocessing  
- **NumPy** – numerical operations  
- **Matplotlib** – basic data visualization  
- **Seaborn** – statistical visualization  
- **Plotly** – interactive and accessible visualizations  
- **Scikit-Learn** – machine learning models and evaluation  

### Development Environment
- Jupyter Notebook
- Git and GitHub for version control and collaboration

---

# Methodology

The project followed a structured data science workflow:

1. **Business Understanding**  
   Define the analytical objective and identify the key prediction problem.

2. **Data Exploration and Validation**  
   Review dataset structure, verify data quality, and identify potential limitations.

3. **Exploratory Data Analysis (EDA)**  
   Examine distributions, relationships, and potential predictors.

4. **Feature Preparation**  
   Prepare variables for modeling through encoding and preprocessing.

5. **Model Development**  
   Train classification models to predict product category.

6. **Model Evaluation**  
   Assess model performance using standard evaluation metrics.

7. **Visualization and Interpretation**  
   Communicate insights through clear and accessible visualizations.

---

# Exploratory Data Analysis

Exploratory data analysis was conducted to understand the distribution of demographic and transactional variables and to identify potential predictive relationships.

### Key Observations

- **Age distribution** is relatively balanced across the dataset but limited to customers aged 18–64.
- **Purchase quantity** is typically small, with most customers buying three or fewer items.
- **Price per unit** shows that most purchases are low-value items, with a smaller number of higher-priced transactions.
- **Total transaction amount** is strongly right-skewed, indicating a small number of high-value purchases.
- **Gender differences** appear primarily in Beauty purchases, which show a female skew.

Despite some observable patterns, product categories show significant overlap across demographic and transactional variables.

This suggests that predicting product category will require combining multiple features rather than relying on a single strong predictor.

---

# Data Visualization

Data visualization played an important role in both **exploring patterns** and **communicating insights** from the dataset.

Visualizations were created using **Matplotlib, Seaborn, and Plotly**, with attention to readability and accessibility, including color-blind-friendly palettes.

One key visualization is a **stacked bar chart** illustrating the distribution of product category purchases across five age groups:

- 18–24  
- 25–34  
- 35–44  
- 45–54  
- 55–64  

### Observed Patterns

- Customers aged **45–54** show the highest overall purchasing activity.
- The **18–24** age group has the lowest purchase counts.
- **Clothing purchases remain relatively consistent** across age groups.
- **Electronics purchases increase among middle-age customers**.

Although these visualizations highlight demographic patterns, the distributions still overlap significantly across product categories.

---

# Classification Modeling

To predict product category, we implemented a **supervised classification approach** using logistic regression.

### Model Inputs
The model used the following predictors:

- Age  
- Gender  
- Transaction-related features (such as purchase amount)

### Model Evaluation Metrics
Model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Model Performance

- **Accuracy:** ~37%  
- **F1 Score:** ~0.35  

Since there are three product categories, random guessing would yield an expected accuracy of approximately **33%**.

The model therefore performs only slightly better than random classification.

The confusion matrix shows that the model frequently confuses **Clothing and Electronics**, while **Beauty** products are often misclassified into the other categories.

---

# Key Findings

Several insights emerged from the analysis:

- Demographic variables such as **age and gender provide limited predictive power**.
- Transaction-level variables show **some signal but still overlap heavily across categories**.
- The absence of repeat purchase history significantly reduces behavioral insight.
- Product categories in the dataset are not clearly separable using the available features.

These findings suggest that **the available variables are insufficient for strong predictive modeling**.

---

# Recommendations

For improved predictive performance in real-world applications, future analyses should consider:

- Incorporating **repeat purchase behavior**
- Expanding the number of **product categories**
- Including **customer browsing behavior**
- Adding **temporal information** such as purchase dates
- Integrating **customer loyalty or engagement metrics**

Richer behavioral data would significantly improve the ability to model customer purchasing patterns.

---

# Conclusion

This project explored whether customer demographics and transaction data could predict product category purchases.

The classification model achieved modest predictive performance, only slightly exceeding random guessing. This outcome reflects the limited predictive information available in the dataset, particularly the absence of repeat customer behavior and the restricted number of product categories.

Despite these limitations, the project demonstrates the application of a full data science workflow, including exploratory analysis, visualization, feature preparation, and classification modeling.

Future work using larger and more behaviorally rich datasets could significantly improve predictive performance and provide stronger insights for retail decision-making.

---

## Individual Presentation Videos

| Name | Link |
|-----|-----|
| Aram Dezfuli | [Video Link](PASTE_LINK_HERE) |
| Junaid Ghani | [Video Link](PASTE_LINK_HERE) |
| Nicole Latendresse | [Video Link](PASTE_LINK_HERE) |
| Mary Randle  | [Video Link](PASTE_LINK_HERE) |
| Pavi Chandrasegaram  | [Video Link](PASTE_LINK_HERE) |

---

## Setup Instructions (Optional)

1. Clone the repository
   git clone https://github.com/your-repo/D6_Retail-Sales-Dataset.git

2. Navigate to the project folder
   cd D6_Retail-Sales-Dataset

3. Install dependencies
   pip install -r requirements.txt

4. Open the Jupyter notebooks in the `experiments/` folder to reproduce the analysis.








    
