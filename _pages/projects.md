---
layout: single
title: "Projects"
permalink: /projects/
author_profile: false
classes: wide
---

<style>
.portfolio-projects-intro {
  max-width: 850px;
  color: #526477;
  font-size: 1.05rem;
  line-height: 1.7;
  margin-bottom: 2rem;
}

.portfolio-projects-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 22px;
  margin: 2rem 0;
}

.portfolio-project-card {
  border: 1px solid #dce5ec;
  border-radius: 14px;
  padding: 25px;
  background: #ffffff;
  display: flex;
  flex-direction: column;
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}

.portfolio-project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(23, 54, 93, 0.10);
}

.portfolio-project-number {
  color: #087f8c;
  font-weight: 700;
  font-size: 0.85rem;
  letter-spacing: 0.08em;
  margin-bottom: 12px;
}

.portfolio-project-card h2 {
  color: #17365d;
  font-size: 1.35rem;
  line-height: 1.3;
  margin: 0 0 12px;
  border: none;
}

.portfolio-project-card p {
  color: #526477;
  font-size: 0.94rem;
  line-height: 1.65;
  margin-bottom: 15px;
}

.portfolio-project-tags {
  color: #087f8c;
  font-size: 0.83rem;
  font-weight: 600;
  margin-top: auto;
  padding-top: 8px;
}

.portfolio-project-link {
  display: inline-block;
  margin-top: 18px;
  padding: 11px 16px;
  border-radius: 7px;
  background: #17365d;
  color: #ffffff !important;
  font-size: 0.88rem;
  font-weight: 600;
  text-decoration: none !important;
  align-self: flex-start;
}

.portfolio-project-link:hover {
  background: #087f8c;
}

.portfolio-project-upcoming {
  display: inline-block;
  margin-top: 18px;
  padding: 10px 14px;
  border-radius: 7px;
  background: #eef3f7;
  color: #64748b;
  font-size: 0.85rem;
  font-weight: 600;
  align-self: flex-start;
}

.portfolio-projects-footer {
  border-top: 1px solid #dce5ec;
  padding-top: 24px;
  margin-top: 35px;
}

@media (max-width: 700px) {
  .portfolio-projects-grid {
    grid-template-columns: 1fr;
  }

  .portfolio-project-card {
    padding: 20px;
  }
}
</style>

<div class="portfolio-projects-intro">
  Explore my work across machine learning, financial
  analytics, predictive modeling, cloud data engineering,
  and business strategy.

  These projects reflect my interest in combining
  financial expertise with analytical techniques to
  solve practical business problems.
</div>

<div class="portfolio-projects-grid">

  <!-- PROJECT 1: KAGGLE -->

  <div class="portfolio-project-card">
    <div class="portfolio-project-number">01 / MACHINE LEARNING</div>

    <h2>Kaggle: Digital Ad Click Prediction</h2>

    <p>
      Developed an ensemble combining XGBoost, LightGBM,
      and CatBoost to predict digital advertising clicks.
      Compared the approach with the team's selected
      LightGBM–spline blend.
    </p>

    <p>
      <strong>Achievement:</strong> Team ranked 6th among
      20 teams on the private leaderboard, achieving
      a ROC-AUC of 0.7941.
    </p>

    <div class="portfolio-project-tags">
      Python · XGBoost · LightGBM · CatBoost
    </div>

    <a class="portfolio-project-link"
       href="/projects/kaggle-ad-click-prediction/">
       View Case Study &rarr;
    </a>
  </div>

  <!-- PROJECT 2: LOAN DEFAULT -->

  <div class="portfolio-project-card">
    <div class="portfolio-project-number">02 / FINANCIAL ANALYTICS</div>

    <h2>Loan Default Prediction</h2>

    <p>
      Applying predictive classification techniques
      to assess credit risk and identify borrowers
      with a higher likelihood of default.
    </p>

    <p>
      Exploring model evaluation, decision thresholds,
      confusion matrices, and the financial implications
      of incorrect lending decisions.
    </p>

    <div class="portfolio-project-tags">
      Credit Risk · Classification · Predictive Modeling
    </div>

    <a class="portfolio-project-link"
   href="/projects/customer-targeting/">
  View Case Study &rarr;
</a>
  </div>

  <!-- PROJECT 3: CUSTOMER TARGETING -->

  <div class="portfolio-project-card">
    <div class="portfolio-project-number">03 / BUSINESS ANALYTICS</div>

    <h2>Customer Targeting &amp; Profitability</h2>

    <p>
      Evaluating how predictive analytics can improve
      direct-mail marketing decisions by identifying
      customers most likely to respond.
    </p>

    <p>
      Comparing logistic regression and random forest
      models, and translating predictions into
      expected profit and return on investment.
    </p>

    <div class="portfolio-project-tags">
      Logistic Regression · Random Forest · Marketing ROI
    </div>

    <span class="portfolio-project-upcoming">
      Case Study Coming Soon
    </span>
  </div>

  <!-- PROJECT 4: CLOUD AUTOMATION -->

  <div class="portfolio-project-card">
    <div class="portfolio-project-number">04 / DATA ENGINEERING</div>

    <h2>Google Cloud POS Data Automation</h2>

    <p>
      Developing an event-driven data pipeline to
      ingest point-of-sale files, process incoming
      data, and refresh analytical tables.
    </p>

    <p>
      Using Google Cloud services to automate
      ingestion workflows and monitor missing
      source files.
    </p>

    <div class="portfolio-project-tags">
      BigQuery · Cloud Run · Eventarc · SQL
    </div>

    <span class="portfolio-project-upcoming">
      Case Study Coming Soon
    </span>
  </div>

  <!-- PROJECT 5: HOUSING ANALYTICS -->

  <div class="portfolio-project-card">
    <div class="portfolio-project-number">05 / PREDICTIVE ANALYTICS</div>

    <h2>Housing Price Prediction</h2>

    <p>
      Analyzing housing price drivers across
      multiple cities using statistical modeling
      and machine-learning techniques.
    </p>

    <p>
      Exploring regression, interaction effects,
      multicollinearity, and model performance
      on validation data.
    </p>

    <div class="portfolio-project-tags">
      Regression · Random Forest · Model Evaluation
    </div>

    <span class="portfolio-project-upcoming">
      Case Study Coming Soon
    </span>
  </div>

  <!-- PROJECT 6: BRAND STRATEGY -->

  <div class="portfolio-project-card">
    <div class="portfolio-project-number">06 / BUSINESS STRATEGY</div>

    <h2>Charles Schwab Brand Strategy</h2>

    <p>
      Developing a brand positioning concept
      focused on strengthening Charles Schwab's
      association with financial advisory expertise.
    </p>

    <p>
      Exploring differentiation, brand reputation,
      and creative communication strategies
      in financial services.
    </p>

    <div class="portfolio-project-tags">
      Brand Positioning · FinTech · Marketing Strategy
    </div>

    <span class="portfolio-project-upcoming">
      Case Study Coming Soon
    </span>
  </div>

</div>

<div class="portfolio-projects-footer">
  <p>
    Interested in discussing my projects or
    opportunities in financial analytics,
    business analytics, and FinTech?
  </p>

  <a href="https://www.linkedin.com/in/mitisha-shah-9a83b717b">
    Connect with me on LinkedIn &rarr;
  </a>
</div>

