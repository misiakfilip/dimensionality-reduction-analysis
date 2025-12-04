# Dimensionality Reduction Analysis

A comprehensive comparative study of dimensionality reduction techniques (PCA, Kernel PCA) applied to spam email classification using the Spambase dataset from UCI Machine Learning Repository.

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Methods Implemented](#methods-implemented)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## 🎯 Overview

This project investigates the impact of various dimensionality reduction methods on prediction quality in machine learning tasks. The analysis compares baseline models (using all features) against PCA and Kernel PCA variants with different hyperparameters.

The study aims to answer:
- Does dimensionality reduction improve prediction quality?
- How does the number of components affect accuracy and training time?
- Which methods are most suitable for spam classification?

## ✨ Features

- **Comprehensive EDA**: Exploratory data analysis with visualizations
- **Multiple Methods**: PCA, Kernel PCA (RBF and Linear kernels)
- **Extensive Testing**: 20+ model configurations tested
- **Performance Metrics**: Accuracy, cross-validation, training time
- **Rich Visualizations**: Correlation matrices, scree plots, confusion matrices, comparative charts
- **Reproducible Pipeline**: All preprocessing steps in sklearn pipelines
- **Modular Code**: Reusable functions for repeated operations

## 📊 Dataset

**Spambase Dataset** from UCI Machine Learning Repository
- **Instances**: 4,601 emails
- **Features**: 57 numerical attributes
  - Word frequency features (48)
  - Character frequency features (6)
  - Capital letter statistics (3)
- **Target**: Binary classification (spam/not spam)
- **Class Distribution**: 39.4% spam, 60.6% legitimate emails

The dataset contains frequency information about specific words and characters in emails, along with statistics about capital letter usage.

## 🔬 Methods Implemented

### 1. Baseline Model
- StandardScaler + Logistic Regression
- All 57 features retained
- Serves as performance benchmark

### 2. Principal Component Analysis (PCA)
- Tested configurations: 2, 5, 10, and components for 90%, 95%, 99% variance
- Variance analysis with scree plots
- 2D visualization of principal components

### 3. Kernel PCA - RBF (Gaussian)
- Non-linear dimensionality reduction
- Tested gamma values: 0.001, 0.01, 0.1
- Tested n_components: 2, 5, 10

### 4. Kernel PCA - Linear
- Linear kernel for comparison with standard PCA
- Tested n_components: 2, 5, 10

## 📂 Project Structure

```
dimensionality-reduction-analysis/
│
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
├── LICENSE                            # MIT License
├── .gitignore                        # Git ignore file
│
├── notebooks/
│   └── dimensionality_reduction_analysis.ipynb   # Main Jupyter notebook
│
├── src/
    └── dimensionality_reduction.py   # Python script version

```

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/misiakfilip/dimensionality-reduction-analysis.git
cd dimensionality-reduction-analysis
```

2. **Create virtual environment (recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

## 💻 Usage

### Option 1: Jupyter Notebook (Recommended)

```bash
jupyter notebook notebooks/dimensionality_reduction_analysis.ipynb
```

Run all cells to:
- Download and explore the Spambase dataset
- Train all models
- Generate visualizations
- Compare results

### Option 2: Python Script

```bash
cd src
python dimensionality_reduction.py
```

## 📊 Visualizations

The project generates comprehensive visualizations:

1. **Feature Distributions**: Histograms of 5 random features
2. **Correlation Matrix**: Heatmap showing feature correlations
3. **Confusion Matrix**: Classification performance visualization
4. **Scree Plot**: Explained variance by component
5. **Cumulative Variance**: Variance accumulation curve
6. **2D PCA Projection**: Data visualization in 2D space
7. **Method Comparison**: Bar chart of test accuracies
8. **Components vs Accuracy**: Line plots for different methods
9. **Accuracy vs Training Time**: Trade-off visualization

## 📦 Requirements

```
numpy>=1.24.0
pandas>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
scikit-learn>=1.3.0
jupyter>=1.0.0
ucimlrepo>=0.0.3
```

See `requirements.txt` for complete list with versions.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions

- Add more dimensionality reduction methods (t-SNE, UMAP, Factor Analysis)
- Test on additional datasets
- Implement feature selection methods for comparison
- Add interactive visualizations (Plotly)
- Optimize hyperparameter tuning with GridSearchCV
- Add unit tests

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Filip Misiak**
- GitHub: [@misiakfilip](https://github.com/misiakfilip)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- Email: filip.misiak11@example.com

## 🙏 Acknowledgments

- UCI Machine Learning Repository for the Spambase dataset
- scikit-learn community for excellent documentation
- Course instructors and peers for valuable feedback

## 📚 References

1. UCI Machine Learning Repository - Spambase Dataset
2. Hastie, T., Tibshirani, R., & Friedman, J. (2009). The Elements of Statistical Learning
3. Scikit-learn Documentation: https://scikit-learn.org/
4. Jolliffe, I. T. (2002). Principal Component Analysis

## 📝 Citation

If you use this project in your research, please cite:

```bibtex
@misc{dimensionality_reduction_2025,
  author = {Filip Misiak},
  title = {Dimensionality Reduction Analysis for Spam Classification},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/misiakfilip/dimensionality-reduction-analysis}
}
```

---

⭐ **If you find this project useful, please consider giving it a star!** ⭐

*Last updated: December 2025*
