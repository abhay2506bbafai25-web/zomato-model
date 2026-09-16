# 🍴 Zomato AI/ML Restaurant Recommendation System

## 📌 Project Overview

This project proposes an **AI/ML-powered restaurant recommendation system for Zomato**.

The system is designed to understand a user's restaurant preferences from their previous ratings and recommend restaurants that are more relevant to their taste.

The proposed approach combines:

**User Ratings → Random Forest Classifier → Preference Prediction → Weighted Restaurant Ranking → Top-N Recommendations**

> **Note:** This is an academic AI/ML case-study prototype and is not an official Zomato production system.

---

## 🎯 Problem Statement

Zomato provides users with a very large number of restaurant choices. Generic search and filters may not fully understand an individual user's preferences.

This can make restaurant discovery difficult and increase **choice overload**.

Our proposed solution is to use AI/ML to:

* Understand user preferences
* Predict preferred cuisine and price tier
* Rank suitable restaurants
* Provide personalized Top-N recommendations

---

## 🤖 Model Used

### 1. Random Forest Classifier

The **Random Forest Classifier** is used for preference modelling.

It predicts a user's likely:

* Cuisine preference
* Price preference

based on their previous restaurant-rating behaviour.

Random Forest was selected because it works with mixed types of features, is suitable for a modest dataset, and provides feature-importance information.

### 2. Weighted Restaurant Ranking

After predicting user preferences, restaurants are ranked using a **weighted scoring approach**.

The score considers factors such as:

* ⭐ Average restaurant rating
* 📊 Rating volume/popularity
* 🍛 Cuisine match
* 💰 Price fit

The highest-scoring restaurants are selected for the user's **Top-N recommendations**.

---

## 🔄 How the Model Works

```text
User Rating History
        ↓
Feature Engineering
        ↓
Random Forest Classifier
        ↓
User Preference Prediction
        ↓
Weighted Restaurant Scoring
        ↓
Restaurant Ranking
        ↓
Top-N Recommendations
```

### Example

If a user has rated several **North Indian** and **Cafe** restaurants highly, the system can identify those preferences and rank restaurants matching those cuisines higher.

The final output can be a personalized list such as:

```text
1. Restaurant A
2. Restaurant B
3. Restaurant C
4. Restaurant D
5. Restaurant E
```

---

## 📊 Dataset

For this academic prototype, the project uses a **demo restaurant dataset** and **synthetically generated user-rating data**.

The presentation specifies:

* **200 restaurants**
* **5,000 synthetic user ratings**

Restaurant information includes attributes such as:

* Restaurant ID
* Restaurant name
* Cuisine
* City/locality
* Average rating
* Cost for two
* Rating count

User interaction data includes:

* User ID
* Restaurant ID
* Rating given

The synthetic ratings are used because real Zomato user-rating/order history was not available.

---

## 🛠️ Technologies Used

* Python
* Google Colab / Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Random Forest

---

## 📁 Project Files

```text
Zomato-AI-ML-Recommendation/
│
├── zomato_model.ipynb
├── README.md
└── requirements.txt
```

### `zomato_model.ipynb`

Contains the Python/ML workflow for the Zomato recommendation-system prototype.

### `README.md`

Documentation explaining the project, model, dataset, workflow, and limitations.

### `requirements.txt`

Contains the Python libraries required for the project.

---

## ▶️ How to Run

### Using Google Colab

1. Open **Google Colab**.
2. Upload `zomato_model.ipynb`.
3. Run the notebook cells in order.
4. Review the generated data, model workflow, and recommendation outputs.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

Then run:

```bash
jupyter notebook
```

Open `zomato_model.ipynb` and execute the cells.

---

## ⚠️ Limitations

This project is a **proposed academic prototype**, not a live Zomato recommendation engine.

Important limitations include:

* The user-rating data is synthetic.
* Real Zomato user behaviour was not available.
* Synthetic ratings cannot represent genuine user preferences.
* The prototype should not be used to claim real-world recommendation accuracy.
* A production system would require real, consented user interaction data.
* Proper train/test evaluation and performance metrics would be required.
* Recommendations would need to be tested for bias and fairness.

The PPT specifically notes that the project presents a proposed approach rather than measured real-world performance.

---

## 🔐 Responsible AI

A production recommendation system should consider:

### Data Privacy

User ratings and order history should be properly protected.

### Bias & Fairness

The ranking system should avoid systematically favouring large restaurant chains over smaller/local restaurants.

### Transparency

The factors used to rank restaurants should be explainable.

### Incorrect Predictions

Recommendations are predictions of taste, not guarantees.

### Human Oversight

Important ranking changes should remain reviewable.

These responsible-AI considerations are part of the proposed case study.

---

## 🚀 Future Improvements

The proposed system could be improved by:

1. Using real opt-in user rating/order data.
2. Completing proper model training and evaluation.
3. Adding train/test splitting and performance metrics.
4. Handling new users with no rating history.
5. Handling newly listed restaurants.
6. Improving recommendation diversity.
7. Auditing recommendations for potential bias.
8. Testing the recommendation system through a controlled pilot/A/B test.

---

## 🎓 Academic Purpose

This project was created as a **Business AI/ML Case Study** to demonstrate how machine learning can be applied to a real-world business problem.

The project focuses on connecting:

**Data → AI/ML → Prediction → Business Action → Business Outcome**

The proposed business outcomes include improved restaurant discovery, faster decision-making, engagement, and potentially higher order frequency.

---

## 👥 Team

**Zomato AI/ML Case Study**

* Abhay Trehan
* Arush
* Harry Chalana
* Hardik Gagneja
* Kartik Juneja
* Gurkimat Singh

**Institution:** Chitkara Business School

---

## 📚 References

The accompanying case-study presentation references:

* Zomato / Eternal Ltd. FY25 Annual Report
* The Strategy Story — *Zomato Business Model in 2026*
* Zomato Google Play listing

---

## 📌 Disclaimer

This project is created for **educational and academic purposes only**.

It is an independent proposed AI/ML solution and is **not affiliated with, endorsed by, or an official implementation of Zomato**.
