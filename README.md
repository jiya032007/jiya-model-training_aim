# VibeCheck: LLM Fine-Tuning Experiment

## Overview
This repository contains my individual model fine-tuning experiment for the VibeCheck project. The goal was to practice the full training pipeline using a pretrained language model, an instruction-style dataset, and Google Colab.

## Model
- **Base model:** Llama-3.2-1B-Instruct
- **Model loading:** 4-bit quantization
- **Fine-tuning method:** LoRA (Low-Rank Adaptation)
- **Trainable parameters:** Approximately 0.9%

## Dataset
- **Dataset:** [Databricks Dolly 15K](https://huggingface.co/datasets/databricks/databricks-dolly-15k)
- **Subset used:** First 1,000 examples
- **Format:** Instruction, optional context, and response
- **Data preparation:** Converted examples into user/assistant conversations and formatted them using the Llama 3.1 chat template.

Dolly is a general-purpose instruction-following dataset containing human-written responses across tasks such as question answering, summarization, and brainstorming. It was used to practice the training pipeline, not specifically to train a cybersecurity detector.

## Training Setup
- **Platform:** Google Colab
- **Hardware:** Free NVIDIA T4 GPU
- **Notebook template:** Unsloth Llama 3.2 (1B + 3B) Conversational
- **Training steps:** 60
- **Batch size:** 8
- **Training duration:** Approximately 1.5 minutes

## Results
The training run completed without errors. The observed training loss decreased from approximately 2.5 to 2.3, although the short run and noisy loss values are insufficient to establish meaningful learning or improved performance.

A longer training run and evaluation on held-out examples would be needed to assess the results more reliably.

## Next Steps
- Run a longer training experiment.
- Compare training and evaluation loss.
- Test the fine-tuned model on sample prompts.
- Explore security-focused datasets relevant to VibeCheck.

## Notebook
(https://colab.research.google.com/drive/1P7eeajBzG66eB8iseAC8EReEVoMpP5ji?usp=sharing)
