​🐾 Cats vs. Dogs Classification with Explainable AI (Grad-CAM)
​This repository features a robust, end-to-end Deep Learning pipeline for binary image classification. Leveraging Transfer Learning and Explainable AI (XAI), the model achieves high precision while providing visual justifications for its predictions.
​🚀 Key Features
​Architecture: Built using the ResNet50 backbone for superior feature extraction.
​Transfer Learning: Utilized pre-trained ImageNet weights with custom dense layers for domain adaptation.
​Explainable AI (Grad-CAM): Integrated Gradient-weighted Class Activation Mapping to visualize and audit model decision-making.
​Professional Evaluation: Complete performance analysis using Confusion Matrices and Classification Reports.
​📊 Dataset & Preprocessing
​The model was trained on a balanced dataset of cats and dogs:
​Training Samples: 6,403 images.
​Validation Samples: 1,602 images.
​Test Samples: 2,023 images.
​Pipeline: Automated data flow using ImageDataGenerator with ResNet50-specific preprocessing.
​Input Resolution: Images resized to 224 \times 224 \times 3.

​🏗️ Model Architecture
# Strategic Architecture
base_model = ResNet50(weights='imagenet', include_top=False, input_shape=(224, 224, 3))
model = Sequential([
    base_model,
    GlobalAveragePooling2D(),
    Dense(256, activation='relu'),
    Dropout(0.2),
    Dense(1, activation='sigmoid') # Binary Classification
])
The model was compiled using the Adam optimizer and Binary Crossentropy loss function.

​📈 Performance Results
​The model demonstrated exceptional stability and accuracy during training:
​Test Accuracy: 98.42%.
​Precision (Cat): 1.00.
​Recall (Dog): 1.00.
​Confusion Matrix
​The matrix reveals minimal misclassifications, showing only 34 errors out of 2,023 test samples.
(Insert your Confusion Matrix image here)
​🔍 Model Interpretability (Grad-CAM)
​To ensure the model isn't "cheating," Grad-CAM heatmaps were generated to highlight the regions influencing the classification.
​Observation: The model accurately focuses on feline/canine facial features and body textures rather than background noise.
​🛠️ Tech Stack
​Frameworks: TensorFlow / Keras
​Visualization: Matplotlib, Seaborn, OpenCV
​Data Handling: Pandas, NumPy
​Environment: Google Colab / Kaggle

## 📊 Model Performance & Results

### **1. Accuracy & Loss Curves (Training vs Validation)**
These plots show how the model learned over epochs.

![Accuracy and Loss Curves](<   <img width="510" height="228" alt="Classification_Report" src="https://github.com/user-attachments/assets/572f07f7-c8b4-464c-a082-86cb985e183d" />
 >)

### **2. Confusion Matrix**
The confusion matrix provides insights into how many images were correctly classified versus those that were misclassified.
(ارفع صورة الـ Confusion Matrix هنا)
![Confusion Matrix](<حط لينك صورة الـ Confusion Matrix هنا>)

### **3. Classification Report**
This table details precision, recall, f1-score, and support for each class (Cat, Dog).
(ارفع صورة الـ Classification Report هنا)
![Classification Report](<حط لينك صورة الـ Classification Report هنا>)

### **4. Grad-CAM Visualization**
Grad-CAM (Gradient-weighted Class Activation Mapping) highlights the regions of the image that the model focused on to make its prediction.
(ارفع صورة الـ Grad-CAM هنا)
![Grad-CAM Visualization](<حط لينك صورة الـ Grad-CAM هنا>)
