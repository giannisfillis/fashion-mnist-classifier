# Machine Learning - Academic Year 2023-2024

[![Course](https://img.shields.io/badge/Course-Machine_Learning-blue.svg)]()
[![Institution](https://img.shields.io/badge/Institution-University_of_Ioannina-red.svg)]()
[![Language](https://img.shields.io/badge/Language-Python%20/%20Jupyter-orange.svg)]()

This repository contains the laboratory assignments and project reports for the Machine Learning course at the University of Ioannina, Department of Computer Science & Engineering. 

The projects focus on supervised learning (classification) using the Fashion MNIST dataset. The implementations showcase a progression from traditional machine learning algorithms to deep neural networks.

**Team Members:**
* Giannis Fillis, AM: 5380

---

## 📖 Table of Contents
1. [Project 1: Data Classification (Traditional ML & CNNs)](#project-1-data-classification-traditional-ml--cnns)
2. [Setup and Execution](#setup-and-execution)

---

## 🧠 Project 1: Data Classification (Traditional ML & CNNs)

### Overview
The first assignment explores various classification models on image data. It is divided into two main parts: evaluating traditional machine learning models on flattened, dimensionality-reduced data, and training deep learning architectures directly on the 2D image matrices.

### Dataset
* **Fashion MNIST**: A dataset comprising 28x28 grayscale images of 10 different clothing categories.
* **Splits**: 60,000 images for the training set and 10,000 for the testing set.
* Data was normalized prior to model training.

### Implementation Details
**Part A: Vector Representation (1D)**
* Applied a 4x4 Max Pooling window to reduce the initial 784-dimensional vectors to 49 dimensions.
* **Models Implemented:**
  * **K-Nearest Neighbors (KNN):** Tested with K=1, 3, and 5 using Euclidean distance.
  * **Tree-based Models:** Decision Tree (max depth = 10) and Random Forest (100 estimators).
  * **Support Vector Machines (SVM):** Linear SVM and RBF Kernel SVM tested across various hyperparameters (C={1, 10, 100}, gamma={0.02, 0.1, 1}).
  * **Multilayer Perceptron (MLP):** A Feed-Forward Neural Network with 3 hidden layers (100, 100, and 50 neurons), Leaky ReLU activations, Adam optimizer, and MSE loss. 

**Part B: Image Representation (2D)**
* **Convolutional Neural Network (CNN):** * Architecture: Three consecutive 2D convolutional layers (3x3 kernels), followed by 2x2 Max Pooling, a fully connected layer (100 neurons) with Dropout ($\alpha=0.3$), and a Softmax output layer.
  * Optimization: Categorical cross-entropy loss, trained over 100 epochs with a batch size of 50.
  * Evaluated the impact of varying the number of filters per layer.

---

## 🚀 Setup and Execution

The project is implemented in Python using Jupyter Notebooks. To run the code, ensure you have a standard data science environment installed (e.g., Anaconda) with the necessary deep learning frameworks.

### Prerequisites
* Python 3.x
* Jupyter Notebook
* Required Libraries: `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `tensorflow` / `keras`.

### Running the Notebooks
1. Clone this repository to your local machine.
2. Navigate to the respective project directory.
3. Launch Jupyter Notebook via terminal:
   `jupyter notebook`
4. Open `Assignment1.ipynb` and execute the cells sequentially. All necessary comments and analysis reports are included directly within the notebook markdown cells.
