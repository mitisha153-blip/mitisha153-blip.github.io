---
layout: single
title: ""
classes: wide
author_profile: false
permalink: /
---

<style>
.portfolio-hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  margin: 35px 0 55px;
}

.portfolio-intro {
  flex: 1 1 60%;
  min-width: 0;
}

.portfolio-photo {
  flex: 0 1 35%;
  width: 260px;
  max-width: 100%;
  height: auto;
  border-radius: 14px;
  object-fit: cover;
}

.portfolio-intro {
  flex: 1;
}

.portfolio-intro h1 {
  font-size: clamp(1.8rem, 3vw, 2.5rem);
  line-height: 1.15;
  margin-bottom: 20px;
  color: #17385f;
}

.portfolio-intro p {
  font-size: 1rem;
  line-height: 1.7;
}

.portfolio-photo {
  width: 260px;
  max-width: 100%;
  border-radius: 14px;
  object-fit: cover;
}

.portfolio-button {
  display: inline-block;
  background: #17385f;
  color: white !important;
  padding: 11px 20px;
  border-radius: 6px;
  text-decoration: none !important;
  margin-top: 15px;
}

.portfolio-projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin-top: 25px;
}

.project-card {
  border: 1px solid #e2e8f0;
  border-radius: 10px;
  padding: 22px;
  background: #f8fafc;
}

.project-card h3 {
  margin-top: 0;
  color: #17385f;
}

@media (max-width: 700px) {
  .portfolio-hero {
    flex-direction: column-reverse;
    gap: 20px;
  }

  .portfolio-photo {
    width: 220px;
  }

  .portfolio-projects {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="portfolio-hero">
  <div class="portfolio-intro">
    <h1>Hi, I'm Mitisha Shah!</h1>

    <h3>Finance × Business Analytics</h3>

    <p>
      I'm a Chartered Accountant currently pursuing
      my MS in Business Analytics and Information
      Management at Purdue University.
    </p>

    <p>
      With over five years of professional experience
      in finance and taxation, I combine financial
      expertise with analytical thinking to solve
      business problems.
    </p>

    <a class="portfolio-button" href="/projects/">
      Explore My Projects
    </a>
  </div>

  <img
    class="portfolio-photo"
    src="/assets/images/mitisha-profile.jpg"
    alt="Professional headshot of Mitisha Shah">
</div>

<h2>Featured Projects</h2>

<div class="portfolio-projects">

  <div class="project-card">
    <h3>Loan Default Prediction</h3>
    <p>
      Applying predictive analytics to assess
      credit risk and support lending decisions.
    </p>
  </div>

  <div class="project-card">
    <h3>Customer Targeting Analytics</h3>
    <p>
      Using machine learning to evaluate
      customer targeting and marketing profitability.
    </p>
  </div>

  <div class="project-card">
    <h3>Google Cloud POS Automation</h3>
    <p>
      Building an event-driven data pipeline
      using Google Cloud and BigQuery.
    </p>
  </div>

  <div class="project-card">
    <h3>Charles Schwab Brand Strategy</h3>
    <p>
      Exploring financial-services brand
      positioning and advisory differentiation.
    </p>
  </div>

</div>

<h2>Let's Connect</h2>

<p>
  <a href="https://www.linkedin.com/in/mitisha-shah-9a83b717b">
    LinkedIn
  </a>
  |
  <a href="https://github.com/mitisha153-blip">
    GitHub
  </a>
</p>
