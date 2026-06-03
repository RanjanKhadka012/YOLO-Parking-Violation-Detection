# Drone-Assisted Campus Parking Violation Detection Using YOLO and Geofenced Parking Regions

## Overview

This project explores the use of computer vision, aerial imagery, and deep learning to automatically identify potential parking violations in university parking lots. The system utilizes drone-captured images and videos, YOLO object detection models, and geofenced parking-space annotations to detect vehicles and determine whether they are parked within designated parking areas.

The project is designed as a research prototype and educational tool. It is not intended to issue citations, fines, or legal determinations. Instead, it demonstrates how modern AI and computer vision techniques can assist campus operations, parking management, and infrastructure monitoring.

---

## Research Motivation

University parking lots frequently experience issues such as:

- Vehicles parked outside designated spaces
- Vehicles occupying multiple parking spaces
- Parking in restricted zones
- Blocking entrances, exits, or driving lanes
- Accessibility and safety concerns

Traditional monitoring relies on manual inspection, which can be time-consuming and resource-intensive. This project investigates whether drone imagery combined with deep learning can provide an efficient and scalable approach for identifying potential parking violations.

---

## Project Objectives

The primary goals of this project are:

1. Collect aerial parking lot imagery using drone platforms.
2. Detect vehicles using state-of-the-art YOLO object detection models.
3. Define legal parking regions through manually annotated parking-space polygons.
4. Identify potential parking violations using rule-based geofencing logic.
5. Evaluate system performance under different environmental conditions.
6. Compare multiple YOLO architectures for aerial vehicle detection.
7. Develop a reproducible research framework for future smart-campus applications.

---

## System Architecture

### Data Collection Layer

Drone flights are conducted over approved campus parking areas.

Captured data includes:

- High-resolution images
- Video footage
- Multiple flight altitudes
- Various camera angles
- Different lighting conditions

Potential flight heights:

- 20 meters
- 30 meters
- 40 meters

---

### Object Detection Layer

The system uses YOLO (You Only Look Once) object detection models to identify vehicles in aerial imagery.

Models evaluated include:

#### YOLOv8 Series

- YOLOv8n
- YOLOv8s
- YOLOv8m
- YOLOv8l
- YOLOv8x

#### YOLO11 Series

- YOLO11n
- YOLO11s
- YOLO11m
- YOLO11l
- YOLO11x

Detected classes may include:

- Car
- Truck
- Bus
- Motorcycle
- Other vehicles

---

### Parking Space Geofencing

Parking spaces and restricted areas are manually annotated using polygon regions.

Annotated regions include:

- Standard parking spaces
- Accessible parking spaces
- Fire lanes
- No-parking zones
- Loading zones
- Driving lanes
- Building entrances

Annotation tools:

- CVAT
- Roboflow
- LabelMe

---

### Violation Detection Engine

After vehicle detection, the system evaluates each vehicle against predefined parking rules.

Potential violations include:

#### Out-of-Bounds Parking

Vehicle center falls outside a legal parking region.

#### Multi-Space Occupancy

Vehicle overlaps two or more parking spaces.

#### Restricted Area Parking

Vehicle appears within a no-parking zone.

#### Lane Obstruction

Vehicle blocks traffic flow within a designated driving lane.

#### Boundary Crossing

Vehicle significantly extends beyond a parking-space boundary.

The system flags these as:

"Potential Parking Violations"

All detections require human review.

---

## YOLO Benchmarking Study

A secondary objective of this project is to perform a comprehensive comparison of YOLO architectures for aerial vehicle detection.

Metrics evaluated include:

### Accuracy Metrics

- Precision
- Recall
- F1 Score
- mAP@50
- mAP@50-95

### Performance Metrics

- Inference Speed (FPS)
- Processing Time
- GPU Memory Usage
- Model Size
- Training Time

### Experimental Variables

- Drone altitude
- Camera angle
- Lighting conditions
- Image resolution
- Model architecture

The resulting benchmark will provide insight into the tradeoffs between accuracy and computational efficiency.

---

## Technology Stack

### Hardware

- NVIDIA RTX 5000 Ada Generation GPU (32GB VRAM)
- Drone platform with camera
- Ubuntu Linux workstation

### Software

- Python 3
- PyTorch
- Ultralytics YOLO
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Streamlit

### Annotation Tools

- CVAT
- Roboflow
- LabelMe

### Development Environment

- Ubuntu 24.04 LTS
- Visual Studio Code
- Git
- GitHub

---

## Project Structure

```text
parking-yolo/
│
├── data/
│   ├── raw/
│   ├── processed/
│   ├── annotated/
│   └── datasets/
│
├── models/
│
├── notebooks/
│
├── src/
│   ├── detect.py
│   ├── train.py
│   ├── evaluate.py
│   ├── geofence.py
│   └── violations.py
│
├── results/
│
├── papers/
│
├── dashboards/
│
└── README.md
```

---

## Dataset Preparation

The dataset consists of aerial parking-lot imagery and corresponding annotations.

Data preprocessing may include:

- Image resizing
- Data augmentation
- License plate blurring
- Face blurring
- Class balancing
- Annotation validation

Dataset splits:

- Training Set
- Validation Set
- Test Set

---

## Evaluation Methodology

Ground-truth labels will be manually generated for comparison.

Performance evaluation includes:

- Vehicle detection accuracy
- Parking violation classification accuracy
- False positive rate
- False negative rate
- Processing latency

Results will be analyzed across multiple environmental conditions.

---

## Privacy and Ethics

This project emphasizes privacy and responsible AI practices.

Measures include:

- License plate anonymization
- Face anonymization
- Restricted dataset access
- Academic use only
- Human verification of flagged detections

No automated enforcement actions are performed.

---

## Expected Contributions

This project contributes:

- A drone-based parking monitoring framework
- A geofenced parking violation detection system
- A benchmark comparison of YOLO architectures
- A reproducible computer vision research pipeline
- Experimental insights into aerial object detection

The project demonstrates the integration of artificial intelligence, computer vision, software engineering, and smart-campus technologies.

---

## Future Work

Potential future enhancements include:

- Real-time drone video analysis
- Multi-drone coverage systems
- Automatic parking-space detection
- License plate recognition (with appropriate permissions)
- Smart-campus integration
- Edge deployment on embedded AI hardware
- Real-time dashboard and alerting systems

---

## Author

Ranjan Khadka

Software Engineering Student
University of Minnesota Crookston

Research Areas:

- Artificial Intelligence
- Computer Vision
- Deep Learning
- Smart Campus Technologies
- Software Engineering
