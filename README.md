# Continuous Authentication Using Gait Patterns

This repository implements a continuous user authentication system using gait patterns captured from motion sensors (accelerometer and gyroscope). Unlike traditional password-based or one-time authentication, this approach enables ongoing verification of a user’s identity while they interact with a system, improving security and resilience against impersonation attacks.

This project is based on the work published in:

Aparna J. Nair, B. Premjith, Diksha Shukla, K. P. Soman.  
*Continuous Authentication Using Gait Patterns*.  
Proceedings of the 2nd International Conference on Signal and Data Processing, Springer Nature Singapore, 2023, pp. 447–459.  
DOI: [10.1007/978-981-99-1410-4_37](https://doi.org/10.1007/978-981-99-1410-4_37)


### Motivation

- Passwords and PINs are vulnerable to theft and shoulder-surfing attacks.

- Video-based gait authentication is prone to imitation and privacy concerns.

- IMU-based (Inertial Measurement Unit) gait authentication provides a lightweight, privacy-preserving, and continuous security mechanism.

### Features

- Collection of gait data from accelerometer and gyroscope sensors.

- Extraction of statistical features (time-domain and frequency-domain).

- Feature selection to minimize redundancy and correlation.

- Two modeling strategies:

    - One-Class Classification – handles class imbalance by training only on the genuine user.

    - Balanced Binary Classification – balances genuine and impostor data using sampling.

- Evaluation metrics: Equal Error Rate (EER), accuracy, and per-user performance.

### Dataset

- Data collected from 15 users using mobile/wearable IMU sensors.

- Each instance includes accelerometer and gyroscope readings.

- Dataset preprocessed into fixed-size gait windows for training/testing.

### Models

- Support Vector Machines (SVM) – best performing in balanced binary classification.

- Other classifiers: Decision Trees, Random Forests, Logistic Regression.

- Models trained in a per-user one-vs-rest setup.

### Results

- Balanced classification with SVM achieved the lowest Equal Error Rate (EER).

- System is lightweight, fast, and resistant to video-based spoofing.

- Demonstrates the feasibility of continuous gait-based authentication in real-world settings.

## Citation

If you use this work, please cite:

```bibtex
@inproceedings{nair2023gait,
  title={Continuous Authentication Using Gait Patterns},
  author={Nair, Aparna J and Premjith, B and Shukla, Diksha and Soman, KP},
  booktitle={Proceedings of the 2nd International Conference on Signal and Data Processing},
  pages={447--459},
  year={2023},
  publisher={Springer Nature Singapore},
  doi={10.1007/978-981-99-1410-4_37},
  isbn={978-981-99-1410-4}
}
