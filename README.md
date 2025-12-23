<p align="center">
  <a href="https://www.shiga-med.ac.jp/english">
    <img src="docs/sums-logo.png" width="300" alt="Shiga University of Medical Science Logo">
  </a>
</p>


# Advanced Multi-Modal Sensor Fusion System for Detecting Falling Humans 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Journal: Vehicles](https://img.shields.io/badge/Journal-Vehicles-blue.svg)](https://doi.org/10.3390/vehicles7040149)
[![Affiliation: SUMS](https://img.shields.io/badge/Affiliation-Shiga_University_of_Medical_Science-red.svg)](https://www.shiga-med.ac.jp/english)

### Quantitative Evaluation for Enhanced Vehicle Safety
# sensor-fusion-fall-detection
# Advanced Multi-Modal Sensor Fusion System for Detecting Falling Humans

This repository contains the software framework and quantitative evaluation for the **Advanced Falling Object Detection System (AFODS)**, as published in *Vehicles* (2025). 

AFODS is designed to enhance vehicle safety by detecting and predicting human falls in real-time using a novel multi-modal sensor fusion approach.

## 📌 Abstract
Collisions with fallen pedestrians pose a lethal challenge to current ADAS. This project introduces a safety framework that architecturally integrates **Long-Wave Infrared (LWIR)**, **Near-Infrared (NIR) Stereo**, and **Ultrasonic sensors**. The system utilizes a custom AI pipeline combining **YOLOv7-Tiny** for detection and a **Recurrent Neural Network (RNN)** for proactive threat assessment.

## 🛠 System Architecture
* **Sensors:** LWIR Thermal Imaging, NIR Stereo Vision, and Ultrasonic Transducers.
* **Detection Backbone:** YOLOv7-Tiny optimized for edge-case pedestrian postures.
* **Threat Assessment:** RNN-based predictive modeling to assess fall dynamics and collision probability.
* **Innovation:** Includes an architectural "Hypothermia Detection Mode" via thermal variance analysis.

---

## 📊 Quantitative Evaluation
The system was validated using Anthropomorphic Test Devices (ATDs) and pneumatic fall rigs to ensure experimental control and repeatability.

| Metric | System Performance (AFODS) |
| :--- | :--- |
| **Backbone Model** | YOLOv7-Tiny + RNN |
| **Primary Sensors** | LWIR + NIR + Ultrasonic |
| **Validation Context** | Forensic-based fall archetypes |

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
---

## 🤝 Acknowledgments
This research was supported by and conducted at the **Department of Legal Medicine, Shiga University of Medical Science**, Otsu, Shiga, Japan. 

We would like to acknowledge the contribution of the university’s laboratory facilities, specifically for providing the controlled environment required for the pneumatic fall-rig experiments and the validation of the **AFODS** framework.
