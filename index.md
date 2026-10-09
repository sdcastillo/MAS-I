---
layout: default
title: MAS-I
description: Study notes and R code for the CAS Modern Actuarial Statistics I exam.
samwiki: true
---

<div class="sw-lede">
  <div class="sw-lede-copy">
    <h2>Modern Actuarial Statistics I</h2>
    <p>MAS-I is a Casualty Actuarial Society exam on the statistics used in pricing and reserving. The CAS content outline splits it into three domains. Probability models, including stochastic processes and survival models, are about 20–30% of the exam. Statistics, at the level of a second undergraduate course, is about 20–30%. Extended linear models are about 45–55%, and that is the domain these notes work through in R.</p>
    <p>This repository is one study installment: a single R Markdown note from August 2018, the HTML page already rendered from it, and five small tables used in the examples. The write-up is practice for the exam. It sits beside the CAS outline and the readings, and the model comparisons in the note are left as they were drafted.</p>
    <p>The note opens with six response distributions that show up in severity and survival work: exponential, gamma, Weibull, Pareto, lognormal, and beta. Each one has a short reminder of how it is built, then a simulated density and distribution function. A Gaussian model on the Dobson carbohydrate data asks whether age belongs beside weight and protein, and compares the two fits with deviance, AIC, an extra-sum-of-squares test, residual plots, and variance inflation factors. An added exercise indicator turns the same regression into an ANCOVA.</p>
    <p>The later examples are categorical and count models, each tied to a CSV in this repository. Beetle mortality is a grouped binomial response, fit with logit, probit, and complementary log-log links. Car preferences are an ordered rating of power steering, fit once as a nominal multinomial model and once as a cumulative-odds model. Smoking and coronary deaths are a Poisson rate with a person-years offset, a quadratic age term, and a smoking interaction. Aspirin and ulcer counts are a contingency table fit by Poisson regression, from a short interaction model out to the saturated model, so the drop in AIC and deviance is visible. Third-party claim counts by local government area are overdispersed relative to a Poisson; the note refits them with a negative binomial and with quasi-likelihood.</p>
    <p>The files are arranged as that one installment, Linear Models Part I. The probability-model and statistics domains are the setting for the distributions and the hypothesis tests, and they are not written out as separate chapters here. <a href="{{ '/Linear_Models_Part_I.html' | relative_url }}">Linear_Models_Part_I.html</a> is the rendered note, with the plots. <code>Linear Models Part I.Rmd</code> is the source, and the five CSVs sit in the repository root beside it. The R chunks still read those tables from an old local path, so the copies here are the ones to point at if you knit the note yourself.</p>
  </div>
  <aside class="sw-find">
    <h2>In this repository</h2>
    <ul>
      <li><strong>Rendered note</strong> Linear Models Part I, HTML with the figures.</li>
      <li><strong>Source</strong> The R Markdown file in the repository root.</li>
      <li><strong>Five tables</strong> Beetles, car preferences, smoking deaths, aspirin and ulcers, third-party claims.</li>
      <li><strong>Exam weight</strong> Extended linear models are about half of MAS-I.</li>
      <li><strong>What stays put</strong> The fitted models and the commentary in the note.</li>
    </ul>
  </aside>
</div>

## The exam

- **Probability models (about 20–30%).** Stochastic processes and survival models, including the severity distributions the note simulates first.
- **Statistics (about 20–30%).** Estimation, hypothesis tests, and insurance frequency, severity, and aggregate claims. The note uses that toolkit when it compares AIC, deviance, and nested models.
- **Extended linear models (about 45–55%).** Link functions, response distributions, categorical and ordinal predictors, offsets, model comparison, and software output. The worked examples are this section.

## How the note is organized

- Six response distributions, each with an empirical density and distribution function.
- A continuous response: Gaussian ANOVA, then ANCOVA after an exercise factor is added.
- Grouped binary data: logit, probit, and complementary log-log on beetle mortality.
- An ordered preference: nominal logistic regression, then a cumulative-odds model, on the car survey.
- Counts: a Poisson rate for smoking deaths, Poisson regression on the aspirin–ulcer table, and negative binomial plus quasi-likelihood for overdispersed third-party claims.

## Read the note

<div class="sw-grid">
  <article class="sw-card">
    <div class="sw-card-top">
      <h3 class="sw-name"><a href="{{ '/Linear_Models_Part_I.html' | relative_url }}">Linear Models Part I</a></h3>
      <span class="sw-lang">R Markdown</span>
    </div>
    <p class="sw-badge">Rendered</p>
    <p class="sw-desc">Distributions, ANOVA and ANCOVA, grouped binomial links, nominal and proportional-odds models, Poisson rates, and overdispersion. Plots are in the HTML.</p>
    <div class="sw-actions">
      <a class="sw-btn sw-btn-live" href="{{ '/Linear_Models_Part_I.html' | relative_url }}">Open note</a>
      <a class="sw-btn sw-btn-source" href="https://github.com/sdcastillo/MAS-I/blob/master/Linear%20Models%20Part%20I.Rmd">Source</a>
    </div>
  </article>
