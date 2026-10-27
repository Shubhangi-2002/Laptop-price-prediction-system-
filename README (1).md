# Laptop Price Prediction System

A machine-learning web application that estimates laptop prices from
selected specifications such as brand, laptop type, RAM, weight, and
other hardware features. The app provides an interactive interface built
with **Streamlit** and uses a trained regression pipeline to generate
predictions.

## Project Overview

Laptop prices vary based on brand, performance, memory, storage, and
device specifications. This project demonstrates an end-to-end
machine-learning workflow: preparing laptop data, training a regression
model, saving the trained artifacts, and serving predictions through a
web interface.

## Features

-   Interactive laptop-price prediction interface
-   Brand and laptop-type selection
-   Hardware specification inputs, including RAM and weight
-   Machine-learning regression pipeline for price estimation
-   Data processing and model-training notebook
-   Streamlit-based web application

## Technology Stack

-   **Language:** Python
-   **Web app:** Streamlit
-   **Machine learning:** scikit-learn
-   **Data processing:** Pandas, NumPy
-   **Model/artifact storage:** Pickle
-   **Exploration and experimentation:** Jupyter Notebook

## Repository Structure

``` text
Laptop-price-prediction-system/
├── app.py                         # Streamlit application
├── df.pkl                         # Saved data artifact used by the app
├── pipe.pkl                       # Trained prediction pipeline
├── laptop_data.csv                # Laptop dataset
├── laptop-price-predictor.ipynb   # Data analysis and model development
├── requirements.txt               # Python dependencies
├── setup.sh                       # Setup script (if applicable)
├── Profile                        # Project/profile file
└── README.md                      # Project documentation
```

> The application expects `app.py`, `pipe.pkl`, and `df.pkl` to be
> available at the paths referenced in the code. Keep these files in the
> project directory unless you update the paths.

## Getting Started

### 1. Clone the repository

``` bash
git clone https://github.com/Shubhangi-2002/Laptop-price-prediction-system-.git
cd Laptop-price-prediction-system-
```

### 2. Create and activate a virtual environment (recommended)

**Windows**

``` bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**

``` bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

``` bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If the repository's `requirements.txt` is incomplete, install the main
packages:

``` bash
pip install streamlit pandas numpy scikit-learn
```

Use compatible package versions for the environment in which `pipe.pkl`
was trained. Pickled scikit-learn models may not load correctly across
incompatible scikit-learn versions.

### 4. Run the application

From the project directory, run:

``` bash
streamlit run app.py
```

Streamlit will print a local URL in the terminal, usually
`http://localhost:8501`. Open that URL in your browser.

## How to Use

1.  Start the Streamlit app.
2.  Select a laptop brand and type.
3.  Enter the available hardware specifications.
4.  Submit the inputs using the prediction control in the app.
5.  Review the estimated laptop price.

The available inputs and the prediction button depend on the
implementation in `app.py`.

## Machine-Learning Workflow

1.  **Data preparation:** Load and inspect the laptop dataset.
2.  **Feature engineering:** Prepare laptop specifications for
    modelling.
3.  **Model training:** Train a regression model or pipeline on the
    prepared data.
4.  **Model persistence:** Save the trained pipeline as `pipe.pkl`.
5.  **Web deployment:** Load the pipeline in Streamlit and use it to
    estimate prices from user inputs.

The repository includes a Jupyter notebook for exploring the dataset and
developing the model.

## Model Performance

The repository's original project description reports **88% accuracy**.
For regression, the meaning of "accuracy" should be clarified with the
actual evaluation metric (for example, R² score, MAE, or RMSE). Re-run
the notebook and document the evaluation method and test-set results
before treating this figure as a verified performance result.

## Troubleshooting

-   **`FileNotFoundError` for `pipe.pkl` or `df.pkl`:** Check that both
    files are in the project directory and that the paths in `app.py`
    match their locations.
-   **`ModuleNotFoundError`:** Activate the intended virtual environment
    and install the dependencies.
-   **Model-loading or scikit-learn errors:** Use compatible versions of
    the libraries used when the pickle files were created.
-   **Streamlit command not found:** Run
    `python -m pip install streamlit`, then start the app with
    `python -m streamlit run app.py`.
-   **Input feature-name warning:** Ensure prediction inputs use the
    same feature names and preprocessing expected by the trained
    pipeline. Review the notebook and pipeline construction to correct
    any mismatch.

## Future Improvements

-   Display a clear currency format and prediction summary
-   Add input validation and helpful error messages
-   Evaluate the model using R², MAE, and RMSE on a held-out test set
-   Add visualizations for price trends by brand, RAM, and laptop type
-   Improve responsive layout and accessibility
-   Deploy the app to a suitable hosting platform

## Limitations

-   Predictions depend on the dataset and the specifications represented
    in the training data.
-   Estimated prices may not reflect current retail prices or discounts.
-   Model quality depends on the data, feature processing, and
    evaluation method.
-   Do not use the model output as a guaranteed market price.

## Author

**Shubhangi Gaud**

GitHub: [Shubhangi-2002](https://github.com/Shubhangi-2002)

## License

No license is specified in this repository. Unless a license is added,
reuse and redistribution are subject to the repository owner's rights.
Add a `LICENSE` file if you want to define permissions for others to
use, modify, or distribute this project.
