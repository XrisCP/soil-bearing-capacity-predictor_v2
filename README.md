# Python Soil Bearing Capacity Predictor
An Artificial Neural Network (ANN) model built in Python (Jupyter Notebook) to predict the bearing capacity of spread footings in soil based on geotechnical parameters. This is another version of the same project in the main repository done in MATLAB.

## 🚀 Project Overview
- **Problem**: Predicting soil bearing capacity is crucial for foundation design in civil engineering. However, accurate predictions of the bearing capacity require full-scale load tests that are usually very expensive, or model foundations plate load tests which are less expensive yet less accurate, or bearing capacity theories which the least expensive at the cost of accuracy.
- **Solution**: Developed a machine learning model (a shallow neural network) using scikit-learn Multilayer Perceptron (MLP) in Python, that takes soil parameters as input and outputs bearing capacity predictions, presenting itself as an optimal solution for the problem: a cheap yet accurate method of bearing capacity predictions.
- **Result**: Model achieved 89% $R^2$ score on test data. Comparative analysis also showed that the model performed better than the traditional bearing capacity theories on the test data.

## 📁 Project Structure
```
soil-bearing-capacity-predictor_v2/
├── BC_Data.csv                                        # Entire Dataset - minimally pre-processed
├── BC_theories.csv                                    # Bearing capacity predictions using traditional bearing capacity theories on test data
├── Bearing_Capacity_Predictor.ipynb                   # Jupyter Notebook outlining model development workflow
├── ann_bc_predictor.joblib                            # Saved trained model using joblib
├── test_set.csv                                       # test dataset in csv format
├── results/                                           # Generated plots and results
│   ├── ann_bc_architecture.png                        # Simplified model architecture
│   ├── error_bar_plot.png                             # bar plot of the errors of the model and bearing capacity theories' predictions on test data
│   ├── predictions_vs_actual.png                      # scatter plot of the model predictions vs actual bearing capacity (i.e. Load Test results)
│   └── r2_bar_plot.png                                # bar plot of R^2 (Coefficient of correlation) for each method
└── README.md                                          # Readme file
```

## 🛠️ Technologies Used
- **Primary Platform**: Jupyter Notebook.
  - Versions: `Python: 3.11.7` | `Jupyter Notebook: 7.4.5`
- **Primary Framework**: `Scikit-learn 1.5.1`

## 📊 Dataset Features
- Input parameters: Foundation width ($m$), Foundation length ($m$), Foundation embedment depth ($m$), Soil effective friction angle (degrees), Average effective unit weight ($kN/m^3$), Soil effective cohesion ($kN/m^2$), Soil effective stress ($kN/m^2$)
- Target variable: Bearing capacity ($kN/m^2$)
- Dataset size: 134 samples
- Data source: from literature

## 🧠 Model Architecture
- **Type:** Feedforward Neural Network
- **Layout:** [Input neurons (7)] - [Hidden layer neurons (10)] - [Output neuron]
- **Solver:** lbfgs
- **Activation Functions:** ReLu
- **Performance Function:** Root Mean Squared Error (RMSE)

## 🚀 Running the Project
1. **Clone this repository**

2. **Open the Jupyter Notebook for model development workflow**
OR
3. **Load the trained main model using `joblib` library for inference**

## 👨‍💻 Author
**Chrispin Emmanuel Phiri**
- Email: x6cemma@gmail.com
- LinkedIn: https://www.linkedin.com/in/chrispin-phiri-07880216a
- GitHub: https://github.com/XrisCP

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
