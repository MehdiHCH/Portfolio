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
    description: "Goal detection and validation"
date: 2025-04-01
company: SPORTSCORE
location: Paris, France (Remote)
duration: April 2025 - September 2025
---

## 🎯 Executive Summary

During my final-year internship at **SPORTSCORE**, I developed an intelligent end-to-end AI pipeline for **automated video analysis of futsal matches**. The system transforms raw multi-camera footage into structured tactical insights by automatically detecting, tracking, and classifying player actions such as passes, shots, dribbles, interceptions, and goals.

### 🏆 Key Achievements

- ✅ **99.95% accuracy** in frame classification
- ✅ **90.1% precision** in ball detection
- ✅ **80% reduction** in manual annotation workload
- ✅ **20% speedup** in processing time

---

## 🏢 Company Background: SPORTSCORE

**SPORTSCORE** is an innovative French company specializing in **real-time sports data exploitation** using AI and computer vision.

### What They Do

- 📊 Automatic extraction of key events and statistics
- 📈 Advanced tactical metrics generation
- 🎨 Interactive visualizations for analysts
- 🎥 Multi-sport video analysis solutions

### Target Clients

- Professional clubs and federations
- Video analysts and coaches
- Sports media and broadcasters
- Performance analysis teams

**Mission:** Transform sports through automation, precision, and speed of analysis.

---

## 🎯 Project Objectives

### Primary Goals

**1. Intelligent Frame Filtering**
   - Automatically exclude non-relevant sequences (replays, timeouts, transitions)
   - Reduce processing load and eliminate false positives
   - Focus computational resources on actual gameplay

**2. Automated Action Detection**
   - Detect and classify key actions: passes, shots, dribbles, interceptions
   - Generate structured event data in JSON format
   - Ensure real-time or near-real-time processing

**3. Tactical Visualizations**
   - Produce heatmaps showing player positioning
   - Generate pass maps and trajectory plots
   - Export comprehensive performance reports

**4. Reduce Manual Workload**
   - Minimize human annotation effort by 80%
   - Accelerate production of actionable insights
   - Enable scalable multi-match processing

---

## 🗃️ Technical Architecture

### System Overview

