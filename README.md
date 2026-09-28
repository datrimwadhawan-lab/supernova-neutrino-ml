# Machine Learning Classification of Supernova Neutrinos

Machine-learning study of simulated supernova-neutrino interactions in liquid-argon time projection chambers (LArTPCs), investigating how detector noise affects event classification.

Developed as part of the Practical Machine Learning for Physicists module at University College London.

Grade: 85%

## Overview

Supernova neutrinos produce low-energy, sparse signals in liquid-argon detectors, making genuine interactions difficult to distinguish from detector backgrounds.

This project investigates how different machine-learning architectures perform as detector noise increases.

The models considered include:

- Logistic Regression
- Dense Neural Networks
- Convolutional Neural Networks (CNNs)
- Inception-style CNNs
- Residual CNNs

Electronic detector noise was simulated using Gaussian fluctuations at varying noise levels. Localised Gaussian backgrounds were also investigated as a simplified model of radioactive backgrounds.

## Key Results

- Logistic regression and dense neural networks achieved near-perfect classification on clean data but degraded rapidly as electronic noise increased.
- A baseline CNN achieved 96.2% accuracy at a noise level of σ = 5.
- An Inception-style CNN improved robustness at intermediate noise levels, achieving 75.1% accuracy at σ = 10.
- At sufficiently high electronic noise, all architectures approached random classification.
- Localised Gaussian backgrounds had significantly less impact, with classification accuracy typically remaining above 98%.

The results suggest that classification performance is ultimately limited by signal-to-noise ratio rather than model complexity alone.

## Methodology

Simulated LArTPC images of supernova-neutrino interactions were treated as signal events.

Background datasets were generated using simulated detector noise, and models were trained to perform binary classification between neutrino interactions and background.

Performance was evaluated using:

- Accuracy
- False Positive Rate
- False Negative Rate
- Confusion matrices

CNN architectures were used to investigate whether spatial information in the detector images improved classification robustness.

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

## Repository Structure

`notebooks/` — Complete analysis and model development  
`figures/` — Selected figures and model-performance results  
`report/` — Full project report

## Author

Datrim Wadhawan  
MSci Physics, University College London
