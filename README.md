# **Understanding Player Behavior in Plaicraft.ai for AGI Research by Aamna, Oliver, Sanchia, and Stephanie**
## **Introduction**
The Pacific Laboratory for Artificial Intelligence (PLAI) at UBC is conducting groundbreaking research on human behavior in video game environments using generative AI and machine learning. A centerpiece of this work is **Plaicraft.ai**, a public platform allowing players to engage with Minecraft in a cloud environment to collect valuable gameplay data. PLAI's ultimate goal is to collect over **10,000 hours of gameplay** to advance research in artificial general intelligence (AGI).

## **Research Objective**
PLAI researchers aim to identify which types of players are most likely to contribute significant gameplay data. This understanding will:
- Optimize recruitment strategies to target specific player profiles.
- Improve resource allocation for software and infrastructure.

To address this objective, we analyzed how player characteristics predict total gameplay hours (**played_hours**) by building and evaluating three models:
1. **K-NN Regression**: Predicting played_hours using age.
2. **Simple Linear Regression**: Predicting played_hours using age.
3. **Multivariable Linear Regression**: Predicting played_hours using age, subscription status, experience level, and number of sessions.

We hypothesized that the multivariable linear regression model would outperform the other models, with **lower age**, **high experience level**, **positive subscription status**, and a **high number of sessions** correlating with higher played_hours.

---

## **Summary of Findings**

### **Model Performance**
- **Multivariable Linear Regression** achieved the lowest root mean squared prediction error (RMSPE) of **6.59**, outperforming the other models.
- **K-NN Regression** and **Simple Linear Regression** had much higher RMSPE values of **29.17** and **30.00**, respectively.

These results indicate that multivariable linear regression was the most effective model, likely due to its ability to account for multiple predictors.

### **Key Insights**
1. **Player Age and Gameplay Hours**
   - Younger players tend to log more gameplay hours, aligning with the expected trend that teens and young adults (aged 15-25) are more engaged with gaming.
   - However, the dataset was heavily skewed towards younger players, which may limit the model's predictive performance for older age groups.

2. **Variable Relationships**
   - Age alone did not show a clear linear relationship with played_hours, making simple linear regression less effective.
   - Number of sessions had a stronger linear relationship with played_hours, highlighting its importance as a predictor.

### **Unexpected Findings**
- **K-NN Regression** performed only slightly better than simple linear regression. This may be due to limited data variety in the age range, with most participants being under 25 years old.

---

## **Challenges and Future Improvements**
- **Data Imbalance**: The dataset lacked diversity in player age, reducing the generalizability of our findings. Future efforts should focus on recruiting players from a broader age range.
- **Model Refinement**: Exploring additional predictive algorithms (e.g., random forests or gradient boosting) may improve accuracy.
- **Feature Engineering**: Incorporating more behavioral metrics, such as in-game actions or achievements, could enhance model performance.

