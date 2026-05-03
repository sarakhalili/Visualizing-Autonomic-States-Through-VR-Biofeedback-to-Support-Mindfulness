# Visualizing Autonomic States Through VR Biofeedback to Support Mindfulness

This repository contains the code used for the paper:

**Designing VR for Chronic Pain: Visualizing Autonomic States Through VR Biofeedback to Support Mindfulness**

The project evaluates a machine learning-based physiological inference pipeline for the *Virtual Meditative Walk* (VMW), a closed-loop virtual reality biofeedback environment designed to support mindfulness-based chronic pain management. The goal is to improve the physiological control signal used for adaptive environmental feedback by moving beyond the original skin conductance slope-based rule and using Electrodermal Activity (EDA) and Heart Rate Variability (HRV) features.

The code supports analysis using the combined WESAD and StressID datasets, including preprocessing, feature extraction, model benchmarking, final Extra Trees evaluation, leave-one-subject-out validation, model interpretation, and latency analysis.

## Project Overview

The original VMW system used a simple skin conductance slope-based feedback mechanism to adapt fog density in the virtual environment. This was easy to implement and interpret, but it relied on a single signal trend. In this work, we evaluate whether a multivariate physiological inference pipeline using EDA and HRV features can provide a more reliable and expressive control signal for adaptive VR biofeedback.

The repository includes code for:

- preprocessing EDA and ECG-derived HRV signals;
- extracting statistical, nonlinear, and domain-specific physiological features;
- preparing binary and multiclass stress-related classification targets;
- benchmarking multiple machine learning models;
- evaluating the final Extra Trees models under cross-sample and leave-one-subject-out validation;
- comparing the machine learning model with the original SCL slope-based VMW feedback rule;
- generating confusion matrices, ROC curves, precision-recall curves, calibration plots, SHAP feature-importance plots, and t-SNE visualizations;
- estimating model-level inference latency for real-time VR integration.

## Repository Structure

```text
.
├── data/                       # Placeholder only; raw datasets are not included
├── figures/                    # Generated figures used in the paper
├── notebooks/                  # Analysis notebooks
├── src/                        # Reusable scripts and helper functions
├── outputs/                    # Model outputs, metrics, and intermediate results
├── requirements.txt            # Python dependencies
└── README.md
