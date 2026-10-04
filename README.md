<div align="center">

# 🚕 Automatidata — NYC Taxi Data Analytics Project

### Google Advanced Data Analytics Professional Certificate · Portfolio Project Series

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Coursera](https://img.shields.io/badge/Coursera-Google-0056D2?style=for-the-badge&logo=coursera&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Progress-success?style=for-the-badge)

*Turning millions of taxi rides into insights for the New York City Taxi & Limousine Commission.*

</div>

---

## 📖 Table of Contents

1. [About the Project](#-about-the-project)
2. [The Business Scenario](#-the-business-scenario)
3. [The PACE Framework](#-the-pace-framework)
4. [The Dataset](#-the-dataset)
5. [Course 1: Foundations of Data Science](#-course-1-foundations-of-data-science)
6. [Repository Structure](#-repository-structure)
7. [How to Run the Notebook](#-how-to-run-the-notebook)
8. [Project Roadmap](#-project-roadmap)
9. [Skills Demonstrated](#-skills-demonstrated)
10. [About Me](#-about-me)
11. [Acknowledgements](#-acknowledgements)

---

## 🎯 About the Project

This repository documents my work on the **Automatidata** portfolio project, part of the **Google Advanced Data Analytics Professional Certificate** on Coursera. The project follows a realistic, end-to-end data analytics workflow: from understanding a client's business needs, to inspecting and cleaning data, to statistical analysis and machine learning.

Each course in the certificate adds a new stage to the project. I'll be pushing each milestone to this repository **in sequential order**, so you can watch the project grow from a first look at the data into a full predictive model.

> 💡 **Ultimate goal:** Help the NYC TLC build a model that predicts taxi fare amounts *before* a ride begins, so riders know what to expect.

---

## 🏢 The Business Scenario

**Automatidata** is a fictional data consulting firm that works with clients to turn raw data into valuable insights. Their latest client is the **New York City Taxi & Limousine Commission (NYC TLC)**, the agency that licenses and regulates the city's iconic yellow taxis and for-hire vehicles.

| Stakeholder | Organization | Role |
|---|---|---|
| Uli King | Automatidata | Senior Project Manager |
| Deshawn Washington | Automatidata | Data Analysis Manager |
| Luana Rodriguez | Automatidata | Senior Data Analyst |
| Juliana Soto | NYC TLC | Finance & Administration Department Manager |
| Titus Nelson | NYC TLC | Operations Manager |

In this project, I play the role of a **data professional on the Automatidata team**, working with these stakeholders to deliver insights from TLC taxi trip data.

---

## 🧭 The PACE Framework

Every stage of this project is guided by Google's **PACE** workflow, a structured approach to data projects:

| Stage | Name | What it means |
|:---:|---|---|
| 🅿️ | **Plan** | Understand the business problem, the stakeholders, and the scope of the project |
| 🅰️ | **Analyze** | Collect, inspect, clean, and explore the data |
| 🅲 | **Construct** | Build models and perform statistical analysis |
| 🅴 | **Execute** | Share results, insights, and recommendations with stakeholders |

📄 My completed **PACE Strategy Document** in this repo shows how I applied each stage to the Automatidata scenario.

---

## 📊 The Dataset

The project uses the **2017 NYC Yellow Taxi Trip Data**, provided by the NYC TLC.

- **Rows:** ~22,699 taxi trips
- **Columns:** 18 features
- **Source:** NYC Taxi & Limousine Commission (via the Google course materials)

<details>
<summary><b>📋 Click to view the data dictionary</b></summary>

| Column | Description |
|---|---|
| `ID` | Unique trip identifier |
| `VendorID` | Technology provider that supplied the record (1 = Creative Mobile Technologies, 2 = VeriFone Inc.) |
| `tpep_pickup_datetime` | Date and time the meter was engaged |
| `tpep_dropoff_datetime` | Date and time the meter was disengaged |
| `passenger_count` | Number of passengers (entered by the driver) |
| `trip_distance` | Trip distance in miles reported by the taximeter |
| `RatecodeID` | Final rate code (1 = Standard, 2 = JFK, 3 = Newark, 4 = Nassau/Westchester, 5 = Negotiated, 6 = Group ride) |
| `store_and_fwd_flag` | Whether the trip record was stored in vehicle memory before sending (Y/N) |
| `PULocationID` | TLC Taxi Zone where the meter was engaged |
| `DOLocationID` | TLC Taxi Zone where the meter was disengaged |
| `payment_type` | Payment method (1 = Credit card, 2 = Cash, 3 = No charge, 4 = Dispute, 5 = Unknown, 6 = Voided) |
| `fare_amount` | Time-and-distance fare calculated by the meter |
| `extra` | Miscellaneous extras and surcharges |
| `mta_tax` | $0.50 MTA tax |
| `tip_amount` | Tip amount (auto-populated for credit card tips; cash tips not included) |
| `tolls_amount` | Total tolls paid during the trip |
| `improvement_surcharge` | $0.30 improvement surcharge |
| `total_amount` | Total amount charged to the passenger (excluding cash tips) |

</details>

---

## 🔍 Course 1: Foundations of Data Science

**Milestone:** *Inspect and understand the data*

In this first stage, the Automatidata team needed someone to take an initial look at the TLC data and organize the project before deeper analysis begins.

### ✅ What I did

- 📝 **Completed a PACE Strategy Document** to plan the project, identify stakeholders, and define the questions to answer
- 🐍 **Built a Python notebook** to load and inspect the dataset using `pandas` and `numpy`
- 🔎 **Explored the data's structure** with `.head()`, `.info()`, `.describe()`, and `.shape`
- 📈 **Sorted and filtered** trips by `trip_distance` and `total_amount` to understand the extremes
- 💳 **Compared payment types** and average tip amounts across credit card and cash payments
- 🚖 **Examined vendor and passenger counts** to understand how trips are distributed
- 📑 **Wrote an Executive Summary** communicating findings to non-technical stakeholders

### 💡 Key takeaways

- The dataset is mostly complete, with no major missing values, which makes it a solid foundation for later modeling.
- Some records contain **unusual values** (for example, negative fares or zero-distance trips) that will need to be cleaned before modeling.
- **Credit card payments** show recorded tips, while cash tips aren't captured in the data, an important limitation for any tip analysis.
- **Trip distance and total amount** are strongly related, which suggests distance will be a key predictor of fare.

> 📄 See the **Executive Summary** in this repository for the full write-up.

---

## 📁 Repository Structure

```
AutomatiData/
│
├── 📂 Course1_Foundations_of_Data_Science/
│   ├── 📓 Automatidata_Course1.ipynb          # Python notebook: data inspection
│   ├── 📊 2017_Yellow_Taxi_Trip_Data.csv       # Dataset
│   ├── 📄 PACE_Strategy_Document.pdf           # Project planning document
│   └── 📄 Executive_Summary.pdf                # Stakeholder-facing summary
│
├── 📂 Course2_Get_Started_with_Python/          # 🔜 Coming soon
├── 📂 Course3_Go_Beyond_the_Numbers/            # 🔜 Coming soon
├── 📂 Course4_Power_of_Statistics/              # 🔜 Coming soon
├── 📂 Course5_Regression_Analysis/              # 🔜 Coming soon
├── 📂 Course6_Nuts_and_Bolts_of_ML/             # 🔜 Coming soon
│
└── 📘 README.md
```

> ✏️ *File and folder names above are a suggested layout; update them to match your actual repository.*

---

## ⚙️ How to Run the Notebook

**1. Clone the repository**
```bash
git clone https://github.com/<Gowthamch9>/AutomatiData.git
cd AutomatiData
```

**2. Install the required libraries**
```bash
pip install pandas numpy jupyter
```

**3. Launch Jupyter and open the notebook**
```bash
jupyter notebook
```

Then open the Course 1 notebook and run the cells from top to bottom. 🎉

---

## 🗺️ Project Roadmap

This repository grows with each course in the certificate. Here's where the project is heading:

| # | Course | Project Milestone | Status |
|:---:|---|---|:---:|
| 1 | Foundations of Data Science | Project planning & initial data inspection | ✅ Complete |
| 2 | Get Started with Python | Data exploration & structuring in Python | 🔜 Upcoming |
| 3 | Go Beyond the Numbers | Exploratory data analysis & visualizations | 🔜 Upcoming |
| 4 | The Power of Statistics | Hypothesis testing (payment type vs. fare amount) | 🔜 Upcoming |
| 5 | Regression Analysis | Multiple linear regression to predict fares | 🔜 Upcoming |
| 6 | The Nuts and Bolts of Machine Learning | Machine learning model building | 🔜 Upcoming |
| 7 | Capstone | End-to-end portfolio project | 🔜 Upcoming |

---

## 🛠️ Skills Demonstrated

<table>
<tr>
<td valign="top" width="50%">

**Technical**
- Python programming
- Data inspection with `pandas`
- Numerical computing with `numpy`
- Jupyter Notebooks
- Version control with Git & GitHub

</td>
<td valign="top" width="50%">

**Professional**
- Project planning with the PACE framework
- Stakeholder identification
- Writing executive summaries
- Translating data into business insights
- Clear, structured documentation

</td>
</tr>
</table>

---

## 👋 About Me

**Gowtham Venkat Eathamokkala**
🎓 First-year Ph.D. student in **Information Science** (Data Science Concentration)
🏫 **University of North Texas (UNT)**

I'm passionate about using data to solve real-world problems, and this repository is part of my journey through the Google Advanced Data Analytics Professional Certificate. Feedback and suggestions are always welcome!

<!-- Add your links below -->
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/your-profile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/your-username)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat&logo=gmail&logoColor=white)](mailto:your.email@example.com)

---

## 🙏 Acknowledgements

- **Google** and **Coursera** for the Advanced Data Analytics Professional Certificate and project materials
- **NYC Taxi & Limousine Commission** for the publicly available trip data
- *Automatidata is a fictional company created for educational purposes.*

---

<div align="center">

⭐ **If you found this project helpful, consider giving it a star!** ⭐

*Last updated: October 2026*

</div>
