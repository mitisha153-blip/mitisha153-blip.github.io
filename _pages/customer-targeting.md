---
layout: single
title: "Customer Targeting & Profitability Optimization"
permalink: /projects/customer-targeting/
author_profile: false
classes: wide
---

<style>
.profit-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 12px;
  margin: 25px 0;
}
.profit-card {
  padding: 18px 12px;
  background: #f1f6f8;
  border: 1px solid #dce5ec;
  border-radius: 10px;
  text-align: center;
}
.profit-number {
  display: block;
  font-size: 1.5rem;
  font-weight: 700;
  color: #17365d;
}
.profit-label {
  display: block;
  font-size: 0.8rem;
  color: #526477;
  margin-top: 5px;
}
.profit-chart-row {
  margin: 18px 0;
}
.profit-chart-track {
  height: 20px;
  background: #e8edf2;
  border-radius: 5px;
  overflow: hidden;
  margin-top: 7px;
}
.profit-chart-fill {
  height: 100%;
  border-radius: 5px;
}
@media (max-width: 650px) {
  .profit-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<p style="color:#64748b;font-size:1.05rem;">
  Predictive Analytics | Machine Learning | Marketing ROI
</p>

## Business Problem

A fashion retailer wanted to improve the profitability
of its direct-mail marketing campaign.

Mailing every customer incurs unnecessary costs,
particularly when only a small proportion are
likely to purchase.

The challenge was to identify customers worth
targeting and determine whether predictive models
could generate better financial returns than
mailing the entire customer base.

## Analytical Approach

I evaluated predictive classification models,
including:

- L2-regularized Logistic Regression
- Random Forest
- Extra Trees
- Gradient Boosting

Model performance was evaluated using ROC-AUC,
average precision, and probability calibration.

I then translated predicted purchase probabilities
into marketing decisions using a profitability-based
mailing threshold of **8.33%**.

This threshold reflects a $2 mailing cost and
$24 contribution per purchase.

## Results

<div class="profit-grid">
  <div class="profit-card">
    <span class="profit-number">$833K</span>
    <span class="profit-label">Estimated net profit: tuned Random Forest</span>
  </div>
  <div class="profit-card">
    <span class="profit-number">255%</span>
    <span class="profit-label">Estimated ROI: tuned Random Forest</span>
  </div>
  <div class="profit-card">
    <span class="profit-number">67%</span>
    <span class="profit-label">Fewer customers mailed vs. baseline</span>
  </div>
</div>

### Estimated Profitability Comparison

| Strategy | Customers Mailed | Estimated Net Profit | ROI |
|---|---:|---:|---:|
| Non-targeted mailing | 500,000 | $160,000 | 16.0% |
| L2 Logistic Regression | 165,000 | $790,000 | 239.4% |
| Tuned Random Forest | 163,333 | $833,333 | 255.1% |

## Visual — Estimated Net Profit

<div role="img" aria-label="Estimated net profit comparison: non-targeted mailing $160,000, logistic regression $790,000, and tuned random forest $833,333.">

  <div class="profit-chart-row">
    <strong>Non-targeted mailing — $160K</strong>
    <div class="profit-chart-track">
      <div class="profit-chart-fill" style="width:19.2%;background:#94a3b8;"></div>
    </div>
  </div>

  <div class="profit-chart-row">
    <strong>L2 Logistic Regression — $790K</strong>
    <div class="profit-chart-track">
      <div class="profit-chart-fill" style="width:94.8%;background:#087f8c;"></div>
    </div>
  </div>

  <div class="profit-chart-row">
    <strong>Tuned Random Forest — $833K</strong>
    <div class="profit-chart-track">
      <div class="profit-chart-fill" style="width:100%;background:#17365d;"></div>
    </div>
  </div>

</div>

*Estimated net profit for a simulated customer base of
500,000. Bar lengths are proportional to net profit.*

## Business Impact

The tuned Random Forest strategy produced an
estimated net profit of approximately **$833,333**,
compared with **$160,000** from non-targeted mailing.

This represents approximately **$673,333 in
additional estimated profit**, while mailing
approximately **67% fewer customers**.

These are model-based estimates from the
case analysis, not realized commercial results.

## Key Takeaways

- Predictive models can improve marketing profitability
  by prioritizing higher-value customers.
- The best classification threshold depends on
  business economics, not necessarily 50%.
- Model selection should consider financial impact
  alongside statistical performance.
- Combining analytics with business assumptions
  can turn model predictions into actionable decisions.

---

[Back to All Projects](/projects/)
