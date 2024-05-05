# Project Adaptation for Code Modeling models
## Introduction
This project aims to enhance Language Model (LM) performance on underrepresented programming languages, focusing specifically on Kotlin. 
The task involves adapting a pre-trained Transformer model for code completion in Kotlin and evaluating its performance. 
The project follows a structured approach, including dataset creation, model adaptation, fine-tuning, and evaluation.

## Task Overview
The main objectives of the project are as follows:

1. Pick a large open-source project, written mostly in Kotlin, e.g. Kotlin
2. Extract all code in Kotlin from the project to create a Kotlin code completion dataset
3. Adapt a Python-oriented pre-trained Transformer model such as Phi-1.5 to do code completion and evaluate it on the Kotlin dataset test part and CodeXGLUE Python code completion test part (prompts, answers)
4. Fine-tune the model on the Kotlin dataset you have collected
5. Report the changes of quality on both Kotlin and Python data after the finetuning

## Solution Overview
The project solution involves the following steps:

1. Dataset Creation: Kotlin code is extracted from the **Ktor framework** to create a comprehensive dataset for code completion tasks.
2. Model Adaptation: The pre-trained CodeBERT model is selected and adapted for Kotlin code completion. Tokenization and model loading are performed using Hugging Face's Transformers library.
3. Data Preprocessing: The Kotlin dataset is tokenized using the CodeBERT tokenizer, split into training, validation, and test sets, and prepared for training using PyTorch DataLoader.
4. Fine-Tuning: The adapted model is fine-tuned on the Kotlin dataset using the AdamW optimizer and a linear scheduler. Training and validation losses are monitored during the fine-tuning process.
5. Evaluation: The performance of the fine-tuned model is evaluated on the Kotlin test dataset by calculating the average loss.

## Challenges Faced
During the fine-tuning process, challenges were encountered, particularly in obtaining meaningful training and validation losses. 
Additionally, limitations in the evaluation procedure hindered the accurate assessment of the model's performance.

## Next Steps
 - Hyperparameter Tuning: Experiment with different hyperparameter configurations to improve training stability and convergence.
 - Evaluation Enhancement: Implement comprehensive evaluation metrics to assess the model's performance accurately.
 - Debugging and Troubleshooting: Investigate and resolve potential issues in the training pipeline to ensure reliable results.

By addressing these areas for improvement and refining the training and evaluation processes, the model's performance can be enhanced for Kotlin code completion tasks.
