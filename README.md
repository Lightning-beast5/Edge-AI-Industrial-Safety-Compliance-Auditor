# Edge-AI-Industrial-Safety-Compliance-Auditor
An end-to-end simulation of an edge-deployed, real-time safety monitoring system tailored for construction sites, smart warehouses, and manufacturing plants. This project goes beyond passive object detection by integrating dynamic business logic, custom geofencing, and automated alert systems to actively mitigate workplace hazards.

# Key Features
Real-Time PPE Detection: Processes live video feeds to detect essential Personal Protective Equipment (PPE), specifically focusing on hard hats and high-visibility safety vests.

Dynamic Restricted Zones: Features an interactive interface allowing users to draw custom "virtual keep-out zones" directly onto the live camera stream.

Intrusion & Hazard Alerting: Instantly triggers an automated visual/audio alarm system the moment a human presence intersects with a designated hazardous area.

Edge-Optimized Architecture: Designed with low-latency constraints in mind, simulating how the system runs locally on resource-constrained edge hardware.

# Tech Stack 
Computer Vision & AI: OpenCV, YOLOv8 / YOLOv11 (or equivalent lightweight detector), PyTorch

GUI / Interface: Tkinter / PyQt (for drawing zones) or a lightweight web UI (Streamlit / Flask)

Deployment: ONNX Runtime / OpenVINO (for edge optimization simulation)

# How It Works
Video Ingestion: The system captures frames from a live webcam or pre-recorded industrial site footage.

Inference Pipeline: Frames are passed through an object detection model to locate workers, vests, and helmets simultaneously.

Geofencing Logic: The system checks if the bounding box coordinates of any detected person overlap with the user-defined polygon (Restricted Zone).

Compliance Audit: If a worker is inside a valid zone but missing PPE, or if anyone enters a restricted zone, the system flags a violation and fires an alert.
