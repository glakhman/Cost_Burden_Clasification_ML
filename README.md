# 🏠 Cost Burden Classification (ML Project)

## 1. Problem Statement  
This project explores whether **housing cost burden** (whether a household is cost-burdened or not) can be predicted using features like income, rent, and household characteristics.

> A household is *cost-burdened* if it spends more than 30% of its gross income on housing (rent, mortgage, utilities, etc.).

The goal: **Classify** households as cost-burdened or not using machine learning.

---

## 2. Dataset  
- **Source**: *Kaggle – Charlotte Housing Data* (`clt_housing_cleaned.csv`)  
- **Key features**:  
  - `HINCP`: Household income  
  - `RNTP`: Gross rent  
  - `HHT`, `PUMA`: Demographic categorical codes  
  - `COST_BURDALL`: Target variable (1 = cost burdened, 0 = not)

---

## 3. Preprocessing  
- Removed irrelevant column: `TEN`  
- Converted income to monthly: `HINCP / 12`  
- Encoded `HHT` and `PUMA` using `pd.get_dummies()` for modeling  
- Split dataset into features (`X`) and target (`y`), then into training/testing sets

---

## 4. Data Understanding & Visualization  
- Used `pairplot` and `scatterplot` to explore feature relationships  
- 📌 **Insight**: High rent + low income often results in cost burden  
- Helped identify `RNTP` and `HINCP` as key features

---

## 5. Modeling  
- **Model**: Decision Tree Classifier  
- ✅ Pros: Easy to interpret, handles non-linear relationships  
- ❌ Cons: Can overfit on training data  
- Trained using `train_test_split` and evaluated with 10-fold cross-validation

---

## 6. Evaluation  
- Evaluation metrics: `.score()` and average accuracy from cross-validation  
- Feature importance: `HINCP` and `RNTP` ranked highest  
- ✔️ The model performed reasonably well (see notebook for detailed results)

---

## 7. Results & Insights  
- The model effectively classified cost-burdened households  
- Confirmed that basic housing and income data can predict affordability pressure

---

## 8. Potential Impact  
- Can assist **housing agencies** in identifying at-risk populations  
- ⚠️ Important to consider bias and ethical use of predictions

---

## 📌 To Run
1. Clone this repo  
2. Install dependencies (`scikit-learn`, `pandas`, `seaborn`, `matplotlib`)  
3. Open and run the notebook

---

*Made with ❤️ using Python and Scikit-Learn*
