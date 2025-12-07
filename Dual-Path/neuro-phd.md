**Longitudinal Project:** "The Synaptic Atlas" – A comprehensive, open-source computational pipeline and accompanying R01-style grant proposal for analyzing spatial memory dynamics.

**Tier 1: Data Ingestion & Sanitization**
* **New Concepts:** Raw data parsing, outlier detection, data typing.
* **PART A: Side Quest:**
    * **The Puzzle:** Write a script to ingest a "dirty" CSV file containing neuronal firing rates, convert string timestamps to objects, and remove rows where firing rates are negative (errors).
    * **Synthetic Data:** `["Time,Rate", "10:00,50Hz", "10:01,-5Hz", "10:02,NaN", "10:03,60Hz"]`
    * **Deliverable:** A cleaned Pandas DataFrame with proper dtypes.
* **PART B: Main Build:**
    * **The Feature Goal:** Establish the base data loader for "The Synaptic Atlas."
    * **Field Data Task:** Download a raw behavioral dataset from a public repository (e.g., CRCNS.org or OpenNeuro) related to spatial navigation or memory.
    * **Deliverable:** A `load_data.py` module that ingests the raw files and standardizes column names.

**Tier 2: Descriptive Statistics & Baseline Metrics**
* **New Concepts:** Central tendency, variability, standard error of the mean (SEM).
* **PART A: Side Quest:**
    * **The Puzzle:** Calculate the mean and standard deviation of reaction times for two conditions and determine if the variance is equal.
    * **Synthetic Data:** `Condition_A = [200, 210, 190, 205]; Condition_B = [400, 300, 500, 200]`
    * **Deliverable:** A summary table printing Mean, SD, and SEM for both groups.
* **PART B: Main Build:**
    * **The Feature Goal:** Implement an automated "Table 1" generator for your pipeline.
    * **Field Data Task:** Extract demographic or baseline behavioral metrics (speed, error rate) from your downloaded dataset.
    * **Deliverable:** A function that outputs a formatted demographic/baseline table.

**Tier 3: Basic Visualization**
* **New Concepts:** Histograms, Boxplots, avoiding "chart junk."
* **PART A: Side Quest:**
    * **The Puzzle:** Create a histogram of Inter-Spike Intervals (ISIs) with a specific bin size.
    * **Synthetic Data:** Random exponential distribution list of 1000 integers.
    * **Deliverable:** A PNG image of the histogram with labeled axes.
* **PART B: Main Build:**
    * **The Feature Goal:** Create the "Data Quality Check" module.
    * **Field Data Task:** Identify the primary dependent variable in your real dataset (e.g., path length).
    * **Deliverable:** A script generating distribution plots for your primary variable to check for normality.

