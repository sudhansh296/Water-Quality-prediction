# 🌊 Water Quality Prediction Using Machine Learning

A comprehensive machine learning project that predicts water quality and potability using various physicochemical parameters. This system helps in early detection of unsafe water and provides meaningful insights for water resource management.

## 🎯 Project Overview

This project focuses on developing an intelligent water quality assessment system using machine learning algorithms to predict the Water Quality Index (WQI) and determine water potability. The system analyzes multiple water parameters to classify whether water is safe for consumption.

## 🔬 Features

- **Multi-Parameter Analysis**: Evaluates pH, turbidity, temperature, dissolved oxygen, and other key parameters
- **Machine Learning Models**: Implements various ML algorithms for accurate predictions
- **Water Quality Index (WQI)**: Calculates comprehensive water quality scores
- **Potability Classification**: Determines if water is safe for drinking
- **Data Visualization**: Interactive charts and graphs for better insights
- **Real-time Prediction**: Fast and accurate water quality assessment

## 🛠️ Tech Stack

### Machine Learning & Data Science
- **Python 3.8+**
- **Scikit-learn** - Machine learning algorithms
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib/Seaborn** - Data visualization
- **Jupyter Notebook** - Interactive development

### Algorithms Used
- **Random Forest Regression** - Primary prediction model
- **Support Vector Machine (SVM)** - Classification tasks
- **Neural Networks** - Deep learning approach
- **XGBoost** - Gradient boosting for enhanced accuracy
- **Linear Regression** - Baseline model

## 📊 Dataset Features

The model analyzes the following water quality parameters:

| Parameter | Description | Unit |
|-----------|-------------|------|
| **pH** | Acidity/Alkalinity level | pH scale (0-14) |
| **Hardness** | Mineral content | mg/L |
| **Solids** | Total dissolved solids | ppm |
| **Chloramines** | Disinfectant level | ppm |
| **Sulfate** | Sulfate concentration | mg/L |
| **Conductivity** | Electrical conductivity | μS/cm |
| **Organic Carbon** | Total organic carbon | ppm |
| **Trihalomethanes** | Chemical compounds | μg/L |
| **Turbidity** | Water clarity | NTU |
| **Potability** | Safe for drinking | 0/1 (Target) |

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sudhansh296/Water-Quality-prediction.git
   cd Water-Quality-prediction
   ```

2. **Create virtual environment**
   ```bash
   python -m venv water_quality_env
   source water_quality_env/bin/activate  # On Windows: water_quality_env\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Run the main notebook**
   Open `Water_Quality_Prediction.ipynb` and run all cells

## 📁 Project Structure

```
Water-Quality-prediction/
├── data/
│   ├── water_potability.csv          # Main dataset
│   ├── processed_data.csv            # Cleaned dataset
│   └── sample_predictions.csv        # Sample outputs
├── notebooks/
│   ├── Water_Quality_Prediction.ipynb    # Main analysis notebook
│   ├── Data_Exploration.ipynb            # EDA notebook
│   └── Model_Comparison.ipynb            # Model evaluation
├── src/
│   ├── data_preprocessing.py         # Data cleaning functions
│   ├── feature_engineering.py       # Feature creation
│   ├── model_training.py            # ML model training
│   ├── prediction.py                # Prediction functions
│   └── visualization.py             # Plotting utilities
├── models/
│   ├── random_forest_model.pkl      # Trained RF model
│   ├── svm_model.pkl               # Trained SVM model
│   └── scaler.pkl                  # Feature scaler
├── results/
│   ├── model_performance.png        # Performance metrics
│   ├── feature_importance.png       # Feature analysis
│   └── confusion_matrix.png         # Classification results
├── requirements.txt                 # Python dependencies
├── README.md                       # Project documentation
└── app.py                         # Streamlit web app (optional)
```

## 🔍 Model Performance

### Accuracy Metrics
- **Random Forest**: 85.2% accuracy
- **SVM**: 82.7% accuracy
- **Neural Network**: 84.1% accuracy
- **XGBoost**: 86.3% accuracy

### Key Performance Indicators
- **Precision**: 0.84
- **Recall**: 0.82
- **F1-Score**: 0.83
- **ROC-AUC**: 0.89

## 📈 Data Analysis Insights

### Feature Importance
1. **pH Level** (23.5%) - Most critical factor
2. **Sulfate** (18.2%) - High impact on potability
3. **Conductivity** (15.7%) - Electrical properties
4. **Hardness** (12.4%) - Mineral content
5. **Chloramines** (10.8%) - Disinfection levels

### Water Quality Patterns
- pH range 6.5-8.5 indicates good water quality
- High sulfate levels (>400 mg/L) reduce potability
- Turbidity above 4 NTU suggests contamination
- Optimal conductivity range: 200-800 μS/cm

## 🎯 Usage Examples

### Basic Prediction
```python
import pandas as pd
from src.prediction import predict_water_quality

# Load your water sample data
sample_data = {
    'ph': 7.2,
    'Hardness': 180.5,
    'Solids': 15000,
    'Chloramines': 7.8,
    'Sulfate': 250.3,
    'Conductivity': 450.2,
    'Organic_carbon': 12.5,
    'Trihalomethanes': 65.8,
    'Turbidity': 3.2
}

# Make prediction
result = predict_water_quality(sample_data)
print(f"Water Quality: {'Safe' if result == 1 else 'Unsafe'}")
```

### Batch Processing
```python
# Process multiple samples
df = pd.read_csv('water_samples.csv')
predictions = model.predict(df)
df['Potability'] = predictions
df.to_csv('results.csv', index=False)
```

## 🌐 Web Application

Optional Streamlit web interface for easy predictions:

```bash
streamlit run app.py
```

Features:
- Interactive parameter input
- Real-time predictions
- Visualization dashboard
- Export results

## 📊 Visualizations

The project includes comprehensive visualizations:

- **Correlation Heatmap** - Parameter relationships
- **Distribution Plots** - Data distribution analysis
- **Feature Importance** - Model interpretability
- **ROC Curves** - Model performance
- **Confusion Matrix** - Classification accuracy

## 🔬 Research Applications

This project can be applied to:

- **Municipal Water Systems** - Public water quality monitoring
- **Industrial Applications** - Process water assessment
- **Environmental Studies** - Water pollution research
- **Health Monitoring** - Drinking water safety
- **Agricultural Use** - Irrigation water quality

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Sudhanshu Kumar**
- GitHub: [@sudhansh296](https://github.com/sudhansh296)
- Portfolio: [https://portfolio-sand-delta-56anb24ojn.vercel.app/](https://portfolio-sand-delta-56anb24ojn.vercel.app/)
- LinkedIn: [Connect with me](https://linkedin.com/in/sudhansh296)

## 🙏 Acknowledgments

- Water quality dataset providers
- Scikit-learn community
- Environmental research papers
- Open source contributors

## 📚 References

- [WHO Water Quality Guidelines](https://www.who.int/publications/i/item/9789241549950)
- [EPA Water Quality Standards](https://www.epa.gov/standards-water-body-health)
- [Machine Learning for Environmental Science](https://www.nature.com/articles/s41598-025-23775-5)

---

⭐ **Star this repository if you found it helpful!**

🌊 **Contributing to water safety through data science and machine learning**

📧 **Questions?** Feel free to open an issue or contact me directly.