# 🚀 Scaler Learner Profiling — Unsupervised Learning 

Welcome to the **Scaler Learner Profiling Case Study** repo!  
This project showcases my end-to-end problem-solving as a Data Scientist, tackling a real-world business problem using **unsupervised learning techniques** and robust data analysis methods.

---

## 📚 Problem Statement

Scaler, a leading tech-versity, aims to deliver a world-class, personalized learning experience for professionals across the tech spectrum.  
A big challenge? **Understanding the backgrounds of thousands of learners** — their job roles, companies, and experience levels — to tailor content, improve retention, and deliver targeted mentoring.

**Goal:**  
Cluster learners based on profile data (roles, companies, experience, compensation) for more effective learner and company profiling, enabling Scaler to:

- Design customized learning paths and recommendations  
- Support targeted mentoring and career guidance  
- Recognize top workplaces and trending job roles within the tech ecosystem  

---
Dataset Explanation:
1. Unnamed 0: The index of the dataset.
2. Email_hash: An anonymized identifier representing the email of the learner.
3. Company_hash: An anonymized identifier indicating the current employer of the
learner.
4. orgyear: Represents the year the learner began employment at the current
company.
5. CTC: Current Compensation to the Company (CTC) of the learner.
6. Job_position: Represents the job profile or role of the learner within their
company.
7. CTC_updated_year: The year in which the learner's CTC was most recently
updated. This could be due to yearly increments, promotions, or other factors.

## 🔍 Methodology & Approach

The end-to-end pipeline includes:

1. **Exploratory Data Analysis (EDA)**
   - Data cleaning, summary stats, visualizations  
   - Outlier analysis, distribution checks, missing value imputation, regex text cleaning  

2. **Feature Engineering**
   - Years of experience calculation, converting CTC to lakhs per annum  
   - Aggregated medians and flags (“Designation”, “Class”, “Tier”) for relative compensation across company/job/experience  

3. **Manual Segmentation & Clustering**
   - Multi-level flags to compare each learner’s CTC against relevant peer groups  
   - Understanding company- and job-based compensation dynamics  

4. **Unsupervised Clustering**
   - **KMeans** and **GMM** applied to engineered features  
   - Optimal cluster selection via **Elbow method**  
   - Cluster interpretability using **PCA/UMAP** and scaled feature analysis  

5. **Cluster Insights & Recommendations**
   - In-depth analysis of cluster characteristics (identifying high, average, and low earners)  
   - Actionable findings for business strategy, learner support, and product personalization  

---

## 💡 Key Results & Insights

- **Strong validation of feature engineering**: Clustering algorithms (KMeans, GMM) closely matched manually-created compensation tiers, underlining the power of the “relative CTC” flag methodology.
- **Distinct segments discovered**:  
  - **Cluster 1**: High earners with significant experience — leadership/advanced IC roles in top-paying companies  
  - **Cluster 2**: Average earners, median experience  
  - **Cluster 3**: Early-career or lower-compensated learners, often in more populous companies/roles  
- **Notable findings**:  
  - Backend and Fullstack Engineer roles dominate, but there is high variance in CTC even among similar roles  
  - Company “tier” frequency correlates with compensation clusters — crowding in Tier 3 by popular companies and entry-level positions  
  - Years of experience do not guarantee higher CTC; key outliers are highlighted  
  - Entry-level roles like “Support Engineer” can have outliers with unusually high CTCs  

**Business-ready recommendations:**
- Use clustering results to develop career tracks, peer comparison dashboards, and company/role benchmarking for learners  
- Guide content and mentorship programs for mid/low-tier clusters to elevate retention and satisfaction  

---

## 📈 Project Highlights

- **230K+** data points processed, all steps clearly documented in Jupyter Notebook  
- Both manual and model-based clustering approaches for robust profiling  
- Rich visualizations — EDA plots, Elbow method, cluster projections (PCA/UMAP)  
- Insightful commentary after every major step  

---

## 👨💻 Technologies Used

- Python (`pandas`, `numpy`, `scikit-learn`, `seaborn`, `matplotlib`, `umap-learn`)  
- Jupyter Notebook  

---

Let’s connect on LinkedIn to discuss this further, or explore my other **data science projects**.
Linkedin Link - [www.linkedin.com/in/rahil-qureshi-453a10123](https://www.linkedin.com/in/rahil-qureshi-453a10123/)]