</div>

## Datasets

The tables below are the ones named in the note. Column lists match the files in the repository root. They are study copies; this repository does not claim ownership of the underlying data.

<div class="sw-grid">
  <article class="sw-card">
    <div class="sw-card-top">
      <h3 class="sw-name"><a href="{{ '/beetle_mortality.csv' | relative_url }}">beetle_mortality.csv</a></h3>
      <span class="sw-lang">Grouped binomial</span>
    </div>
    <p class="sw-desc">Dose, number tested, and number killed. Used for logit, probit, and complementary log-log.</p>
    <div class="sw-actions">
      <a class="sw-btn sw-btn-source" href="{{ '/beetle_mortality.csv' | relative_url }}">CSV</a>
    </div>
  </article>
  <article class="sw-card">
    <div class="sw-card-top">
      <h3 class="sw-name"><a href="{{ '/car_preferences.csv' | relative_url }}">car_preferences.csv</a></h3>
      <span class="sw-lang">Ordinal response</span>
    </div>
    <p class="sw-desc">Sex, age band, a numeric age code, the importance rating, and a frequency weight. Used for the multinomial and proportional-odds fits.</p>
    <div class="sw-actions">
      <a class="sw-btn sw-btn-source" href="{{ '/car_preferences.csv' | relative_url }}">CSV</a>
    </div>
  </article>
  <article class="sw-card">
    <div class="sw-card-top">
      <h3 class="sw-name"><a href="{{ '/smoking_death.csv' | relative_url }}">smoking_death.csv</a></h3>
      <span class="sw-lang">Poisson rate</span>
    </div>
    <p class="sw-desc">Age band, numeric age, smoking status, deaths, and person-years. The person-years column is the offset.</p>
    <div class="sw-actions">
      <a class="sw-btn sw-btn-source" href="{{ '/smoking_death.csv' | relative_url }}">CSV</a>
    </div>
  </article>
  <article class="sw-card">
    <div class="sw-card-top">
      <h3 class="sw-name"><a href="{{ '/aspirin_ulcers.csv' | relative_url }}">aspirin_ulcers.csv</a></h3>
      <span class="sw-lang">Contingency table</span>
    </div>
    <p class="sw-desc">Ulcer type, case or control, aspirin use, and the count in that cell. Fit as a Poisson regression on the frequencies.</p>
    <div class="sw-actions">
      <a class="sw-btn sw-btn-source" href="{{ '/aspirin_ulcers.csv' | relative_url }}">CSV</a>
    </div>
  </article>
  <article class="sw-card">
    <div class="sw-card-top">
      <h3 class="sw-name"><a href="{{ '/Third_party_claims.csv' | relative_url }}">Third_party_claims.csv</a></h3>
      <span class="sw-lang">Overdispersion</span>
    </div>
    <p class="sw-desc">Local government area, a dispersion summary, claims, accidents, an index, population, and population density. Compared under Poisson, negative binomial, and quasi-likelihood.</p>
    <div class="sw-actions">
      <a class="sw-btn sw-btn-source" href="{{ '/Third_party_claims.csv' | relative_url }}">CSV</a>
    </div>
  </article>
</div>

## Using the files

The rendered note is the page to read. The R Markdown source stays in the GitHub repository and is left out of the Jekyll build so its own front matter is not published as a second page. Contributions of further MAS-I notes, code fixes, or practice problems are welcome. The project license is the [MIT License]({{ '/LICENSE' | relative_url }}).

<section class="sw-videos" aria-labelledby="sw-videos-title">
  <h2 id="sw-videos-title">Videos</h2>
  <p>Sam Castillo's video on GLM link functions, the core of the linear-models material in this note.</p>
  <div style="position:relative;padding-top:56.25%;margin:1rem 0;">
    <iframe src="https://www.youtube.com/embed/xDJXuoM6ZCI" title="Mastering GLM Link Functions: A Comprehensive Guide" style="position:absolute;inset:0;width:100%;height:100%;border:0;" allowfullscreen loading="lazy"></iframe>
  </div>
  <ul>
    <li><a href="https://www.youtube.com/watch?v=xDJXuoM6ZCI">Mastering GLM Link Functions: A Comprehensive Guide</a> (YouTube)</li>
  </ul>
</section>
