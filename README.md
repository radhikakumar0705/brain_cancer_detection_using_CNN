# Brain Cancer Detection Using MRI Images

This project implements a deep learning model to classify brain cancer using MRI images. The dataset used is obtained from Kaggle, and the solution involves data preprocessing, model training, and evaluation of performance metrics.

---

## Dataset

- **Source**: [Brain Cancer Detection MRI Images Dataset](https://www.kaggle.com/datasets/hamzahabib47/brain-cancer-detection-mri-images)
- **Structure**: 800 images belonging to 2 classes (Brain Cancer/No Brain Cancer).

---

## Installation

### Prerequisites

Ensure you have the following installed:
- Python 3.7 or later
- TensorFlow
- OpenCV
- Matplotlib
- scikit-learn
- Kaggle API for dataset download

### Steps

1. Install the Kaggle API:
   ```bash
   pip install kaggle
   ```

2. Download the dataset:
   ```bash
   !kaggle datasets download -d hamzahabib47/brain-cancer-detection-mri-images
   ```

3. Extract the dataset:
   ```python
   from zipfile import ZipFile
   fn = "brain-cancer-detection-mri-images.zip"
   with ZipFile(fn, 'r') as zip:
       zip.extractall()
       print("done")
   ```

---

## Model Pipeline

### Data Preprocessing

1. **Loading Images**: Read images and their labels into a TensorFlow dataset.
2. **Scaling**: Normalize the pixel values by dividing by 255.
3. **Splitting**: The dataset is split into:
   - **Training Set**: 70%
   - **Validation Set**: 20%
   - **Testing Set**: 10%

### Model Architecture

- Sequential model with the following layers:
  - **Conv2D Layers**: Feature extraction with ReLU activation.
  - **MaxPooling2D Layers**: Down-sampling feature maps.
  - **Flatten**: Converts 2D matrices into a single vector.
  - **Dense Layers**:
    - Fully connected layers for classification.
    - Final layer uses a sigmoid activation for binary classification.

### Compilation

- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Metrics**: Accuracy

### Training

- 20 epochs with TensorBoard logging enabled.

---

## Results

### Metrics

- Precision: **1.0**
- Recall: **1.0**
- Accuracy: **1.0**

### Performance Graphs

- Loss and Accuracy trends are plotted for training and validation data.

---

## How to Run

1. Clone the repository or copy the code into your project directory.
2. Install the required Python libraries.
3. Run the script for preprocessing, training, and evaluation.

---

## Acknowledgements

- Dataset provided by [Hamza Habib on Kaggle](https://www.kaggle.com/datasets/hamzahabib47/brain-cancer-detection-mri-images).

--- 
