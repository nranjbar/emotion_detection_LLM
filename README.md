# emotion_detection_LLM

This repository contains code and resources related to emotion detection using Large Language Models (LLMs), specifically focusing on fine-tuning Llama-3 for this task. This project participates in SemEval-2025 Task 11: Bridging the Gap in Text-Based Emotion Detection :https://github.com/emotion-analysis-project/SemEval2025-Task11

## Project Overview

This project introduces a novel method for improving multi-label emotion classification by leveraging the explanatory capabilities of Llama-3.  Existing methods often struggle with ambiguous emotional expressions and overlapping emotional cues.  Our approach addresses this challenge by using Llama-3 to generate explanatory content that clarifies ambiguous text.  This explanatory context is then incorporated into the input provided to RoBERTa, a robust pre-trained language model for emotion classification. By providing richer contextual information, we aim to improve RoBERTa's ability to accurately identify multiple emotions within a given text. We hypothesize that this will lead to significantly improved F1-scores, particularly for emotions that are often confused or under-represented, such as fear, joy, and sadness.  Our experiments demonstrate that this method surpasses the performance of text-only models, showcasing the effectiveness of incorporating explanatory context for resolving ambiguity and enhancing the accuracy of multi-label emotion detection.
The core code for fine-tuning Llama-3 is derived from the excellent work in [Link to the unsloth repository]: https://github.com/unslothai/unsloth. This repository provides the foundational scripts and utilities which we adapt and extend for our specific needs in this SemEval task. 

## Code Structure

This repository builds upon the codebase from https://github.com/unslothai/unsloth.  Key modifications and additions in this repository include:

• **`data/`**: This directory contains the dataset used for fine-tuning Llama-3 to generate explanations for sentences. This dataset of explanations was generated using GPT-4 and contains 150 sentences. Data for training, validation, and testing are available at: https://github.com/emotion-analysis-project/SemEval2025-Task11/tree/main/task-dataset
• **`codes/`**: This directory contains Notebooks used for data preparation specific to this task, model training modifications, evaluation, and analysis.  