**Tier 4: Hypothesis Testing (Parametric)**
* **New Concepts:** T-tests (paired vs. unpaired), p-values, effect sizes (Cohen's d).
* **PART A: Side Quest:**
    * **The Puzzle:** Determine if "Drug X" significantly changed firing rates compared to baseline using a paired t-test.
    * **Synthetic Data:** `Baseline = [10, 12, 11, 13]; PostDrug = [15, 16, 15, 17]`
    * **Deliverable:** A script outputting the t-statistic, p-value, and Cohen's d.
* **PART B: Main Build:**
    * **The Feature Goal:** Add the "Preliminary Stats" engine.
    * **Field Data Task:** Compare your primary variable across two conditions (e.g., Trial Start vs. Trial End, or Group A vs. Group B) in the real data.
    * **Deliverable:** A Python class that runs the comparison and saves the statistical report to a text file.

**Tier 5: Reproducibility & Version Control**
* **New Concepts:** Git commit history, branching, `.gitignore`.
* **PART A: Side Quest:**
    * **The Puzzle:** Initialize a repo, create a `feature-branch`, add a script, and merge it back to `main`.
    * **Synthetic Data:** A text file named `experiment_log.txt`.
    * **Deliverable:** A screenshot of the `git log --graph`.
* **PART B: Main Build:**
    * **The Feature Goal:** Version control "The Synaptic Atlas."
    * **Field Data Task:** N/A (Project management focus).
    * **Deliverable:** A GitHub repository link containing all previous Tier code, properly structured with a README.

**Tier 6: Literature Synthesis**
* **New Concepts:** Reference management, annotated bibliographies, identifying gaps.
* **PART A: Side Quest:**
    * **The Puzzle:** Create a citation key system and export a `.bib` file for 3 mock papers.
    * **Synthetic Data:** Title: "Paper A", Author: "Doe", Year: 2020; Title: "Paper B", Author: "Smith", Year: 2021.
    * **Deliverable:** A correctly formatted `.bib` file.
* **PART B: Main Build:**
    * **The Feature Goal:** The "Background" section of your Grant Proposal.
    * **Field Data Task:** Find 10 seminal papers related to your longitudinal dataset's topic.
    * **Deliverable:** A 1-page "State of the Field" summary identifying a specific knowledge gap your pipeline solves.

**Tier 7: Scientific Illustration (Vector Graphics)**
* **New Concepts:** Vector vs. Raster, schematics, Adobe Illustrator/Inkscape.
* **PART A: Side Quest:**
    * **The Puzzle:** Draw a simplified neuron (soma, axon, dendrites) using only vector primitives (circles, bezier curves).
    * **Synthetic Data:** N/A (Visual task).
    * **Deliverable:** An SVG file of the neuron.
* **PART B: Main Build:**
    * **The Feature Goal:** The "Conceptual Model" figure.
    * **Field Data Task:** Sketch the theoretical framework of how your variables interact (e.g., Hippocampus -> Spatial Map -> Behavior).
    * **Deliverable:** A professional-grade schematic figure (Figure 1 of your future paper).

**Tier 8: Advanced Visualization (High-Dimensional)**
* **New Concepts:** Heatmaps, correlation matrices, dimensionality reduction (PCA).
* **PART A: Side Quest:**
    * **The Puzzle:** Perform PCA on a 3-dimensional dataset and plot the first two principal components.
    * **Synthetic Data:** A 10x3 matrix of random floats.
    * **Deliverable:** A scatter plot of PC1 vs. PC2.
* **PART B: Main Build:**
    * **The Feature Goal:** The "Multivariate Analysis" module.
    * **Field Data Task:** Select 5+ continuous variables from your dataset (e.g., velocity, acceleration, turn angle, firing rate).
    * **Deliverable:** A correlation heatmap and a PCA projection of the behavioral state space.

**Tier 9: Time-Series Analysis**
* **New Concepts:** Smoothing, rolling windows, Fourier Transform (FFT).
* **PART A: Side Quest:**
    * **The Puzzle:** Apply a moving average filter to noisy sine wave data and extract the dominant frequency.
    * **Synthetic Data:** `y = sin(x) + random_noise`
    * **Deliverable:** A plot overlaying raw vs. smoothed data and the power spectrum.
* **PART B: Main Build:**
    * **The Feature Goal:** Temporal dynamics processing.
    * **Field Data Task:** Analyze a time-dependent variable from your real data (e.g., position over time or LFP trace).
    * **Deliverable:** A function that filters the signal and plots the spectral density.

**Tier 10: The Methods Section**
* **New Concepts:** Passive voice vs. active voice, precision, replicability.
* **PART A: Side Quest:**
    * **The Puzzle:** Rewrite a "cooking recipe" paragraph into formal scientific methods style.
    * **Synthetic Data:** "First, I broke two eggs into a bowl and mixed them fast."
    * **Deliverable:** A formal paragraph: "Two gallus domesticus ova were homogenized..."
* **PART B: Main Build:**
    * **The Feature Goal:** Draft the "Methods" section for your paper/grant.
    * **Field Data Task:** Document the exact preprocessing steps used in Tiers 1-9.
    * **Deliverable:** A 500-word technical document detailing data acquisition and analysis parameters.

**Tier 11: Power Analysis & Experimental Design**
* **New Concepts:** Effect size estimation, G*Power, sample size determination.
* **PART A: Side Quest:**
    * **The Puzzle:** Calculate the required sample size to detect a Cohen's d of 0.5 with 80% power at alpha=0.05.
    * **Synthetic Data:** Parameters: d=0.5, power=0.8, alpha=0.05.
    * **Deliverable:** The integer number of subjects required.
* **PART B: Main Build:**
    * **The Feature Goal:** The "Future Experiments" justification.
    * **Field Data Task:** Use the effect sizes observed in Tier 4 to calculate the N needed for a proposed follow-up study.
    * **Deliverable:** A "Statistical Power" subsection for your grant proposal.

**Tier 12: Bootstrapping & Resampling**
* **New Concepts:** Non-parametric stats, confidence intervals via resampling.
* **PART A: Side Quest:**
    * **The Puzzle:** Generate a 95% confidence interval for a median using 1000 bootstrap resamples.
    * **Synthetic Data:** `[1, 2, 5, 6, 9, 20, 22, 25, 30]`
    * **Deliverable:** The Lower and Upper CI bounds.
* **PART B: Main Build:**
    * **The Feature Goal:** Robust validation of your metrics.
    * **Field Data Task:** Apply bootstrapping to the correlation coefficients calculated in Tier 8.
    * **Deliverable:** Updated figures showing confidence intervals around your main effects.

**Tier 13: Linear Modeling (GLM)**
* **New Concepts:** Regression, residuals, R-squared, beta weights.
* **PART A: Side Quest:**
    * **The Puzzle:** Fit a linear regression line to predict Y from X and plot the residuals.
    * **Synthetic Data:** `X = [1, 2, 3, 4, 5]; Y = [2.1, 3.9, 6.2, 8.1, 9.8]`
    * **Deliverable:** The equation of the line and a residual plot.
* **PART B: Main Build:**
    * **The Feature Goal:** Predictive modeling.
    * **Field Data Task:** Build a GLM to predict a behavioral outcome (e.g., success/fail) based on neural/physiological predictors.
    * **Deliverable:** A regression table summarizing significant predictors.

**Tier 14: Data Management & Ethics**
* **New Concepts:** Anonymization, FAIR principles, IRB application logic.
* **PART A: Side Quest:**
    * **The Puzzle:** "De-identify" a dataset by hashing names and removing dates of birth.
    * **Synthetic Data:** `{"Name": "John Doe", "DOB": "1990-01-01", "Score": 99}`
    * **Deliverable:** The JSON object with name hashed and DOB removed.
* **PART B: Main Build:**
    * **The Feature Goal:** The "Human/Animal Subjects" section.
    * **Field Data Task:** Review the ethics protocol associated with your public dataset or draft a mock IRB protocol for your proposed study.
    * **Deliverable:** A 1-page "Protection of Subjects" statement.

**Tier 15: Introduction to Machine Learning**
* **New Concepts:** Train/Test split, Cross-validation, Overfitting.
* **PART A: Side Quest:**
    * **The Puzzle:** Split a dataset 80/20 and train a simple k-Nearest Neighbors classifier.
    * **Synthetic Data:** 20 points with (x, y) coordinates and binary labels (0 or 1).
    * **Deliverable:** The accuracy score on the test set.
* **PART B: Main Build:**
    * **The Feature Goal:** Decoding analysis.
    * **Field Data Task:** Attempt to classify the "trial type" or "animal location" based on the physiological variables using a classifier.
    * **Deliverable:** A confusion matrix of the classifier's performance.

**Tier 16: Grant Writing: Specific Aims**
* **New Concepts:** The "Hook," the hypothesis, independent/dependent variables.
* **PART A: Side Quest:**
    * **The Puzzle:** Condense a complex paragraph into a 3-bullet point "Aim" structure.
    * **Synthetic Data:** A rambling 500-word description of an experiment.
    * **Deliverable:** A concise "Specific Aims" page (1 page).
* **PART B: Main Build:**
    * **The Feature Goal:** The core of your R01 Proposal.
    * **Field Data Task:** Define 2 aims based on your "Synaptic Atlas" project (Aim 1: Analysis of current data; Aim 2: Proposed new experiment).
    * **Deliverable:** The "Specific Aims" page for your longitudinal project.

**Tier 17: Containerization (Docker)**
* **New Concepts:** Environment isolation, Dockerfiles, images vs. containers.
* **PART A: Side Quest:**
    * **The Puzzle:** Create a Dockerfile that installs Python and Numpy, and runs a "Hello World" script.
    * **Synthetic Data:** A Python script `hello.py`.
    * **Deliverable:** The built Docker image ID.
* **PART B: Main Build:**
    * **The Feature Goal:** Portable Science.
    * **Field Data Task:** Wrap your entire analysis pipeline (Tiers 1-15) into a Docker container.
    * **Deliverable:** A `Dockerfile` that allows anyone to run your analysis with one command.

**Tier 18: Collaboration & Cold Outreach**
* **New Concepts:** Networking, crafting emails, "The Ask."
* **PART A: Side Quest:**
    * **The Puzzle:** Draft an email to a potential collaborator asking for a specific reagent/dataset, keeping it under 150 words.
    * **Synthetic Data:** Recipient: Dr. Strange (Expert in Magic/Time).
    * **Deliverable:** The email text.
* **PART B: Main Build:**
    * **The Feature Goal:** Building your network.
    * **Field Data Task:** Identify 3 professors who would be ideal reviewers for your grant/paper.
    * **Deliverable:** A list of 3 potential reviewers with a 1-sentence justification for each (based on their recent pubs).

**Tier 19: The "Results" Section**
* **New Concepts:** Narrative flow, referencing figures, statistical reporting standards.
* **PART A: Side Quest:**
    * **The Puzzle:** Write a "Results" paragraph describing a provided graph.
    * **Synthetic Data:** A plot showing Group A > Group B (p<0.01).
    * **Deliverable:** A paragraph: "As shown in Figure 1, Group A demonstrated significantly higher..."
* **PART B: Main Build:**
    * **The Feature Goal:** Drafting the core manuscript.
    * **Field Data Task:** Compile your analyses from Tiers 4, 8, 13, and 15 into a cohesive narrative.
    * **Deliverable:** The complete "Results" section of your paper.

**Tier 20: Peer Review Simulation**
* **New Concepts:** Critical analysis, constructive criticism, spotting flaws.
* **PART A: Side Quest:**
    * **The Puzzle:** Identify 3 methodological flaws in a provided mock abstract.
    * **Synthetic Data:** "We tested 3 people and found a global cure for amnesia."
    * **Deliverable:** A short "Reviewer Report."
* **PART B: Main Build:**
    * **The Feature Goal:** Self-Audit.
    * **Field Data Task:** Act as "Reviewer #2" for your own project. Attack your sample size, your noise filtration, and your GLM assumptions.
    * **Deliverable:** A 1-page "Limitations" section for your Discussion.

**Tier 21: Advanced Signal Processing (LFP/EEG)**
* **New Concepts:** Spectrograms, coherence, phase-locking value.
* **PART A: Side Quest:**
    * **The Puzzle:** Generate a chirped sine wave (increasing frequency) and plot its spectrogram.
    * **Synthetic Data:** `t = 0 to 10s`.
    * **Deliverable:** A time-frequency heat map.
* **PART B: Main Build:**
    * **The Feature Goal:** Oscillatory dynamics.
    * **Field Data Task:** If your data has time-series, compute a spectrogram around a specific behavioral event (e.g., crossing a threshold).
    * **Deliverable:** Figure 3 of your paper: "Event-Related Spectral Perturbation."

**Tier 22: Lab Budgeting & Finance**
* **New Concepts:** Direct vs. Indirect costs, personnel salaries, equipment depreciation.
* **PART A: Side Quest:**
    * **The Puzzle:** Calculate the total cost of a grant given $100k direct costs and a 50% indirect cost rate.
    * **Synthetic Data:** Directs: $100,000. F&A Rate: 50%.
    * **Deliverable:** Total budget calculation.
* **PART B: Main Build:**
    * **The Feature Goal:** The Budget Justification.
    * **Field Data Task:** Create a mock budget for the "Aim 2" experiment you designed in Tier 16. Include personnel, equipment, and travel.
    * **Deliverable:** A Modular Budget Justification document.

**Tier 23: Mixed Effects Models (LME)**
* **New Concepts:** Fixed vs. Random effects, hierarchical data structures.
* **PART A: Side Quest:**
    * **The Puzzle:** Write the formula string for a model where "Subject" is a random effect and "Condition" is a fixed effect.
    * **Synthetic Data:** N/A (Syntax task).
    * **Deliverable:** `Response ~ Condition + (1|Subject)`
* **PART B: Main Build:**
    * **The Feature Goal:** Advanced Statistical Rigor.
    * **Field Data Task:** Re-analyze your main result using a Linear Mixed Effect model to account for repeated measures per subject.
    * **Deliverable:** Comparison table: GLM results vs. LME results.

**Tier 24: Mentorship & Pedagogy**
* **New Concepts:** Learning objectives, scaffolding, delegation.
* **PART A: Side Quest:**
    * **The Puzzle:** Design a 1-week mini-project for an undergraduate based on cleaning a specific column of data.
    * **Synthetic Data:** "The intern knows Python basics."
    * **Deliverable:** A 1-page "Syllabus/Assignment" sheet.
* **PART B: Main Build:**
    * **The Feature Goal:** Scaling the lab.
    * **Field Data Task:** Identify a subsection of your analysis pipeline that could be improved or refactored by a student.
    * **Deliverable:** A "Help Wanted" project description for a rotation student.

**Tier 25: The "Discussion" Section**
* **New Concepts:** Contextualization, speculation, connecting back to the gap.
* **PART A: Side Quest:**
    * **The Puzzle:** Write a concluding sentence that links a specific finding to a broad theory.
    * **Synthetic Data:** Finding: "Neurons fire more in the dark." Theory: "Sensory substitution."
    * **Deliverable:** The linking sentence.
* **PART B: Main Build:**
    * **The Feature Goal:** Completing the Manuscript text.
    * **Field Data Task:** Interpret your results in the context of the 10 papers you found in Tier 6.
    * **Deliverable:** The full "Discussion" section.

**Tier 26: Pre-Registration & Open Science**
* **New Concepts:** OSF (Open Science Framework), HARKing (Hypothesizing After Results Known).
* **PART A: Side Quest:**
    * **The Puzzle:** Draft a timestamped hypothesis for a coin flip experiment BEFORE flipping.
    * **Synthetic Data:** "I predict Heads."
    * **Deliverable:** A text file with a hash/timestamp.
* **PART B: Main Build:**
    * **The Feature Goal:** Transparency.
    * **Field Data Task:** Create a "Pre-registration" document for the analysis you performed (simulating that you wrote it before the analysis).
    * **Deliverable:** An OSF-style pre-registration PDF.

**Tier 27: Public Speaking & Slides**
* **New Concepts:** Slide design, "The 10-20-30 Rule," storytelling.
* **PART A: Side Quest:**
    * **The Puzzle:** Create a single slide explaining "P-value" to a layperson using only images and <10 words.
    * **Synthetic Data:** Concept: P-value < 0.05.
    * **Deliverable:** The slide image.
* **PART B: Main Build:**
    * **The Feature Goal:** Conference Presentation.
    * **Field Data Task:** Create a 10-slide deck summarizing "The Synaptic Atlas" findings.
    * **Deliverable:** A `.pptx` or PDF slide deck.

**Tier 28: Response to Reviewers**
* **New Concepts:** Diplomacy, "The Sandwich Method," distinct point-by-point rebuttal.
* **PART A: Side Quest:**
    * **The Puzzle:** Write a polite rebuttal to a reviewer who claims your sample size is too small, citing a paper that says it's adequate.
    * **Synthetic Data:** Reviewer Comment: "N=3 is too low."
    * **Deliverable:** The rebuttal paragraph.
* **PART B: Main Build:**
    * **The Feature Goal:** Defense of the work.
    * **Field Data Task:** Take the "Limitations" you wrote in Tier 20 and write a "Response" as if a reviewer pointed them out.
    * **Deliverable:** A "Response to Reviewers" document.

**Tier 29: The "Elevator Pitch"**
* **New Concepts:** Brevity, hook, value proposition.
* **PART A: Side Quest:**
    * **The Puzzle:** Record a 30-second audio clip explaining what a "neuron" is to a 5-year-old.
    * **Synthetic Data:** N/A.
    * **Deliverable:** The audio file or transcript.
* **PART B: Main Build:**
    * **The Feature Goal:** Professional Branding.
    * **Field Data Task:** Write the 2-minute pitch of your Longitudinal Project for a hiring committee.
    * **Deliverable:** A 150-word "Research Summary" text.

**Tier 30: The Job Talk**
* **New Concepts:** The 45-minute arc, the "Vision," the future lab.
* **PART A: Side Quest:**
    * **The Puzzle:** Outline the 3 sections of a job talk: Past, Present, Future.
    * **Synthetic Data:** N/A.
    * **Deliverable:** An outline structure.
* **PART B: Main Build:**
    * **The Feature Goal:** The Final Package.
    * **Field Data Task:** Assemble the Paper, The Grant Aims, The Codebase, and The Slides into a single folder.
    * **Deliverable:** "The Portfolio."

**Tier 31: CAPSTONE - THE TENURE TRACK**
* **Objective:** You are applying for a functional Assistant Professor position.
* **The Boss Fight:**
    1.  Take a *new*, raw dataset you have never seen before (find a different one on OpenNeuro).
    2.  In 48 hours, deploy "The Synaptic Atlas" pipeline on it.
    3.  Generate a 3-figure report (Behavior, Neural activity, Correlation).
    4.  Write a 1-page "Grant Letter of Intent" based on this pilot data.
    5.  Produce a 5-minute video presentation of the findings.
* **Condition:** No tutorials. No guides. You must debug all pipeline errors that arise from the new data format alone.
* **Deliverable:** The "Job Application Package."
