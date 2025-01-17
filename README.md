# Sentiment Analysis with Fine-Tuned LLaMA 3

This project demonstrates fine-tuning a LLaMA 3 8B parameter chat model for sentiment analysis, specifically targeting financial news headlines. The model classifies headlines as positive, neutral, or negative.  QLoRA (Quantized Low-Rank Adaptation) is employed to reduce memory usage and training time.

## Dataset

The project uses the Financial Sentiment Analysis dataset ([link to dataset](https://www.kaggle.com/datasets/sbhatti/financial-sentiment-analysis)), which provides financial sentences labeled with sentiment.

## Model and Fine-tuning

* **Model:** LLaMA 3 8B chat model (8b-chat-hf).
* **Fine-tuning Method:** QLoRA (Quantized Low-Rank Adaptation) within the PEFT (Parameter-Efficient Fine-Tuning) framework.
* **Trainer:** `SFTTrainer` from the TRL (Transformer Reinforcement Learning) library.
* **Quantization:** 4-bit quantization (NF4) for reduced memory footprint.
* **Prompt Engineering:** Clear prompts were designed to guide the model towards accurate sentiment classification.

## Evaluation

The fine-tuned model achieves an accuracy of **86.1%** on the held-out test set.  A detailed classification report and confusion matrix are provided in the notebook, showcasing performance across the different sentiment categories.


## Results

| Metric        | Score |
|----------------|-------|
| Accuracy      | 0.861 |
| Macro F1      | 0.86  |
| Precision (macro) | 0.86 |
| Recall (macro)  | 0.86  |

