# High-Energy Particle Classification Model

<a href="https://colab.research.google.com/github/RanaMagdyisaac/High-Energy-Particle-Classification-Model-/blob/main/High_Energy_Particle_Model.ipynb" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## 📌 Project Overview
This project focuses on the classification of high-energy particles into two distinct categories: **Gamma (g)** and **Hadron (h)**. Using the **MAGIC Gamma Telescope dataset**, I developed a robust machine learning pipeline in Python. The primary goal was to address the inherent class imbalance in the data and build ensemble models capable of accurately distinguishing between the two particle types.

**Key Achievements:**
*   Handled a dataset of over 19,000 records, performing essential Data Preprocessing and Exploratory Data Analysis (EDA).
*   Successfully resolved class imbalance using **Downsampling** techniques.
*   Developed, tuned, and compared multiple machine learning models.
*   Achieved **85.8% Accuracy** and **88.2% Recall** for Gamma events using a tuned Random Forest Classifier.

## 🛠️ Technologies & Libraries Used
*   **Language:** Python 3
*   **Data Manipulation:** Pandas, NumPy
*   **Machine Learning:** Scikit-Learn (`DecisionTreeClassifier`, `AdaBoostClassifier`, `RandomForestClassifier`, `GaussianNB`, `GridSearchCV`)
*   **Data Visualization:** Matplotlib, Seaborn

## 📊 Dataset Description
The dataset used is the MAGIC Gamma Telescope dataset, which contains 11 features (10 numerical features and 1 target class):
*   `fLength`, `fWidth`, `fSize`, `fConc`, `fConc1`, `fAsym`, `fM3Long`, `fM3Trans`, `fAlpha`, `fDist`
*   `class`: The target variable, representing either a **Gamma (g)** or **Hadron (h)** event.

### EDA & Preprocessing Highlights
*   **Class Imbalance:** The original dataset was highly imbalanced with 12,332 Gamma (g) events and only 6,688 Hadron (h) events.
*   **Balancing Strategy:** I implemented a **downsampling** technique on the majority class (Gamma) to match the minority class (Hadron), resulting in a perfectly balanced dataset of 13,146 samples.

## 🚀 Models Developed & Evaluated
1.  **Decision Tree Classifier (Baseline):** Accuracy 78.82%
2.  **AdaBoost Classifier:** Accuracy 80.35% (Tuned with 150 estimators)
3.  **Random Forest Classifier 🏆 (Best Model):** 
    *   *Accuracy:* **85.80%**
    *   *Recall (Gamma):* **88.21%**
    *   *Observation:* Outperformed all other models, providing the best balance between precision and sensitivity.
4.  **Naïve Bayes (GaussianNB):** Accuracy 65.22% (High recall, but very low precision)

## 📈 Final Comparative Analysis

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **Random Forest** | **0.8580** | **0.8265** | 0.8821 | **0.8534** |
| **AdaBoost** | 0.8035 | 0.8001 | 0.7940 | 0.7971 |
| **Decision Tree** | 0.7882 | 0.7764 | 0.7925 | 0.7844 |
| **Naïve Bayes** | 0.6522 | 0.5904 | **0.8922** | 0.7106 |

### 💡 Conclusion
The **Random Forest Classifier** proved to be the absolute winner for this specific dataset. By leveraging ensemble learning and successfully mitigating the class imbalance, the model demonstrated superior robustness and classification power.

## 👨‍💻 Author
**Rana Magdy Isaac**
