# Personalized Online Course Recommender System with Machine Learning

## Problem Statement
With the proliferation of online learning platforms offering a vast array of courses, learners often face the challenge of selecting courses that align with their interests, goals, and skill levels. The sheer volume and diversity of available courses can overwhelm users, leading to suboptimal course choices or decision paralysis. This project aims to develop a personalized online course recommender system that addresses these challenges. By leveraging user preferences, historical behavior data, and course characteristics, the system will intelligently recommend courses tailored to each user's unique needs. The goal is to enhance user experience, increase course engagement, and facilitate continuous learning by providing relevant and personalized course recommendations.

## Table of Contents
1. [Introduction](#introduction)
2. [Exploratory Data Analysis](#exploratory-data-analysis)
3. [Content-based Recommender System](#content-based-recommender-system)
4. [Collaborative-filtering Recommender System](#collaborative-filtering-recommender-system)
5. [Conclusions](#conclusions)
6. [Appendix](#appendix)

## Introduction

A course recommendation system is crucial for helping users find better and more personalized course options. This project explores multiple approaches to building such a system, each with unique assumptions and methodologies.

### Objectives:

- **Find better courses**: Enhance the course discovery process.
- **Personalized recommendations**: Tailor recommendations to individual interests.
- **Multiple approaches**: Compare various recommendation algorithms.

## Exploratory Data Analysis

This section involves analyzing the dataset to understand the distribution and popularity of courses. Key visualizations include:

##### Course Counts Per Genre

![Course Counts Per Genre](https://github.com/abhishek-sriram/Personalized-Online-Course-Recommender-System/blob/main/Screenshots/Screenshot_1.png)

##### Course Enrollment Distribution

![Course Enrollment Distribution](https://github.com/abhishek-sriram/Personalized-Online-Course-Recommender-System/blob/main/Screenshots/Screenshot_2.png)


##### Top 20 Most Popular Courses

![Top 20 Most Popular Courses](https://github.com/abhishek-sriram/Personalized-Online-Course-Recommender-System/blob/main/Screenshots/Screenshot_3.png)


##### Word Cloud of Course Titles

![Word Cloud of Course Titles](https://github.com/abhishek-sriram/Personalized-Online-Course-Recommender-System/blob/main/Screenshots/Screenshot_4.png)

## Content-Based Recommender System

This approach involves recommending courses based on user profiles and course content.

### Unsupervised Learning

A flowchart of the content-based recommender system using user profiles and course genres is illustrated below:

![Content-based Recommender Flowchart](flowchart1.png)

**Process:**
1. **User profile vector**: Calculate the user profile vector.
2. **Course genres**: Analyze course genres for unknown courses.
3. **Dot product calculation**: Compute dot products to determine similarity.
4. **Threshold check**: Compare scores against a threshold to make recommendations.

**Evaluation:**
- Most frequently recommended courses
- Average number of new/unseen courses recommended per user

## Collaborative-filtering Recommender System

This system leverages user interactions to recommend courses. Three different methods are explored: K-Nearest Neighbors (KNN), Non-negative Matrix Factorization (NMF), and Neural Network Embedding.

### KNN-based Recommender System
![KNN-based Flowchart](flowchart2.png)

**Process:**
1. **Train-test split**: Split the data.
2. **User interaction matrix**: Create a matrix based on user interactions.
3. **Cosine similarity**: Calculate similarity between users.
4. **Model training**: Train the KNN model using Scikit-surprise.
5. **Predictions**: Make course recommendations.

### NMF-based Recommender System
![NMF-based Flowchart](flowchart3.png)

**Process:**
1. **Matrix split**: Divide data into two dense matrices (U and I).
2. **NMF**: Apply Non-negative Matrix Factorization.
3. **Matrix product**: Calculate similarity and make predictions.

### Neural Network Embedding-based Recommender System
![Neural Network Flowchart](flowchart4.png)

**Process:**
1. **One-hot encoding**: Encode user and course vectors.
2. **Neural network**: Train the model using neural network embedding.
3. **Scoring**: Predict scores and recommend courses.

**Evaluation:**
- Compare the performance of collaborative-filtering models.
- Identify the highest performing model and key insights.

## Conclusions

- **Model Performance**: User profile-based model has the highest number of recommendations, while the stacking classifier shows the best performance.
- **Complexity**: The similarity matrix's high complexity can be managed using NMF.
- **Recommendations**: Effective personalized recommendations can significantly improve user experience.

## Appendix

For further details, data, and scripts, refer to the following link:
[Project Materials](https://drive.google.com/drive/folders/1OKcl56MRC4ShCSxeGA7x3dQPyf84i6rm?usp=sharing)
