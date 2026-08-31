# Project Overview

## SIGN SPEAK: A Smart Glove for Real-Time Sign Language to Speech Conversion

### 1. Introduction

SIGN SPEAK is a wearable assistive-technology prototype developed to facilitate communication between sign-language users and people who may not understand sign language.

The system uses a combination of wearable sensors, embedded computing, machine learning, and audio output to recognize selected hand gestures and convert them into corresponding spoken phrases.

The project brings together concepts from **electronics engineering, embedded systems, sensor fusion, machine learning, and assistive technology**.

---

## 2. Problem Statement

Communication can become challenging when a person using sign language interacts with someone who does not understand it.

SIGN SPEAK explores a technology-based approach in which hand gestures can be detected electronically and translated into speech, providing an additional communication interface.

The goal was to develop a compact and practical prototype capable of performing gesture recognition and speech output with minimal reliance on external computing infrastructure.

---

## 3. Proposed Solution

The developed smart glove captures hand and motion information through multiple sensors integrated into the wearable system.

The collected sensor information is processed and passed to a machine-learning-based classification system. Once a gesture is recognized, the corresponding predefined phrase is selected and converted into audible output through the integrated audio system.

### System Flow

**Hand Gesture**
↓
**Wearable Sensors**
↓
**Sensor Data Processing**
↓
**Machine Learning Classification**
↓
**Gesture Recognition**
↓
**Audio Output**

---

## 4. Hardware Architecture

The prototype is built around an ESP32-based embedded platform.

### Major Components

| Component            | Purpose                                |
| -------------------- | -------------------------------------- |
| ESP32                | Embedded processing and system control |
| Flex Sensors         | Detect finger bending and movement     |
| MPU6050 IMU          | Capture hand motion and orientation    |
| Audio Module         | Handle speech/audio playback           |
| Amplifier & Speaker  | Produce audible output                 |
| Rechargeable Battery | Portable power supply                  |
| Custom PCB           | Hardware integration                   |

The combination of finger-position information and motion information allows the system to capture multiple aspects of a hand gesture.

---

## 5. Sensor Fusion

One of the key aspects of SIGN SPEAK is the use of information from multiple sensor types.

Flex sensors provide information related to finger movement, while the IMU provides motion and orientation information.

Combining these sensor signals creates a richer representation of a gesture than relying on a single sensor type.

This sensor-fusion approach was incorporated into the machine-learning pipeline for gesture classification.

---

## 6. Machine Learning Approach

A lightweight machine-learning approach was developed to classify the collected sensor patterns into predefined gesture categories.

The development process included:

* Sensor-data collection
* Data preprocessing
* Feature preparation
* Dataset augmentation
* Model training
* Model evaluation
* Model optimization
* Embedded deployment

The model was designed with the limitations of microcontroller-based hardware in mind, with an emphasis on computational efficiency and real-time operation.

> Detailed preprocessing parameters, model architecture, trained model files, and deployment-specific implementation details are intentionally not included in this public repository.

---

## 7. Gesture Vocabulary

The prototype was evaluated using six selected gesture categories:

1. Are you fine
2. Call the Doctor
3. I am Hungry
4. I'm not feeling well
5. Thank you
6. Wait for me

Each recognized gesture is associated with a predefined audio phrase.

---

## 8. Embedded Deployment

A major objective of the project was to move the machine-learning inference process onto the embedded platform rather than depending entirely on an external computer.

The trained model was optimized for deployment on resource-constrained hardware, enabling the prototype to perform gesture classification locally.

This approach demonstrates the potential of **Edge AI** for wearable and assistive applications.

---

## 9. Performance

The final prototype was evaluated using the collected gesture dataset.

### Selected Results

* **Gesture classes:** 6
* **Original samples:** 480
* **Neural-network test accuracy:** 97.92%
* **Model parameters:** 12,838
* **Approximate model size:** 50 KB
* **Inference:** Real-time on embedded hardware

These results demonstrate the feasibility of combining wearable sensing and lightweight machine learning for real-time gesture-to-speech applications.

---

## 10. Engineering Challenges

The project involved several engineering challenges, including:

* Integrating multiple sensors into a wearable form factor
* Managing sensor variability
* Designing a reliable data-collection process
* Preparing sensor data for machine-learning applications
* Deploying a lightweight model on embedded hardware
* Maintaining consistency between training and embedded inference
* Achieving responsive real-time operation
* Integrating hardware, software, and audio output into a single prototype

---

## 11. Future Improvements

Potential future improvements include:

* Increasing the number of recognizable gestures
* Improving generalization across different users
* Supporting continuous gesture recognition
* Improving sensor robustness and calibration
* Reducing hardware size and weight
* Exploring more efficient Edge AI techniques
* Adding wireless connectivity
* Developing a more ergonomic wearable design
* Expanding the system toward a larger sign-language vocabulary

---

## 12. Intellectual Property

This repository is intended for **academic and portfolio demonstration purposes**.

The public repository does not contain the complete implementation of the project.

The following materials are intentionally withheld:

* Complete source code
* Raw dataset
* Trained model files
* Calibration parameters
* Detailed preprocessing parameters
* PCB design/source files
* Schematics and fabrication files
* Other implementation-specific materials

These materials are retained privately by the project team.

**© 2026 SIGN SPEAK Project. All rights reserved.**
