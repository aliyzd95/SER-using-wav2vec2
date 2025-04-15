# Emotion Recognition in Persian Speech using Wav2Vec2

This project focuses on **emotion recognition in Persian speech** using the powerful `Wav2Vec2` model. The implementation is entirely contained in a single notebook named `wav2vec2_SER.ipynb`, which covers data loading, model fine-tuning, evaluation, and analysis.

## 🔍 Project Overview

We use the **`m3hrdadfi/wav2vec2-large-xlsr-persian-v3`** pretrained model for speech representation learning. The model is fine-tuned on a custom enhanced dataset called **Modified ShEMO**, which is an improved version of the original ShEMO dataset for Persian emotional speech.

📄 An academic [paper](https://arxiv.org/abs/2211.09956) introducing Modified ShEMO has been written, which also includes performance comparisons of various models trained on this dataset.

## 📙 Description

The model is trained and evaluated on the **Modified ShEMO** dataset, an improved version of the original ShEMO dataset for Persian emotional speech. The notebook demonstrates how a fine-tuned Wav2Vec2 model can outperform previous state-of-the-art models in emotion classification tasks for Persian speech.

The trained model is available on Hugging Face:  
👉 [aliyzd95/wav2vec2-xlsr-shemo-speech-emotion-recognition](https://huggingface.co/aliyzd95/wav2vec2-xlsr-shemo-speech-emotion-recognition)

## 📊 Results

The Modified ShEMO paper evaluates multiple models. Below are some of the reported results. 
This project achieves a **WA (Weighted Accuracy)** of `0.8401`, which surpasses the results reported in the original research paper introducing the Modified ShEMO dataset.

| Model                             | Features                                 | WA%   | UA%   |
|----------------------------------|------------------------------------------|-------|-------|
| SVM (Baseline)              | eGeMAPS                                   | 76.65 | 63.62 |
| CNN (1D) – Acoustic Model        | emo_large                                 | 79.68 | 66.12 |
| CNN (2D) – Linguistic Model      | fastText (GT)                             | 58.01 | 51.37 |
| Early-Fusion Model (DNN)         | emo_large + fastText (GT)                 | 81.60 | 74.68 |
| Early-Fusion Model (DNN)         | emo_large + fastText (ASR transcriptions) | 80.51 | 69.73 |
| **Wav2Vec2 (This project)**      | Raw Audio                                    | **84.01**  |   -   |


Also, a comparison of SVM performance before and after dataset modification:

| Machine Learning Model | Dataset           | WA%   | UA%   |
|------------------------|--------------------|-------|-------|
| SVM (After Modification) | Modified ShEMO     | 76.65 | 63.62 |
| SVM (Before Modification)| Original ShEMO     | 72.95 | 58.66 |
| SVM (ShEMO Paper)   | Original ShEMO          | 58.02 |   -   |

## 🚀 Project Results

In this project, the fine-tuned Wav2Vec2 model achieved a weighted accuracy of:

```
Weighted Accuracy = 0.8401510657904797
```

🔹 This result outperforms all previously reported methods in the paper, including the best-performing Early-Fusion model (WA = 81.60%).

## 📁 Project Structure

- `wav2vec2_SER.ipynb`: The notebook includes:
  - Loading and preprocessing audio data
  - Fine-tuning Wav2Vec2 on Modified ShEMO
  - Model evaluation
  - Visualization and error analysis

## 📦 Dataset

We used the **[Modified ShEMO](https://github.com/aliyzd95/modified_shemo)** dataset, an improved version of the original ShEMO dataset. Enhancements include:

- Improved audio quality
- Corrected labels
- Preprocessing suitable for deep learning models

## 📈 Error Analysis

At the end of the notebook, samples of correct and incorrect predictions are visualized and discussed, offering insights into model limitations and possible future improvements.

## 🔮 Future Work

- Compare with other models like HuBERT and Whisper
- Apply audio augmentation for diversity
- Integrate larger language models to enhance semantic understanding

## 🤝 Contributions

Feel free to cite or extend this project. For any questions or improvements, contributions are welcome!

---

