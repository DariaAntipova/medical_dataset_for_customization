# Medical Dataset for Fine-Tuning

This repository focuses on compiling a comprehensive, disease-representative dataset for training large language models in the medical field. The dataset is derived from detailed translation memories provided by specific clients. The goal is to extract and analyze drug mentions, including trade names, international nonproprietary names (INNs), associated diseases, and disease groups.

## Workflow Overview
1. retrieve_medical_entities.ipynb:

Objective: Extract medical entities, including drug trade names.
Inputs: List of medical/non-medical entities to test libriaries for extraction, detailed translation memory (source segment, target segment, client name, order number).
Outputs: Augmented translation memory with medical entities, clean list of medical entities.

2. compile_drug_portfolio.ipynb:

Objective: Identify and catalog drug trade names, INNs, treatment indications, and disease groups.
Inputs: Clean list of medical entities from the previous step.
Outputs: Drug portfolio with columns: Manufacturer, Trade name, INN, Indications, Disease group.

3. drug_portfolio_stats.ipynb:

Objective: Analyze translation memory for segments containing drug names and compile statistics on prevalent disease groups.
Inputs: Drug portfolio from compile_drug_portfolio.ipynb, augmented translation memory from retrieve_medical_entities.ipynb.
Outputs: Detailed translation memory with added drug information, disease group statistics for dataset customization.
