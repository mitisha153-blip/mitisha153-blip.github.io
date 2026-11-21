---
layout: single
title: "Predicting Digital Ad Clicks with Ensemble Machine Learning"
permalink: /projects/kaggle-ad-click-prediction/
author_profile: false
classes: wide
---

# Predicting Digital Ad Clicks with Ensemble Machine Learning

**Kaggle Machine Learning Competition | Team RAM**

**Python · XGBoost · LightGBM · CatBoost · Scikit-learn · Ensemble Learning**

> **Competition achievement:** Our three-member team
> ranked **6th among 20 teams**, achieving a private
> leaderboard ROC-AUC of **0.7941**.

## Project Overview

Digital advertising platforms need to predict which
advertisements are most likely to receive clicks.
Accurate predictions can help improve campaign
targeting and advertising efficiency.

In this team competition, we developed machine-learning
models to predict whether an advertising impression
would result in a click.

The dataset contained:

- **60,000 training impressions**
- **20,000 test impressions**
- **34 predictor variables**
- **809 positive clicks**, approximately **1.35%**
  of the training data

The extremely low click rate made model validation,
regularization, and reliable ranking especially
important.

## My Contribution

I participated across the project lifecycle, including
data preprocessing, feature engineering, model
development, evaluation, and collaborative model
selection.

My primary modeling approach combined three
gradient-boosting algorithms:

1. **XGBoost**
2. **LightGBM**
3. **CatBoost**

I experimented with engineered features,
hyperparameter tuning, and ensemble predictions
to improve ROC-AUC performance.

My three-model ensemble achieved a cross-validation
ROC-AUC of approximately **0.7915**.

## Analytical Approach

### 1. Data Preparation

We investigated missing values, categorical features,
and the highly imbalanced target variable.

Some variables used `-1` to represent unavailable
information. We evaluated how missingness could
carry useful predictive information rather than
automatically replacing every missing value.

### 2. Model Development

We compared multiple algorithms, including:

- Logistic Regression
- Spline Logistic Regression
- Random Forest
- XGBoost
- LightGBM
- CatBoost

My approach focused on combining XGBoost, LightGBM,
and CatBoost using rank-based ensemble predictions.

### 3. Validation Strategy

We evaluated competing approaches using
stratified five-fold cross-validation repeated
across three random seeds.

This produced **15 validation folds**.

For models using early stopping, an additional
inner training split helped prevent the outer
validation fold from influencing model training.

The primary evaluation metric was **ROC-AUC**,
which measures how effectively a model ranks
clicked impressions above non-clicked impressions.

## Model Comparison

| Approach | Cross-Validation ROC-AUC |
|---|---:|
| Linear Logistic Regression | 0.7825 |
| Spline Logistic Regression | 0.7902 |
| Regularized LightGBM | 0.7908 |
| **My XGBoost + LightGBM + CatBoost ensemble** | **0.7915** |
| **Team's selected LightGBM + Spline blend** | **0.7940** |

The difference between the two ensemble approaches
was approximately **0.0026 ROC-AUC**.

Because validation results varied across folds,
we considered consistency and generalization
rather than relying on small differences in
average performance alone.

## Visual 1 — Cross-Validation Performance

The following chart compares the main approaches
using their cross-validation ROC-AUC scores.

<div style="margin: 1.5rem 0;">
  <div style="font-weight:600;margin-bottom:1rem;">
    Model comparison
  </div>

  <div style="margin-bottom:1rem;">
    <div>Linear Logistic Regression — 0.7825</div>
    <div style="background:#e8edf2;border-radius:6px;">
      <div style="width:78.25%;background:#8296aa;height:18px;border-radius:6px;"></div>
    </div>
  </div>

  <div style="margin-bottom:1rem;">
    <div>Spline Logistic Regression — 0.7902</div>
    <div style="background:#e8edf2;border-radius:6px;">
      <div style="width:79.02%;background:#8296aa;height:18px;border-radius:6px;"></div>
    </div>
  </div>

  <div style="margin-bottom:1rem;">
    <div>Regularized LightGBM — 0.7908</div>
    <div style="background:#e8edf2;border-radius:6px;">
      <div style="width:79.08%;background:#8296aa;height:18px;border-radius:6px;"></div>
    </div>
  </div>

  <div style="margin-bottom:1rem;">
    <div><strong>My three-model ensemble — 0.7915</strong></div>
    <div style="background:#e8edf2;border-radius:6px;">
      <div style="width:79.15%;background:#087f8c;height:18px;border-radius:6px;"></div>
    </div>
  </div>

  <div>
    <div><strong>Team's final blend — 0.7940</strong></div>
    <div style="background:#e8edf2;border-radius:6px;">
      <div style="width:79.40%;background:#17365d;height:18px;border-radius:6px;"></div>
    </div>
  </div>
</div>

*Bar lengths represent ROC-AUC on a 0–1 scale;
the numerical labels provide the precise comparison.*

## Final Team Solution

After comparing the alternatives, our team selected
a **50/50 probability blend** of:

- A heavily regularized LightGBM model
- A spline-based logistic regression model

LightGBM captured thresholds and interactions,
while the spline model captured smoother,
nonlinear relationships.

The selected blend performed better than LightGBM
alone in **13 of 15 validation folds**.

## Visual 2 — Validation vs. Leaderboard Results

| Evaluation | ROC-AUC |
|---|---:|
| Cross-validation | 0.7940 |
| Public leaderboard | 0.8304 |
| Private leaderboard | 0.7941 |

The public leaderboard score was noticeably higher
than both cross-validation and private leaderboard
performance.

Our cross-validation estimate closely matched
the private leaderboard result.

This reinforced an important lesson:
**reliable validation is more valuable than
optimizing for a potentially noisy public leaderboard.**

## Results & Key Takeaways

Our team finished **6th among 20 participating teams**
on the private leaderboard.

The project strengthened my experience in:

- Developing and comparing machine-learning models
- Building gradient-boosting ensembles
- Working with imbalanced classification datasets
- Feature engineering and hyperparameter tuning
- Designing leakage-aware validation procedures
- Collaborating to select models based on evidence

One of my biggest takeaways was that more complex
models do not automatically perform better.

Although my three-model ensemble performed
competitively, the team's LightGBM–spline blend
produced a slightly stronger result.

Selecting the better-performing approach helped
us prioritize the quality of the final solution
over any individual model.

---

[Back to All Projects](/projects/)
