# Tennis Player Tracking System using YOLO, ByteTrack, and Homography

This repository implements a computer vision pipeline for tennis player tracking and real-world kinematic analysis using deep learning–based object detection, multi-object tracking, and homography-based coordinate transformation.

The system processes video input to extract player trajectories and transform image-space coordinates into real-world court coordinates, enabling quantitative motion analysis including displacement, velocity, and acceleration.

This implementation extends a research-oriented tracking base into a more robust, reproducible, and engineering-focused sports tracking system.

---

# Core Features

• Player detection using YOLO (Ultralytics)  
• Multi-object tracking using ByteTrack  
• Tennis court keypoint detection  
• Homography transformation (image → real-world coordinates)  
• Real-world trajectory reconstruction  

Kinematic analysis:

• Distance traveled  
• Velocity estimation  
• Acceleration estimation  
• Time-resolved trajectory analysis  

Additional engineering features:

• Structured pipeline design  
• Persistent storage integration (Google Drive compatible)  
• Reproducible execution environment  

---

# System Architecture

Pipeline overview:

Video Input  
↓  
YOLO Player Detection  
↓  
ByteTrack Multi-Object Tracking  
↓  
Court Keypoint Detection  
↓  
Homography Computation  
↓  
Coordinate Transformation  
↓  
Kinematic Analysis  
↓  
Structured Data Output  

---

# Mathematical Foundation

This system uses planar homography to map image coordinates to real-world court coordinates:

x_real = H · x_image

Where:

• H = homography matrix  
• x_image = pixel coordinates  
• x_real = real-world coordinates (meters)  

This enables physically meaningful motion analysis.

---

# Engineering Contributions

This repository introduces the following engineering and modeling extensions:

Infrastructure Engineering:

• Google Drive integration  
• Reproducible file path management  
• Structured pipeline architecture  

Tracking Improvements:

• Improved tracking consistency  
• Robust trajectory handling  
• Improved tracking stability  

Homography and Geometric Modeling:

• Robust court keypoint handling  
• Improved homography computation pipeline  
• Reliable coordinate normalization  

Kinematic Modeling (Original Contribution):

• Real-world distance computation  
• Velocity estimation  
• Acceleration estimation  
• Trajectory reconstruction  

Pipeline Robustness:

• Error handling improvements  
• Improved execution stability  

---

# Technologies Used

Python 3.x  
YOLO — Ultralytics  
ByteTrack  
OpenCV  
NumPy  
Pandas  
PyTorch  
Google Colab  

---

# Repository Structure

```
tennis-player-tracking/
│
├── notebook/
│   └── tennis_tracking_performance.ipynb
│
├── README.md
│
└── requirements.txt
```


---

# Example Outputs

The system produces:

• Player trajectories  
• Real-world coordinate reconstruction  
• Velocity and acceleration metrics  
• Structured datasets for further analysis  

---

# Use Cases

Sports performance analysis  
Biomechanics research  
Athlete monitoring systems  
Sports analytics research  
Computer vision research  

---

# Installation

Clone repository:

```bash
git clone https://github.com/peterson-scbr/tennis-player-tracking.git
cd tennis-player-tracking
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open notebook:

```bash
jupyter notebook notebook/tennis_tracking.ipynb
```
---

# Download required data (Google Drive)

Download the project data and models from:

Google Drive folder:

https://drive.google.com/drive/folders/1UtBqFwioyK1UMoWDczqu9E0g-zUhMqc5

Extract and place the folder inside your Google Drive root directory:

Required structure:
```
MyDrive/
└── tennis_analysis/
    ├── input_videos/
    ├── models/
    ├── results/
```
Do not rename folders.

---

# Run in Google Colab
Mount Google Drive:
```
from google.colab import drive
drive.mount('/content/drive')
```
Then open and run:
notebook/tennis_tracking_performance.ipynb

---

# Attribution

This project builds upon open-source detection and tracking frameworks:

YOLO — Ultralytics  
ByteTrack — ByteDance Research  
OpenCV  

All pipeline integration, homography modeling, and kinematic analysis extensions were implemented in this repository.

---

# Author

Peterson Antonio  
Sports Scientist & Developer  
Brazil
