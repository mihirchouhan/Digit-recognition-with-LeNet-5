# Handwritten Digit Recognition using LeNet-5 CNN

A deep learning project that implements the **LeNet-5 Convolutional Neural Network (CNN)** for handwritten digit recognition using the **MNIST dataset**. The model is trained to classify handwritten digits (0–9) and includes a custom inference pipeline for predicting user-provided handwritten digit images.

---

## 📌 Features

- Implemented the LeNet-5 CNN architecture from scratch using TensorFlow/Keras.
- Trained on the MNIST dataset (60,000 training and 10,000 testing images).
- Achieved **98%+ test accuracy** on handwritten digit classification.
- Supports prediction on custom handwritten digit images.
- Includes image preprocessing (grayscale conversion, resizing, normalization, thresholding, and inversion).
- Visualizes training performance using accuracy and loss graphs.

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- Pillow

---

## 📂 Project Structure

```
Digit-recognition-with-LeNet-5/
│── dataset/
│   ├── train-images.idx3-ubyte
│   ├── train-labels.idx1-ubyte
│   ├── t10k-images.idx3-ubyte
│   └── t10k-labels.idx1-ubyte
│
│── model/
│   └── lenet_mnist.h5
│
│── images/
│   ├── accuracy.png
│   ├── loss.png
│   └── sample_prediction.png
│
│── train.py
│── predict.py
│── requirements.txt
│── README.md
```

---

## 📊 Dataset

The project uses the **MNIST Handwritten Digit Dataset**.

- Training Images: **60,000**
- Testing Images: **10,000**
- Image Size: **28 × 28**
- Number of Classes: **10 (Digits 0–9)**

Dataset:
https://www.kaggle.com/datasets/hojjatk/mnist-dataset

---

## 🧠 LeNet-5 Architecture

| Layer | Output Shape | Activation |
|--------|--------------|------------|
| Input | 28 × 28 × 1 | — |
| Conv2D (6, 5×5) | 24 × 24 × 6 | tanh |
| Average Pooling | 12 × 12 × 6 | — |
| Conv2D (16, 5×5) | 8 × 8 × 16 | tanh |
| Average Pooling | 4 × 4 × 16 | — |
| Flatten | 256 | — |
| Dense | 120 | tanh |
| Dense | 84 | tanh |
| Output | 10 | Softmax |

---

## ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Batch Size | 128 |
| Epochs | 10 |
| Activation | tanh |
| Output Activation | Softmax |

---

## 📈 Model Performance

- **Training Accuracy:** ~99%
- **Test Accuracy:** ~98%
- **Loss Function:** Categorical Crossentropy

The model demonstrates excellent performance on the MNIST dataset and successfully predicts custom handwritten digits after preprocessing.

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/mihirchouhan/Digit-recognition-with-LeNet-5.git
```

Move to the project directory:

```bash
cd Digit-recognition-with-LeNet-5
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Training the Model

Run:

```bash
python train.py
```

The trained model will be saved as:

```
lenet_mnist.h5
```

---

## 🔍 Predict Custom Handwritten Digits

Place your handwritten digit image inside the project folder.

Run:

```bash
python predict.py
```

The model will preprocess the image and output the predicted digit.

Example Output:

```
Predicted Digit: 4
Confidence: 99.2%
```

---

## 📷 Sample Results

### Training Accuracy

(Add `accuracy.png` here)

### Training Loss

(Add `loss.png` here)

### Custom Digit Prediction

(Add `sample_prediction.png` here)

---

## 📌 Future Improvements

- Real-time digit recognition using webcam
- Streamlit web application
- Data augmentation for better real-world accuracy
- Support for noisy and ruled-paper handwritten inputs
- Deployment using Flask or FastAPI

---

## 👨‍💻 Author

**Mihir Chouhan**

- GitHub: https://github.com/mihirchouhan
- LinkedIn: https://www.linkedin.com/in/mihirchouhan/

---

## 📜 License

This project is developed for educational and learning purposes.