The pipeline consists of 6 interconnected modules that process video input sequentially:

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 1400" style="background: linear-gradient(135deg, #0d1117 0%, #1a1d29 100%);">
  <defs>
    <!-- Gradients -->
    <linearGradient id="blueGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00bfff;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#007bff;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="purpleGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#8a2be2;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#6a1bb2;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="greenGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00ff88;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#00cc66;stop-opacity:1" />
    </linearGradient>
    
    <!-- Glow effects -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <!-- Arrow marker -->
    <marker id="arrowBlue" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#00bfff" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="400" y="40" font-family="Arial, sans-serif" font-size="28" font-weight="bold" fill="url(#blueGrad)" text-anchor="middle">
    Futsal Analysis Pipeline
  </text>
  
  <!-- INPUT MODULE -->
  <g>
    <rect x="100" y="80" width="600" height="70" rx="10" fill="#1e1e2f" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <circle cx="130" cy="115" r="15" fill="url(#blueGrad)"/>
    <text x="130" y="121" font-size="20" fill="#fff" text-anchor="middle">🎥</text>
    <text x="160" y="110" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#00bfff">
      VIDEO INPUT
    </text>
    <text x="160" y="132" font-family="Arial, sans-serif" font-size="14" fill="#bbb">
      Multi-Camera Footage
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="150" x2="400" y2="190" stroke="#00bfff" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- MODULE 1: Frame Classification -->
  <g>
    <rect x="100" y="200" width="600" height="90" rx="10" fill="#1e1e2f" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <rect x="105" y="205" width="4" height="80" rx="2" fill="url(#blueGrad)"/>
    <circle cx="140" cy="230" r="18" fill="url(#blueGrad)"/>
    <text x="140" y="238" font-size="22" fill="#fff" text-anchor="middle">1</text>
    <text x="170" y="227" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#00bfff">
      MODULE 1: Frame Classification
    </text>
    <text x="170" y="250" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Model: YOLOv11m-cls
    </text>
    <text x="170" y="270" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ Filter relevant gameplay frames (99.95% accuracy)
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="290" x2="400" y2="330" stroke="#00bfff" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- MODULE 2: Object Detection & Tracking -->
  <g>
    <rect x="100" y="340" width="600" height="100" rx="10" fill="#1e1e2f" stroke="url(#purpleGrad)" stroke-width="2" filter="url(#glow)"/>
    <rect x="105" y="345" width="4" height="90" rx="2" fill="url(#purpleGrad)"/>
    <circle cx="140" cy="375" r="18" fill="url(#purpleGrad)"/>
    <text x="140" y="383" font-size="22" fill="#fff" text-anchor="middle">2</text>
    <text x="170" y="372" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#8a2be2">
      MODULE 2: Object Detection &amp; Tracking
    </text>
    <text x="170" y="395" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ YOLOv11x: Detect players &amp; ball (90.1% precision)
    </text>
    <text x="170" y="415" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ DeepSORT: Multi-object tracking with Re-ID
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="440" x2="400" y2="480" stroke="#8a2be2" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- MODULE 3: Spatial Projection -->
  <g>
    <rect x="100" y="490" width="600" height="90" rx="10" fill="#1e1e2f" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <rect x="105" y="495" width="4" height="80" rx="2" fill="url(#blueGrad)"/>
    <circle cx="140" cy="520" r="18" fill="url(#blueGrad)"/>
    <text x="140" y="528" font-size="22" fill="#fff" text-anchor="middle">3</text>
    <text x="170" y="517" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#00bfff">
      MODULE 3: Spatial Projection
    </text>
    <text x="170" y="540" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Homography: Pixel → Pitch coordinates
    </text>
    <text x="170" y="560" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ 2D tactical positioning &amp; distance calculation
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="580" x2="400" y2="620" stroke="#00bfff" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- MODULE 4: Player Re-Identification -->
  <g>
    <rect x="100" y="630" width="600" height="110" rx="10" fill="#1e1e2f" stroke="url(#purpleGrad)" stroke-width="2" filter="url(#glow)"/>
    <rect x="105" y="635" width="4" height="100" rx="2" fill="url(#purpleGrad)"/>
    <circle cx="140" cy="670" r="18" fill="url(#purpleGrad)"/>
    <text x="140" y="678" font-size="22" fill="#fff" text-anchor="middle">4</text>
    <text x="170" y="667" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#8a2be2">
      MODULE 4: Player Re-Identification
    </text>
    <text x="170" y="690" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ HSV Clustering: Team color detection
    </text>
    <text x="170" y="710" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ OCR: Jersey number recognition
    </text>
    <text x="170" y="730" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ Trajectory-based identity confirmation
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="740" x2="400" y2="780" stroke="#8a2be2" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- MODULE 5: Pose Estimation -->
  <g>
    <rect x="100" y="790" width="600" height="90" rx="10" fill="#1e1e2f" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <rect x="105" y="795" width="4" height="80" rx="2" fill="url(#blueGrad)"/>
    <circle cx="140" cy="820" r="18" fill="url(#blueGrad)"/>
    <text x="140" y="828" font-size="22" fill="#fff" text-anchor="middle">5</text>
    <text x="170" y="817" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#00bfff">
      MODULE 5: Pose Estimation
    </text>
    <text x="170" y="840" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ 17 Keypoints extraction (OpenPose/MediaPipe)
    </text>
    <text x="170" y="860" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ Gesture analysis for action validation
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="880" x2="400" y2="920" stroke="#00bfff" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- MODULE 6: Action Detection & Classification -->
  <g>
    <rect x="100" y="930" width="600" height="130" rx="10" fill="#1e1e2f" stroke="url(#purpleGrad)" stroke-width="2" filter="url(#glow)"/>
    <rect x="105" y="935" width="4" height="120" rx="2" fill="url(#purpleGrad)"/>
    <circle cx="140" cy="975" r="18" fill="url(#purpleGrad)"/>
    <text x="140" y="983" font-size="22" fill="#fff" text-anchor="middle">6</text>
    <text x="170" y="972" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#8a2be2">
      MODULE 6: Action Detection &amp; Classification
    </text>
    <text x="170" y="995" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Ball possession attribution (temporal buffer)
    </text>
    <text x="170" y="1015" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Pass detection: 7 types (Basic, Progressive, Key, Assist...)
    </text>
    <text x="170" y="1035" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Shot classification: On/Off target, Blocked
    </text>
    <text x="170" y="1055" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ Dribble, Interception, Goal confirmation
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="400" y1="1060" x2="400" y2="1100" stroke="#8a2be2" stroke-width="3" marker-end="url(#arrowBlue)"/>
  
  <!-- OUTPUT MODULE -->
  <g>
    <rect x="100" y="1110" width="600" height="130" rx="10" fill="#1e1e2f" stroke="url(#greenGrad)" stroke-width="2" filter="url(#glow)"/>
    <circle cx="130" cy="1155" r="18" fill="url(#greenGrad)"/>
    <text x="130" y="1163" font-size="22" fill="#fff" text-anchor="middle">📊</text>
    <text x="160" y="1142" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="#00ff88">
      OUTPUT: Structured Data + Visualizations
    </text>
    <text x="160" y="1165" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Event timeline with timestamps (JSON)
    </text>
    <text x="160" y="1185" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Player trajectories &amp; heatmaps
    </text>
    <text x="160" y="1205" font-family="Arial, sans-serif" font-size="13" fill="#888">
      ├─ Pass maps &amp; tactical statistics
    </text>
    <text x="160" y="1225" font-family="Arial, sans-serif" font-size="13" fill="#888">
      └─ Automated performance reports
    </text>
  </g>
  
  <!-- Footer Stats -->
  <g>
    <rect x="150" y="1270" width="150" height="60" rx="8" fill="rgba(0, 191, 255, 0.1)" stroke="#00bfff" stroke-width="1"/>
    <text x="225" y="1295" font-family="Arial, sans-serif" font-size="20" font-weight="bold" fill="#00bfff" text-anchor="middle">
      99.95%
    </text>
    <text x="225" y="1315" font-family="Arial, sans-serif" font-size="11" fill="#888" text-anchor="middle">
      Frame Accuracy
    </text>
    
    <rect x="325" y="1270" width="150" height="60" rx="8" fill="rgba(138, 43, 226, 0.1)" stroke="#8a2be2" stroke-width="1"/>
    <text x="400" y="1295" font-family="Arial, sans-serif" font-size="20" font-weight="bold" fill="#8a2be2" text-anchor="middle">
      90.1%
    </text>
    <text x="400" y="1315" font-family="Arial, sans-serif" font-size="11" fill="#888" text-anchor="middle">
      Ball Detection
    </text>
    
    <rect x="500" y="1270" width="150" height="60" rx="8" fill="rgba(0, 255, 136, 0.1)" stroke="#00ff88" stroke-width="1"/>
    <text x="575" y="1295" font-family="Arial, sans-serif" font-size="20" font-weight="bold" fill="#00ff88" text-anchor="middle">
      80%
    </text>
    <text x="575" y="1315" font-family="Arial, sans-serif" font-size="11" fill="#888" text-anchor="middle">
      Time Saved
    </text>
  </g>
  
  <!-- Watermark -->
  <text x="400" y="1370" font-family="Arial, sans-serif" font-size="12" fill="#fcf4f4ee" text-anchor="middle">
    SPORTSCORE © 2025 | Hicham El Mehdi
  </text>
</svg>

---

## ⚙️ Core Pipeline Components

### 1️⃣ Frame Classification Module

**Objective:** Filter out non-relevant frames to reduce processing overhead.

#### Architecture
- **Model:** YOLOv11m-cls fine-tuned for binary classification
- **Classes:**
  - `Main` - Gameplay sequences (useful for analysis)
  - `Other` - Replays, timeouts, crowd shots, transitions

#### Training Data
- **Total:** 67,801 annotated frames
- **Training set:** 54,240 frames (25,655 Main + 28,585 Other)
- **Validation set:** 13,561 frames (6,414 Main + 7,147 Other)

#### Performance Results

| Metric | Score |
|--------|-------|
| **Accuracy** | 99.95% |
| **Precision** | 99.91% |
| **Recall** | 100% |
| **False Positives** | 6 |
| **False Negatives** | 0 |

**Impact:** Reduced inference time from **19.98 min → 16.05 min** (~20% speedup)

---

### 2️⃣ Object Detection & Multi-Object Tracking

#### Detection System
**Model:** YOLOv11x custom-trained on futsal datasets

**Detected Classes:**
- Player
- Ball
- Referee
- Goal

**Ball Detection Performance (After Fine-tuning):**

| Metric | Score |
|--------|-------|
| **Precision** | 90.1% |
| **Recall** | 83.4% |
| **mAP@50** | 83.4% |
| **Inference Speed** | 9.6ms/frame (~4.7 FPS) |

#### Tracking System
**Algorithm:** DeepSORT with appearance-based association

**Components:**
- **Kalman Filter:** Motion prediction and state estimation
- **Deep Features:** OSNet for appearance-based Re-ID
- **Association:** Hungarian algorithm for optimal matching
- **Track Management:** Dynamic buffer and adaptive thresholds

**Challenges Addressed:**
- Ball often occluded or moving at high speed
- Created custom dataset with CVAT annotations from FIFA Futsal footage
- Temporal smoothing to fill detection gaps

---

### 3️⃣ Homography & Spatial Projection

**Purpose:** Convert pixel coordinates to real-world pitch coordinates

#### Process
1. **Detect pitch keypoints** (corners, circles, lines)
2. **Compute homography matrix** using perspective transformation
3. **Project positions** onto 2D pitch model

#### Benefits
- ✅ Enable distance calculations between players
- ✅ Validate actions based on pitch zones (penalty area, goal)
- ✅ Generate tactical heatmaps and pass maps
- ✅ Calculate speeds and distances traveled

---

### 4️⃣ Player Re-Identification (Re-ID)

**Multi-Modal Approach combining:**

#### 1. Team Detection
**Method:** HSV color clustering on jerseys
- Extract dominant colors from player bounding boxes
- Cluster into 2 teams based on color similarity
- Robust to lighting variations

#### 2. Jersey Number Recognition
**Tools:** PaddleOCR / Tesseract
- Extract ROI (Region of Interest) from player chest area
- Apply OCR with Tifinagh-trained models
- Validate using digit constraints (0-99)

#### 3. Trajectory Continuity
**Method:** DeepSORT feature matching
- Track player movements across frames
- Maintain identity despite occlusions
- Use appearance features for re-association

**Robustness:** Maintains player identity despite:
- ✅ Temporary occlusions
- ✅ Camera angle changes
- ✅ Posture variations
- ✅ Lighting changes

---

### 5️⃣ Pose Estimation & Keypoint Detection

**Model:** Pre-trained keypoint detector (OpenPose/MediaPipe)

#### Extracted Landmarks
- Head, shoulders, elbows, wrists
- Hips, knees, ankles, feet

#### Applications
- Detect shooting/passing gestures
- Determine striking foot (left/right)
- Validate action types (e.g., header vs. foot pass)
- Analyze player posture and body orientation

---

### 6️⃣ Action Detection & Classification

**Core Logic:** Spatio-temporal rule-based system

#### Ball Possession Attribution

**Methods Tested:**
1. Distance to player center
2. Distance to feet (via keypoints)
3. Distance to bounding box center
4. Distance to projected position

**Final Solution:** Temporal buffer + minimum distance heuristic

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

**Types Detected:**
- **Shot on Target:** Ball directed toward goal without interception
- **Shot off Target:** Ball misses goal frame
- **Blocked Shot:** Shot blocked by defender before reaching goal

#### Other Actions Detected

- **Dribble:** Possession maintained while moving >1.5m
- **Interception:** Opponent recovers pass attempt
- **Incomplete Pass:** Pass not received after 2 seconds (~60 frames)
- **Goal:** Ball enters goal mask zone with possession validation

---

## 🚀 Key Contributions

### Contribution 1: Intelligent Frame Classification

#### Before
- ❌ All frames processed indiscriminately
- ❌ High computational cost
- ❌ Many false positives from replays

#### After
- ✅ 99.95% classification accuracy
- ✅ 20% reduction in inference time
- ✅ Cleaner event sequences
- ✅ Better resource utilization

**Training Process:**
1. Manual annotation using CVAT
2. Fine-tuning YOLOv11m-cls (200 epochs)
3. Integration as first pipeline stage
4. Validation on diverse match footage

---

### Contribution 2: Advanced Action Detection System

**Developed from Scratch:**

```python
class ActionDetection:
    def __init__(self):
        self.possession_buffer = deque(maxlen=30)
        self.action_history = []
        
    def detect_pass(self, current_state, history):
        """Detect and classify passes"""
        # 7 types: Basic, Progressive, Into-Penalty, 
        # Pressure, Smart, Key, Assist
        pass
    
    def detect_shot(self, ball_trajectory, goal_mask):
        """Classify shots: on target, off target, blocked"""
        pass
    
    def validate_goal(self, ball_position, possession):
        """Confirm goal and attribute assist"""
        pass
```

**Logical Validation (Inspired by PoeClim):**
- Decision trees to verify actions post-detection
- Example: Goal validated only if ball enters goal mask without possession change
- Example: Assist attributed if goal preceded by Key/Smart/Progressive pass

---

### Contribution 3: Performance Optimization

#### Ball Detection Enhancement

**Custom Dataset:**
- Source: FIFA Futsal footage annotated in CVAT
- Fine-tuned YOLOv11x (100 epochs on RTX 3090)

**Results:**

| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| **Precision** | 75.3% | 90.1% | +15% |
| **Recall** | 68.7% | 83.4% | +14.7% |
| **mAP@50** | 70.2% | 83.4% | +13.2% |

**Impact:**
- ✅ Reliable ball tracking in critical zones (goal area)
- ✅ Accurate goal detection and assist attribution
- ✅ Reduced false negatives during fast plays

---

### Contribution 4: Structured Data Export

#### Output Formats

**JSON - Event Timeline:**
```json
{
  "event_id": 142,
  "type": "Progressive Pass",
  "timestamp": "12:34.56",
  "passer": {
    "id": 7,
    "team": "A",
    "position": [15.3, 22.1],
    "jersey_number": 7
  },
  "receiver": {
    "id": 10,
    "team": "A",
    "position": [28.7, 18.9],
    "jersey_number": 10
  },
  "outcome": "completed",
  "distance": 18.5,
  "duration": 1.2
}
```

**CSV - Tabular Statistics:**
- Player-wise action counts
- Team possession percentages
- Pass completion rates
- Shot accuracy metrics

**Visualizations:**
- Heatmaps (player positioning density)
- Pass maps (network diagrams)
- Trajectory plots (movement patterns)

---

## 📊 Results & Performance

### Quantitative Metrics

| Metric | Value | Impact |
|--------|-------|--------|
| **Frame Classification Accuracy** | 99.95% | Reduces processing time |
| **Ball Detection Precision** | 90.1% | Reliable goal detection |
| **Ball Detection Recall** | 83.4% | Minimal missed balls |
| **Processing Speed** | 4.7 FPS | Near real-time |
| **Inference Time Reduction** | 20% | Faster turnaround |
| **Manual Annotation Reduction** | 80% | Cost savings |

### Qualitative Impact

#### For Analysts
- ✅ **Automated Event Detection:** No manual tagging needed for passes/shots/goals
- ✅ **Consistent Data:** Eliminates human bias and subjectivity
- ✅ **Faster Insights:** Match analysis available within hours

#### For Coaches
- ✅ **Tactical Insights:** Heatmaps, pass networks, pressure zones
- ✅ **Player Performance:** Individual metrics for training focus
- ✅ **Opponent Analysis:** Patterns and weaknesses identification

#### For Technical Teams
- ✅ **Reliable Re-ID:** Players tracked consistently despite occlusions
- ✅ **Scalable:** Modular architecture ready for multi-match processing
- ✅ **Extensible:** Easy to add new action types

---

## 🛠️ Challenges & Solutions

### Challenge 1: Ball Detection in Critical Zones

#### Problem
- Ball often undetected near goal due to:
  - Small size + motion blur
  - Occlusion by goalkeeper/goalposts
  - High speed during shots

#### Solution
1. Created custom dataset from FIFA Futsal footage
2. Fine-tuned YOLOv11x with 100 epochs
3. Added temporal smoothing to fill detection gaps
4. Implemented ball trajectory prediction

**Result:** 90.1% precision enabling reliable goal confirmation

---

### Challenge 2: Tracking Instability

#### Problem
- DeepSORT ID switches during player collisions
- Ball tracking lost during occlusions
- Jersey numbers misread in poor lighting

#### Solution
1. Added temporal buffer for possession continuity
2. Integrated appearance features (OSNet) for Re-ID
3. Implemented Kalman filter predictions during gaps
4. Multi-modal approach (color + number + trajectory)

**Result:** Stable player identities across entire matches

---

### Challenge 3: Action Ambiguity

#### Problem
- Differentiating pass types (e.g., Smart vs Key pass)
- Validating incomplete passes vs interceptions
- Determining shot accuracy

#### Solution
- Defined strict spatio-temporal rules:
  - **Pressure Pass:** opponent <2m from passer
  - **Smart Pass:** receiver unmarked + attacking zone
  - **Key Pass:** followed by shot within 3 seconds
- Temporal validation windows (e.g., 60 frames for incomplete pass)
- Zone-based validation using homography

**Result:** Clear classification with minimal ambiguity

---

### Challenge 4: Processing Time

#### Problem
- Full match (40 min) took ~60 minutes to process
- Not scalable for multi-match analysis

#### Solution (Ongoing)
1. Implemented frame classification filter (20% speedup)
2. Prepared for multi-threading (batch processing)
3. Optimized data structures (dict → numpy arrays)
4. GPU optimization for inference

**Target:** Real-time processing (<1.5x match duration)

---

## 💼 Impact & Business Value

### For SPORTSCORE

#### Operational Benefits
- ✅ **80% reduction** in manual annotation workload
- ✅ **Scalability:** Can now process multiple matches simultaneously
- ✅ **Product Enhancement:** Automated reports add value to offerings
- ✅ **Competitive Edge:** Faster turnaround than manual analysis services

#### Business Metrics
- 📈 **Cost Savings:** ~€10,000/month in annotation costs
- 🚀 **Throughput:** 5x more matches processed
- 💰 **Revenue Growth:** New clients attracted by automation
- 🎯 **Market Position:** Technology leader in futsal analytics

---

### For Clients (Clubs, Analysts, Federations)

#### Tactical Advantages
- ✅ **Instant Insights:** Match analysis available within hours (vs days)
- ✅ **Objective Data:** Eliminates human bias in event tagging
- ✅ **Tactical Intelligence:** Heatmaps, pass networks, pressure zones
- ✅ **Player Development:** Individual performance metrics for training

#### Use Cases
- 🎯 **Post-Match Analysis:** Identify tactical strengths/weaknesses
- 📊 **Scouting:** Evaluate potential recruits objectively
- 🏆 **Competition Prep:** Analyze opponent patterns
- 📈 **Performance Tracking:** Monitor player progression over time

---

## 🔮 Future Perspectives

### Short-Term Improvements (3-6 months)

#### 1. Real-Time Processing
- Optimize for <1.5x match duration
- Implement GPU batch processing
- Add multi-threading for parallel module execution
- Target: Process 40-min match in <60 minutes

#### 2. Enhanced Ball Tracking
- Integrate TrackNetV2 for ball trajectory prediction
- Add segmentation-based detection for occluded ball
- Improve detection in goal area (currently 83.4% recall)

#### 3. Advanced Action Recognition
- Train deep learning model (Transformer-based) for action spotting
- Incorporate temporal context (xLSTM encoder)
- Improve pass classification accuracy (current: rule-based)

---

### Long-Term Vision (1-2 years)

#### 1. Multi-Sport Extension
- Adapt pipeline for basketball, handball, hockey
- Transfer learning from futsal model
- Sport-specific action detection modules

#### 2. Live Streaming Integration
- Real-time event detection during broadcast
- Automated highlight generation
- Live tactical dashboards for coaches

#### 3. 3D Reconstruction
- Multi-camera calibration for 3D player positioning
- Depth estimation for offside detection
- Volumetric capture for immersive replays

#### 4. Predictive Analytics
- **Expected Goals (xG)** model based on shot context
- **Pass success probability** using historical data
- **Tactical pattern recognition** (e.g., pressing schemes)
- **Match outcome prediction** using team metrics

---

## 🛠️ Technical Stack

### Deep Learning Frameworks
- **PyTorch 2.0** - Model training and inference
- **Ultralytics YOLOv11** - Object detection
- **TensorFlow/Keras** - Supplementary models

### Computer Vision Libraries
- **OpenCV** - Video processing, homography
- **DeepSORT** - Multi-object tracking
- **PaddleOCR** - Jersey number recognition
- **Tesseract** - Backup OCR engine

### Data Processing
- **NumPy** - Numerical operations
- **Pandas** - Data structuring
- **JSON** - Event serialization

### Annotation & Training Tools
- **CVAT** - Video annotation tool
- **Roboflow** - Dataset management
- **Weights & Biases** - Experiment tracking
- **TensorBoard** - Training visualization

### Hardware
- **NVIDIA RTX 3090** (24GB VRAM) - Training
- **NVIDIA RTX 4060** (8GB VRAM) - Inference
- **AMD Ryzen 7 5700X** - CPU processing

---

## 🎓 Skills Developed

### Technical Skills
- ✅ Advanced computer vision (detection, tracking, homography)
- ✅ Deep learning model fine-tuning (YOLO, CNNs)
- ✅ Multi-object tracking algorithms (DeepSORT, Kalman Filter)
- ✅ Spatio-temporal reasoning and action recognition
- ✅ Data pipeline design and optimization

### Software Engineering
- ✅ Modular code architecture
- ✅ Performance profiling and optimization
- ✅ Version control (Git) and collaboration
- ✅ Documentation and technical writing

### Domain Expertise
- ✅ Sports analytics and tactical analysis
- ✅ Video processing workflows
- ✅ Real-time system design

---

## 📚 References & Related Work

This project builds upon state-of-the-art research in sports video analysis:

1. **PoeClim** (Mohtaram et al., 2025): Spatio-temporal framework for action spotting
2. **Deep-EIoU** (Huang et al., 2024): Advanced multi-object tracking
3. **YOLOv11** (Ultralytics, 2024): Latest YOLO architecture
4. **DeepSORT** (Wojke et al., 2017): Deep association metric tracking
5. **TrackNetV2** (Huang et al., 2022): Ball tracking in sports videos

---

## 👨‍💻 About This Project

**Duration:** April 2025 - September 2025  
**Type:** Final-Year Internship (Master's in Artificial Intelligence)  
**Institution:** Ibn Tofail University, Faculty of Sciences, Kenitra  
**Company:** SPORTSCORE (Paris, France - Remote)  
**Supervisor:** Mr. Noureddine Mohtaram (SPORTSCORE)  
**Academic Supervisor:** Mr. Anass Nouri (FSK, Ibn Tofail University)

### Jury Members
- Mr. Anass Nouri (FSK, Ibn Tofail University)
- Mrs. Khadija Lekdioui (FSK, Ibn Tofail University)
- Mrs. Khaoula Boukir (ENSC, Ibn Tofail University)

**Defense Date:** September 15, 2025

---

## 📧 Contact & Links

**Author:** Hicham El Mehdi  
**Email:** mehdihicham736@gmail.com  
**LinkedIn:** [linkedin.com/in/elmehdihicham](https://linkedin.com/in/elmehdihicham)  
**GitHub:** [github.com/MehdiHCH](https://github.com/MehdiHCH)  

**Company Website:** [sportscore.tech](https://sportscore.tech)  
**Project Repository:** [github.com/MehdiHCH/futsal-analysis](https://github.com/MehdiHCH/futsal-analysis)

---

*This project represents a significant step toward fully automated sports video analysis, combining cutting-edge AI with domain expertise to deliver actionable insights for coaches, analysts, and federations.*