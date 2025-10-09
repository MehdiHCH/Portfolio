---
title: Automated Futsal Video Analysis for Performance Reporting
image: /assets/img/projects/SportScore.gif
description: End-to-end AI pipeline for automated detection, tracking, and classification of player actions in futsal matches using YOLOv11, DeepSORT, and advanced computer vision techniques.
category: sports-analytics
tags:
  - Computer Vision
  - YOLOv11
  - DeepSORT
  - Sports Analytics
  - Action Recognition
  - Multi-Object Tracking
  - Deep Learning
  - OCR
  - Homography
demos:
  - title: "Frame classification"
    video: /assets/videos/sportscore/Class.mp4
    description: "Complete automated analysis of a futsal match"
  - title: "Action Detection & Classification"
    video: /assets/videos/sportscore/Action_detection.mp4
    description: "Real-time detection of passes, shots, dribbles, and goals"
  - title: "Object Detection (Goal Recognition)"
    video: /assets/videos/sportscore/IS_But.mp4
    description: "But"
date: 2025-04-01
company: SPORTSCORE
location: Paris, France (Remote)
duration: April 2025 - September 2025
---

## 🎯 Executive Summary

During my final-year internship at **SPORTSCORE**, I developed an intelligent end-to-end AI pipeline for **automated video analysis of futsal matches**. The system transforms raw multi-camera footage into structured tactical insights by automatically detecting, tracking, and classifying player actions such as passes, shots, dribbles, interceptions, and goals.

**Key Achievement:** Reduced manual annotation workload by **80%** while achieving **99.95% accuracy** in frame classification and **90.1% precision** in ball detection.

---

## 📋 Table of Contents

