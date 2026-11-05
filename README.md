# 📊 Job Market Analytics

### Turning Job Market Data into Actionable Insights

An end-to-end Data Analytics and Machine Learning project that explores remote job-market trends, identifies in-demand technical skills, analyzes salary patterns, and predicts salaries using Machine Learning. The project combines Python-based data processing with an interactive Power BI dashboard.

---

## 🚀 Project Overview

Job Market Analytics aims to transform publicly available job postings into meaningful insights about the evolving employment landscape.

Using the **Jobicy Public Remote Jobs API**, the project collects job listings and processes them through data cleaning, feature engineering, exploratory data analysis (EDA), and predictive modeling.

The final results are presented through an interactive Power BI dashboard, allowing users to explore job opportunities across industries, companies, locations, skills, experience levels, and salary ranges.

## 📈 Project Highlights

| Metric | Result |
|---|---:|
| Job Postings Analyzed | 1,021 |
| Unique Companies | 290 |
| Location Categories | 116 |
| Processed Dataset Fields | 61 |
| Skill Indicators | 30+ |
| Salary Records | 510 |
| ML Algorithm | Random Forest |

## ✨ Key Features

### 1. Data Collection
- Integrated the Jobicy Public Remote Jobs API using Python.
- Collected job postings across multiple keywords and industries.
- Processed JSON API responses into structured datasets.
- Removed duplicate records using unique Job IDs.

### 2. Data Cleaning & Preprocessing
- Handled missing and inconsistent values.
- Removed HTML tags and unnecessary formatting from job descriptions.
- Standardized employment types and job levels.
- Converted salary values into annual equivalents.
- Processed dates and categorical variables.

### 3. Feature Engineering
- Extracted experience requirements using Regular Expressions.
- Created 30+ skill-specific binary indicators.
- Calculated Skill Count, Description Length, and Word Count.
- Prepared analytical features for exploratory analysis and machine learning.

### 4. Exploratory Data Analysis (EDA)
Analyzed:
- Industry-wise job distribution.
- Most demanded technical skills.
- Salary distribution and compensation patterns.
- Experience requirements across job levels.
- Employment type and geographic distribution.
- Relationships between skills, experience, and salary.
- Job posting trends over time.

### 5. Machine Learning – Salary Prediction

Implemented a Random Forest Regression model to estimate annual salaries in USD.

**Model Configuration**

- Algorithm: Random Forest Regressor
- Number of Estimators: 100
- Train-Test Split: 80:20
- Categorical Encoding: One-Hot Encoding
- Evaluation Metrics: RMSE, MAE, R² Score

**Model Performance**

| Evaluation Metric | Result |
|---|---:|
| RMSE | $68,289.40 |
| MAE | $51,715.36 |
| R² Score | 0.2493 |
| 5-Fold CV Mean R² | -0.0299 |

The model serves as an initial predictive baseline. Its performance indicates that salary prediction requires additional features and further optimization.

### 6. Interactive Power BI Dashboard

Developed a multi-page Power BI dashboard featuring:

- Job Market Overview – KPIs and industry distribution.
- Skills & Salary Analysis – Skill demand and compensation insights.
- Trends Analysis – Job posting trends and detailed records.
- Interactive filtering and drill-through functionality.
- Key Influencers and comparative visualizations.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Programming and data processing |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical computations |
| Requests | API integration |
| BeautifulSoup | HTML parsing and text cleaning |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine Learning |
| Jupyter Notebook | Analysis and experimentation |
| Power BI | Interactive dashboards |

## 🔄 Project Workflow

```text
       Jobicy Public API
              |
              v
       Data Collection
              |
              v
        Raw Dataset
              |
              v
     Data Cleaning & ETL
              |
              v
      Feature Engineering
              |
              v
    Exploratory Data Analysis
              |
        +-----+------+
        |            |
        v            v
   Machine       Visualizations
   Learning           |
        |             |
        v             |
  Salary Prediction   |
        |             |
        +------+------+
               |
               v
       Power BI Dashboard
               |
               v
       Actionable Insights
```

## 📁 Repository Structure

```text
Job-Market-Analytics/
│
├── 01_web_scraping_job_market.py
│
├── 02_data_analysis_and_modeling.ipynb
│
├── raw_job_market_data.csv
│
├── cleaned_job_market_data.csv
│
├── Final_Project.pbix
│
├── README.md
│
└── requirements.txt
```

## ⚙️ Installation & Setup

### Prerequisites
- Python 3.9+
- Jupyter Notebook
- Power BI Desktop (for dashboard exploration)

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd Job-Market-Analytics
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
```

Activate it:

**Windows**
```bash
venv\Scripts\activate
```

**macOS / Linux**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Alternatively:

```bash
pip install requests pandas numpy beautifulsoup4 matplotlib seaborn scikit-learn jupyter
```

### 4. Run Data Collection

```bash
python 01_web_scraping_job_market.py
```

This executes the API-based data collection script and generates the raw CSV dataset.

### 5. Run the Analysis

```bash
jupyter notebook
```

Open:

`02_data_analysis_and_modeling.ipynb`

Run the notebook cells sequentially to perform data cleaning, preprocessing, feature engineering, exploratory data analysis, and salary prediction.

### 6. Explore the Dashboard

Open `Final_Project.pbix` using Microsoft Power BI Desktop.

---

## 📊 Key Insights

The analysis revealed several patterns within the collected dataset:

- Software Engineering represented the largest job-industry category.
- Python, AWS, Machine Learning, and SQL were among the most frequently detected technical skills.
- Full-time positions dominated the collected job postings.
- Job listings showed a concentration of postings from the USA.
- Experience alone showed a relatively weak relationship with salary.

*These findings describe the collected dataset and should not be generalized to the entire global employment market.*

## 🔮 Future Improvements

- Integrate multiple job-market APIs for broader data coverage.
- Implement NLP-based skill extraction from job descriptions.
- Improve salary prediction through hyperparameter tuning and additional features.
- Explore XGBoost and other regression algorithms.
- Introduce automated data updates and scheduled refreshes.
- Develop a web-based interface for interactive job-market exploration.
- Add job recommendation based on skills and experience.

## 📚 Data Source

**Jobicy Public Remote Jobs API**

https://jobicy.com/api/v2/remote-jobs

The project uses publicly available job-posting information for educational and analytical purposes.

## 👨‍💻 Author

**Ishaan Sahi**

B.Tech – Computer Science & Engineering  
Jaypee Institute of Information Technology, Noida

---

⭐ If you find this project interesting, consider giving the repository a star!

