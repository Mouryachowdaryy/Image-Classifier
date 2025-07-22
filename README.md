# Image Classifier (Google Colab)

A lightweight Google Colab notebook that lets you upload any image (dog, donkey, car, etc.) and instantly classifies it using a pre‑trained MobileNetV2 model (ImageNet).

---

## 🚀 Quick Start

1. **Open in Colab**  
   Click [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17Jq_PRwJ0IE5XC7-fO6mYwnwYRtfzlRA?usp=sharing)

2. **Run All Cells**  
   - Select **Runtime → Run all**  
   - Wait for TensorFlow and model download

3. **Upload an Image**  
   - Click **Choose File** in the notebook UI  
   - Select any `.jpg` / `.png`

4. **See Your Prediction**  
   - A preview of your image appears  
   - The model displays “✅ Predicted Class: *label* (*confidence*%)”

---

## 🎯 Features

- **Instant classification** of any image (dog, donkey, car, etc.)  
- Real‑time **browser upload widget**  
- Pre‑trained **MobileNetV2** on ImageNet  
- Displays **class name** + **confidence score**  
- **Zero setup** beyond opening the notebook

---

## 🛠️ How It Works

1. **Frontend (HTML + JS)**  
   - File input captures your image  
   - Displays a preview and “Predicting…” indicator  

2. **Backend (Python / Colab)**  
   - Receives image bytes via Base64  
   - Converts to a 224×224 RGB array  
   - Applies `preprocess_input`  
   - Runs through `MobileNetV2(weights='imagenet')`  
   - Retrieves top‑1 label and confidence with `decode_predictions`

3. **UI Update**  
   - Injects the prediction back into the page dynamically

---
## 📂 Repository Structure

```bash
image-classifier-colab/
├── Image_Classifier.ipynb    ← Colab notebook with UI + model code
└── README.md                 ← This documentation

