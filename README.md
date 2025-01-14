# CIFAR-10 Object Recognition Using CNN and ResNet50

This project implements and evaluates deep learning models to classify images from the CIFAR-10 dataset. The models include a Simple Neural Network (NN), a Convolutional Neural Network (CNN), and ResNet50.

---

## Dataset

The CIFAR-10 dataset consists of 60,000 32x32 color images categorized into 10 classes:

- **Classes:** Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck
- **Dataset Split:** 50,000 training images and 10,000 testing images.

---

## Preprocessing

- **Normalization:** Pixel values were normalized to range [0, 1].
- **Data Augmentation:** Techniques such as random flips, rotations, and color jittering were applied.
- **Splitting:** Training (80%) and validation (20%) sets.

---

## Implemented Models

### Simple Neural Network (NN)
- **Input layer:** 32x32x3 (image size)
- **Hidden layers:** Two layers with 128 units each, ReLU activation.
- **Output layer:** 10 units, softmax activation.

### Convolutional Neural Network (CNN)
- **Convolutional Layers:**
  - Layer 1: 32 filters, kernel size 3x3, ReLU activation.
  - Layer 2: 64 filters, kernel size 3x3, ReLU activation.
- **Max-pooling:** Applied after each convolutional layer.
- **Fully Connected Layers:**
  - Layer 1: 128 units, ReLU activation.
  - Layer 2: 10 units, softmax activation.

### ResNet50
- **Architecture:** A deep network with 50 layers using residual connections.
- **Input Layer:** 32x32x3 (image size).
- **Pre-trained Weights:** From ImageNet.
- **Output Layer:** 10 units, softmax activation.

---

## Results

| Model       | Accuracy | Precision | Recall | F1-score | Loss  |
|-------------|----------|-----------|--------|----------|-------|
| NN          | 0.55     | 0.53      | 0.56   | 0.54     | 1.23  |
| CNN         | 0.72     | 0.70      | 0.73   | 0.71     | 0.83  |
| ResNet50    | 0.85     | 0.83      | 0.86   | 0.84     | 0.43  |

---

## Visualizations

- **Training and Validation Accuracy:** Shows accuracy over epochs.
- **Training and Validation Loss:** Tracks model loss during training.
- **Confusion Matrix:** Displays true positives, false positives, and false negatives for each model.

---

## Key Findings

- ResNet50 achieved the highest accuracy but required more computational resources.
- CNN provided a balance between accuracy and efficiency.
- Simple NN showed baseline performance but struggled with complex features.

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/username/cifar10-object-recognition.git
   ```
2. Navigate to the project directory:
   ```bash
   cd cifar10-object-recognition
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the training script:
   ```bash
   python train.py
   ```
5. View results and visualizations:
   - Training logs and metrics will be saved in the `results/` directory.

---

## Future Work

- Explore other architectures such as EfficientNet or Vision Transformers.
- Optimize computational efficiency for ResNet50.
- Experiment with larger datasets like CIFAR-100.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

