# 🧠 Student Mental Health & Acculturative Stress Analysis

## 📖 Project Overview
Does going to university in a different country affect your mental health? 

This project explores survey data from a Japanese international university (collected in 2018) to investigate the mental health difficulties faced by international students. Using **PostgreSQL**, the analysis examines how **social connectedness** and **acculturative stress** (stress associated with joining a new culture) act as predictors for depression, and specifically tests whether the **length of stay** in the host country is a contributing factor.

## 📊 The Dataset
The dataset (`students.csv`) contains demographic, linguistic, and psychological survey responses from both domestic and international students. 

**Key metrics analyzed include:**
*   **`todep`**: Total score of depression (PHQ-9 test)
*   **`tosc`**: Total score of social connectedness (SCS test)
*   **`toas`**: Total score of acculturative stress (ASISS test)
*   **`stay`**: Current length of stay in the host country (in years)
*   **`inter_dom`**: Student type (International vs. Domestic)

## 🔍 Key Findings
By filtering for international students (`inter_dom = 'Inter'`) and grouping the data by their `stay` (length of stay in years), the SQL analysis revealed the following trends:

1.  **Acculturative Stress Increases Over Time:** As the length of stay increases, acculturative stress (`toas`) generally trends upward. For example, students in their 1st year had an average stress score of **72.80**, which rose to **87.71** by their 4th year.
2.  **Social Connectedness Decreases Over Time:** The sense of social connectedness (`tosc`) tends to drop the longer students stay. First-year students averaged **38.11**, while 4th-year students dropped to **33.93**.
3.  **Depression Fluctuates but Persists:** Depression scores (`todep`) fluctuate across different years (ranging from `7.48` in year 1 to `9.09` in year 3), indicating that mental health challenges remain a persistent factor regardless of how long the student has been in the country.

*(Note: Sample sizes for stays longer than 4 years were very small in this dataset, so the 1-to-4-year trend is the most statistically significant).*

## 🛠️ Technologies Used
*   **Database:** PostgreSQL
*   **Query Language:** SQL (Aggregations, Grouping, Filtering, Window Functions)
*   **Environment:** Jupyter Notebook / DataCamp Workspace
*   **Data Handling:** Pandas (via Python integration)

## 📂 Project Files
*   `students.csv` - The raw dataset containing the survey responses.
*   `notebook.ipynb` - The Jupyter Notebook containing the SQL queries, data exploration, and analysis.
*   `mentalhealth.jpg` - Visual output/summary of the analysis.

## 🎓 Acknowledgments
This project was completed as part of the **DataCamp** curriculum to practice SQL querying, data aggregation, and exploratory data analysis (EDA) on real-world psychological datasets.
