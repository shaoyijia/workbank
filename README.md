<p align="center">
<img src="assets/workbank-text.svg" style="width: 40%; height:auto" />
</p>
<h3 align="center">
<p>Large-scale audit of worker desire and technological capability of AI agents for work
</h3>
<img src="assets/workbank.png" style="width: 100%; height: auto" />

## Overview

**WORKBank** (AI Agent Worker Outlook and Readiness Knowledge Bank) is a database that captures worker desire and technological capability of AI agents for occupational tasks.

The current version of WORKBank includes preferences from 1,500 U.S. domain workers and capability assessments from AI experts, covering over 844 tasks across 104 occupations collected between January and May 2025.

## Database Access

To download our database, run:

```python
from datasets import load_dataset


worker_desire = load_dataset("SALT-NLP/WORKBank", data_files="worker_data/domain_worker_desires.csv")["train"]

expert_ratings = load_dataset("SALT-NLP/WORKBank", data_files="expert_ratings/expert_rated_technological_capability.csv")["train"]

task_meta_data = load_dataset("SALT-NLP/WORKBank", data_files="task_data/task_statement_with_metadata.csv")["train"]
```

You can also manually download the CSV files [here](https://huggingface.co/datasets/SALT-NLP/WORKBank/tree/main).

## Data Analysis Code

- [automation_desire.ipynb](analysis/automation_desire.ipynb): Analysis of the distribution of automation desire ratings, analysis of the reason behind automation desire.
- [automation_viability.ipynb](analysis/automation_viability.ipynb): Analysis of the automation desire-capability landscape.
- [human_agency_scale.ipynb](analysis/human_agency_scale.ipynb): Analysis of the worker-desired human agency level and the expert-assessed feasible human agency level for different tasks.
- [human_skill_shift.ipynb](analysis/human_skill_shift.ipynb): Analysis of demographic and occupational coverage of WORKBank and mixed-effects model regression on worker responses.

## Want to Launch the Audit in Your Organization?

Unlike traditional surveys, our auditing framework features an audio-enhanced interface and combines quantitative ratings with analysis of audio transcripts. This approach enables more calibrated and context-rich responses. We are also working to support input from additional modalities.
