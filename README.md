# DeepFaceEmotion 🎭  
A deep learning project for facial emotion recognition using the FER-2013 dataset and personal real-world images.

---

## 🔍 Overview  
This project explores different machine learning and deep learning techniques for classifying facial expressions into seven basic emotions:

- 😠 Angry  
- 🤢 Disgusted  
- 😨 Fearful  
- 😊 Happy  
- 😐 Neutral  
- 😢 Sad  
- 😲 Surprised

The goal is to evaluate the performance of various models and preprocessing techniques, and to assess their generalization ability on personal, real-world facial images.

---

## 📁 Dataset  
We use the [FER-2013 dataset](https://www.kaggle.com/datasets/msambare/fer2013), a benchmark dataset for facial emotion classification.  
It contains **35,887 grayscale facial images (48x48 pixels)**, labeled with one of the 7 emotion classes.

---

## 🧠 Models Compared  

| Model              | Preprocessing              | Feature Extraction      |
|-------------------|----------------------------|-------------------------|
| SVM               | HOG                        | Hand-crafted features   |
| CNN               | Raw / Sobel-filtered       | Learned via Conv layers |
| EfficientNet (B0) | RGB + Resize to 224x224    | Transfer learning       |

---

## 🧪 Evaluation Metrics  
Each model is evaluated using:

- **Accuracy**
- **Precision, Recall, F1-score** (per class)
- **Confusion Matrix**
- **Training/Validation Accuracy & Loss plots**

---

## 💡 Key Features  

- 📊 Exploratory Data Analysis (EDA)
- 🧼 Anomaly Detection: corrupted, duplicate, low-quality images
- ⚙️ Preprocessing: HOG, grayscale normalization, Sobel filtering
- 🧪 SVM hyperparameter tuning (GridSearch & RandomizedSearch)
- 📦 Transfer Learning with EfficientNet
- 📷 Prediction on real-world personal images (with face detection)

---

## 📈 Results

| Model            | Test Accuracy | Macro F1 | Weighted F1 |
|------------------|---------------|----------|-------------|
| SVM + HOG        | ~40%          | ~0.34    | ~0.38       |
| CNN (Raw)        | 60.4%         | 0.56     | 0.59        |
| CNN (Sobel)      | 58.99%        | 0.55     | 0.58        |
| EfficientNet B0  | **62.87%**    | **0.57** | **0.62**    |

---

## 📸 Real-World Evaluation  
The best model (CNN with Sobel) was tested on **47 manually labeled personal images**.  
It achieved **64% accuracy**, with strong performance on *angry*, *neutral*, and *happy* expressions.  
Some underrepresented emotions like *fearful* and *disgusted* remained challenging.

---

## 🔧 Installation & Usage  
To run the project on Google Colab:

1. Clone or download this repository  
2. Upload your own images to the folder:  
   `/content/DeepFaceEmotion-main/emotion photos/`  
   Filenames should start with the correct emotion label (e.g., `happy_01.jpg`)
3. Run the notebook cell by cell  
4. Visualizations and metrics will be printed for each model

---

## 📂 Structure

```bash
DeepFaceEmotion/
│
├── DeepFaceEmotion.ipynb         # Main Colab notebook
├── emotion photos/               # Folder for real-world test images
├── AI_Emotion_Recognition_theory.pdf  # (Optional) in Hebrew
└── README.md                     # Project documentation
