# Multi-Task Used Car Price Prediction

A deep learning project that uses the **Keras Functional API** to simultaneously:

- Predict the price of a used car (Regression)
- Classify the car into Low, Medium, or High price tiers (Classification)

The model uses separate numerical and categorical input branches, categorical embeddings, shared layers, and two output heads.

The complete implementation, EDA, preprocessing, experiments, visualizations, model architecture, and findings are available in the notebook.

## Dataset

Used-car dataset containing vehicle specifications, location, seller information, condition, and price.

**Source:** [Kaggle Dataset]((https://www.kaggle.com/datasets/taeefnajib/bikroy-car-price-prediction))

## Key Concepts

- Keras Functional API
- Multi-Input Neural Network
- Multi-Output Neural Network
- Categorical Embeddings
- Multi-Task Learning
- Regression + Multiclass Classification
- Loss Weight Optimization
- Early Stopping
- Learning Rate Scheduling

## Models Compared

### Price Prediction
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Multi-Task ANN

### Price Tier Classification
- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier
- Multi-Task ANN

## Final Results

| Model | Task | MAE | RMSE | R² | Accuracy | Macro F1 |
|---|---|---:|---:|---:|---:|---:|
| Linear Regression | Price | 0.21 | 0.56 | 0.60 | - | - |
| Random Forest | Price | 0.17 | 0.39 | 0.81 | - | - |
| Gradient Boosting | Price | **0.13** | **0.30** | **0.88** | - | - |
| Logistic Regression | Tier | - | - | - | 0.854 | 0.854 |
| Random Forest | Tier | - | - | - | 0.889 | 0.889 |
| Gradient Boosting | Tier | - | - | - | **0.895** | **0.895** |
| **Multi-Task ANN** | Both | 0.15 | 0.44 | 0.75 | 0.850 | 0.850 |

The Gradient Boosting models achieved the best individual task performance, while the Multi-Task ANN successfully handled both regression and classification simultaneously within a single architecture.

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras
- Jupyter Notebook
- Kaggle

## Notebook

The complete project is available here:

[`used_car_multitask.ipynb`](./used_car_multitask.ipynb)

## How to Run

1. Download or clone this repository.
2. Download the dataset from the Kaggle source.
3. Open `used_car_multitask.ipynb`.
4. Update the dataset path if required.
5. Run the notebook from top to bottom.

## Author

**Saurabh Kumar**
