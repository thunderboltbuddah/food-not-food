# Food / Not Food Text Classifier

A lightweight NLP text classification project that predicts whether a given image caption describes food or not, built using Hugging Face's `transformers` and `datasets` libraries.

## 🎯 Overview

This project fine-tunes a **DistilBERT** model to classify short image captions into two categories: `food` or `not_food`. It was built as a hands-on introduction to the Hugging Face ecosystem — covering dataset loading, tokenization, model fine-tuning, evaluation, and deployment as a live interactive demo.

## 📊 Dataset

Trained on the [`food_not_food_image_captions`](https://huggingface.co/datasets/mrdbourke/learn_hf_food_not_food_image_captions) dataset — 250 synthetically generated image captions (via Mistral/Mixtral), each labeled `food` or `not_food`. Captions range from dishes like curries, pizza, and sushi to non-food scenes like furniture, pets, and household objects, giving the model a clear binary decision boundary to learn.

## 🧠 Model & Approach

- **Base model:** `distilbert-base-uncased`
- **Task:** Binary text classification (sequence classification head)
- **Framework:** Hugging Face `transformers` + `datasets`
- **Training:** Fine-tuned on the labeled caption dataset using the Hugging Face `Trainer` API
- **Evaluation:** Accuracy / F1 tracked on a held-out split

## 🚀 Deployment

The trained model was deployed as an interactive **Hugging Face Space**, allowing users to input any caption and instantly see whether it's classified as food or not — a simple way to demo the model without needing local setup.

## 🛠️ Tech Stack

Python · Hugging Face `transformers` · `datasets` · PyTorch · DistilBERT · Gradio (Spaces)
