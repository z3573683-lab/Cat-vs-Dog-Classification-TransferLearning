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

![Accuracy and Loss Curves](< <img width="1341" height="512" alt="Loss_Accuracy" src="https://github.com/user-attachments/assets/5c2d4b78-437d-44f2-89b9-8e38fcfd0dbb" />
  >)

### **2. Confusion Matrix**
The confusion matrix provides insights into how many images were correctly classified versus those that were misclassified.

![Confusion Matrix](< <img width="664" height="622" alt="Confusion_Matrix" src="https://github.com/user-attachments/assets/25e6895b-c554-4dae-ab2b-e216a1998154" />
>) 

### **3. Classification Report**
This table details precision, recall, f1-score, and support for each class (Cat, Dog).

![Classification Report](<<img width="510" height="228" alt="Classification_Report" src="https://github.com/user-attachments/assets/f188b55d-df4f-45dd-96c6-db9eee774242" />
 >)

### **4. Grad-CAM Visualization**
Grad-CAM (Gradient-weighted Class Activation Mapping) highlights the regions of the image that the model focused on to make its prediction.

![Grad-CAM Visualization](<<img width="936" height="477" alt="Grad_CAM" src="https://github.com/user-attachments/assets/a3e2d5fe-4d05-4cae-a2ef-48e9be7992b0" />
 >)


## 👤 Author
**[MOHAMED BELAL]** *Deep Learning & Data Engineering Enthusiast*

MY PHONE [01018689118]


