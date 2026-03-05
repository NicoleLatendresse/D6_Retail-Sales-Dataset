# D6_Retail-Sales-Dataset

# Retail Sales Behaviour Predition 
Data Science Certificate Cohort 8 - Group 6 

## Group Members: 

* Aram Dezfuli
* Junaid Ghani
* Nicole Latendresse
* Mary Randle
* Pavi Chandrasegaram


## Business Motivation 
The goal of this project is to develop a classification model to predict the product category a customer most likely is to purchase based on demographic attributes, such as age and gender/sex, and their previous purchasing history.  

The insights from this analysis will then inform and enhance the business strategies to increase customer engagement by supporting the development of targeted product recommendations, tailored marketing campaigns to provide personalized customer interactions which in turn will increase customer engagements and ultimately drive higher sales. 


## Source
The dataset  used in this project is the Retail Sales Dataset from Kaggle: https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset


## Risks or Unknowns Identified

1. A lot of retail especially in the cateogies of 'Beauty,' 'Clothing' and 'Electonics' would skew more towards either Male or Female as their target demogrpahic. This dataset is very balanced at Female/Male = 510/490. This would be rare in most retail

2. Customer age typically runs the gamut anywhere between as young as 12 to as old as 85, especicially in these generic cateogires which signal a more 'general retailer' but in this dataset the range is only 18-64 which suggests maybe outliers were taken out of the dataset which we don't know

3. 'Beauty', 'Clothing', and 'Electonics' are the only 3 product cateogries in the dataset which seems like an odd mix of categories for any one retailer suggesting cateogires are missing. This would not give a full picture of the total customer basket and customer profile

4. The mean is 2.51 and the range of quantities is only 1-4, there are typically a small portion of customers that would purchase in bulk, stocking up on products or buying for a group of people or a business. Sometimes retailers put on a limit on the max quantity of a product any one customer can purchase, we don't know if this is the cause for the small quantity range 

5. Pricing seems odd for retail with price points of 25,30,50,300,500. Pricing normally has two decemicals such as .99 (24.99, 29.99, etc.). The dataset does not specify if promo pricing, regular pricing, etc. was used 

6. Total amounts for all transactions are exactly the calculation of quantity multiplied by price, but typically there would be tax, service fees, environmental fees, shipping, etc. included in the total price not shown in the retail price

7. There are no missing data points. In retail, it's common for failed transactions to occur, such as failed payment, returns, cancelled orders, etc.

8. 1000 rows and 1000 unique customer IDs means that each customer only transacted once in one year, which might be normal for high price points such as the 300,500, but would be unlikely for the lower price points of 25,30,50, since there would typically be at least a small subset that would be 'loyal/high value customers' which would normally tranact more than once a year for the 'Beauty' and 'Clothing' categories. Does this mean the dataset is limited to just the customer IDs first purchase, the last purchase, etc. Or does the system assign a new customer ID each time a customer transacts? If it truely is only one transaction occured per true unique customer, the dataset is not robust or long enough to support customer lifecycle analysis, any repeat purchasing pattern analysis or repeat purchase planning. One transaction per customer limits patterns on customer behavior. 


## Analysis Approach
To answer our business question, we will frame this as a supervised classification problem. 

We will:
- Develop two classification models:
    - Logistic Regression
    - Random Forest Classifier
- Evaluate both models using cross-validation
- Compare performance using relevant factors such as:
    - Accuracy
    - Precision
    - Recall
    - F1-score
- Select the best-performing model
- Evaluate final performance using a confusion matrix

This approach allows us to compare a linear model (logistic regression) with a non-linear ensemble method (random forest) to determine which better captures patterns in customer purchasing behavior.


## Project Plan

Our project follows a structured data science workflow:
1. Understand the business context
2. Identify the analytical opportunity
3. Define scope and assumptions
4. Develop predictive models

### Business Question

Can we predict the product category a customer is likely to purchase based on age, gender, and purchase-related features?

