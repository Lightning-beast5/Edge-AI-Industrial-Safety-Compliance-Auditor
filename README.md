# 🛡️ Edge-AI Industrial Safety & Compliance Auditor

## 📌 Project Overview
This project is an automated AI auditor designed to enhance safety on construction and industrial sites. Using computer vision, it monitors real-time video feeds or images to ensure workers are wearing proper Personal Protective Equipment (PPE) and are not entering restricted hazard zones.

## 🏭 Application
*   **PPE Compliance**: Automatically detects if workers are missing hard hats, vests, or safety boots.
*   **Hazard Zone Monitoring**: Defines virtual restricted areas and triggers alerts if a person enters a dangerous zone.
*   **Edge Deployment**: Optimized for real-time monitoring on site without requiring heavy infrastructure.

## ✨ Key Features
*   **YOLOv11 Detection**: High-accuracy detection of PPE items and personnel.
*   **Virtual Safety Fence**: Uses polygon-based detection to identify zone intrusions based on personnel foot placement.
*   **Multi-Source Input**: Supports local image files, local video files, and direct YouTube stream links.
*   **High-Visibility UI**: Color-coded bounding boxes with high-contrast text backgrounds for clear visibility in busy industrial environments.

## 🛠️ Tech Stack & Libraries
*   **Language**: Python
*   **Model Architecture**: YOLOv11 (Ultralytics)
*   **Computer Vision**: OpenCV (cv2)
*   **Video Handling**: yt-dlp (for YouTube processing)
*   **Data Handling**: NumPy, Roboflow (Dataset management)
*   **Platform**: Google Colab / Linux Edge Devices

## 🚀 How it Works
1.  **Detection**: The model identifies classes like `person`, `helmet`, `no-helmet`, `vest`, etc.
2.  **Safety Logic**: 
    *   If a `person` bounding box intersects with the defined `hazard_zone`, a **RED INTRUSION** alert is triggered.
    *   If a `no-` class (e.g., `no-helmet`) is detected, an **ORANGE MISSING PPE** alert is triggered.
3.  **Visualization**: Results are displayed with real-time annotations and safety warnings.
