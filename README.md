# Advanced Multi-Modal Sensor Fusion System for Detecting Falling Humans 

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Journal: Vehicles](https://img.shields.io/badge/Journal-Vehicles-blue.svg)](https://doi.org/10.3390/vehicles7040149)
[![Affiliation: SUMS](https://img.shields.io/badge/Affiliation-Shiga_University_of_Medical_Science-red.svg)](https://www.shiga-med.ac.jp/english)

### Quantitative Evaluation for Enhanced Vehicle Safety

This repository contains the software framework and quantitative evaluation for the **Advanced Falling Object Detection System (AFODS)**, as published in *Vehicles* (2025). 

AFODS is designed to enhance vehicle safety by detecting and predicting human falls in real-time using a novel multi-modal sensor fusion approach.

---

## 📌 Abstract
Collisions with fallen pedestrians pose a lethal challenge to current ADAS (Advanced Driver Assistance Systems). This project introduces a safety framework that architecturally integrates **Long-Wave Infrared (LWIR)**, **Near-Infrared (NIR) Stereo**, and **Ultrasonic sensors**. The system utilizes a custom AI pipeline combining **YOLOv7-Tiny** for real-time detection and a **Recurrent Neural Network (RNN)** for proactive threat assessment.



## 🛠 System Architecture
* **Sensors:** LWIR Thermal Imaging, NIR Stereo Vision, and Ultrasonic Transducers.
* **Detection Backbone:** YOLOv7-Tiny optimized for edge-case pedestrian postures (prone/falling).
* **Threat Assessment:** RNN-based predictive modeling to assess fall dynamics and collision probability.
* **Innovation:** Includes an architectural "Hypothermia Detection Mode" via thermal variance analysis between the subject and ambient environment.

## 🧮 Mathematical Logic: Multi-Modal Fusion
The AFODS framework employs a Weighted Fusion of Thermal (LWIR) and Stereo (NIR) signals to calculate a **Collision Threat Index (CTI)**.

### 1. Weighted Detection Probability
The combined detection probability $P_d$ is adjusted dynamically based on environmental temperature variance:
$$P_d = w_{LWIR} \cdot C_{thermal} + w_{NIR} \cdot C_{visual}$$
where $w$ represents the confidence weight and $C$ represents the classifier's confidence score. In low-visibility or thermal-heavy environments, weights are redistributed to maintain system integrity.

### 2. Fall Velocity Estimation
Using NIR stereo disparity, the system calculates the vertical velocity component ($V_z$) to distinguish a fall from standard pedestrian motion:
$$V_z = \frac{\Delta d}{\Delta t} \cdot \frac{B \cdot f}{Z^2}$$
*(where $B$ is the baseline and $f$ is the focal length of the NIR stereo pair).*

---

## 📊 Quantitative Evaluation
The system was validated using Anthropomorphic Test Devices (ATDs) and pneumatic fall rigs to ensure experimental control and repeatability across various forensic-based fall archetypes.

| Metric | System Performance (AFODS) |
| :--- | :--- |
| **Backbone Model** | YOLOv7-Tiny + RNN |
| **Primary Sensors** | LWIR + NIR + Ultrasonic |
| **Detection Latency** | < 100ms |
| **Validation Context** | Forensic-based fall archetypes |

---

## 🤝 Acknowledgments
This research was supported by and conducted at the **Department of Legal Medicine, Shiga University of Medical Science**, Otsu, Shiga, Japan. 

Special thanks to [Kinetik Dynamics](https://kinetik.tech/) for their insightful guidance and technical expertise, which were instrumental in the conceptual development of the system’s hardware architecture presented in this paper. 

---

## 📝 Citation

If you use this research or the AFODS framework in your work, please cite the original article:

**BibTeX:**
```bibtex
@article{vehicles7040149,
    AUTHOR = {Barua, Nick and Hitosugi, Masahito},
    TITLE = {Advanced Multi-Modal Sensor Fusion System for Detecting Falling Humans: Quantitative Evaluation for Enhanced Vehicle Safety},
    JOURNAL = {Vehicles},
    VOLUME = {7},
    YEAR = {2025},
    NUMBER = {4},
    PAGES = {149},
    DOI = {10.3390/vehicles7040149},
    URL = {[https://doi.org/10.3390/vehicles7040149](https://doi.org/10.3390/vehicles7040149)}
}