### Value to Industry
If successful, this model can:
- Support targeted marketing campaigns
- Improve product recommendation systems
- Enhance customer personalization strategies
- Increase engagement and conversion rates

### Project Risks & Uncertainties
- Synthetic or simplified dataset structure
- Limited product categories (3 only)
- One transaction per customer
- No missing or real-world noise in data
- No repeat purchase behavior

These factors may limit generalizability to real-world retail environments.


### Project Management Approach

We followed a structured yet iterative workflow. 

The overall project scope and task breakdown were defined upfront; however, modeling and analysis were developed iteratively with continuous review and refinement.

Work was completed in pairs for major task groups. All changes were implemented using feature branches and submitted via pull requests to ensure version control integrity and peer review prior to merging into the main branch.

## Project Task Breakdown & Roles

### 1. README  (Midpoint Submission)
- Lead – Aram
- Mary – Review
- Tasks:
    - Contents 1-2-3 - Pavi, Mary, Nicole
    - Other Contents - Aram
    - Compile - Aram
    - Review - Mary

### 2. Data Cleanup & Preparation
- Lead: Mary
- Reviewer: Nicole
- Tasks:
    - Data validation
    - Feature formatting
    - Outlier check
    - Data consistency verification

### 3. Exploratory Data Analysis (EDA)
- Lead: Junaid
- Reviewer: Pavi
- Tasks:
    - Visual exploration
    - Distribution analysis
    - Correlation analysis
    - Outlier detection

### 4. Feature Engineering & Processing
- Lead: Nicole – Lead
- Reviewer: Mary
- Support: Aram
- Tasks:
    - Encoding categorical variables
    - Scaling if required
    - Train/test split preparation

### 5. Classification Modeling
- Lead: Nicole
- Reviewer: Aram, Junaid
- Models:
    - Logistic Regression
    - Random Forest

### 6. Training & Cross-Validation Implementation
- Lead: Nicole
- Reviewer: Aram, Pavi 
- Tasks
    - k-fold cross-validation
    - Model comparison
    - Performance metrics evaluation

### 7. Visualization & Styling
- Lead: Pavi
- Support: Junaid
- Reviewer: Junaid
- Tasks:
    - Plot styling
    - Clean presentation charts
    - Model comparison visuals

### 8. Reproducibility & Repository Cleanup
- Lead: Aram (-> Junaid)
- Reviewer: Junaid (-> Aram)
- Tasks: 
    - Folder structure cleanup
    - Removing duplicate plots
    - Ensuring clear README instructions
    - Requirements.txt validation

### 9. Final Submission - README file 
- Lead: Aram
- Reviewer: Mary
- Tasks: 
  - Review course slides and provided examples
  - Confirm submission expectations with instructor and Learning Support (LS)
  - Draft and structure final README content
  - Incorporate feedback
  - Final formatting and repository cleanup


### 10. Final Live Presentation 
- Leads: Pavi, Mary
- Supports: Junaid, Aram




----------------

## Reference Notes [Remove form final submission]
### Tech Setup Hints:

1. Create .venv 
    requirement.txt file from visualiation module [Mary]
    copy it into D6_RETAIL... folder

2. Run codes:
    uv venv --python 3.11
    uv pip install -r requirements.txt 

3. If we underline under a library command, it would mean what packages we are missing. WE can then use following command:
    use uv pip install <package name>


------------------------
    

### For Final README: 

Crafting a Comprehensive Main README File (see slide 31-33 of first project session)

- Purpose & Overview:
    Introduce the project with essential details, concise descriptionand a project objective.
- Goals & Objectives:
    Articulate what the project aims to achieve.
- Techniques & Technologies:
    Highlight the tools and methods used.
- Key Findings & Instructions:
    Summarize outcomes and provide setup instructions.
- Visuals & Credits:
    Enhance with visuals; acknowledge contributors.


Good Project Example: 
https://github.com/sunshinesharon/Customer-Purchasing-Behaviors






    
