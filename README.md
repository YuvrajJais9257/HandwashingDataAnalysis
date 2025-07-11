## 📊 Dr Semmelweis & the Discovery of Handwashing

This notebook explores how Dr Ignaz Semmelweis discovered the life-saving impact of handwashing by analyzing historical data from maternity wards.

---

### 🧰 **Setup & Context**

* Brief historical background on Dr Semmelweis and childbed fever.
* Links to the original German text and English translation of his publication.
* Upgrade Plotly version (for Colab users).

---

### 📦 **Importing libraries**

* Data analysis: `pandas`, `numpy`
* Visualization: `matplotlib.pyplot`, `seaborn`, `plotly.express`

---

### 🗂 **Data loading**

* Read monthly and yearly datasets about childbirths and deaths at Vienna General Hospital.

---

### 📊 **Data exploration & visualization**

* Plot the number of births and deaths over time.
* Calculate and plot the proportion of deaths per total births (monthly and yearly).
* Visualize differences between two hospital clinics.

---

### 🧪 **Statistical analysis**

* Focused analysis on the period **before and after handwashing** was introduced.
* Used a two-sample **t-test**:

  ```python
  from scipy import stats
  t_stat, p_value = stats.ttest_ind(a=monthly_subset_before['deaths%'], 
                                    b=monthly_subset_after['deaths%'])
  ```
* Checked if p-value < 0.01 → statistically significant at the 99% confidence level.

---

### ✅ **Conclusion**

* Found very strong evidence (t-statistic ≈ 5.51, p-value ≈ 0.00) that **handwashing significantly reduced the death rate**.
* p-value < 0.01 ⇒ difference not due to chance; the practice of handwashing saved lives.

---

### 📈 **Key visual outputs**

* Line plots showing death rates over time.
* Charts comparing clinics and periods before/after intervention.

---

## 📌 **Notes**

* Notebook designed for educational purposes: visual storytelling and reproducible statistical analysis.
* Uses publicly available historical data.
