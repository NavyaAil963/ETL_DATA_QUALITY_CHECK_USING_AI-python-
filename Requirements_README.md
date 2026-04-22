Tools & Technologies Used
Tool                  Purpose
Python 3.x            Data analysis and scripting
Jupyter Notebook      Interactive analysis environment
Pandas                Data loading and manipulation
Matplotlib            Data visualization and charts
NumPy                 Numerical computations
PostgreSQL            Backend database for storing and querying ETL pipeline 
datapsycopg2          Python library to connect and interact with PostgreSQL
Microsoft Excel(.xlsx)Survey data storage

Requirements
To run the Jupyter Notebook, install the required Python libraries:

bashpip install pandas matplotlib numpy openpyxl jupyter psycopg2-binary

Set up PostgreSQL and configure your connection:

pythonimport psycopg2

conn = psycopg2.connect(
    host="localhost",
    database="your_database_name",
    user="your_username",
    password="your_password"
)

⚠️ Never hardcode credentials. Use environment variables or a .env file — and add .env to your .gitignore.

Then launch the notebook:

bashjupyter notebook ETL_Python_file.ipynb

Make sure AI_ETL_Data_Quality_Survey_Responses.xlsx is in the same folder as the notebook before running.


Visualizations Produced
The notebook generates the following charts used in the thesis:

Bar Chart — Data Quality Score: Before vs After AI Implementation
Line Graph — AI Detection Rate vs Manual Detection Rate (per respondent)
Pie Chart — Types of Data Errors Detected by AI (Missing Values, Inconsistencies, Duplications)


Survey Data Structure
The file AI_ETL_Data_Quality_Survey_Responses.xlsx contains responses from 50 participants (R001–R050) across 10 questions (Q1–Q10) on a 1–5 Likert scale.
QuestionsRepresentsQ1 – Q5Data quality metrics before AI implementationQ6 – Q10Data quality metrics after AI implementation

Research Objectives

Determine the role of AI in automating data quality monitoring in ETL
Measure the effectiveness of AI models in identifying and fixing data inaccuracies
Assess the impact of AI-driven data quality on business reporting accuracy and cost

