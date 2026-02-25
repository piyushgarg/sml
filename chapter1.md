Chapter 1, **"The Machine Learning Landscape,"** serves as a high-level map of the field. It moves away from the "magic" of AI and focuses on the practical definitions, categories, and challenges you'll face as a practitioner.

---

## 1. What is Machine Learning?

Machine Learning (ML) is the science of programming computers so they can **learn from data**. Instead of hard-coding a long list of rules (like a spam filter based on specific keywords), an ML system builds a model based on patterns found in examples.

* **Training Set:** The examples the system uses to learn.
* **Model:** The part of the system that learns and makes predictions.
* **Accuracy:** A common metric to evaluate how well the model is performing.

---

## 2. Why Use Machine Learning?

ML shines in scenarios where:

* **Existing problems** require a long list of hand-tuned rules.
* **Complex problems** have no known algorithmic solution (like speech recognition).
* **Fluctuating environments:** The system needs to adapt to new data constantly.
* **Data Mining:** Helping humans find patterns they didn't know existed.

---

## 3. Types of Machine Learning Systems

Gerion classifies ML systems based on four main criteria:

### A. How they are supervised

1. **Supervised Learning:** The data includes the "answers" (labels). Examples: Linear Regression, SVMs, Decision Trees.
2. **Unsupervised Learning:** The data is unlabeled. The system tries to learn without a teacher. Examples: Clustering (K-Means), Dimensionality Reduction (PCA), Association Rule Learning.
3. **Semisupervised Learning:** Deals with partially labeled data (usually a lot of unlabeled data and a little bit of labeled data).
4. **Reinforcement Learning:** An **agent** observes the environment, selects actions, and gets **rewards** or **penalties**. It learns the best strategy (**policy**) over time.

### B. Batch vs. Online Learning

* **Batch Learning:** The system is incapable of learning incrementally; it must be trained using all available data. This usually happens offline.
* **Online Learning:** The system is trained incrementally by feeding it data instances sequentially, either individually or in small groups (mini-batches). Great for systems receiving a continuous flow of data.

### C. Instance-based vs. Model-based Learning

* **Instance-based:** The system learns the examples by heart, then generalizes to new cases by comparing them to the learned examples (e.g., K-Nearest Neighbors).
* **Model-based:** The system builds a model of the examples and uses that model to make predictions (e.g., a linear equation $y = \theta_0 + \theta_1x$).

---

## 4. Main Challenges of Machine Learning

Most "failures" in ML come from either **bad data** or **bad algorithms**.

### Bad Data Problems:

* **Insufficient Quantity:** Even simple problems need thousands of examples; complex ones (like image recognition) need millions.
* **Non-representative Data:** If your training data doesn't represent the real world, your model will be biased (Sampling Bias).
* **Poor Quality:** Data full of errors, outliers, and noise makes it hard for the model to see patterns.
* **Irrelevant Features:** "Garbage in, garbage out." Feature engineering is crucial.

### Bad Algorithm Problems:

* **Overfitting:** The model is too complex for the amount of data and learns the "noise" instead of the pattern. It performs great on training data but poorly on new data.
* **Underfitting:** The model is too simple (e.g., trying to fit a line to a curve). It performs poorly on both training and test data.

---

## 5. Testing and Validating

To know if a model will work in production, you must test it.

* **Train/Test Split:** You typically split your data (e.g., 80% train, 20% test).
* **Generalization Error:** The error rate on new cases (test set).
* **Validation Set:** Used to compare different models and tune hyperparameters. If you use the test set to tune your model, you risk "leaking" information, and the model won't generalize well.

---

## Non-interactive version of the practice quiz.

### **Chapter 1: The Machine Learning Landscape Quiz**

**1. A system is trained on a dataset where each example is paired with a specific target value (label). What type of learning is this?**

* A) Unsupervised Learning
* B) Reinforcement Learning
* C) Supervised Learning
* D) Instance-based Learning

**2. Which of the following is a classic example of an Unsupervised Learning task?**

* A) Identifying spam emails in an inbox
* B) Grouping similar customers based on purchasing habits (Clustering)
* C) Predicting the future price of a stock based on historical data
* D) Classifying images of handwritten digits

