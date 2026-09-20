# Hybrid SGP4 + LSTM Orbit Tracking

A hybrid physics and machine learning model to improve space debris trajectory predictions in Low Earth Orbit (LEO).

## How It Works

Standard SGP4 models handle baseline orbital physics, while an LSTM neural network predicts remaining residual errors. Residuals are converted from the ECI frame to the local RTN (Radial, Along-Track, Cross-Track) frame to isolate drag error along the direction of travel.

# Key Results

. Uncorrected SGP4 3D RMSE: 82.03 km

. Hybrid SGP4 + LSTM 3D RMSE: 0.91 km

. 3D Error Reduction: 98.89%

# Future Work

. Test the pipeline on real space track TLE observation datasets.

. Integrate an Unscented Kalman Filter (UKF) for real-time state estimation.

. Add physics-informed loss penalties for orbital energy conservation.

# Quickstart

pip install -r requirements.txt
Download my notebook (LSTM_training.ipynb) and run it, you can use Google Colab for running the script easily without installing the requirements.txt file.

