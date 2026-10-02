# Fantasy Sports Math League (FSML) — Quasi-Experimental Design (QED) Data

This repository contains the dataset supporting the research paper abstract **"Fantasy Sports for Good: Reclaiming the Analytics Playbook to Close the Math Equity Gap,"** submitted to the MIT Sloan Sports Analytics Conference (SSAC) 2027 Research Papers Competition, Business of Sports track.

## Overview

Fantasy Sports Math League (FSML) is a COPPA/FERPA-compliant, web-based fantasy football curriculum supplement for grades 6–8. Students draft NFL players under a budget constraint, compute weekly fantasy points from real box-score statistics (fractions, decimals, multi-step equations), and graph team and player performance over a season.

This dataset comes from a five-week quasi-experimental study conducted in May 2026 across six middle school math and STEM classes, assigned to an FSML intervention group or a comparison (delayed-intervention) group. The study examines whether FSML participation is associated with gains in math performance, math self-efficacy, and in-platform scoring accuracy, with particular attention to historically underserved student subgroups.

## Repository Contents

| File | Description |
|---|---|
| `FSML_QED_data_deidentified.csv` | De-identified, student-level pre/post assessment and survey data (171 rows), plus platform usage variables. Direct identifiers removed; teacher names replaced with pseudonymous IDs (`Teacher_1`–`Teacher_6`) to preserve the clustering structure used in the analysis. |
| `FSML_codebook.csv` | Data dictionary listing every variable name, label, value-label coding, missing-value codes, and any residual privacy notes. |
| `README.md` | This file. |

> **Note on the raw `.sav` file:** The original SPSS file is **not** included in this repository. It contains direct and quasi-identifiers for minors (a name fragment, birth day, and teacher name used for pre/post survey matching) and is retained privately by the authors under the study's IRB protocol. Only the de-identified CSV derived from it is published here. See **Data Privacy & Ethics** below.

## Sample

- **Matched analytic sample (assessment data):** N = 131 students (105 FSML; 26 comparison), across 6 teacher clusters (4 FSML; 2 comparison)
- **Platform usage sample (analyzed separately):** N = 123 students
- Demographics: 56% boys, 38% girls; 46% Black or African American, 37% white, 18% other race, 11% Hispanic/Latinx (ethnicity, non-exclusive with race categories)

## Methods Summary

- **Design:** Quasi-experimental, intervention vs. delayed-intervention comparison groups, non-randomized
- **Measures:** 11-item standardized math assessment (pre/post), math efficacy and interest scales (pre/post), platform usage logs (team creation, scoring activity, feature use)
- **Analysis:** Regression models comparing post-test performance between groups, adjusting for baseline performance and grade, using HC3 robust standard errors; Grade-6-only sensitivity analysis; paired Wilcoxon test on platform scoring-error trends
- **Key limitation:** Non-randomized design limits causal inference; HC3 standard errors do not account for clustering within the study's six teacher clusters, so reported uncertainty is likely understated. Larger cluster-randomized studies are needed to confirm these findings.

Full methodology and results are reported in the accompanying SSAC 2027 abstract.

## Data Privacy & Ethics

- Data were collected under dfusion IRB approval **IRB00014382**.
- The published CSV is de-identified: the student first-name fragment, birth day, and raw teacher name used for pre/post matching have been removed. Teacher identity was pseudonymized (`Teacher_1`–`Teacher_6`) rather than dropped, since teacher clustering is part of the reported analysis.
- Two free-text response fields (reflections on what students learned, and how FSML changed their feelings about math) were excluded from the public file, since open-ended responses from minors can contain incidental identifying information that is impractical to screen at scale.
- Collection and handling comply with COPPA and FERPA. Platform usage data were analyzed separately from survey/assessment data per IRB privacy protections and are not linked at the student level.
- Despite de-identification, the sample remains small (N=171 across 6 classrooms); residual indirect re-identification risk (e.g., via combinations of grade, gender, and teacher cluster) cannot be fully ruled out. Treat the data accordingly and do not attempt re-identification.

## How to Cite

If you use this dataset, please cite:

> Laris, B.A., & Ferreira, A. (2026). *Fantasy Sports for Good: Reclaiming the Analytics Playbook to Close the Math Equity Gap.* MIT Sloan Sports Analytics Conference 2027, Business of Sports Track. [link to abstract/paper when available]

## License — Non-Commercial Research Use (CC BY-NC 4.0)

This repository (code and documentation) is publicly visible to satisfy the MIT SSAC 2027 open-source submission requirement. The dataset (`FSML_QED_data_deidentified.csv`) is licensed under **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**:

- **Permitted:** Non-commercial research use — including academic analysis, replication, teaching, and secondary research — with attribution to the authors, B.A. Laris and Alamim Ferreira.
- **Not permitted without prior written permission from the authors:** any commercial use, including use by for-profit entities, incorporation into commercial products or services, or any use intended for commercial advantage.
- To request permission for commercial use, contact the authors at the address below.
- This restriction applies regardless of the de-identification steps already taken, given the small sample size and the population studied (minors, under an active IRB protocol).
- Full license text: https://creativecommons.org/licenses/by-nc/4.0/ (also included in this repo's `LICENSE` file, along with the commercial-use contact clause above)

## Contact

Questions about the dataset or methodology, and requests for permission to use the data, can be directed to:

> B.A. Laris, dfusion Inc.
> ba.laris@dfusioninc.com



