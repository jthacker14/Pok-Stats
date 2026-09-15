# PokéStats: Advanced Machine Learning & Statistical Analysis of Pokémon Mechanics

**SSDI Final Project**
*   **S058** - Ishita Kaur Sahni
*   **S071** - Jiya Thacker

---

## 🌟 Project Rationale & Overview
This dataset was purposefully selected to serve two distinct domains: **competitive gaming** and **cartoon/animation referencing**. By mapping the raw statistical data of the Pokémon universe, this project provides animators and fans with a structured reference guide for the entire creature roster across all generations. Concurrently, it decodes the hidden mathematical balance of the games, utilizing advanced predictive models and variance analysis to understand power scaling, typing advantages, and rarity mechanics.

Starting with a raw dataset of 1025 entries, we filtered the roster down to 13 essential combat and biological features, rigorously cleaning the data to ensure zero duplicates and accurate formatting. 

---

## 📈 Probability & Distribution Modeling
We applied robust probability models to understand the baseline mechanics of the Pokémon universe:
*   **Probability Mass Function (PMF):** Visualized Pokémon generations, revealing that expansion occurs in distinct, non-uniform bursts, with Generation V and Generation I introducing the most species.
*   **Probability Density Function (PDF):** Mapped hit points (HP) to show that the vast majority of Pokémon fall into a stable survival range, while extreme HP values are statistically rare.
*   **Maximum Likelihood Estimation (MLE):** Calculated the mathematically ideal mean HP (mu = 70.18) and standard deviation (sigma = 26.62) that best fits the normal distribution of the roster.
*   **Poisson Distribution:** Modeled the deliberate design choice of introducing Legendary Pokémon, estimating an average arrival rate of lambda = 7.89 per generation.
*   **Geometric & Exponential Distributions:** Analyzed capture rates, proving mathematically that elusive species requiring high capture attempts are statistically rare by design.
*   **Bayes' Theorem:** Computed posterior probabilities to prove that specific typings, specifically Dragon and Psychic, act as strong mathematical evidence that a Pokémon is Legendary.

---

## 🧪 Hypothesis Testing
To validate perceived game mechanics, we executed strict statistical tests:
*   **T-Tests & Z-Tests:** Confirmed that Legendary Pokémon possess significantly superior base stats across every single category compared to non-Legendaries (p = 0.0000).
*   **Welch's T-Test:** Evaluated unequal variances to prove that Dragon-type Pokémon hit significantly harder in Attack than Normal-types (t = 4.4111, p = 0.000023).
*   **Proportion Testing:** Demonstrated that while dual-typing adds complexity, the proportion of dual-types does not differ significantly between Legendary and standard Pokémon (p = 0.2612).

---

## 📊 Variance Analysis (ANOVA & MANOVA)
We analyzed how different classifications jointly impact power levels:
*   **One-Way ANOVA:** Proved that the average base stat total differs significantly depending on the generation (p = 0.0002).
*   **Multi-Way ANOVA:** Confirmed that generation, Legendary status, and dual-typing all independently and significantly contribute to a Pokémon's overall power scaling.
*   **MANOVA:** Evaluated multivariate effects, demonstrating that a Pokémon's generation simultaneously impacts its combined Attack and Defense profile (Wilks' lambda p = 0.0004).

---

## 🤖 Predictive Machine Learning Models
To predict competitive viability and classification, we deployed an array of machine learning algorithms:

### Data Preprocessing
*   **Standardization:** Applied a Standard Scaler fitted exclusively to the training data to neutralize magnitude biases, giving features a mean of 0 and standard deviation of 1.
*   **Encoding:** Utilized One-Hot Encoding to transform categorical generation strings into machine-learning-friendly binary dummy variables.

### Regression Models
*   **Ordinary Least Squares (OLS):** Revealed that while total base stats strongly predict Attack, adding Speed to the formula produces a negative coefficient. This mathematically highlights game balancing: faster Pokémon are given slightly lower attack powers.
*   **Multiple Linear Regression:** Predicted base stat totals using HP, Defense, and Speed, achieving an R-squared of 0.84.
*   **Lasso & Ridge Regularization:** Both L1 and L2 regularized models produced nearly identical error rates (RMSE = 45.9), proving that the standard OLS model was not overfitting and that the selected stats hold genuine predictive value without severe multicollinearity.

### Classification Models
*   **Naive Bayes:** Predicted Legendary status based on core combat stats with an impressive 92.86% accuracy.
*   **Logistic Regression:** Achieved an exceptional 96.10% accuracy in binary Legendary classification (MSE: 0.039), excelling perfectly at identifying standard Pokémon.
*   **Random Forest Classifier:** This ensemble learning method achieved 94.15% accuracy. By extracting feature importances, the model revealed that Special Defense, Speed, and Special Attack are the most critical factors decision trees use to separate Legendary Pokémon from regular ones.

---
*“I see now that the circumstances of one's birth are irrelevant. It is what you do with the gift of life that determines who you are.”* - Mewtwo
