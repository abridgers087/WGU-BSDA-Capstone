BSDA Capstone – Sprint 1 (Baseline & Gold Annotations)
Project Overview

This repository contains the initial phase (Sprint 1) of a BSDA capstone project focused on evaluating named entity extraction from SEC 10-K filings. The goal of this sprint was to establish a reliable gold-standard dataset and evaluate a regex-based baseline extraction approach using standard NER metrics.

Sprint 2 will build on this work by developing and evaluating a machine learning–based extraction pipeline.

Objectives (Sprint 1)

Define entity labeling rules and scope

Create a manually annotated gold dataset

Implement a regex-based baseline extractor

Evaluate baseline performance using precision, recall, and F1 score

Key Files:

gold_annotations/
Contains finalized gold-standard annotations used as ground truth.

gold_raw_text/
Raw text extractions used as the basis for manual annotation.

baseline_regex_outputs.json
Output from the regex-based entity extraction baseline.

Notebooks/

data_structuring.ipynb: Data loading and normalization

gold_labeling.ipynb: Manual annotation workflow and validation

regex_analysis.ipynb: Baseline evaluation and metric computation

Docs/Labeling Rules.docx
Entity definitions, inclusion/exclusion criteria, and labeling guidance.