# US Data Job Market Analysis

This project was born from my journey to becoming a Data Analyst — I wanted to put my skills into practice while gaining a deeper understanding of the job market and the skills required not just for Data Analysts, but across the data ecosystem as a whole.

## Dataset

This analysis uses a dataset of **785,000+ job postings** for data-related roles in the United States (2023), sourced from the [data_jobs](https://huggingface.co/datasets/lukebarousse/data_jobs) Hugging Face dataset. It includes job titles, salaries, locations, required skills, and company information.

## Questions Explored

1. What are the most demanded skills for the top 3 data roles?
2. How are in-demand skills trending for Data Analysts throughout 2023?
3. How well do jobs and skills pay for Data Analysts?
4. How do remote vs on-site positions compare in salary and skills?
5. What are the most optimal skills to learn? (High Demand + High Paying)

## Tools & Technologies

- **Python** - Core language for all analysis
- **pandas** - Data manipulation and aggregation
- **matplotlib & seaborn** - Data visualization
- **Jupyter Notebooks** - Interactive analysis environment
- **Hugging Face Datasets** - Data loading

## Project Structure

```
.
├── Project/
│   ├── 0_EDA_Intro.ipynb           # Exploratory data analysis
│   ├── 1_Skill_Demand.ipynb        # Top skills per role
│   ├── 2_Skills_Trend.ipynb        # Monthly skill trends
│   ├── 3_Salary_Analysis.ipynb     # Salary distributions
│   ├── 4_Remote_Analysis.ipynb     # Remote vs on-site comparison
│   ├── 5_Optimal_Skills.ipynb      # High-demand & high-paying skills
│   └── images/                     # Generated visualizations
├── pyproject.toml
└── README.md
```

## Analysis & Findings

### Exploratory Data Analysis

Before diving into the specific questions, I explored the full dataset to understand its shape and scope: job distribution by title, country, and company, as well as benefits like remote work, degree requirements, and health insurance. This helped define the focus of the analysis on the **US market** and the **top 3 data roles**.

**Notebook:** [0_EDA_Intro.ipynb](Project/0_EDA_Intro.ipynb)

---

### 1. Most Demanded Skills by Role

I identified the top 5 skills for Data Analysts, Data Engineers, and Data Scientists by calculating the percentage of job postings that mention each skill.

**Notebook:** [1_Skill_Demand.ipynb](Project/1_Skill_Demand.ipynb)

![Likelihood of Skills Requested in US Job Postings](Project/images/Likelihood_of_Skills_Requested_in_US_Job_Postings.png)

**Key findings:**
- **SQL** dominates for Data Analysts (51%) and Data Scientists (51%), while **Python** leads for Data Engineers (68%)
- Data Engineers require more cloud/infrastructure skills (AWS, Azure, Spark) vs. the analysis tools expected from Analysts (Excel, Tableau)
- Python is highly valued across all three roles (29%-72%)

---

### 2. Skill Trends Over 2023

I tracked how the top 5 Data Analyst skills fluctuated month by month throughout 2023, using percentage of total job postings per month.

**Notebook:** [2_Skills_Trend.ipynb](Project/2_Skills_Trend.ipynb)

![Trending Top Skills for Data Analysts in the US](Project/images/Trending_Top_Skills_for_Data_Analysts_in_the_US.png)

**Key findings:**
- SQL remained the most demanded skill all year, though showing a gradual decline from ~63% to ~53%
- Excel saw a notable increase starting in September, surpassing Python and Tableau by year's end
- Python and Tableau stayed relatively stable, while Power BI showed a slight upward trend

---

### 3. Salary Analysis

I examined salary distributions across the top 6 data roles using box plots, then drilled into Data Analyst salaries by skill.

**Notebook:** [3_Salary_Analysis.ipynb](Project/3_Salary_Analysis.ipynb)

![Salary Distributions of Data Jobs in the US](Project/images/Salary_Distributions_of_Data_Jobs_in_the_US.png)

![Highest Paid and Most In-Demand Skills for Data Analysts in the US](Project/images/Highest_Paid_and_Most_In_Demand_Skills_for_Data_Analysts_in_the_US.png)

**Key findings:**
- Senior Data Scientists have the highest salary potential (up to $600K), with significant outliers
- Specialized skills (dplyr, Bitbucket, GitLab) command salaries up to ~$200K but appear in very few postings
- Foundational skills (Excel, SQL, PowerPoint) are the most in-demand but offer lower median salaries (~$82K-$97K)

---

### 4. Remote vs On-site Comparison

I compared remote and on-site positions across data roles to see how they differ in availability, salary, and the skills they demand.

**Notebook:** [4_Remote_Analysis.ipynb](Project/4_Remote_Analysis.ipynb)

![Percentage of Remote Jobs by Data Role in the US](Project/images/Remote_Percentage_by_Data_Role_in_the_US.png)

![Salary Remote vs On-site for Data Analysts in the US](Project/images/Salary_Remote_vs_Onsite_Data_Analysts_in_the_US.png)

![Skills Remote vs On-site for Data Analysts in the US](Project/images/Skills_Remote_vs_Onsite_Data_Analysts_in_the_US.png)

**Key findings:**
- Engineering roles have the most remote opportunities: Senior Data Engineers (20.2%) and Data Engineers (17.9%), while Data Analysts have the least (7.5%)
- Remote Data Analysts earn a higher median salary ($87K) compared to on-site positions
- Remote roles demand higher proficiency in technical skills overall — SQL jumps from 50% (on-site) to 60% (remote), and Python from 27% to 30%

---

### 5. Optimal Skills (High Demand + High Pay)

I created a scatter plot mapping skill demand percentage against median salary, then categorized skills by technology type.

**Notebook:** [5_Optimal_Skills.ipynb](Project/5_Optimal_Skills.ipynb)

![Most Optimal Skills for Data Analysts in the US with Coloring by Technology](Project/images/Most_Optimal_Skills_for_Data_Analysts_in_the_US_with_Coloring_by_Technology.png)

**Key findings:**
- **Programming skills** (Python, R) cluster at higher salary levels compared to other categories
- **Database skills** (Oracle, SQL Server) are associated with some of the highest salaries among all tool types
- **Analyst tools** (Tableau, Power BI) offer a good balance of demand and competitive pay
- SQL and Excel have the highest demand but are not the highest paying individually

## What I Learned

- What I mainly learned was to improve my step-by-step thinking process for manipulating and improving the quality of tables and DataFrames.
- What caught my attention the most was that in practically every job, **SQL** and **Python** always stand out.
- I improved a lot in creating visualizations, mainly with the `for/in` loop method.
- The languages that everyone in this field must absolutely know are **SQL** and **Python** — they are the foundation for working with data.

## Setup

```bash
# Clone the repository
git clone https://github.com/eliasfigueroa22/PYTHON_DATA_COURSE.git

# Install dependencies (requires uv)
uv sync

# Open notebooks
jupyter notebook Project/
```

Requires Python 3.14+.
