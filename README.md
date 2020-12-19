# [A Repo for Mechanism of Action competition on Kaggle](https://www.kaggle.com/c/lish-moa)

**What is the Mechanism of Action (MoA) of a drug? And why is it important?**

In the past, scientists derived drugs from natural products or were inspired by traditional remedies. Very common drugs, such as paracetamol, known in the US as acetaminophen, were put into clinical use decades before the biological mechanisms driving their pharmacological activities were understood. Today, with the advent of more powerful technologies, drug discovery has changed from the serendipitous approaches of the past to a more targeted model based on an understanding of the underlying biological mechanism of a disease. In this new framework, scientists seek to identify a protein target associated with a disease and develop a molecule that can modulate that protein target. As a shorthand to describe the biological activity of a given molecule, scientists assign a label referred to as mechanism-of-action or MoA for short.

**How do we determine the MoAs of a new drug?**

One approach is to treat a sample of human cells with the drug and then analyze the cellular responses with algorithms that search for similarity to known patterns in large genomic databases, such as libraries of gene expression or cell viability patterns of drugs with known MoAs.

A unique dataset that combines gene expression and cell viability data is based on a new technology that measures simultaneously (within the same samples) human cells’ responses to drugs in a pool of 100 different cell types (thus solving the problem of identifying ex-ante, which cell types are better suited for a given drug). 

The task is to develop an algorithm that automatically labels each case in the test set as one or more MoA classes. Note that since drugs can have multiple MoA annotations, the task is formally a multi-label classification problem.

**Data can be downloaded from:**

* [train_features.csv](https://www.kaggle.com/c/lish-moa/data?select=train_features.csv)

* [train_targets_scored.csv](https://www.kaggle.com/c/lish-moa/data?select=train_targets_scored.csv)

**Files**

* **train_features.csv** - Features for the training set. Features g- signify gene expression data, and c- signify cell viability data. cp_type indicates samples treated with a compound (cp_vehicle) or with a control perturbation (ctrl_vehicle); control perturbations have no MoAs; cp_time and cp_dose indicate treatment duration (24, 48, 72 hours) and dose (high or low).

* **train_targets_scored.csv** - The binary MoA targets that are scored.

This repo contains the following files:
* **[DataExploration-and-visulization.ipynb](DataExploration-and-visulization.ipynb)** (for submission): This notebook contains the code for visualization and data explorations.
* **[Model_1_to_3-LR_RF_GBT.ipynb](Model_1_to_3-LR_RF_GBT.ipynb)** (for submission): This notebook contains the code for the first pipeline (logistic regression), second pipeline (random forest), and the thrid pipeline (gradient boosting machine).
* **[Model_4-Challenger-Model.ipynb](Model_4-Challenger-Model.ipynb)** (for submission): This notebook contains the code for the fourth pipeline (random forest + logistic regression).
* **[MBE.csv](MBE.csv)** (for submission): This csv file contains the MBE loss for **ALL** four pipelines (tuned and untuned) that we attampted.
* **[scv.py](scv.py)** (for reference): The stratified cross-validation Python module. This module is referenced by [Model_4-Challenger-Model.ipynb](Model_4-Challenger-Model.ipynb) notebook.
* Folder **[./misc](./misc)** (for reference) contains our other attampts in terms of feature engineering  These attampts were not adopted by any of the four models


