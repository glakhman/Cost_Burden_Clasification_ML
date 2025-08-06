________________________________________

1. Introduce the Problem
In this project, I explored whether housing cost burden (classified as cost burdened* or not) can be predicted using features related to income, rent, and household characteristics. The main question I wanted to answer was: Can we accurately classify if a household is cost burdened based on available housing and demographic data?
*A household is considered cost-burdened when it spends more than 30% of its gross income on housing costs, including rent, mortgage payments, property taxes, utilities, and other housing-related expenses.
________________________________________
2. Introduce the Data
The dataset is from Kaggle: Charlotte housing data (clt_housing_cleaned.csv).
Key features include:
•	HINCP: Household income
•	RNTP: Gross rent
•	HHT, PUMA: Categorical demographic codes
•	COST_BURDALL: Target variable (1 = cost burdened, 0 = not)
________________________________________
3. Pre-processing the Data
•	Removed TEN column (irrelevant).
•	Converted income from yearly to monthly (HINCP/12).
•	Used pd.get_dummies() to transform the categorical columns HHT and PUMA into binary (0/1) columns, enabling the model to interpret these features numerically. 
•	Split data into features (X) and target (y), then into training and testing sets.
________________________________________
4. Data Understanding / Visualization
Used pairplot and scatterplot to explore the relationship between rent, income, and cost burden.
Key insight: Higher rent with lower income mostly results in cost burden.
This helped in selecting important variables like RNTP and HINCP for modeling.
________________________________________
5. Modeling
Used a Decision Tree Classifier for its interpretability and ease of visualization.
Pros:
•	Easy to understand
•	Handles non-linear data
Cons:
•	Prone to overfitting
Trained the model using train_test_split and evaluated with cross-validation (cv=10).
________________________________________
6. Evaluation
•	Used .score() (accuracy) and 10-fold cross-validation.
•	Final accuracy: ~(score printed in code, placeholder).
•	Feature importance showed HINCP and RNTP as most influential features.
________________________________________
7. Storytelling
The model helped show how income and rent strongly influence cost burden.
Yes, the project answered the original question — it’s possible to predict cost burden using basic housing data.
________________________________________
8. Impact Section
The model can help policy-makers and housing agencies target assistance to at-risk households.
However, it’s important to avoid bias from incomplete or outdated data, and ensure fair use of predictions in real-world decisions.

.

