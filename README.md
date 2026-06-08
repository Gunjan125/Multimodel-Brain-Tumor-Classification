# 🧠 Multimodal Brain Tumor Detection using CT & MRI Scans

A Deep Learning-based Multimodal Brain Tumor Detection System that combines features extracted from CT scans and MRI scans using VGG16 Transfer Learning and Feature Fusion to improve tumor classification performance.

---

## 📌 Project Overview

Brain tumor diagnosis often relies on multiple imaging modalities such as CT scans and MRI scans. Each modality provides unique information about brain tissues and abnormalities.

This project utilizes:

- CT Scan Images
- MRI Scan Images
- VGG16 Transfer Learning
- Feature Extraction
- Feature Fusion
- Binary Classification

to build a multimodal deep learning framework capable of detecting brain tumors more effectively than using a single imaging modality.

---

## 🚀 Key Features

✅ CT Scan Tumor Classification

✅ MRI Scan Tumor Classification

✅ Transfer Learning using VGG16

✅ Automatic Feature Extraction

✅ Feature Scaling using StandardScaler

✅ Multimodal Feature Fusion

✅ Binary Tumor Detection

✅ Performance Evaluation using Classification Metrics

---

## 🏗️ System Architecture

```text
                CT Scan Images
                       │
                       ▼
                VGG16 Feature Extractor
                       │
                       ▼
                 CT Features
                       │
                       │
                       ▼
                MRI Scan Images
                       │
                       ▼
                VGG16 Feature Extractor
                       │
                       ▼
                 MRI Features
                       │
                       │
                       ▼
          ┌────────────────────────┐
          │ Feature Concatenation  │
          └────────────────────────┘
                       │
                       ▼
               Dense Neural Network
                       │
                       ▼
               Tumor Prediction
```

---

## 📂 Dataset

The project uses the **Brain Tumor Multimodal Image Dataset** containing:

### MRI Dataset

- Glioma
- Meningioma
- Pituitary
- Tumor

### CT Dataset

- Healthy
- Tumor

The dataset includes thousands of CT and MRI brain images used for training and evaluation.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Programming Language |
| TensorFlow | Deep Learning Framework |
| Keras | Model Building |
| VGG16 | Transfer Learning |
| NumPy | Numerical Computation |
| Pandas | Data Handling |
| OpenCV | Image Processing |
| Matplotlib | Visualization |
| Seaborn | Data Visualization |
| Scikit-Learn | Data Splitting & Evaluation |
| Kaggle | Training Environment |

---

## ⚙️ Methodology

### 1. Data Collection

- Load CT Scan images
- Load MRI Scan images
- Create labeled datasets

### 2. Data Preprocessing

- Image resizing to 224×224
- Pixel normalization
- Label encoding
- Train-validation-test split

### 3. Data Balancing

To avoid class imbalance:

- Oversampling of minority classes
- Balanced training dataset creation

### 4. Transfer Learning

Two independent VGG16 models are used:

#### CT Feature Extractor

- Pretrained VGG16
- Frozen convolution layers
- Global Average Pooling
- Dense Feature Layer (256 neurons)

#### MRI Feature Extractor

- Pretrained VGG16
- Frozen convolution layers
- Global Average Pooling
- Dense Feature Layer (256 neurons)

### 5. Feature Fusion

Extracted CT and MRI features are:

- Standardized
- Concatenated
- Combined into a unified feature representation

### 6. Classification

Merged features are passed through:

```text
Input Layer
     ↓
Dense Layer (128)
     ↓
ReLU Activation
     ↓
Output Layer
     ↓
Sigmoid Activation
```

---

## 📊 Model Training

### CT Model

- Backbone: VGG16
- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Epochs: 10

### MRI Model

- Backbone: VGG16
- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Epochs: 10

### Fusion Model

- Dense Neural Network
- Feature Fusion Architecture
- Binary Classification

---

## 📈 Evaluation Metrics

The model performance is evaluated using:

- Accuracy
- Loss
- Confusion Matrix
- Classification Report
- Precision
- Recall
- F1 Score

---

## 🔥 Results

The multimodal architecture demonstrates improved classification performance by combining complementary information from both CT and MRI scans.

The feature fusion approach allows the model to learn richer representations compared to single-modality systems.

---

## 🔮 Future Improvements

- Fine-tuning VGG16 layers
- Use EfficientNet or ResNet
- Multi-class tumor classification
- Grad-CAM explainability
- Real-time prediction system
- Streamlit web application deployment
- Clinical decision support integration

---

## 👩‍💻 Author

### Gunjan Soni

Computer Science Student | AI/ML Enthusiast | Deep Learning Researcher

---
