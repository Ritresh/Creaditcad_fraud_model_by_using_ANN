# 💳 Credit Card Fraud Detection using Artificial Neural Network (ANN)

_A machine learning project that detects fraudulent credit card transactions using an Artificial Neural Network (ANN). The system analyzes transaction features to classify whether a transaction is fraudulent or legitimate, helping financial institutions detect fraud and reduce financial losses._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#problem-statement">Problem-Statement</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning">Data Cleaning</a>
- <a href="#data-preprocessing">Data Preprocessing</a>
- <a href="#handling-imbalanced-data">Handling Imbalanced Data</a>
- <a href="#model-building">Model Building</a>
- <a href="#model-training">Model Training</a>
- <a href="#model-evaluation">Model Evaluation</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#future-improvements">Future Improvements</a>
- <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

Credit card fraud is a major challenge for financial institutions. Fraudulent transactions can cause significant financial losses and damage customer trust.

This project builds a **Credit Card Fraud Detection system using an Artificial Neural Network (ANN)**. The model learns patterns from historical transaction data and predicts whether a transaction is **fraudulent** or **legitimate**.

The system uses machine learning techniques such as:

- Data preprocessing
- Feature scaling
- Handling class imbalance
- Artificial Neural Networks (ANN)

The goal is to build a predictive model that can help detect fraudulent transactions effectively.

---

<h2><a class="anchor" id="problem-statement"></a>Problem-Statement</h2>

Credit card transactions are highly imbalanced because fraudulent transactions are very rare compared to normal transactions.

The goal of this project is to:

- Detect fraudulent credit card transactions.
- Handle highly imbalanced datasets.
- Build a neural network model to classify transactions.
- Train and evaluate the model using validation and test datasets.

This helps financial institutions **identify fraud early and minimize financial losses**.

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

The project uses the **Credit Card Fraud Detection Dataset**, which contains anonymized transaction data.

Dataset features include:

- V1 to V28 (anonymized features)
- Amount (transaction amount)
- Time (seconds elapsed between transactions)
- Class (target variable)

Target variable:

- **0 → Normal Transaction**
- **1 → Fraudulent Transaction**

Dataset location:

```
dataset/raw/creditcard.csv
```

The dataset is highly imbalanced, meaning fraud cases are much fewer compared to legitimate transactions.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

Programming & Libraries
- Python
- Pandas
- NumPy

Data Visualization
- Matplotlib
- Seaborn

Machine Learning / Deep Learning
- TensorFlow
- Keras
- Artificial Neural Network (ANN)

Preprocessing
- StandardScaler
- Train-Test Split
- Class Weight Balancing

Development Environment
- Jupyter Notebook (VS Code Jupyter Extension)

Version Control
- Git
- GitHub

---

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
fraud/
│
├── dataset/
│   └── raw/
│       └── creditcard.csv
│
├── notebook/
│   └── fraud_by_ANN.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

<h2><a class="anchor" id="data-cleaning"></a>Data Cleaning</h2>

Several data cleaning steps are applied to ensure dataset quality.

Key steps include:

1. Checking Missing Values
   - Verify whether any null values exist in the dataset.

2. Removing Duplicate Transactions
   - Duplicate rows are removed to avoid bias in training.

3. Removing Unnecessary Columns
   - The **Time** column is removed because it does not significantly contribute to fraud detection.

These steps ensure the dataset is clean and ready for modeling.

---

<h2><a class="anchor" id="data-preprocessing"></a>Data Preprocessing</h2>

Feature preprocessing is applied before training the neural network.

Scaling Transaction Amount

The **Amount** column is scaled using **StandardScaler** to normalize the data.

Example:

```
Amount_scaled = StandardScaler()
```

Feature and Target Separation

Features (X) → All columns except **Class**  
Target (y) → **Class**

---

<h2><a class="anchor" id="handling-imbalanced-data"></a>Handling Imbalanced Data</h2>

Fraud detection datasets are highly imbalanced.

To address this issue, **class weights** are calculated using:

```
compute_class_weight()
```

Class weights ensure that the model gives more importance to the minority class (fraud cases) during training.

---

<h2><a class="anchor" id="model-building"></a>Model Building</h2>

An **Artificial Neural Network (ANN)** is built using TensorFlow and Keras.

Network architecture:

Input Layer  
↓  
Dense Layer (32 neurons, ReLU)  
↓  
Dense Layer (16 neurons, ReLU)  
↓  
Dense Layer (8 neurons, ReLU)  
↓  
Output Layer (1 neuron, Sigmoid)

Activation functions used:

- ReLU for hidden layers
- Sigmoid for binary classification output

Loss function:

- Binary Crossentropy

Optimizer:

- Adam

---

<h2><a class="anchor" id="model-training"></a>Model Training</h2>

The dataset is divided into three parts:

Training Set  
Validation Set  
Test Set

Training configuration:

- Epochs: 10
- Batch Size: 256
- Class weights applied to handle imbalance

During training, the model learns patterns that distinguish fraudulent transactions from legitimate ones.

---

<h2><a class="anchor" id="model-evaluation"></a>Model Evaluation</h2>

The trained model is evaluated using the test dataset.

Evaluation metrics include:

- Accuracy
- Training vs Validation Accuracy
- Training vs Validation Loss

Training performance is visualized using:

- Accuracy curves
- Loss curves

These plots help analyze whether the model is learning properly or overfitting.

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:

```bash
git clone https://github.com/yourusername/fraud-detection-ann.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```
notebook/fraud_by_ANN.ipynb
```

4. Run the notebook cells to:

- Load and clean the dataset
- Preprocess features
- Train the ANN model
- Evaluate model performance

---

<h2><a class="anchor" id="future-improvements"></a>Future Improvements</h2>

- Apply advanced deep learning models
- Add precision, recall, and F1-score evaluation
- Deploy the model using a web application
- Implement real-time fraud detection systems

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Ritresh Kumar**  
BCA Student | Aspiring Data Scientist

Skills:
- Python
- Machine Learning
- Deep Learning
- Data Analysis
- Neural Networks

📧 Email: ritresh273@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/feed/)  
🔗 [GitHub](https://github.com/Ritresh/Ritresh)
