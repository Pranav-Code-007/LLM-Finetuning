# Finetuning LLM with LoRA for Biomedical Abstract Summarization

This project demonstrates how to finetune a large language model (LLM) using Low-Rank Adaptation (LoRA) for summarizing biomedical abstracts. The Jupyter Notebook (`.ipynb` file) contains the complete process, from loading and preprocessing PubMed data to training a LoRA-adapted FLAN-T5-small model.

## Overview

The Jupyter Notebook performs the following steps:

1.  Installs necessary libraries.
2.  Loads and parses a PubMed XML file to extract article titles and abstracts.
3.  Filters articles based on abstract length.
4.  Creates a JSONL dataset for instruction-based fine-tuning.
5.  Loads this dataset using Hugging Face `datasets`.
6.  Splits the dataset into training and validation sets.
7.  Loads the tokenizer for the FLAN-T5-small model.
8.  Preprocesses the data for the model.
9.  Loads the pre-trained FLAN-T5-small model.
10. Configures and applies LoRA to the model.
11. Defines training arguments and a data collator.
12. Initializes and runs the `Seq2SeqTrainer`.
13. Shows an example of generating a summary.
14. Evaluates the finetuned model.
15. Saves the LoRA-adapted model and tokenizer.
16. Merges the LoRA layers into the base model.

## Prerequisites

* Python 3.6 or higher
* Jupyter Notebook installed
* Internet connection to download libraries and models

## Installation

To run this notebook, you will need to install the required libraries. You can do this within the Jupyter Notebook cells by executing the following commands:

```python
! pip install pubmed_parser peft datasets
! pip install --upgrade transformers peft
