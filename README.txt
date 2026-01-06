# WGU BSDA Capstone – Entity Extraction from SEC 10-K Filings

This repository contains the code, notebooks, and supporting artifacts for my
Western Governors University BS in Data Analytics capstone project.

## Project Summary
The project evaluates whether a machine learning–based Named Entity Recognition (NER)
pipeline can outperform a traditional regex-based approach when extracting executive,
organizational, and revenue-related entities from SEC Form 10-K filings.

The analysis compares:
- A rule-based regex baseline
- Unaugmented spaCy NER pipelines
- Domain-augmented spaCy pipelines using EntityRuler patterns

Performance is evaluated using precision, recall, and micro-averaged F1 score.

## Repository Structure
- `Notebooks/` – Data exploration, model evaluation, and metric generation
- `Docs/` – Labeling rulebook and project documentation
- `gold_annotations/` – Manually labeled gold-standard dataset
- `baseline_regex/` – Regex extraction logic and outputs
- `outputs/` – Aggregated evaluation results and intermediate files

## Relationship to Capstone Paper
All metrics, tables, and figures reported in the capstone paper were generated
using the code and notebooks in this repository.

This repository is provided for transparency and reproducibility; evaluators
are not expected to run the code.

## Data Source
SEC Form 10-K filings sourced from the public Kaggle dataset:
https://www.kaggle.com/datasets/pranjalverma08/sec-edgar-annual-financial-filings-2021
