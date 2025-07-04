# 🎬 Fine-Tuning BERT for Sentiment Analysis on IMDb

This project fine-tunes the **BERT base model** (`bert-base-uncased`) for binary sentiment classification on the **IMDb Large Movie Review Dataset**, with post-hoc model interpretation using **LIME**.

Developed in **Google Colab**, using **TensorFlow** and **Hugging Face Transformers**.

---

## 📁 Overview

- **Dataset**: [IMDb Large Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)
- **Model**: BERT (base, uncased)
- **Task**: Sentiment Classification (Positive / Negative)
- **Tools**: TensorFlow, Hugging Face Transformers, LIME, Kaggle API
- **Environment**: Google Colab (GPU runtime recommended)

---

## 🚀 Running the Project (Colab Workflow)

1. Upload the full project folder to your Google Drive.

2. Open the notebook in Colab. It is structured into sequential steps (1–9).

3. For dataset access via Kaggle:
   - Download `kaggle.json` from [Kaggle API settings](https://www.kaggle.com/settings)
   - Place it in:  
     ```
     /DataCoach/kaggle.json
     ```
   - Run Step 2 in the notebook to download the dataset.

4. Run Steps 3–6.  
   Training (Step 6) is optional — a pre-trained model is provided.  
   - ⏱️ Training takes **at least 2 hours**, depending on your Colab runtime.

5. Steps 7–9 visualize model predictions using LIME.

---

## 📊 LIME Example

Sample LIME explanation for a review:

![LIME explanation](Assets/lime_visualization.png)


- Positive contributions: `incredible`, `hooked`, `this`
- Negative: `watching`, `show`

> Ref: [“Why Should I Trust You?” – Ribeiro et al. (2016)](https://arxiv.org/abs/1602.04938)  
> Tool: [`LIME`](https://github.com/marcotcr/lime)

---

## 🧰 Stack

- Python
- TensorFlow
- Transformers (Hugging Face)
- Google Colab
- Kaggle API
- LIME

---

## 📂 Structure

project-folder/
├── README.md
├── DataCoach/
│   └── sentiment_model/
│       ├── config.json
│       ├── special_tokens_map.json
│       ├── tokenizer_config.json
│       ├── vocab.txt
│   ├── Fine_tune_BERT_Model_for_Se... 
│   ├── tf_model.h5_download
├── Assets/
│   └── lime_visualization.png
