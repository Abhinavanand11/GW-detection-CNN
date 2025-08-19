# Gravitational Wave Detection with CNN

This repository contains the full pipeline for generating synthetic gravitational wave signals, preprocessing the data, training a CNN model, and evaluating its performance for gravitational wave detection.

---

## 📦 Installation

Clone the repository and install all required dependencies:

```bash
pip install -r requirements.txt
```

## 📂 Repository Structure

### 🔹 Pre-processing

The `Pre-processing/` directory contains scripts for:

- Generating synthetic signals
- Estimating the Power Spectral Density (PSD)
- PSD estimation using Welch's method
- Match filtering
- Frequency cutoffs
- Q-transform visualizations

## 🧠 CNN Model Workflow

### 1. Generate Training & Validation Data
```bash
python gen.py
```

### 2. Train the CNN Model
```bash
python train.py
```

### 3. Generate Test Data
```bash
python generate_data.py
```

### 4. Apply CNN Model to Test Data
```bash
python apply.py
```

## 📊 Model Evaluation

### False Alarm Rate (FAR) & True Alarm Rate (TAR):
```bash
python evaluate.py
```

### Sensitivity Plots (Effective Distance vs FAR / TAR):
```bash
python sensitivity_plot.py
```
These plots show how far (in Mpc) the model can effectively detect gravitational wave signals for a given alarm rate.

### Found vs Missed Events (Bar & Scatter Plots):
```bash
python plot_found_missed.py
```

## 🚀 Main Entry Point

To run the full pipeline and demonstrate the application of all scripts, use:

```bash
python main.py
```

## 📌 Notes

- Ensure all datasets are generated before training/testing.
- Adjust parameters (like frequency cutoffs, segment durations, etc.) in the preprocessing scripts as needed.