1. [Context & Problem Statement](#context--problem-statement)
2. [Company Background: SPORTSCORE](#company-background-sportscore)
3. [Project Objectives](#project-objectives)
4. [Technical Architecture](#technical-architecture)
5. [Core Pipeline Components](#core-pipeline-components)
6. [Key Contributions](#key-contributions)
7. [Results & Performance](#results--performance)
8. [Challenges & Solutions](#challenges--solutions)
9. [Impact & Business Value](#impact--business-value)
10. [Future Perspectives](#future-perspectives)
11. [Technical Stack](#technical-stack)

---

## 🔍 Context & Problem Statement

### The Challenge

Traditional sports video analysis is:
- ⏱️ **Time-consuming:** Manual annotation takes hours per match
- 💰 **Expensive:** Requires dedicated video analysts
- 🎯 **Subjective:** Human bias affects consistency
- 🔄 **Non-scalable:** Cannot process multiple matches simultaneously

### Futsal-Specific Complexities

Futsal presents unique challenges for automated analysis:
- ⚡ **Rapid gameplay** with frequent transitions
- 🏟️ **Confined space** causing constant occlusions
- 🔄 **High player density** with overlapping trajectories
- 🎥 **Multi-camera** setups requiring spatial alignment

### The Solution

An AI-powered pipeline leveraging:
- **Computer Vision** for object detection and tracking
- **Homography** for 2D pitch projection
- **Spatio-temporal Rules** for action recognition
- **Automated Classification** to filter irrelevant frames

---

## 🏢 Company Background: SPORTSCORE

**SPORTSCORE** is an innovative French company specializing in **real-time sports data exploitation** using AI and computer vision. They develop software solutions that automatically extract:
- 📊 Key events and statistics
- 📈 Advanced tactical metrics
- 🎨 Interactive visualizations

**Target Clients:**
- Professional clubs and federations
- Video analysts and coaches
- Sports media and broadcasters

**Mission:** Transform sports through automation, precision, and speed of analysis.

---

## 🎯 Project Objectives

### Primary Goals

1. **Intelligent Frame Filtering**
   - Automatically exclude non-relevant sequences (replays, timeouts, transitions)
   - Reduce processing load and false positives

2. **Automated Action Detection**
   - Detect and classify key actions: passes, shots, dribbles, interceptions
   - Generate structured event data (JSON format)

3. **Tactical Visualizations**
   - Produce heatmaps, pass maps, and trajectory plots
   - Export performance reports for analysts

4. **Reduce Manual Workload**
   - Minimize human annotation effort
   - Accelerate production of actionable insights

---

## 🏗️ Technical Architecture

### System Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    VIDEO INPUT (Multi-Camera)                │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  MODULE 1: Frame Classification (YOLOv11m-cls)              │
│  ├─ Filter "Main" (useful) frames                           │
│  └─ Discard "Other" (replays, transitions)                  │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  MODULE 2: Object Detection & Tracking                      │
│  ├─ YOLOv11x: Detect players & ball                         │
│  └─ DeepSORT: Multi-object tracking with Re-ID              │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  MODULE 3: Spatial Projection (Homography)                  │
│  ├─ Map pixel coordinates → pitch coordinates               │
│  └─ Detect pitch lines & zones (penalty area, goal)         │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  MODULE 4: Player Re-Identification                         │
│  ├─ HSV Clustering: Team color extraction                   │
│  ├─ OCR: Jersey number recognition                          │
│  └─ Trajectory-based identity confirmation                  │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  MODULE 5: Pose Estimation (Keypoints)                      │
│  └─ Extract anatomical landmarks for gesture analysis       │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  MODULE 6: Action Detection & Classification                │
│  ├─ Ball possession attribution                             │
│  ├─ Pass detection (7 types)                                │
│  ├─ Shot classification (on target, off target, blocked)    │
│  ├─ Dribble & interception detection                        │
│  └─ Goal confirmation & assist attribution                  │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────────┐
│  OUTPUT: Structured Data (JSON) + Visualizations            │
│  ├─ Event timeline with timestamps                          │
│  ├─ Player trajectories & heatmaps                          │
│  ├─ Pass maps & tactical statistics                         │
│  └─ Automated performance reports                           │
└─────────────────────────────────────────────────────────────┘
```

---

## ⚙️ Core Pipeline Components

### 1. Frame Classification Module

**Objective:** Filter out non-relevant frames to reduce processing overhead.

**Architecture:** YOLOv11m-cls fine-tuned for binary classification
- **Class "Main":** Gameplay sequences (useful for analysis)
- **Class "Other":** Replays, timeouts, crowd shots, transitions

**Training Data:**
- **67,801 annotated frames** from multiple matches
- **Training set:** 54,240 frames (25,655 Main + 28,585 Other)
- **Validation set:** 13,561 frames (6,414 Main + 7,147 Other)

**Performance:**
- **Accuracy:** 99.95%
- **Precision:** 99.91% (only 6 false positives)
- **Recall:** 100% (zero false negatives)
- **Impact:** Reduced inference time from **19.98 min → 16.05 min** (~20% speedup)

---

### 2. Object Detection & Multi-Object Tracking

**Detection:** YOLOv11x custom-trained on futsal datasets
- **Classes:** Player, Ball, Referee, Goal
- **Ball Detection (Fine-tuned):**
  - Precision: 90.1%
  - Recall: 83.4%
  - mAP@50: 83.4%

**Tracking:** DeepSORT with appearance-based association
- Kalman Filter for motion prediction
- Deep feature extraction (OSNet) for Re-ID
- Dynamic buffer and adaptive matching threshold

**Challenge:** Ball often occluded or moving at high speed
**Solution:** Created custom dataset with **CVAT annotations** from FIFA Futsal footage

---

### 3. Homography & Spatial Projection

**Purpose:** Convert pixel coordinates to real-world pitch coordinates

**Method:**
1. Detect pitch keypoints (corners, circles, lines)
2. Compute homography matrix
3. Project player/ball positions onto 2D pitch model

**Benefits:**
- Enables distance calculations between players
- Validates actions based on pitch zones (penalty area, goal)
- Generates tactical heatmaps and pass maps

---

### 4. Player Re-Identification (Re-ID)

**Multi-Modal Approach:**

1. **Team Detection:** HSV color clustering on jerseys
2. **Jersey Number:** OCR using PaddleOCR/Tesseract
3. **Trajectory Continuity:** DeepSORT feature matching

**Robustness:** Maintains player identity despite:
- Temporary occlusions
- Camera angle changes
- Posture variations

---

### 5. Pose Estimation & Keypoint Detection

**Model:** Pre-trained keypoint detector (OpenPose/MediaPipe)

**Extracted Landmarks:**
- Head, shoulders, elbows, knees, ankles
- Used to:
  - Detect shooting/passing gestures
  - Determine striking foot
  - Validate action types (e.g., header vs. foot pass)

---

### 6. Action Detection & Classification

**Core Logic:** Spatio-temporal rule-based system

#### Ball Possession Attribution
- **Methods tested:**
  1. Distance to player center
  2. Distance to feet (via keypoints)
  3. Distance to bounding box center
  4. Distance to projected position
- **Solution:** Temporal buffer + minimum distance heuristic

#### Pass Classification (7 Types)

| Pass Type | Criteria |
|-----------|----------|
| **Basic Pass** | Simple ball transmission between teammates |
| **Progressive Pass** | Forward pass advancing >10m toward goal |
| **Into-Penalty-Area Pass** | Pass ending inside opponent's penalty area |
| **Pressure Pass** | Pass made with opponent <2m away |
| **Smart Pass** | Pass to unmarked teammate in attacking position |
| **Key Pass** | Pass directly leading to a shot |
| **Assist** | Pass directly leading to a goal |

#### Shot Classification

- **Shot on Target:** Ball directed toward goal without interception
- **Shot off Target:** Ball misses goal frame
- **Blocked Shot:** Shot blocked by defender before reaching goal

#### Other Actions

- **Dribble:** Possession maintained while moving >1.5m
- **Interception:** Opponent recovers pass attempt
- **Incomplete Pass:** Pass not received after 2 seconds (~60 frames)
- **Goal:** Ball enters goal mask zone with possession validation

---

## 🚀 Key Contributions

### Contribution 1: Intelligent Frame Classification

**Before:**
- All frames processed indiscriminately
- High computational cost
- Many false positives from replays

**After:**
- 99.95% classification accuracy
- 20% reduction in inference time
- Cleaner event sequences

**Training Process:**
1. Manual annotation using CVAT
2. Fine-tuning YOLOv11m-cls (200 epochs)
3. Integration as first pipeline stage

---

### Contribution 2: Advanced Action Detection System

**Developed from Scratch:**
- `ActionDetection` class with spatio-temporal logic
- Ball possession tracking with temporal smoothing
- 7-type pass classifier
- Shot/dribble/interception detectors
- Goal confirmation + automatic assist attribution

**Logical Validation (Inspired by PoeClim):**
- Decision trees to verify actions post-detection
- Example: Goal validated only if ball enters goal mask without possession change
- Example: Assist attributed if goal preceded by Key/Smart/Progressive pass

---

### Contribution 3: Performance Optimization

**Ball Detection Enhancement:**
- Custom dataset: FIFA Futsal footage annotated in CVAT
- Fine-tuned YOLOv11x (100 epochs, RTX 3090)
- **Results:**
  - Precision: 90.1% (↑15% vs baseline)
  - Recall: 83.4%
  - Inference: 9.6ms/frame (~4.7 FPS)

**Impact:**
- Reliable ball tracking in critical zones (goal area)
- Accurate goal detection and assist attribution

---

### Contribution 4: Structured Data Export

**Output Formats:**
- **JSON:** Event timeline with timestamps, player IDs, coordinates
- **CSV:** Tabular statistics for analysts
- **Visualizations:** Heatmaps, pass maps, trajectory plots

**Example JSON Structure:**
```json
{
  "event_id": 142,
  "type": "Progressive Pass",
  "timestamp": "12:34.56",
  "passer": {
    "id": 7,
    "team": "A",
    "position": [15.3, 22.1]
  },
  "receiver": {
    "id": 10,
    "team": "A",
    "position": [28.7, 18.9]
  },
  "outcome": "completed"
}
```

---

## 📊 Results & Performance

### Quantitative Metrics

| Metric | Value |
|--------|-------|
| **Frame Classification Accuracy** | 99.95% |
| **Ball Detection Precision** | 90.1% |
| **Ball Detection Recall** | 83.4% |
| **Processing Speed** | 4.7 FPS (YOLOv11x) |
| **Inference Time Reduction** | 20% (with frame filtering) |
| **Manual Annotation Reduction** | ~80% |

### Qualitative Impact

✅ **Automated Event Detection:** No manual tagging needed for passes/shots/goals  
✅ **Reliable Re-ID:** Players tracked consistently despite occlusions  
✅ **Tactical Insights:** Heatmaps, pass networks, pressure zones generated automatically  
✅ **Scalable:** Modular architecture ready for multi-match processing  

---

## 🛠️ Challenges & Solutions

### Challenge 1: Ball Detection in Critical Zones

**Problem:**
- Ball often undetected near goal due to:
  - Small size + motion blur
  - Occlusion by goalkeeper/goalposts
  - High speed during shots

**Solution:**
- Created custom dataset from FIFA Futsal footage
- Fine-tuned YOLOv11x with 100 epochs
- Added temporal smoothing to fill detection gaps

**Result:** 90.1% precision, enabling reliable goal confirmation

---

### Challenge 2: Tracking Instability

**Problem:**
- DeepSORT ID switches during player collisions
- Ball tracking lost during occlusions

**Solution:**
- Added temporal buffer for possession continuity
- Integrated appearance features (OSNet) for Re-ID
- Implemented Kalman filter predictions during gaps

---

### Challenge 3: Action Ambiguity

**Problem:**
- Differentiating pass types (e.g., Smart vs Key pass)
- Validating incomplete passes vs interceptions

**Solution:**
- Defined strict spatio-temporal rules:
  - Pressure Pass: opponent <2m from passer
  - Smart Pass: receiver unmarked + attacking zone
  - Key Pass: followed by shot within 3 seconds
- Temporal validation windows (e.g., 60 frames for incomplete pass)

---

### Challenge 4: Processing Time

**Problem:**
- Full match (40 min) took ~60 minutes to process

**Solution (Ongoing):**
- Implemented frame classification filter (20% speedup)
- Prepared for multi-threading (batch processing)
- Optimized data structures (dict → numpy arrays)

**Target:** Real-time processing (<1.5x match duration)

---

## 💼 Impact & Business Value

### For SPORTSCORE

✅ **Operational Efficiency:** 80% reduction in manual annotation workload  
✅ **Scalability:** Can now process multiple matches simultaneously  
✅ **Product Enhancement:** Automated reports add value to client offerings  
✅ **Competitive Edge:** Faster turnaround than manual analysis services  

### For Clients (Clubs, Analysts, Federations)

✅ **Instant Insights:** Match analysis available within hours (vs days)  
✅ **Objective Data:** Eliminates human bias in event tagging  
✅ **Tactical Intelligence:** Heatmaps, pass networks, pressure zones  
✅ **Player Development:** Individual performance metrics for training  

---

## 🔮 Future Perspectives

### Short-Term Improvements

1. **Real-Time Processing**
   - Optimize for <1.5x match duration
   - Implement GPU batch processing
   - Add multi-threading for parallel module execution

2. **Enhanced Ball Tracking**
   - Integrate TrackNetV2 for ball trajectory prediction
   - Add segmentation-based detection for occluded ball

3. **Advanced Action Recognition**
   - Train deep learning model (Transformer-based) for action spotting
   - Incorporate temporal context (xLSTM encoder)

### Long-Term Vision

1. **Multi-Sport Extension**
   - Adapt pipeline for basketball, handball, hockey
   - Transfer learning from futsal model

2. **Live Streaming Integration**
   - Real-time event detection during broadcast
   - Automated highlight generation

3. **3D Reconstruction**
   - Multi-camera calibration for 3D player positioning
   - Depth estimation for offside detection

4. **Predictive Analytics**
   - Expected Goals (xG) model
   - Pass success probability
   - Tactical pattern recognition (e.g., pressing schemes)

---

## 🛠️ Technical Stack

### Deep Learning Frameworks
- **PyTorch** 2.0 - Model training and inference
- **Ultralytics YOLOv11** - Object detection
- **TensorFlow/Keras** - Supplementary models

### Computer Vision Libraries
- **OpenCV** - Video processing, homography
- **DeepSORT** - Multi-object tracking
- **PaddleOCR** - Jersey number recognition

### Data Processing
- **NumPy** - Numerical operations
- **Pandas** - Data structuring
- **JSON** - Event serialization

### Annotation & Training
- **CVAT** - Video annotation tool
- **Roboflow** - Dataset management
- **Weights & Biases** - Experiment tracking

### Hardware
- **NVIDIA RTX 3090** (24GB VRAM) - Training
- **NVIDIA RTX 4060** (8GB VRAM) - Inference

---

## 📚 References & Related Work

This project builds upon state-of-the-art research in sports video analysis:

1. **PoeClim** (Mohtaram et al., 2025): Spatio-temporal framework for action spotting
2. **Deep-EIoU** (Huang et al., 2024): Advanced multi-object tracking
3. **YOLOv11** (Ultralytics, 2024): Latest YOLO architecture
4. **DeepSORT** (Wojke et al., 2017): Deep association metric tracking

---

## 👨‍💻 About This Project

**Duration:** April 2025 - September 2025  
**Type:** Final-Year Internship (Master's in Artificial Intelligence)  
**Institution:** Ibn Tofail University, Faculty of Sciences, Kenitra  
**Company:** SPORTSCORE (Paris, France - Remote)  
**Supervisor:** Mr. Noureddine Mohtaram (SPORTSCORE)  
**Academic Supervisor:** Mr. Anass Nouri (FSK, Ibn Tofail University)

**Jury Members:**
- Mr. Anass Nouri (FSK, Ibn Tofail University)
- Mrs. Khadija Lekdioui (FSK, Ibn Tofail University)
- Mrs. Khaoula Boukir (ENSC, Ibn Tofail University)

**Defense Date:** September 15, 2025

---

## 🎓 Skills Developed

### Technical Skills
- Advanced computer vision (detection, tracking, homography)
- Deep learning model fine-tuning (YOLO, CNNs)
- Multi-object tracking algorithms (DeepSORT, Kalman Filter)
- Spatio-temporal reasoning and action recognition
- Data pipeline design and optimization

### Software Engineering
- Modular code architecture
- Performance profiling and optimization
- Version control (Git) and collaboration
- Documentation and technical writing

### Domain Expertise
- Sports analytics and tactical analysis
- Video processing workflows
- Real-time system design

---

## 📧 Contact & Links

**Author:** Hicham El Mehdi  
**Email:** mehdihicham736@gmail.com  
**LinkedIn:** [linkedin.com/in/elmehdihicham](https://linkedin.com/in/elmehdihicham)  
**GitHub:** [github.com/MehdiHCH](https://github.com/MehdiHCH)  

**Company Website:** [sportscore.tech](https://sportscore.tech) *(hypothetical)*  
**Project Repository:** [github.com/MehdiHCH/futsal-analysis](https://github.com/MehdiHCH/futsal-analysis)

---

*This project represents a significant step toward fully automated sports video analysis, combining cutting-edge AI with domain expertise to deliver actionable insights for coaches, analysts, and federations.*
