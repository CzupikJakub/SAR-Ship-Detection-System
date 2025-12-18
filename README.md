# 🛰️ Maritime Ship Detection & Intelligence System (SAR)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Domain](https://img.shields.io/badge/Domain-SAR%20%7C%20Radar-7f8c8d?style=for-the-badge)
![Tech](https://img.shields.io/badge/Computer%20Vision-OpenCV-green?style=for-the-badge)
![Target](https://img.shields.io/badge/Target-Maritime%20Surveillance-003366?style=for-the-badge)

## 📋 Project Overview
This project is an automated pipeline for detecting, classifying, and analyzing maritime vessels using **Synthetic Aperture Radar (SAR)** imagery logic. Unlike optical sensors, this system operates on intensity-based data, simulating real-world monitoring capabilities used in the **NewSpace sector**.

The system processes satellite imagery to provide actionable intelligence: ship location, heading (orientation), estimated physical size, and classification.

## 🚀 Key Features
* **Computer Vision Pipeline:** Gaussian noise reduction (despeckling) and Adaptive Thresholding for robust segmentation.
* **Pose Estimation:** Utilizing `cv2.minAreaRect` to determine the precise heading (orientation) of vessels.
* **Physical Analysis:** Implementing **Ground Sample Distance (GSD)** calibration (2.5m/px) to estimate real-world dimensions.
* **Automated Classification:** Logic-based categorization of vessels into *Small*, *Medium*, and *Large* classes.
* **Reporting:** Automatic generation of a mission report (CSV) ready for database integration.

## 🛠️ Tech Stack
* **Python 3.10+**
* **OpenCV:** Image processing and contour analysis.
* **NumPy:** Matrix operations and geometry calculations.
* **Pandas:** Data structuring and export.
* **Matplotlib:** Visualization of tactical maps.

## 📊 Methodology
1.  **Preprocessing:** Application of Gaussian Blur to mitigate speckle noise inherent in radar data.
2.  **Segmentation:** Binary thresholding to isolate high-backscatter targets (ships) from the background.
3.  **Morphological Operations:** Dilation to merge disjointed ship parts into coherent objects.
4.  **Analysis:** Extraction of geometric properties to calculate length and heading.
5.  **Intelligence Output:** Visual overlay with bounding boxes and a structured report.

## 📈 Sample Results
Here is the output of the classification pipeline. Colors indicate vessel size (Green=Small, Yellow=Medium, Red=Large).

![Detection Result](result_map.png)

*Sample Mission Report Data:*
| ID | Category | Length (m) | Heading (deg) |
| :--- | :--- | :--- | :--- |
| 0 | Small | 77m | 88 |
| 1 | Medium | 87m | 90 |
| 2 | Medium | 100m | 85 |
| 3 | Large | 125m | 89 |
| 4 | Large | 130m | 91 |
| 5 | Large | 136m | 87 |

## 👤 Author
**[Jakub Czupik]**
