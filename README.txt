Entity Extraction from SEC 10-K Filings
Project Overview

This repository contains a complete data analytics capstone project evaluating the feasibility of using machine learning to extract key business entities from SEC Form 10-K filings. The project compares a traditional rule-based (regex) extraction approach against a supervised Named Entity Recognition (NER) model built with spaCy.

The objective is not to deploy a production system, but to assess whether a machine learning–based approach can improve extraction accuracy, consistency, and scalability relative to deterministic methods, while remaining suitable for human-in-the-loop review workflows.

Target entity types include:

PERSON (executive names)

TITLE (leadership and governance roles)

ORG (companies, funds, and institutional entities)

MONEY (revenue-related monetary values)

All analysis is performed on publicly available SEC 10-K filings provided as structured JSON files via kaggle.

Methodology Summary

The project implements and evaluates two extraction strategies:

Rule-based baseline
A deterministic regex-based extractor designed to capture common patterns for names, titles, organizations, and monetary values.

Supervised machine learning model
A spaCy Named Entity Recognition (NER) model trained on a manually annotated gold-standard dataset curated specifically for this project.

Both approaches are evaluated against the same gold annotations using standard NER metrics: precision, recall, and F1 score. Results are compared to determine whether machine learning provides a measurable and practically meaningful improvement over the baseline.

Repository Structure
gold_annotations/

Finalized gold-standard annotation files used as ground truth for evaluation.
These annotations reflect human-first labeling rules and serve as the authoritative reference for all scoring.

gold_raw_text/

Raw narrative text extractions used as the basis for manual annotation.
These files preserve original wording and structure from SEC 10-K filings.

baseline_regex_outputs.json

Output produced by the regex-based baseline extractor.
Used for direct comparison against gold annotations during evaluation.

Notebooks/

This directory contains all analysis notebooks used in the project.

data_structuring.ipynb
Loads raw SEC JSON files, normalizes text structure, and prepares inputs for annotation and modeling.
Recommended environment: VS Code or local Jupyter.

gold_labeling.ipynb
Manual annotation workflow, validation checks, and preparation of training and evaluation datasets.
Recommended environment: VS Code or local Jupyter.

regex_analysis.ipynb
Executes the rule-based baseline extraction and computes precision, recall, and F1 metrics.
Recommended environment: VS Code or local Jupyter.

spacy_analysis.ipynb
Trains and evaluates the supervised spaCy NER model, including model configuration, training loops, and performance evaluation.
Best run in Google Colab due to dependency setup, model training runtime, and environment consistency.

Docs/

Supporting project documentation.

Labeling Rules.docx
Authoritative entity definitions, inclusion/exclusion rules, span boundaries, and annotation guidance used to create the gold dataset.

Tools & Environment

Python

spaCy (Named Entity Recognition)

Pandas (data handling)

scikit-learn (evaluation metrics)

Jupyter Notebook

Visual Studio Code (primary local development environment)

Google Colab (recommended for spaCy model training and analysis)

No proprietary data or external annotation platforms are used. All code and analysis are reproducible using open-source tools.

Scope & Limitations

The project focuses exclusively on narrative sections of SEC 10-K filings (primarily Items 7 and 10).

Structured financial tables and external exhibits are out of scope.

The NER model is trained on a curated subset of filings and is not intended to generalize across all financial document types.

Results are evaluated analytically; no production deployment is attempted.

Purpose & Outcomes

This repository demonstrates:

How human-defined labeling standards can be operationalized into a gold dataset

The strengths and weaknesses of regex-based extraction in complex business text

The feasibility of applying supervised machine learning to improve entity extraction accuracy

Practical considerations for integrating ML outputs into analyst-driven review workflows

The work is intended for academic evaluation and as a reference example of comparative NLP analysis in a regulated document domain.
