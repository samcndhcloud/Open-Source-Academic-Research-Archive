# Open Source Academic Research Archive

An open repository hosting **16,935 words** of original research, raw experimental datasets, and quantitative models across Sports Psychology, Applied Mathematics, Cognitive Psychology, and Microbiology. Authored for the International Baccalaureate (IB) program (2023–2024), this archive provides transparent verification of my analytical methodology and experimental rigor — the exact foundation in data-driven problem dissection and systems thinking behind the architecture of Frictionless Fitness, expanded upon in my **17,770-word** product and systems engineering manifesto: [Why We Built This](https://frictionlessfitness.com/why-we-built-this).

---

## Repository Index

| Document | Primary Discipline | Methodology & Quantitative Tools | Core Focus |
| :--- | :--- | :--- | :--- |
| [`Sports_Psychology_EE.pdf`](./psychology/Sports_Psychology_EE.pdf) | Sports Psychology & Neuroscience | CSAI-2, STAI, Catastrophe Modeling, Linear/Curvilinear Regressions | Motor skill degradation under anxiety & cognitive load in athletes |
| [`NBA_Predictive_Modeling_IA.pdf`](./mathematics/NBA_Predictive_Modeling_IA.pdf) | Applied Mathematics & Statistics | Multiple Linear Regression (MLR), Pearson's `R^2`, Sum of Squares | Multivariable correlation of regular season efficiency to postseason success |
| [`Cognitive_Anchoring_Study_IA.pdf`](./psychology/Cognitive_Anchoring_Study_IA.pdf) | Cognitive Psychology | Repeated Measures, Spearman’s Rho (`ρ`), IQR Outlier Isolation | Priming heuristics and numerical anchoring effects on quantitative estimation |
| [`Microbial_Growth_Kinetics_IA.pdf`](./biology/Microbial_Growth_Kinetics_IA.pdf) | Microbiology & Biochemistry | Two-Factor ANOVA with Replication, Hemocytometer Cell Counting | Proliferation kinetics of bacteria across lipid densities and thermal baselines |

---

## 1. Sports Psychology Extended Essay: Motor Skill Degradation Under Anxiety

* **Title:** *To what extent does anxiety or lack of self-confidence negatively affect motor skills in athletes?*
* **Scope:** 3,956 Words | Sports Psychology Extended Essay
* **File:** [`/psychology/Sports_Psychology_EE.pdf`](./psychology/Sports_Psychology_EE.pdf)

### Background & Research Framework
Investigates the physiological and cognitive mechanisms through which state/trait anxiety and self-confidence fluctuations impair fine and gross motor performance in competitive athletes. Evaluates competitive stress measurement scales including Rainer Martens' Competitive State Anxiety Inventory-2 (CSAI-2) and the Spielberger State-Trait Anxiety Inventory (STAI Form Y).

### Literature Evaluation & Empirical Findings
* [**Trait vs. State Interference (Horikawa & Yagi, 2012):**](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0035727) Analyzed repeated-measures penalty trials (`n = 16`), proving high-trait anxiety directly amplifies state anxiety during pressure tasks, causing a statistically significant collapse in motor execution (`p < 0.01`).
* [**Multidimensional Anxiety Theory (Chamberlain & Hale, 2007):**](https://pubmed.ncbi.nlm.nih.gov/17999224/) Evaluated putting accuracy across 12 golfers. Demonstrated that while somatic anxiety follows an inverted-U curvilinear function (`p < 0.05`), cognitive anxiety exhibits a severe negative linear relationship with execution accuracy (`p < 0.01`). Self-confidence accounted for 30% of performance variance in directional modeling (`p < 0.01`).
* [**Working Memory & Anaerobic Demands (Parfitt & Pates, 1999):**](https://www.tandfonline.com/doi/abs/10.1080/02640419308730022) Conducted hierarchical regression on match analytics (`n = 12` basketball athletes), showing self-confidence predicted 34% of variance in passing (`p < 0.01`) and 57% in playmaking assists (`p < 0.01`), proving high-order working memory tasks are deeply sensitive to psychological state.
* [**Catastrophe Modeling & Hysteresis (Hardy, Parfitt, & Pates, 1994):**](https://www.tandfonline.com/doi/abs/10.1080/02640419408732178) Evaluated physiological arousal against cognitive load in precision bowling (`n = 8`), identifying that when high cognitive anxiety is paired with accelerating heart rates, error scores jump to `0.736 ± 0.334` compared to `0.532 ± 0.122` under decreasing arousal.

---

## 2. Mathematics Internal Assessment: Multivariable Regression & Championship Modeling

* **Title:** *What regular season factors contribute the most to future NBA playoff success, and how can these factors be used to predict a future champion?*
* **Scope:** 4,599 Words | IB SL Analysis & Approaches Internal Assessment
* **File:** [`/mathematics/NBA_Predictive_Modeling_IA.pdf`](./mathematics/NBA_Predictive_Modeling_IA.pdf)

### Mathematical Modeling & Exploration
Evaluates five regular-season team performance metrics across an 80-sample dataset (16 playoff teams × 5 seasons, 2017–18 through 2021–22) against postseason wins (`Y` in range `[0, 16]`):
1. Regular Season Wins (`WINS RS`)
2. Three-Pointers Made (`3PM RS`)
3. Assist Percentage (`AST% RS`)
4. Field Goal Percentage (`FG% RS`)
5. Net Rating (`NETRTG RS`)

### Computations & Results
* Derived manual sum of squares (`SS_x^2`, `SS_y^2`, `SS_xy`) to compute Pearson’s Coefficient of Determination (`R^2`):
  * `NETRTG RS`: `R^2 ≈ 0.344`
  * `WINS RS`: `R^2 ≈ 0.333`
  * `FG% RS`: `R^2 ≈ 0.172`
  * `3PM RS`: `R^2 ≈ 0.0933` (showing a temporal decay from `0.380` to `0.002` as league volume expanded, primarily caused by Stephen Curry in 2016 when he hit a record 402 3s on 45.4% accuracy, the greatest individual shooting season in history, and thereby, the increased usage of mathematical analysis and adoption of high-volume 3-point shooting by NBA teams)
  * `AST% RS`: `R^2 ≈ 0.0666`
* Formulated a Multiple Linear Regression (MLR) equation using high-fit single-season baseline parameters:
  `Y_hat = 1.16(X_1) - 0.00841(X_2) - 0.994(X_3) - 49.4`
  where `X_1 = WINS`, `X_2 = FG%`, and `X_3 = NETRTG`, yielding an adjusted `R^2 ≈ 0.699`.
* Backtested the model on the 2022–23 championship field, isolating the title-winning Denver Nuggets within the top tiers (81.5% model ranking accuracy) and projecting the 2023–24 championship outcome.

---

## 3. Cognitive Psychology Experimental Study: Priming & Numerical Anchoring Biases

* **Title:** *Do numeric anchors have an effect on estimates of math equations?*
* **Scope:** 2,200 Words | IB Psychology HL Internal Assessment
* **File:** [`/psychology/Cognitive_Anchoring_Study_IA.pdf`](./psychology/Cognitive_Anchoring_Study_IA.pdf)

### Experimental Setup & Controls
* Simplified experimental replication of Smith & Windschitl (2011) evaluating Priming Theory and cognitive heuristic anchoring.
* Implemented a repeated-measures design testing high school student participants across both High Anchor (`2100 <= X <= 2300`) and Low Anchor (`700 <= X <= 900`) conditions paired with three-addend math problems (`1100 <= Y <= 1900`).
* Controlled for participant contamination and demand characteristics using multi-room isolation, scripted verbatim instructions, randomized equation generation, and restricted 10-second estimation windows.

### Quantitative Analysis & Inferential Statistics
* Applied formal Interquartile Range (IQR) outlier trimming (`Q_1 - 1.5 * IQR`, `Q_3 + 1.5 * IQR`) to isolate genuine cognitive adjustments from clerical entry errors:
  * **High Anchor Mean Estimation Distance:** `+218.70` units from true solution (`SD = 405.87`)
  * **Low Anchor Mean Estimation Distance:** `-80.72` units from true solution (`SD = 163.83`)
* Ran non-parametric inferential testing via Spearman’s Rank Correlation (`ρ` / `r_s`):
  * High Anchor Condition: `r_s = 0.452`, `p = 0.0518` (two-tailed)
  * Low Anchor Condition: `r_s = 0.035`, `p = 0.8897` (two-tailed)
* Evaluated carryover effects, asymmetric anchor pull, and proposed counterbalancing methodologies to control for order bias in heuristic testing.

---

## 4. Microbiology Research: Microbial Growth Kinetics Across Lipid Densities

* **Title:** *An experiment investigating the effects of fat content on the amount of microbial growth in milk at varying temperatures.*
* **Scope:** 6,180 Words | IB Biology HL Internal Assessment
* **File:** [`/biology/Microbial_Growth_Kinetics_IA.pdf`](./biology/Microbial_Growth_Kinetics_IA.pdf)

### Experimental Design & Methodology
* 12-day controlled biological trial evaluating microbial proliferation across 12 samples of varying lipid concentrations: Whole (`3.25%`), Reduced Fat (`2%`), and Fat-Free (`0%`).
* Dual environmental thermal baselines: Refrigerated (`4.5°C`) and Room Temperature (`22.0°C`).
* Prepared `1:100` serial dilutions and executed manual cell staining using methylene blue dye to distinguish viable cells from dead, membrane-permeable nonviable cells. Cell enumeration was conducted under light microscopy using a specialized hemocytometer chamber (`10^-4 mL` grid volume).

### Quantitative Findings & Error Decomposition
* **Estimated Cell Concentration:**
  * Refrigerated: Whole (`12.25 * 10^6 cells/mL`) vs. Reduced (`2.38 * 10^6 cells/mL`) vs. Fat-Free (`3.75 * 10^6 cells/mL`)
  * Room Temp: Whole (`3.25 * 10^6 cells/mL`) vs. Reduced (`1.38 * 10^6 cells/mL`) vs. Fat-Free (`0.75 * 10^6 cells/mL`)
* **Two-Factor ANOVA with Replication:**
  * Fat Content (Sample): `F = 3.96`, `p = 0.03996` (`p < 0.05`) -> Statistically significant variation across lipid tiers.
  * Temperature Condition (Columns): `F = 27.84`, `p = 0.000075` (`p < 0.001`) -> Statistically significant thermal suppression.
  * Interaction Effect: `p = 0.252` (`p > 0.05`) -> The impact of fat content functions independently of ambient temperature.
* **Systemic Error Analysis:** Detailed methodological deviations including fluid mechanics of capillary action vs. manual droplet loading, emulsion breakdown in ambient conditions, and subjective hemocytometer optical counting constraints.

---

## Data & Asset Access

All raw datasets, calculation spreadsheets, laboratory imagery, and full PDF manuscripts are open for public audit and verification within their respective directories.
