---
layout: project
slug: automated-futsal-analysis
name: Automated Futsal Video Analysis (PFE)
tools: [Python, OpenCV, YOLOv11, DeepSORT, AI, Computer Vision]
image: /Portfolio/assets/img/projects/SportScore.png
description: >
  AI-based video analysis system for futsal games, developed during my final-year project at SportScore.
  The pipeline detects, classifies, and structures player actions (passes, shots, interceptions, goals) from futsal videos,
  with intelligent filtering of irrelevant frames.
external_url: /Portfolio/demos/#futsal-demo
---

## 🧠 Project Overview
This project focuses on **automated understanding of futsal gameplay** using a custom computer vision pipeline.

We built an **end-to-end video analysis system** capable of detecting, tracking, and classifying key player actions
using state-of-the-art deep learning models.

---

## 🧩 System Architecture
Here’s a simplified diagram of the processing pipeline:

![System Architecture](/Portfolio/assets/img/projects/futsal_architecture.png)

1. **Detection**: YOLOv11 detects players and ball in each frame.  
2. **Tracking**: DeepSORT assigns consistent IDs to players across frames.  
3. **Action Recognition**: A CNN-LSTM model classifies temporal actions like passes or shots.  
4. **Event Structuring**: Filter and summarize the game into meaningful stats and highlights.

---

## 🚀 Key Features
- Multi-player tracking and re-identification  
- Intelligent frame selection and filtering  
- Action classification with deep learning  
- Real-time performance optimization  

---

## 🎥 Demo
You can watch the live demo here 👇  

👉 [**Watch the demo video**](/Portfolio/demos/#futsal-demo){: .btn .btn-primary }

---

## 🧰 Tech Stack
| Component | Technology |
|------------|-------------|
| Object Detection | YOLOv11 |
| Tracking | DeepSORT |
| Video Processing | OpenCV |
| Framework | PyTorch |
| Visualization | Matplotlib, Seaborn |

---

[⬅ Back to Projects](/projects/){: .btn .btn-secondary }
