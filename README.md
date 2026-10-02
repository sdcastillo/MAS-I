# 📊 MAS-I: Modern Actuarial Statistics I

## Overview

This is Sam's personal study repository containing study notes and R code for the **Modern Actuarial Statistics I (MAS-I) exam**. While I took a career break, I have continued dedicating time to studying for this challenging actuarial examination.

MAS-I is a Casualty Actuarial Society exam. The CAS content outline splits it into three domains: probability models, including stochastic processes and survival models (about 20–30%); statistics at the level of a second undergraduate course (about 20–30%); and extended linear models (about 45–55%). The note in this repository works through that third domain in R.

The repository holds one installment, Linear Models Part I: `Linear Models Part I.Rmd`, the rendered `Linear_Models_Part_I.html`, and five CSV tables used in the examples. The note starts with six response distributions (exponential, gamma, Weibull, Pareto, lognormal, and beta), each with a simulated density and distribution function. It then fits a Gaussian ANOVA and an ANCOVA on a continuous response, grouped logit, probit, and complementary log-log models on beetle mortality, a nominal logistic model and a cumulative-odds model on car preferences, a Poisson rate for smoking deaths, a Poisson contingency table for aspirin and ulcers, and a negative binomial plus quasi-likelihood comparison for overdispersed third-party claims.

The rendered HTML is the page to read. The R chunks still load the tables from an old local path; the CSV copies in the repository root are the files to use if you knit the note yourself. The probability-model and statistics domains are the setting for the distributions and the tests in the examples. They are not separate chapters in this repository.

## 🎯 About This Project

This repository serves as a learning resource for actuarial science students studying for the MAS-I exam. It contains detailed notes, R code examples, and datasets used in practice problems and analysis.

The GitHub Pages home page uses the SamWiki skin on the Cayman theme. Navigation returns to the hub: [Home](https://sdcastillo.github.io/), [About](https://sdcastillo.github.io/about/), and [Code](https://sdcastillo.github.io/code/).

## 📈 Datasets

This repository includes the following datasets used for statistical analysis and modeling practice:

### 1. **Third_party_claims.csv**
Insurance claims data by geographic region (Local Government Area)
- **lga**: Geographic location identifier
- **sd**: Standard deviation metric
- **claims**: Number of insurance claims reported
- **accidents**: Number of accidents recorded
- **ki**: Index metric
- **population**: Population of the region
- **pop_density**: Population density

### 2. **aspirin_ulcers.csv**
Medical study data on ulcer and aspirin usage
- **ulcer**: Type of ulcer (gastric, duodenal)
- **casecontrol**: Study group (case/control)
- **aspirin**: Aspirin usage status (user/non-user)
- **frequency**: Count of observations

### 3. **beetle_mortality.csv**
Toxicology study on beetle mortality rates
- **dose**: Dose level administered
- **number**: Number of beetles tested
- **killed**: Number of beetles killed in the study

### 4. **car_preferences.csv**
Consumer survey data on car preferences
- **sex**: Gender (women/men)
- **age**: Age range category (18-23, 24-40, >40)
- **age_num**: Numeric age category code
- **response**: Preference response level (no/little, important, very important)
- **freq**: Frequency count of responses

### 5. **smoking_death.csv**
Epidemiological data on smoking and mortality
- **age**: Age range category
- **age_num**: Numeric age category code
- **smoking**: Smoking status (smoker/non-smoker)
- **deaths**: Number of deaths recorded
- **person-years**: Total person-years of exposure

## 📝 Course Content

The note is organized as one linear-models installment:

- Six response distributions, with empirical densities and distribution functions
- Continuous response: Gaussian ANOVA, then ANCOVA
- Grouped binary data: logit, probit, and complementary log-log
- Ordered preference: nominal logistic regression and a cumulative-odds model
- Counts: Poisson rates and offsets, a contingency table, negative binomial and quasi-likelihood for overdispersion

Those examples sit inside the MAS-I extended linear models domain. The probability-model domain (stochastic processes and survival models) and the statistics domain are the background for the distributions, the offsets, and the model comparisons.

## 👥 Join Us!

**Are you studying for the MAS-I exam?** This repository is open for collaboration! If you are preparing for this exam or interested in actuarial statistics, feel free to contribute study notes, code improvements, or additional practice problems.

## ⚖️ Data Attribution

**Important Notice**: I do not claim ownership of the datasets included in this repository. These datasets are used for educational purposes as part of actuarial science training materials. Please use them responsibly and respect any original copyright restrictions.

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: the above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

## 🤝 Contributing

This repository welcomes contributions from fellow actuarial science students and professionals. Whether you're sharing study notes, improving code, or suggesting new resources, your contributions help the community learn together.

---

**Last Updated**: October 2026
