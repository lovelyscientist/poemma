**Poemma** 📓 is a specialized large language model trained to provide annotations to poems. It helps to identify figurative language, metaphors, references, sound analysis and more. Poemma is created using QLoRa adapter with Llama-3.1-8b-Instruct base model.

Poemma is trained on [custom dataset of poetry annotations](https://huggingface.co/datasets/prettyvampire/genius_poems_annotations) based on [Kaggle Genius Song Lyrics dataset](https://www.kaggle.com/datasets/carlosgdcj/genius-song-lyrics-with-language-information/data) and [Genius API](https://docs.genius.com/).

Model card is available on Hugging Face hub by the following id - ```prettyvampire/poemma```

This repository contains code to reproduce Poemma and is structured in the following way:
1. *Filter Data & Extract Annotations* notebook contains code for creating, filtering, merging of the annotations dataset mentioned above.
2. *Custom Dataset Splitting & Upload* to HF contains logic for splitting the dataset into train, test and validation.
3. *SFT QLoRa LLama* notebook has code for fine-tuning the model.
4. *Model Merging and Evaluation* notebook merges base model with adapter and computes various evaluation metrics.
5. *LLM as Judge* notebook contains review of outputs of 3 different models by GPT-4o model.