**3. If a model performs exceptionally well on the training data but fails to generalize to new, unseen data, it is likely experiencing:**

* A) Underfitting
* B) Sampling Bias
* C) Overfitting
* D) Feature Engineering

**4. What is the defining characteristic of "Online Learning"?**

* A) It requires a constant internet connection to function.
* B) It can learn incrementally by feeding data instances sequentially or in mini-batches.
* C) It is only used for unsupervised tasks like clustering.
* D) It must be trained on the entire dataset at once (offline).

**5. Why should you use a "Validation Set" (or cross-validation) during model development?**

* A) To increase the amount of data available for the final training.
* B) To provide the final performance metric for the production report.
* C) To tune hyperparameters and compare different models without biasing the test set.
* D) To replace the test set entirely when data is scarce.

**6. "Garbage In, Garbage Out" in Machine Learning refers to the idea that:**

* A) Complex algorithms can compensate for low-quality data.
* B) The quality of a model’s output is limited by the quality and relevance of the input data.
* C) Old data should be deleted (thrown out) to make room for new data.
* D) Deep Learning models do not require data cleaning.

**7. "Feature Engineering" is the process of:**

* A) Upgrading the hardware (CPU/GPU) used for training.
* B) Selecting and transforming raw data into useful attributes for the learning algorithm.
* C) Automatically adjusting the learning rate of a neural network.
* D) Gathering millions of new data points to fix underfitting.

**8. If you use a simple linear model to try to predict a highly complex, curved relationship and it performs poorly on both training and test data, the model is:**

* A) Overfitting
* B) Underfitting
* C) Regularized
* D) Converged

**9. What is the difference between Instance-based and Model-based learning?**

* A) Instance-based uses an equation; Model-based uses a database.
* B) Instance-based learns by heart and compares new cases to known ones; Model-based builds a generalization (like a function).
* C) Instance-based is for small data; Model-based is for big data.
* D) There is no difference; they are two names for the same thing.

**10. When splitting data, what is the "Generalization Error"?**

* A) The error rate on the training set.
* B) The error caused by choosing the wrong algorithm.
* C) The error rate the model makes on new, unseen cases (typically measured on the test set).
* D) The error rate during the feature engineering phase.

---

### **Answer Key**

1. **C** (Supervised Learning)
2. **B** (Clustering customers)
3. **C** (Overfitting)
4. **B** (Learns incrementally)
5. **C** (To tune hyperparameters)
6. **B** (Quality of output depends on data quality)
7. **B** (Transforming raw data into useful features)
8. **B** (Underfitting)
9. **B** (Generalization vs. heart-learning)
10. **C** (Error on new cases)


## Exercises

In this chapter we have covered some of the most important concepts in machine learning. In the next chapters we will dive deeper and write more code, but before we do, make sure you can answer the following questions:

1. How would you define machine learning?

2. Can you name four types of applications where it shines?

3. What is a labeled training set?

4. What are the two most common supervised tasks?

5. Can you name four common unsupervised tasks?

6. What type of algorithm would you use to allow a robot to walk in various unknown terrains?

7. What type of algorithm would you use to segment your customers into multiple groups?

8. Would you frame the problem of spam detection as a supervised learning problem or an unsupervised learning problem?

9. What is an online learning system?

10. What is out-of-core learning?

11. What type of algorithm relies on a similarity measure to make predictions?

12. What is the difference between a model parameter and a model hyperparameter?

13. What do model-based algorithms search for? What is the most common strategy they use to succeed? How do they make predictions?

14. Can you name four of the main challenges in machine learning?

15. If your model performs great on the training data but generalizes poorly to new instances, what is happening? Can you name three possible solutions?

16. What is a test set, and why would you want to use it?

17. What is the purpose of a validation set?

18. What is the train-dev set, when do you need it, and how do you use it?

19. What can go wrong if you tune hyperparameters using the test set?

[Solutions](https://nbviewer.org/github/ageron/handson-ml3/blob/main/01_the_machine_learning_landscape.ipynb#Exercise-Solutions) to these exercises are available at the end of this chapter’s notebook.

