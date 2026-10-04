**1. Overview of AI and ML**
Artificial Intelligence (AI) is the broad goal of creating systems capable of human-like intelligence. Machine Learning (ML) is the practical engine we use to achieve this: instead of explicitly programming a computer with rigid, human-written rules, we feed the computer data and allow it to learn the patterns and relationships mathematically on its own.

**2. Supervised vs. Unsupervised Learning**
*   **Supervised Learning:** The model learns from "labeled" data, meaning you provide both the input features and the correct answer or label. 
    *   *Regression:* Predicting continuous numbers (e.g., house prices).
    *   *Classification:* Predicting distinct categories (e.g., spam vs. inbox).
*   **Unsupervised Learning:** The model is trained on "unlabeled" data. Without an answer key, the algorithm's job is to discover hidden structures naturally, such as grouping (clustering) customers with similar buying habits.

**3. Training, Validation, and Test Sets**
To ensure a model actually learns rather than just memorizes, data is split into three parts:
*   **Training Set (e.g., 70%):** The material the model studies and learns from.
*   **Validation Set (e.g., 15%):** The practice test used to tweak and tune the model's settings (hyperparameters) while it is still being developed.
*   **Test Set (e.g., 15%):** The final exam. This is completely unseen data used at the very end to judge how the model will perform in the real world.

**4. What a "Model" is and High-Level Training**
A model is essentially a complex mathematical equation or a set of rules. For example, in a simple linear regression model, the equation calculates the output by multiplying the inputs by specific weights (which represent the importance of that input) and adding a baseline offset (the bias). During training, the algorithm looks at the data, makes a guess, calculates its error, and continuously adjusts those weights and biases to minimize that error over time.

**5. Why Data Needs Cleaning and Preprocessing**
Machine learning algorithms are strict mathematical engines—they cannot process messy, real-world formats. If you feed a model messy data, you will get inaccurate predictions (a concept known as "garbage in, garbage out"). Preprocessing formats the data so the math works correctly, transforming raw text and messy numbers into a clean, uniform matrix.

**6. Handling Missing Data (Imputation)**
Real-world datasets often have empty cells. Since you cannot feed an empty space into a math equation, you must handle it:
*   **Dropping:** Removing the entire row or column containing the missing data.
*   **Imputation:** Filling in the blanks using statistical methods. A common approach is replacing the missing value with the column's mean (average) or median.

**7. Handling Outliers**
Outliers are extreme data points (like a $50 million house in a $300k neighborhood) that can heavily skew the model's math. They are handled by removing them, capping them at a threshold, or mathematically transforming the data. To systematically detect an outlier, we often measure how many standard deviations a data point is from the mean; if it falls too far outside the normal range (e.g., more than 3 standard deviations away), it is flagged as an outlier.

**8. Categorical Encoding**
Because algorithms require numbers instead of text, categorical encoding translates text categories into numeric values.
*   **Label Encoding:** Assigning a sequential integer to each category (e.g., Bad = 0, Good = 1, Great = 2).
*   **One-Hot Encoding:** Creating separate binary columns for each category. Instead of a single "Color" column, you create separate "Is_Red" and "Is_Blue" columns filled with 0s and 1s.

**9. Feature Scaling**
Features often have drastically different ranges (e.g., Age 18–90 vs. Salary $30,000–$200,000). If left unscaled, the massive salary numbers will unfairly dominate the model's calculations. We fix this using scaling:
*   **Normalization (Min-Max Scaling):** Shrinks all values to fit exactly between a specific range, typically 0 and 1.
*   **Standardization:** Centers the data around a mean of 0, ensuring larger ranges don't unfairly dominate the algorithm's distance calculations.

**10. Overfitting vs. Underfitting**
*   **Underfitting:** The model is too simple, fails to capture the data's patterns, and performs poorly on both training and test data.
*   **Overfitting:** The model is too complex and "memorizes" the training data perfectly, including the random noise, which causes it to fail completely on new, unseen test data. 
*   **Goal:** A generalized model that sits perfectly in the middle, performing well on data it has never seen before.

**11. Evaluation Metrics**
Metrics tell you mathematically how well the model is doing based on its true positive, true negative, false positive, and false negative predictions:
*   **Accuracy:** The percentage of total predictions that were completely correct.
*   **Precision:** Out of all the times the model predicted "Positive," how many were actually positive? (Useful for avoiding false alarms).
*   **Recall:** Out of all the actual "Positives" that existed, how many did the model successfully find? (Useful when missing a positive case is highly detrimental).
