# Broiler-Spatial-Analytics-YOLO
Real-time poultry flock distribution monitoring system using YOLOv8 and DBSCAN. Implementation of CIBB algorithm for behavioral analysis
# Real-time Broiler Flock Spatial Analytics System

![Python](https://img.shields.io/badge/Python-3.9-blue)
![YOLOv8](https://img.shields.io/badge/YOLO-v8-green)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)

## Abstract
This project implements an automated monitoring system for broiler flock distribution in poultry houses using Computer Vision and Clustering techniques. Based on the methodology proposed by Chiang et al. (2021) [1], the system utilizes **YOLOv8** for object detection and **DBSCAN** for spatial clustering analysis.

[cite_start]Key metric implemented: **Cluster Index of Bounding Box (CIBB)**, which indicates the spatial distribution and potential thermal comfort of the flock[cite: 9, 11].

## System Architecture
The pipeline processes video feeds to extract behavioral metrics:
1.  **Object Detection:** YOLOv8 identifies broilers in the frame.
2.  **Spatial Coordinates:** Extracts centroids of bounding boxes ($x_b, y_b$).
3.  **Cluster Analysis:** Applies DBSCAN to detect huddling behaviors.
4.  **CIBB Calculation:** Computes the ratio of the union area to the perimeter of bounding boxes.

## Key Features
* **Real-time Detection:** High-FPS inference using Ultralytics YOLOv8.
* **Density Analysis:** Quantifiable clustering metrics (CIBB) correlated with temperature/humidity.
* **Containerized Deployment:** Docker support for easy deployment on edge devices (Coming Soon).

## Tech Stack
* **Language:** Python 3.9
* **CV Engine:** OpenCV, Ultralytics YOLOv8
* **ML Algorithm:** Scikit-learn (DBSCAN)
* **Deployment:** Docker


## 📝 References
[1] K. Chiang, L. Mao, and W. Fang, "Automated Monitoring of Broiler Flock Distribution through Computer Vision and Clustering Technology," 2021.
