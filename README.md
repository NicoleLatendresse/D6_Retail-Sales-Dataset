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

1️.A lot of retail especially in the cateogies of 'Beauty,' 'Clothing' and 'Electonics' would skew more towards either Male or Female as their target demogrpahic. This dataset is very balanced at Female/Male = 510/490. This would be rare in most retail

2.Customer age typically runs the gamut anywhere between as young as 12 to as old as 85, especicially in these generic cateogires which signal a more 'general retailer' but in this dataset the range is only 18-64 which suggests maybe outliers were taken out of the dataset which we don't know

3.'Beauty', 'Clothing', and 'Electonics' are the only 3 product cateogries in the dataset which seems like an odd mix of categories for any one retailer suggesting cateogires are missing. This would not give a full picture of the total customer basket and customer profile

4.The mean is 2.51 and the range of quantities is only 1-4, there are typically a small portion of customers that would purchase in bulk, stocking up on products or buying for a group of people or a business. Sometimes retailers put on a limit on the max quantity of a product any one customer can purchase, we don't know if this is the cause for the small quantity range 

5.Pricing seems odd for retail with price points of 25,30,50,300,500. Pricing normally has two decemicals such as .99 (24.99, 29.99, etc.). The dataset does not specify if promo pricing, regular pricing, etc. was used 

6.Total amounts for all transactions are exactly the calculation of quantity multiplied by price, but typically there would be tax, service fees, environmental fees, shipping, etc. included in the total price not shown in the retail price

7.There are no missing data points. In retail, it's common for failed transactions to occur, such as failed payment, returns, cancelled orders, etc.

8.1000 rows and 1000 unique customer IDs means that each customer only transacted once in one year, which might be normal for high price points such as the 300,500, but would be unlikely for the lower price points of 25,30,50, since there would typically be at least a small subset that would be 'loyal/high value customers' which would normally tranact more than once a year for the 'Beauty' and 'Clothing' categories. Does this mean the dataset is limited to just the customer IDs first purchase, the last purchase, etc. Or does the system assign a new customer ID each time a customer transacts? If it truely is only one transaction occured per true unique customer, the dataset is not robust or long enough to support customer lifecycle analysis, any repeat purchasing pattern analysis or repeat purchase planning. One transaction per customer limits patterns on customer behavior. 



4. How you will approach the analysis.
Analyze the dataset using 2 different classification methods (logistic regression and random forest). Evaluate the performance of each model using cross-validation, then fit the best performing model to the training dataset and evaluate using a confusion matrix. 

5. Breakdown of roles/tasks assigned to each team member - see project task break down below
[Aram, Sunday 2 pm]


Project Plan
    
1. Understand the business context
2. Identify an opportunity
3. Scope your analysis

4. Develop your solution

5. Present clear results and recommendations
    
    Classification: Can we predict the product category a customer is likely to purchase based on their age, gender/sex, and previous purchase history?

    What value does your project bring to the industry?
    
    How will you answer your business question with your chosen dataset?
    
    What are the risks and uncertainties?
    
    What methods and technologies will you use?
-------------------
Tech Setup:

Create .venv 
    requirement.txt file from visualiation module [Mary]
    copy it into D6_RETAIL... folder

code:
uv venv --python 3.11
uv pip install -r requirements.txt 



if we see underline under a library comment, it would tell us what packages we are missing. we can then use following command:
    use uv pip install <package name>

we'll put .venv inside gitignore file

EVERYONE: after clone/fetch from Main you can get the updated file (requierement.text and gitignore) that Mary pushed up 02-25

------------------------
    Project Plan
    Task Break-Down
    
    README  file for Monday [Aram, Sunday; Mary to review after Aram

    1- Data Cleanup (may include data processing)
    Mary [core work]
    Nicole [reviewer, update if needed]

    2- Exploratory Analysis
        use visualization to get sense of data 
        in depth analsysis (plotting variables, check for outliers, check for any correlation) [Junaid, Saturday EOD]
        Review by Mary [Sunday]

    3- Data Processing, if needed 
    Nicole [ continue from ]
    Aram]

    4- Classification [Nicole, Saturday + Aram's Review, Sunday]
    
    5- Training and Cross-Validation [Nicole + Aram's Review Sunday]

    6- Reproducibility [Aram; Review by Junaid]

    7- Visulation [Pavi + Junaid]
        select style

    8- Final Cleanup of Folders
        remove duplicate plots, ...

Good Project Example: 
https://github.com/sunshinesharon/Customer-Purchasing-Behaviors


For Final Readme for final submission: 

Crafting a Comprehensive Main README File (slide 31-33 of first project session)

Purpose & Overview:
    Introduce the project with essential details, concise descriptionand a project objective.
Goals & Objectives:
    Articulate what the project aims to achieve.
Techniques & Technologies:
    Highlight the tools and methods used.
Key Findings & Instructions:
    Summarize outcomes and provide setup instructions.
Visuals & Credits:
    Enhance with visuals; acknowledge contributors.




    
