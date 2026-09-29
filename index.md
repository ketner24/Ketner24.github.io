---
layout: single
title: "Operations Research Portfolio"
permalink: /
author_profile: false
toc: false
classes: [wide, profile-home]
profile_hero: true
header:
  overlay_color: "#1a2332"
excerpt: "Bayesian inference, optimization, and decision support for military operations."
section_nav:
  - title: "About"
    url: "#about"
  - title: "Contact"
    url: "#contact"
  - title: "Skills"
    url: "#focus-and-skills"
  - title: "Education"
    url: "#education-and-credentials"
  - title: "Experience"
    url: "#experience"
  - title: "Selected work"
    url: "#selected-work"
  - title: "Coursework"
    url: "#coursework-tools"
  - title: "Other projects"
    url: "#other-projects"
---

## About

I am a U.S. Army Operations Research officer and a graduate student in Operations Research at the Naval Postgraduate School (expected 2027). I build models that turn incomplete information into decisions: exposure and risk under uncertainty, discrete-event logistics, portfolio-style allocation, and geospatial planning tools.

Current work sits at the intersection of Bayesian methods, mathematical programming, and operational planning. Earlier assignments were in combat engineering and theater sustainment, including company command and accountability for Army Prepositioned Stock in the INDOPACIFIC.

---

## Contact

