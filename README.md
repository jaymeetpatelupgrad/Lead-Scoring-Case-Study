# Lead Scoring Case Study

## Project Overview
This project involves analyzing and developing a lead scoring model for **X Education**, an online course provider. The goal is to identify leads most likely to convert into paying customers ("Hot Leads") from a pool of generated leads, thereby optimizing the sales process and increasing conversion rates. The solution was developed using logistic regression, supported by extensive data preprocessing, exploratory data analysis (EDA), and feature engineering techniques.

---

## Dataset Description
The dataset comprises approximately **9,000 rows** of lead data with the following key attributes:

- **Lead Source**: Origin of the lead (e.g., Google, Direct Traffic, Facebook, etc.)
- **Converted**: Target variable indicating conversion status (1 for converted, 0 for not converted)
- **Total Time Spent on Website**: Amount of time a lead spent on the website
- **Last Activity**: Most recent interaction by the lead
- **Total Visits**: Total number of visits made by the lead
- **Other Features**: Fields such as "Lead Quality," "Lead Origin," and demographic information

Key challenges in the dataset included missing values, placeholder values like "Select," and categorical variables requiring encoding.

---

## Steps Followed

### 1. **Data Preprocessing**
- **Handling Missing Values**:
  - Removed columns with a high percentage of missing data.
  - Imputed missing values where feasible.
- **Categorical Variables**:
  - Treated "Select" values as missing data.
  - Created dummy variables for categorical fields.
- **Feature Scaling**:
  - Scaled continuous variables using MinMaxScaler to normalize their values.

### 2. **Exploratory Data Analysis (EDA)**
- Analyzed the relationship between key features (e.g., time spent on the website, lead source) and conversion rates.
- Visualized feature distributions and correlations to identify trends and outliers.
- Found that leads with higher time spent on the website and certain activities (e.g., Email Opened) showed a higher likelihood of conversion.

### 3. **Model Building**
- **Logistic Regression**:
  - Chosen for its simplicity and interpretability in binary classification problems.
- **Feature Selection**:
  - Used Recursive Feature Elimination (RFE) to identify significant predictors.
- **Training and Testing**:
  - Split the data into training and test sets.
  - Tuned hyperparameters to improve model performance.

### 4. **Model Evaluation**
- **Confusion Matrix**:
  - Measured true positives, true negatives, false positives, and false negatives.
- **Precision and Recall**:
  - Ensured the model was balanced in minimizing false positives and false negatives.
- **ROC-AUC Curve**:
  - Evaluated the model’s ability to discriminate between converted and non-converted leads.

---

## Key Learnings

1. **Importance of Data Cleaning**:
   - Placeholder values like "Select" significantly impacted initial results, emphasizing the importance of preprocessing.

2. **Feature Engineering**:
   - Scaling and encoding categorical variables were critical steps in enhancing model accuracy.

3. **Evaluation Metrics**:
   - Using multiple evaluation metrics (e.g., precision-recall, ROC-AUC) provided a comprehensive understanding of model performance.

4. **Business Implications**:
   - The lead scoring model enables the sales team to focus on high-priority leads, significantly improving efficiency and conversion rates.

---

## Results
- **Model Performance**:
  - Achieved an ROC-AUC score of over 85%, indicating a strong ability to classify leads correctly.
  - Precision and recall values were optimized to balance true positives and reduce false negatives.
- **Business Value**:
  - Improved the focus on high-potential leads, enabling the sales team to achieve better conversion rates from the original 30% to a target of 80%.

---

## Conclusion
This case study showcases the potential of data-driven solutions in solving real-world business problems. By implementing a logistic regression model, **X Education** can now identify and prioritize "Hot Leads," improving their sales process and driving higher revenue.

---

## Repository Structure
```
|-- data/                       # Raw and cleaned datasets
|-- notebooks/                  # Jupyter notebooks for EDA, modeling, and evaluation
|-- models/                     # Saved logistic regression model
|-- scripts/                    # Python scripts for preprocessing, feature engineering, and model building
|-- results/                    # Performance metrics, visualizations, and final outputs
|-- README.md                   # Project documentation
```

---

## How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd lead-scoring-case-study
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Notebooks**:
   Use Jupyter Notebook to open and execute the analysis and modeling notebooks.

4. **Generate Lead Scores**:
   Run the scripts in the `scripts/` directory to generate lead scores for new data.

---

## Tools and Technologies Used
- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Environment**: Jupyter Notebook
- **Version Control**: Git

---

## Acknowledgments
Special thanks to Kaggle and the community for providing the dataset and fostering collaborative learning opportunities.