- **Email:** [sketner24@gmail.com](mailto:sketner24@gmail.com) · [shaun.ketner@nps.edu](mailto:shaun.ketner@nps.edu)
- **GitHub:** [github.com/ketner24](https://github.com/ketner24)

---

## Focus and skills

**Focus:** Bayesian inference and uncertainty quantification · mathematical programming and CVaR · discrete-event simulation · geospatial decision support · time-series and regime models

**Tools:** Python · R · SQL · C++ · PyMC · PyTorch · SimPy / Simio · Pyomo · Streamlit · FastAPI · Docker · geospatial stacks

---

## Education and credentials

- **M.S., Operations Research** — Naval Postgraduate School (expected 2027)
- **M.S., Geological Engineering** — Missouri University of Science and Technology (2019)
- **B.S., Electrical Engineering** — The Citadel (2014)
- **Project Management Professional (PMP)** — PMI (originally 2020; current cycle through 2026)

---

## Experience

### Graduate Student, Operations Research
*Naval Postgraduate School · Monterey, CA · 2025 – Present*

Coursework and research in stochastic modeling, simulation analysis, Bayesian computation, and military applications of operations research. Thesis work on measuring adversary use of publicly available information against corps operations; presented at AORS.

### Assistant Operations Officer / APS-3 Property Manager
*8th Special Troops Battalion, 8th Theater Sustainment Command · Aug 2023 – Jun 2025*

- Planned and resourced battalion exercises with joint and allied partners.
- Accountable for four UICs of Army Prepositioned Stock (APS-3) valued at more than $100 million in the INDOPACIFIC.
- Synchronized unit training with higher-headquarters taskings.

### Company Commander, Route Clearance
*95th Engineer Company, 84th Engineer Battalion, 130th Engineer Brigade · Mar 2022 – Jul 2023*

- Commanded 145 Soldiers and Families.
- Accountable for vehicle fleets and equipment valued at more than $64 million.

### Earlier assignments

- Brigade Assistant S4, 130th Engineer Brigade, Schofield Barracks, HI
- Project Engineer (EPEP), 554th RED HORSE Squadron, Guam
- Executive Officer and Platoon Leader, 317th Brigade Engineer Battalion, Fort Polk, LA

---

## Selected work

Projects are ordered by how well they represent the work I want to keep doing: measured uncertainty, optimization under constraints, and tools a staff can actually use.

### Thesis / AORS : Assessing adversary use of PAI against corps operations

How much can an adversary learn about U.S. corps deployment activity from publicly available information alone? The thesis builds a weekly panel of open-source signals and a per-activity exposure metric, then uses Bayesian methods (MAP estimation and Hamiltonian Monte Carlo) to put an uncertainty interval on each estimate. The goal is to let a staff rank OPSEC effort by measured exposure instead of by judgment alone. Presented at AORS.

**Status:** in progress. Findings and the activity-level risk matrix will be posted after sponsor release review.

**Methods:** Bayesian inference · linear models · API / SQL

### Gap-crossing decision support

Planning application for military gap crossing. It pulls an area of operations from live data services, classifies the route network, finds and characterizes gaps and bridges, recommends and sizes crossing means, builds the force and traffic plan, and simulates the crossing end to end.

**Methods:** Python · R · JavaScript · geospatial analysis · combat engineer planning · Bayesian treatment of uncertainty · APIs  
**Code:** not public; walkthrough available on request

<img src="/images/Gap_Crossing_App.png" alt="Gap crossing application" width="640"/>
<img src="/images/Gap_Crossing_App_1.png" alt="Gap crossing route and gap view" width="640"/>
<img src="/images/Gap_Crossing_App_2.png" alt="Gap crossing synchronization view" width="640"/>

### Stochastic portfolio analyzer : regime-aware CVaR

Production-style portfolio API that detects market regimes with a Bayesian hidden Markov model, then solves a CVaR-constrained allocation. Includes walk-forward backtests with transaction costs, an efficient-frontier endpoint, SQLite caching, and scheduled daily updates.

**Methods:** Python · FastAPI · Pyomo · Gaussian HMM · CVaR · Docker  
**Code:** [Stochastic_portfolio_analyzer](https://github.com/ketner24/Stochastic_portfolio_analyzer)

### Big Sur Marathon simulation

Discrete-event simulation of the Big Sur International Marathon in SimPy, with a Streamlit front end for exploring logistics rates, congestion, and support posture. Scenario comparisons use common random numbers with paired t-tests, and a sensitivity sweep finds the point where adding resources stops paying off.

**Methods:** Python · SimPy · Streamlit · common random numbers · Monte Carlo  
**Live:** [Big Sur Marathon Simulator](https://bigsurmarathonsimulation-s2vc5wu3a3qztzhtgiwfdc.streamlit.app/)  
**Code:** [Big_Sur_Marathon_Simulation](https://github.com/ketner24/Big_Sur_Marathon_Simulation)

<img src="/images/Big_Sur_Marathon_Simulator.png" alt="Big Sur marathon simulation dashboard" width="640"/>

### Bayesian FX market model

Quantitative FX pipeline: Bayesian structural time series in PyMC for inference, covariance-aware portfolio construction in Pyomo, OANDA execution, risk limits, audit logging, and Grafana monitoring, with unit tests around risk, optimization, and the trade journal.

**Methods:** Python · PyMC · Bayesian structural time series · portfolio optimization · PyTest · Grafana  
**Live:** [Bayesian FX app](https://bayesian-fx-market-modeling-hkxdjjdryngwi2sau8kshm.streamlit.app/)  
**Code:** [Bayesian-FX-Market-Modeling](https://github.com/ketner24/Bayesian-FX-Market-Modeling)

<img src="/images/Bayesian_FX.png" alt="Bayesian FX architecture" width="640"/>

### Fantasy football as a Markowitz problem

Interactive optimizer against ESPN and Sleeper leagues. Expected points are a blend of platform projections, a recency-weighted multi-season mean, and a defense-versus-position adjustment. The weekly pick maximizes the chance of beating the actual opponent; a risk slider runs both ways, including a deliberate ceiling chase.

**Methods:** mean-variance optimization · Python (scoring engine, leakage-safe walk-forward features) · JavaScript  
**Code:** [Fantasy_Football_Markowitz_Portfolio_Optimizer](https://github.com/ketner24/Fantasy_Football_Markowitz_Portfolio_Optimizer)

<img src="/images/Markowitz_FFL_portfolio.png" alt="Fantasy football Markowitz dashboard" width="640"/>

### CENTCOM situational awareness map

Interactive map that fuses historical conflict data with live aviation and maritime tracks across the USCENTCOM area of responsibility. All data is unclassified and comes from public sources (ACLED, OpenSky Network, AISStream).

**Methods:** Python · Docker · Redis · geospatial analysis  
**Code:** [CENTCOM_Situational_Awareness_Dashboard](https://github.com/ketner24/CENTCOM_Situational_Awareness_Dashboard)

<img src="/images/CENTCOM_Situational_Analysis.png" alt="CENTCOM situational awareness map" width="640"/>

---

## Coursework tools

Built while working through NPS sequences in Bayesian computation and simulation. Each of these is a live GitHub Pages site.

- **Simulation Analysis (OA4333)** — nine modules on design of experiments: intuition, worked example, failure modes, and why it matters. [Live](https://ketner24.github.io/Simulation_Analysis_OA4333_study_guide/) · [Code](https://github.com/ketner24/Simulation_Analysis_OA4333_study_guide)
- **Bayesian neural networks weekly review** — CS4323 companion with a Sunday-prep / weekly-run / recap loop. [Live](https://ketner24.github.io/Bayesian_Neural_Networks_study_guide/) · [Code](https://github.com/ketner24/Bayesian_Neural_Networks_study_guide)
- **Interactive visualizations** — [BNNs](https://ketner24.github.io/BNN_Summary3-visualizations/) · [loss functions](https://ketner24.github.io/Loss_function_visualizations/) · [ensembles, flows, and VI](https://ketner24.github.io/ensembles_flows_vi/) · [random-walk approximate Bayes](https://ketner24.github.io/Random-Walk-Approximate-Bayesian-Methods/) · [Gaussian VI](https://ketner24.github.io/Gaussian_Variational_Inference/) · [VI with dropout](https://ketner24.github.io/Variational_Inference_Dropout/) · [variational policy gradients](https://ketner24.github.io/Returns_to_Variational_Policy_Gradients/)

---

## Other projects

- **Hybrid AFT fitness plan** — eight-week cardio-forward plan with phased loading. [Live](https://ketner24.github.io/Hybrid_AFT_fitness_plan/) · [Code](https://github.com/ketner24/Hybrid_AFT_fitness_plan)
- **Pre-K STEM learning app** — browser activities for ages 3–5. [Live](https://ketner24.github.io/Pre-K-STEM-learning-APP-HTML/) · [Code](https://github.com/ketner24/Pre-K-STEM-learning-APP-HTML)
- **Lottery statistical auditor** — chi-square uniformity tests, confidence intervals, and Poisson wait times on Powerball, Mega Millions, and SuperLotto Plus history, plus an XGBoost classifier backtested against the random-draw baseline. [Live](https://lottery-statistical-auditor-ai-predictor-wqgc5upaajcsjdwafkri2.streamlit.app/) · [Code](https://github.com/ketner24/Lottery-Statistical-Auditor-AI-Predictor)
- **NPS QR code generator** — Streamlit app for custom QR codes. [Live](https://pyqrcodegenpng-qmapgpvpd299hjacuf3wg5.streamlit.app/) · [Code](https://github.com/ketner24/py_qrcode_gen_png)

---
