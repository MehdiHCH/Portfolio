---
title: Automated Futsal Video Analysis for Performance Reporting
image: /assets/img/projects/SportScore.gif
description: End-to-end AI pipeline for automated detection, tracking, and classification of player actions in futsal matches. Achieved 88% system accuracy with 46.7% performance gain through advanced parallelization and optimization techniques.
category: sports-analytics
order: 1
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
  - CUDA
  - TensorRT
  - Parallel Processing
demos:
  - title: "Frame Classification"
    video: /assets/videos/sportscore/Class.mp4
    description: "Automated filtering of relevant gameplay sequences (99.95% accuracy)"
  - title: "Action Detection & Classification"
    video: /assets/videos/sportscore/Action_detection.mp4
    description: "Real-time detection of passes, shots, dribbles, and goals"
  - title: "Object Detection (Goal Recognition)"
    video: /assets/videos/sportscore/IS_But.mp4
    description: "Goal detection and validation with ball tracking"
date: 2025-04-01
company: SPORTSCORE
location: Paris, France (Remote)
duration: April 2025 - October 2025
---

## 🎯 Executive Summary

During my **7-month final-year internship** at **SPORTSCORE** (April - October 2025), I developed an intelligent end-to-end AI pipeline for **automated video analysis of futsal matches**. The system transforms raw multi-camera footage into structured tactical insights by automatically detecting, tracking, and classifying player actions such as passes, shots, dribbles, interceptions, and goals.

This project involved **two major technical contributions**:
1. **Complete parallelization** of the processing pipeline with CUDA Streams and TensorRT
2. **From-scratch development** of an intelligent action detection module

### 🏆 Key Achievements

#### Performance Metrics
- ✅ **88% global system accuracy** across all action types
- ✅ **100% precision** on pass detection
- ✅ **99.95% accuracy** in frame classification (YOLOv11m-cls)
- ✅ **90.1% precision** in ball detection (fine-tuned YOLOv11x)
- ✅ **83.4% recall** on ball tracking (mAP@50)

#### Optimization Results
- 🚀 **+46.7% performance gain** through parallelization
- 🚀 **×1.88 speedup** (22:57 → 12:12 for 1:14 video)
- 🚀 **33% frames automatically filtered** (non-relevant sequences)
- 🚀 **2-2.5× inference speedup** with TensorRT optimization

#### Business Impact
- 💼 **80% reduction** in manual annotation workload
- 💼 **5× increase** in match processing throughput
- 💼 **€10,000/month** estimated cost savings

---

## 📅 Project Timeline

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1400 350" style="background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);">
  <defs>
    <linearGradient id="timelineGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#00d4ff;stop-opacity:1" />
      <stop offset="25%" style="stop-color:#7c3aed;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#ec4899;stop-opacity:1" />
      <stop offset="75%" style="stop-color:#f59e0b;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glowTimeline" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <filter id="shadowTimeline">
      <feDropShadow dx="0" dy="2" stdDeviation="4" flood-opacity="0.3"/>
    </filter>
  </defs>
  
  <!-- Title -->
  <text x="700" y="50" font-family="'SF Pro Display', 'Segoe UI', Arial, sans-serif" font-size="32" font-weight="700" fill="#ffffff" text-anchor="middle" filter="url(#shadowTimeline)">
    Project Timeline: April - October 2025
  </text>
  
  <!-- Timeline base line -->
  <line x1="150" y1="170" x2="1250" y2="170" stroke="url(#timelineGrad)" stroke-width="6" stroke-linecap="round" filter="url(#glowTimeline)"/>
  
  <!-- Phase 1: April 2025 -->
  <g transform="translate(150, 170)">
    <circle r="18" fill="#00d4ff" filter="url(#glowTimeline)"/>
    <circle r="12" fill="#0a1929" opacity="0.8"/>
    <text y="-45" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#00d4ff" text-anchor="middle">APR 2025</text>
    <text y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#e5e7eb" text-anchor="middle">Pipeline</text>
    <text y="80" font-family="'SF Pro Display', Arial" font-size="14" fill="#9ca3af" text-anchor="middle">Setup</text>
    <!-- Icon -->
    <text y="8" font-size="18" text-anchor="middle">🔧</text>
  </g>
  
  <!-- Phase 2: May 2025 -->
  <g transform="translate(370, 170)">
    <circle r="18" fill="#7c3aed" filter="url(#glowTimeline)"/>
    <circle r="12" fill="#0a1929" opacity="0.8"/>
    <text y="-45" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#7c3aed" text-anchor="middle">MAY 2025</text>
    <text y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#e5e7eb" text-anchor="middle">Frame</text>
    <text y="80" font-family="'SF Pro Display', Arial" font-size="14" fill="#9ca3af" text-anchor="middle">Classification</text>
    <text y="100" font-family="'SF Pro Display', Arial" font-size="12" fill="#6366f1" text-anchor="middle" font-weight="600">99.95%</text>
    <text y="8" font-size="18" text-anchor="middle">🎯</text>
  </g>
  
  <!-- Phase 3: June 2025 -->
  <g transform="translate(590, 170)">
    <circle r="18" fill="#ec4899" filter="url(#glowTimeline)"/>
    <circle r="12" fill="#0a1929" opacity="0.8"/>
    <text y="-45" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#ec4899" text-anchor="middle">JUN 2025</text>
    <text y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#e5e7eb" text-anchor="middle">Parallelization</text>
    <text y="80" font-family="'SF Pro Display', Arial" font-size="14" fill="#9ca3af" text-anchor="middle">CUDA + TensorRT</text>
    <text y="100" font-family="'SF Pro Display', Arial" font-size="12" fill="#ec4899" text-anchor="middle" font-weight="600">+46.7%</text>
    <text y="8" font-size="18" text-anchor="middle">⚡</text>
  </g>
  
  <!-- Phase 4: July 2025 -->
  <g transform="translate(810, 170)">
    <circle r="18" fill="#f59e0b" filter="url(#glowTimeline)"/>
    <circle r="12" fill="#0a1929" opacity="0.8"/>
    <text y="-45" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#f59e0b" text-anchor="middle">JUL 2025</text>
    <text y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#e5e7eb" text-anchor="middle">Action Detection</text>
    <text y="80" font-family="'SF Pro Display', Arial" font-size="14" fill="#9ca3af" text-anchor="middle">1208 lines</text>
    <text y="100" font-family="'SF Pro Display', Arial" font-size="12" fill="#f59e0b" text-anchor="middle" font-weight="600">11 actions</text>
    <text y="8" font-size="18" text-anchor="middle">🎬</text>
  </g>
  
  <!-- Phase 5: August 2025 -->
  <g transform="translate(1030, 170)">
    <circle r="18" fill="#10b981" filter="url(#glowTimeline)"/>
    <circle r="12" fill="#0a1929" opacity="0.8"/>
    <text y="-45" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#10b981" text-anchor="middle">AUG 2025</text>
    <text y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#e5e7eb" text-anchor="middle">Ball Detection</text>
    <text y="80" font-family="'SF Pro Display', Arial" font-size="14" fill="#9ca3af" text-anchor="middle">Fine-tuning</text>
    <text y="100" font-family="'SF Pro Display', Arial" font-size="12" fill="#10b981" text-anchor="middle" font-weight="600">90.1%</text>
    <text y="8" font-size="18" text-anchor="middle">⚽</text>
  </g>
  
  <!-- Phase 6: October 2025 -->
  <g transform="translate(1250, 170)">
    <circle r="18" fill="#06b6d4" filter="url(#glowTimeline)"/>
    <circle r="12" fill="#0a1929" opacity="0.8"/>
    <text y="-45" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#06b6d4" text-anchor="middle">OCT 2025</text>
    <text y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#e5e7eb" text-anchor="middle">Integration</text>
    <text y="80" font-family="'SF Pro Display', Arial" font-size="14" fill="#9ca3af" text-anchor="middle">&amp; Deployment</text>
    <text y="100" font-family="'SF Pro Display', Arial" font-size="12" fill="#06b6d4" text-anchor="middle" font-weight="600">88% acc</text>
    <text y="8" font-size="18" text-anchor="middle">🚀</text>
  </g>
  
  <!-- Legend boxes -->
  <g transform="translate(300, 280)">
    <rect width="200" height="35" rx="8" fill="#00d4ff" opacity="0.15" stroke="#00d4ff" stroke-width="1.5"/>
    <text x="100" y="23" font-family="'SF Pro Display', Arial" font-size="13" fill="#00d4ff" text-anchor="middle" font-weight="600">Setup &amp; Research</text>
  </g>
  
  <g transform="translate(520, 280)">
    <rect width="180" height="35" rx="8" fill="#7c3aed" opacity="0.15" stroke="#7c3aed" stroke-width="1.5"/>
    <text x="90" y="23" font-family="'SF Pro Display', Arial" font-size="13" fill="#7c3aed" text-anchor="middle" font-weight="600">Development</text>
  </g>
  
  <g transform="translate(720, 280)">
    <rect width="180" height="35" rx="8" fill="#f59e0b" opacity="0.15" stroke="#f59e0b" stroke-width="1.5"/>
    <text x="90" y="23" font-family="'SF Pro Display', Arial" font-size="13" fill="#f59e0b" text-anchor="middle" font-weight="600">Optimization</text>
  </g>
  
  <g transform="translate(920, 280)">
    <rect width="180" height="35" rx="8" fill="#10b981" opacity="0.15" stroke="#10b981" stroke-width="1.5"/>
    <text x="90" y="23" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" text-anchor="middle" font-weight="600">Deployment</text>
  </g>
</svg>

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

**3. Pipeline Optimization**
   - Implement parallelization techniques (CUDA Streams, TensorRT)
   - Reduce processing time by 40%+
   - Enable scalable multi-match processing

**4. Tactical Visualizations**
   - Produce heatmaps showing player positioning
   - Generate pass maps and trajectory plots
   - Export comprehensive performance reports

**5. Reduce Manual Workload**
   - Minimize human annotation effort by 80%
   - Accelerate production of actionable insights

---

## 🏗️ Technical Architecture

### System Overview

The pipeline consists of **7 interconnected modules** that process video input sequentially, with a foundational parallelization layer ensuring optimal performance:

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 1800" style="background: linear-gradient(135deg, #0a0e1a 0%, #1a1d29 100%);">
  <defs>
    <!-- Modern Gradients -->
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00d4ff;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#0891b2;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="grad2" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#7c3aed;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#5b21b6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="grad3" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#ec4899;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#be185d;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="grad4" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f59e0b;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#d97706;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="grad5" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#10b981;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#059669;stop-opacity:1" />
    </linearGradient>
    
    <!-- Enhanced Glow -->
    <filter id="glowPipe" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="5" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <!-- Shadow -->
    <filter id="shadow">
      <feDropShadow dx="0" dy="4" stdDeviation="6" flood-opacity="0.4"/>
    </filter>
    
    <!-- Arrow marker -->
    <marker id="arrowhead" markerWidth="12" markerHeight="12" refX="11" refY="6" orient="auto">
      <polygon points="0 0, 12 6, 0 12" fill="#00d4ff" opacity="0.8"/>
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="450" y="50" font-family="'SF Pro Display', 'Segoe UI', Arial" font-size="36" font-weight="700" fill="#ffffff" text-anchor="middle" filter="url(#shadow)">
    Pipeline Architecture
  </text>
  
  <!-- INPUT -->
  <g transform="translate(0, 100)">
    <rect x="150" width="600" height="80" rx="12" fill="url(#grad1)" opacity="0.15" stroke="url(#grad1)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <circle cx="190" cy="40" r="22" fill="url(#grad1)" filter="url(#glowPipe)"/>
    <text x="190" y="48" font-size="24" text-anchor="middle">🎥</text>
    <text x="230" y="35" font-family="'SF Pro Display', Arial" font-size="20" font-weight="600" fill="#00d4ff">VIDEO INPUT</text>
    <text x="230" y="58" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8">Multi-Camera Futsal Footage</text>
  </g>
  
  <!-- Arrow -->
  <line x1="450" y1="180" x2="450" y2="230" stroke="#00d4ff" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 0: Parallelization -->
  <g transform="translate(0, 240)">
    <rect x="100" width="700" height="120" rx="12" fill="url(#grad4)" opacity="0.12" stroke="url(#grad4)" stroke-width="3" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="110" rx="2.5" fill="url(#grad4)"/>
    <circle cx="150" cy="55" r="24" fill="url(#grad4)" filter="url(#glowPipe)"/>
    <text x="150" y="63" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">⚡</text>
    <text x="190" y="40" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#f59e0b">MODULE 0: Parallelization Layer</text>
    <text x="190" y="65" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ CUDA Streams (4 parallel GPU streams)</text>
    <text x="190" y="85" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ TensorRT: 2-2.5× inference speedup</text>
    <text x="190" y="105" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ Result: +46.7% gain, ×1.88 speedup</text>
  </g>
  
  <line x1="450" y1="360" x2="450" y2="410" stroke="#f59e0b" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 1: Frame Classification -->
  <g transform="translate(0, 420)">
    <rect x="100" width="700" height="100" rx="12" fill="url(#grad1)" opacity="0.12" stroke="url(#grad1)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="90" rx="2.5" fill="url(#grad1)"/>
    <circle cx="150" cy="50" r="24" fill="url(#grad1)" filter="url(#glowPipe)"/>
    <text x="150" y="58" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">1</text>
    <text x="190" y="38" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#00d4ff">MODULE 1: Frame Classification</text>
    <text x="190" y="60" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ YOLOv11m-cls (67,801 images trained)</text>
    <text x="190" y="80" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ 99.95% accuracy, 33% frames filtered</text>
  </g>
  
  <line x1="450" y1="520" x2="450" y2="570" stroke="#00d4ff" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 2: Detection & Tracking -->
  <g transform="translate(0, 580)">
    <rect x="100" width="700" height="110" rx="12" fill="url(#grad2)" opacity="0.12" stroke="url(#grad2)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="100" rx="2.5" fill="url(#grad2)"/>
    <circle cx="150" cy="55" r="24" fill="url(#grad2)" filter="url(#glowPipe)"/>
    <text x="150" y="63" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">2</text>
    <text x="190" y="40" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#7c3aed">MODULE 2: Detection &amp; Tracking</text>
    <text x="190" y="62" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ YOLOv11x fine-tuned: 90.1% precision</text>
    <text x="190" y="82" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ DeepSORT: Multi-object tracking</text>
  </g>
  
  <line x1="450" y1="690" x2="450" y2="740" stroke="#7c3aed" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 3: Homography -->
  <g transform="translate(0, 750)">
    <rect x="100" width="700" height="100" rx="12" fill="url(#grad1)" opacity="0.12" stroke="url(#grad1)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="90" rx="2.5" fill="url(#grad1)"/>
    <circle cx="150" cy="50" r="24" fill="url(#grad1)" filter="url(#glowPipe)"/>
    <text x="150" y="58" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">3</text>
    <text x="190" y="38" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#00d4ff">MODULE 3: Spatial Projection</text>
    <text x="190" y="60" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ Homography: Pixel → Pitch coords</text>
    <text x="190" y="80" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ 2D tactical positioning</text>
  </g>
  
  <line x1="450" y1="850" x2="450" y2="900" stroke="#00d4ff" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 4: Re-ID -->
  <g transform="translate(0, 910)">
    <rect x="100" width="700" height="110" rx="12" fill="url(#grad2)" opacity="0.12" stroke="url(#grad2)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="100" rx="2.5" fill="url(#grad2)"/>
    <circle cx="150" cy="55" r="24" fill="url(#grad2)" filter="url(#glowPipe)"/>
    <text x="150" y="63" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">4</text>
    <text x="190" y="40" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#7c3aed">MODULE 4: Player Re-ID</text>
    <text x="190" y="62" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ HSV Clustering: Team assignment</text>
    <text x="190" y="82" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ OCR: Jersey number recognition</text>
  </g>
  
  <line x1="450" y1="1020" x2="450" y2="1070" stroke="#7c3aed" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 5: Pose -->
  <g transform="translate(0, 1080)">
    <rect x="100" width="700" height="100" rx="12" fill="url(#grad1)" opacity="0.12" stroke="url(#grad1)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="90" rx="2.5" fill="url(#grad1)"/>
    <circle cx="150" cy="50" r="24" fill="url(#grad1)" filter="url(#glowPipe)"/>
    <text x="150" y="58" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">5</text>
    <text x="190" y="38" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#00d4ff">MODULE 5: Pose Estimation</text>
    <text x="190" y="60" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ 17 keypoints per player</text>
    <text x="190" y="80" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ Posture analysis for actions</text>
  </g>
  
  <line x1="450" y1="1180" x2="450" y2="1230" stroke="#00d4ff" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- MODULE 6: Action Detection -->
  <g transform="translate(0, 1240)">
    <rect x="100" width="700" height="140" rx="12" fill="url(#grad5)" opacity="0.12" stroke="url(#grad5)" stroke-width="3" filter="url(#glowPipe)"/>
    <rect x="105" y="5" width="5" height="130" rx="2.5" fill="url(#grad5)"/>
    <circle cx="150" cy="70" r="24" fill="url(#grad5)" filter="url(#glowPipe)"/>
    <text x="150" y="78" font-size="22" font-weight="700" fill="#ffffff" text-anchor="middle">6</text>
    <text x="190" y="45" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#10b981">MODULE 6: Action Detection</text>
    <text x="190" y="67" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">ActionDetector.py - 1208 lines</text>
    <text x="190" y="87" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ 8 Pass Types (Basic, Progressive, Key, Assist...)</text>
    <text x="190" y="107" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ 3 Shot Types + Defense + Dribbles</text>
    <text x="190" y="127" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ 88% accuracy, 100% on passes</text>
  </g>
  
  <line x1="450" y1="1380" x2="450" y2="1430" stroke="#10b981" stroke-width="3" marker-end="url(#arrowhead)" opacity="0.6"/>
  
  <!-- OUTPUT -->
  <g transform="translate(0, 1440)">
    <rect x="150" width="600" height="120" rx="12" fill="url(#grad5)" opacity="0.15" stroke="url(#grad5)" stroke-width="2.5" filter="url(#glowPipe)"/>
    <circle cx="190" cy="60" r="22" fill="url(#grad5)" filter="url(#glowPipe)"/>
    <text x="190" y="68" font-size="24" text-anchor="middle">📊</text>
    <text x="230" y="45" font-family="'SF Pro Display', Arial" font-size="20" font-weight="600" fill="#10b981">STRUCTURED OUTPUTS</text>
    <text x="230" y="70" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8">├─ JSON: actions_data.json</text>
    <text x="230" y="90" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8">├─ Heatmaps: Pass networks, shot zones</text>
    <text x="230" y="110" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8">└─ Video: Annotated footage</text>
  </g>
  
  <!-- Performance badges -->
  <rect x="200" y="1600" width="500" height="60" rx="30" fill="#f59e0b" opacity="0.2" stroke="#f59e0b" stroke-width="2"/>
  <text x="450" y="1638" font-family="'SF Pro Display', Arial" font-size="20" font-weight="700" fill="#f59e0b" text-anchor="middle">
    ⚡ +46.7% Performance | ×1.88 Speedup
  </text>
  
  <rect x="200" y="1680" width="500" height="60" rx="30" fill="#10b981" opacity="0.2" stroke="#10b981" stroke-width="2"/>
  <text x="450" y="1718" font-family="'SF Pro Display', Arial" font-size="20" font-weight="700" fill="#10b981" text-anchor="middle">
    ✅ 88% Global Accuracy | 100% Pass Detection
  </text>
</svg>

---

## 🚀 Contribution 1: Pipeline Parallelization

### 📁 File: `parallel_tracker.py` (1,041 lines)

Complete optimization of the original tracker integrating three major optimizations.

### Performance Comparison

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 500" style="background: linear-gradient(135deg, #0a0e1a 0%, #1a1d29 100%);">
  <defs>
    <linearGradient id="barGrad1" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#ef4444;stop-opacity:0.8" />
      <stop offset="100%" style="stop-color:#dc2626;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="barGrad2" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#10b981;stop-opacity:0.8" />
      <stop offset="100%" style="stop-color:#059669;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glowBar">
      <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Title -->
  <text x="600" y="50" font-family="'SF Pro Display', Arial" font-size="32" font-weight="700" fill="#ffffff" text-anchor="middle">
    Before vs After Optimization
  </text>
  
  <!-- Y-axis labels -->
  <text x="80" y="120" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">25 min</text>
  <text x="80" y="200" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">20 min</text>
  <text x="80" y="280" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">15 min</text>
  <text x="80" y="360" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">10 min</text>
  <text x="80" y="440" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">5 min</text>
  
  <!-- Grid lines -->
  <line x1="100" y1="120" x2="1100" y2="120" stroke="#334155" stroke-width="1" opacity="0.3"/>
  <line x1="100" y1="200" x2="1100" y2="200" stroke="#334155" stroke-width="1" opacity="0.3"/>
  <line x1="100" y1="280" x2="1100" y2="280" stroke="#334155" stroke-width="1" opacity="0.3"/>
  <line x1="100" y1="360" x2="1100" y2="360" stroke="#334155" stroke-width="1" opacity="0.3"/>
  <line x1="100" y1="440" x2="1100" y2="440" stroke="#334155" stroke-width="1" opacity="0.3"/>
  
  <!-- Bar 1: Original (22:57 ≈ 23 min) -->
  <rect x="250" y="125" width="180" height="315" rx="8" fill="url(#barGrad1)" filter="url(#glowBar)" opacity="0.9"/>
  <text x="340" y="460" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#ef4444" text-anchor="middle">Original</text>
  <text x="340" y="480" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">tracker.py</text>
  <text x="340" y="280" font-family="'SF Pro Display', Arial" font-size="28" font-weight="700" fill="#ffffff" text-anchor="middle">22:57</text>
  
  <!-- Bar 2: Optimized (12:12 ≈ 12 min) -->
  <rect x="550" y="270" width="180" height="170" rx="8" fill="url(#barGrad2)" filter="url(#glowBar)" opacity="0.9"/>
  <text x="640" y="460" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#10b981" text-anchor="middle">Optimized</text>
  <text x="640" y="480" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">parallel_tracker.py</text>
  <text x="640" y="365" font-family="'SF Pro Display', Arial" font-size="28" font-weight="700" fill="#ffffff" text-anchor="middle">12:12</text>
  
  <!-- Improvement arrow and label -->
  <path d="M 450 280 Q 500 240, 550 270" stroke="#fbbf24" stroke-width="3" fill="none" stroke-dasharray="5,5"/>
  <polygon points="550,270 543,265 543,275" fill="#fbbf24"/>
  <rect x="450" y="210" width="120" height="50" rx="10" fill="#fbbf24" opacity="0.2"/>
  <text x="510" y="230" font-family="'SF Pro Display', Arial" font-size="16" font-weight="700" fill="#fbbf24" text-anchor="middle">+46.7%</text>
  <text x="510" y="248" font-family="'SF Pro Display', Arial" font-size="13" fill="#fbbf24" text-anchor="middle">Faster</text>
  
  <!-- Metrics boxes -->
  <g transform="translate(850, 150)">
    <rect width="280" height="100" rx="12" fill="#7c3aed" opacity="0.15" stroke="#7c3aed" stroke-width="2"/>
    <text x="140" y="35" font-family="'SF Pro Display', Arial" font-size="36" font-weight="700" fill="#7c3aed" text-anchor="middle">×1.88</text>
    <text x="140" y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">Speedup Factor</text>
    <text x="140" y="80" font-family="'SF Pro Display', Arial" font-size="12" fill="#64748b" text-anchor="middle">Nearly 2× faster processing</text>
  </g>
  
  <g transform="translate(850, 280)">
    <rect width="280" height="100" rx="12" fill="#ec4899" opacity="0.15" stroke="#ec4899" stroke-width="2"/>
    <text x="140" y="35" font-family="'SF Pro Display', Arial" font-size="36" font-weight="700" fill="#ec4899" text-anchor="middle">-47%</text>
    <text x="140" y="60" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">Time Reduction</text>
    <text x="140" y="80" font-family="'SF Pro Display', Arial" font-size="12" fill="#64748b" text-anchor="middle">10:45 minutes saved</text>
  </g>
</svg>

### Optimization Techniques

| Optimization | Implementation | Result |
|--------------|----------------|--------|
| **CUDA Streams** | 4 parallel GPU streams for model loading | 10-15 sec saved at startup |
| **Frame Classification** | Skip 33% non-relevant frames (replays, ads) | 5-7 minutes saved per video |
| **TensorRT Integration** | Optimized inference engines | 2-2.5× speedup (45-60 FPS) |

---

## 🎯 Contribution 2: Action Detection Module

### 📁 File: `ActionDetector.py` (1,208 lines)

Complete class developed from scratch implementing detection and classification of **11 different action types**.

### Action Detection Workflow

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 900" style="background: linear-gradient(135deg, #0a0e1a 0%, #1a1d29 100%);">
  <defs>
    <linearGradient id="flowGrad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#00d4ff;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#7c3aed;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glowFlow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <marker id="arrowFlow" markerWidth="10" markerHeight="10" refX="9" refY="5" orient="auto">
      <path d="M0,0 L10,5 L0,10 z" fill="#00d4ff"/>
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="500" y="50" font-family="'SF Pro Display', Arial" font-size="32" font-weight="700" fill="#ffffff" text-anchor="middle">
    Action Detection Logic Flow
  </text>
  
  <!-- Start node -->
  <rect x="400" y="100" width="200" height="60" rx="30" fill="#00d4ff" opacity="0.2" stroke="#00d4ff" stroke-width="2.5" filter="url(#glowFlow)"/>
  <text x="500" y="137" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#00d4ff" text-anchor="middle">Possession Tracking</text>
  
  <line x1="500" y1="160" x2="500" y2="210" stroke="#00d4ff" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  
  <!-- Decision diamond -->
  <path d="M 500 210 L 600 280 L 500 350 L 400 280 Z" fill="#7c3aed" opacity="0.15" stroke="#7c3aed" stroke-width="2.5" filter="url(#glowFlow)"/>
  <text x="500" y="287" font-family="'SF Pro Display', Arial" font-size="15" font-weight="600" fill="#7c3aed" text-anchor="middle">Change</text>
  <text x="500" y="305" font-family="'SF Pro Display', Arial" font-size="15" font-weight="600" fill="#7c3aed" text-anchor="middle">Detected?</text>
  
  <!-- Left branch: PASS -->
  <line x1="400" y1="280" x2="250" y2="280" stroke="#10b981" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  <text x="325" y="265" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">Yes</text>
  
  <rect x="100" y="250" width="150" height="60" rx="10" fill="#10b981" opacity="0.2" stroke="#10b981" stroke-width="2.5" filter="url(#glowFlow)"/>
  <text x="175" y="288" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#10b981" text-anchor="middle">PASS</text>
  
  <line x1="175" y1="310" x2="175" y2="390" stroke="#10b981" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  
  <!-- Pass classification -->
  <rect x="80" y="400" width="190" height="120" rx="10" fill="#10b981" opacity="0.15" stroke="#10b981" stroke-width="2"/>
  <text x="175" y="430" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#10b981" text-anchor="middle">Classification</text>
  <text x="90" y="455" font-family="'SF Pro Display', Arial" font-size="12" fill="#94a3b8">• Progressive</text>
  <text x="90" y="475" font-family="'SF Pro Display', Arial" font-size="12" fill="#94a3b8">• Key Pass</text>
  <text x="90" y="495" font-family="'SF Pro Display', Arial" font-size="12" fill="#94a3b8">• Smart Pass</text>
  <text x="90" y="515" font-family="'SF Pro Display', Arial" font-size="12" fill="#94a3b8">• Assist (if goal)</text>
  
  <!-- Right branch: DRIBBLE -->
  <line x1="600" y1="280" x2="750" y2="280" stroke="#f59e0b" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  <text x="675" y="265" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">No</text>
  
  <rect x="675" y="250" width="150" height="60" rx="10" fill="#f59e0b" opacity="0.2" stroke="#f59e0b" stroke-width="2.5" filter="url(#glowFlow)"/>
  <text x="750" y="288" font-family="'SF Pro Display', Arial" font-size="16" font-weight="600" fill="#f59e0b" text-anchor="middle">DRIBBLE</text>
  
  <line x1="750" y1="310" x2="750" y2="390" stroke="#f59e0b" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  
  <!-- Dribble check -->
  <path d="M 750 390 L 830 450 L 750 510 L 670 450 Z" fill="#f59e0b" opacity="0.15" stroke="#f59e0b" stroke-width="2.5"/>
  <text x="750" y="455" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#f59e0b" text-anchor="middle">Movement</text>
  <text x="750" y="473" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8" text-anchor="middle">&gt;1.5m?</text>
  
  <!-- Shot detection -->
  <line x1="175" y1="520" x2="175" y2="600" stroke="#10b981" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  
  <rect x="80" y="610" width="190" height="80" rx="10" fill="#ec4899" opacity="0.2" stroke="#ec4899" stroke-width="2.5"/>
  <text x="175" y="640" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#ec4899" text-anchor="middle">SHOT Detection</text>
  <text x="85" y="665" font-family="'SF Pro Display', Arial" font-size="12" fill="#94a3b8">• On Target</text>
  <text x="85" y="683" font-family="'SF Pro Display', Arial" font-size="12" fill="#94a3b8">• Off Target / Blocked</text>
  
  <!-- Goal check -->
  <line x1="175" y1="690" x2="175" y2="760" stroke="#ec4899" stroke-width="2.5" marker-end="url(#arrowFlow)"/>
  
  <path d="M 175 760 L 240 810 L 175 860 L 110 810 Z" fill="#fbbf24" opacity="0.15" stroke="#fbbf24" stroke-width="2.5"/>
  <text x="175" y="818" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#fbbf24" text-anchor="middle">GOAL?</text>
  
  <!-- Final nodes -->
  <rect x="300" y="785" width="120" height="50" rx="25" fill="#fbbf24" opacity="0.3" stroke="#fbbf24" stroke-width="2"/>
  <text x="360" y="817" font-family="'SF Pro Display', Arial" font-size="14" font-weight="700" fill="#fbbf24" text-anchor="middle">ASSIST</text>
  
  <!-- Stats box -->
  <g transform="translate(550, 600)">
    <rect width="380" height="240" rx="12" fill="#1e293b" stroke="#334155" stroke-width="2"/>
    <text x="190" y="35" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#ffffff" text-anchor="middle">Detection Results</text>
    
    <text x="20" y="70" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#10b981">✓ Passes</text>
    <text x="340" y="70" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">100% acc</text>
    
    <text x="20" y="100" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#ec4899">✓ Shots</text>
    <text x="340" y="100" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">85% acc</text>
    
    <text x="20" y="130" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#f59e0b">✓ Dribbles</text>
    <text x="340" y="130" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">Tracked</text>
    
    <text x="20" y="160" font-family="'SF Pro Display', Arial" font-size="14" font-weight="600" fill="#7c3aed">✓ Interceptions</text>
    <text x="340" y="160" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="end">80% acc</text>
    
    <line x1="20" y1="180" x2="360" y2="180" stroke="#334155" stroke-width="1"/>
    
    <text x="20" y="210" font-family="'SF Pro Display', Arial" font-size="16" font-weight="700" fill="#00d4ff">Global Accuracy</text>
    <text x="340" y="210" font-family="'SF Pro Display', Arial" font-size="18" font-weight="700" fill="#00d4ff" text-anchor="end">88%</text>
  </g>
</svg>

### Performance Metrics by Action Type

| Action Type | Precision | Detections | Notes |
|-------------|-----------|------------|-------|
| **All Passes** | **100%** | 43 | Perfect classification |
| Key Passes | 95% | 14 | Occasional false positives |
| Shots | 85% | 2 | Limited by ball detection |
| Interceptions | 80% | 5 | Requires temporal context |
| **TOTAL (Global)** | **88%** | **50+** | Weighted average |

---

## 📊 Final Metrics Summary

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 450" style="background: linear-gradient(135deg, #0a0e1a 0%, #161b22 100%);">
  <defs>
    <linearGradient id="metricGrad1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00d4ff;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#0891b2;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="metricGrad2" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#7c3aed;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#5b21b6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="metricGrad3" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#10b981;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#059669;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="metricGrad4" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f59e0b;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#d97706;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glowMetric">
      <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Title -->
  <text x="600" y="50" font-family="'SF Pro Display', Arial" font-size="36" font-weight="700" fill="#ffffff" text-anchor="middle">
    Project Metrics at a Glance
  </text>
  
  <!-- Metric 1: Accuracy -->
  <g transform="translate(80, 120)">
    <rect width="240" height="140" rx="16" fill="url(#metricGrad1)" opacity="0.15" stroke="url(#metricGrad1)" stroke-width="2.5" filter="url(#glowMetric)"/>
    <text x="120" y="70" font-family="'SF Pro Display', Arial" font-size="56" font-weight="700" fill="#00d4ff" text-anchor="middle">88%</text>
    <text x="120" y="105" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb" text-anchor="middle">Global System</text>
    <text x="120" y="128" font-family="'SF Pro Display', Arial" font-size="16" fill="#94a3b8" text-anchor="middle">Accuracy</text>
  </g>
  
  <!-- Metric 2: Speedup -->
  <g transform="translate(360, 120)">
    <rect width="240" height="140" rx="16" fill="url(#metricGrad2)" opacity="0.15" stroke="url(#metricGrad2)" stroke-width="2.5" filter="url(#glowMetric)"/>
    <text x="120" y="70" font-family="'SF Pro Display', Arial" font-size="56" font-weight="700" fill="#7c3aed" text-anchor="middle">×1.88</text>
    <text x="120" y="105" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb" text-anchor="middle">Processing</text>
    <text x="120" y="128" font-family="'SF Pro Display', Arial" font-size="16" fill="#94a3b8" text-anchor="middle">Speedup</text>
  </g>
  
  <!-- Metric 3: Performance -->
  <g transform="translate(640, 120)">
    <rect width="240" height="140" rx="16" fill="url(#metricGrad3)" opacity="0.15" stroke="url(#metricGrad3)" stroke-width="2.5" filter="url(#glowMetric)"/>
    <text x="120" y="70" font-family="'SF Pro Display', Arial" font-size="56" font-weight="700" fill="#10b981" text-anchor="middle">+46.7%</text>
    <text x="120" y="105" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb" text-anchor="middle">Performance</text>
    <text x="120" y="128" font-family="'SF Pro Display', Arial" font-size="16" fill="#94a3b8" text-anchor="middle">Gain</text>
  </g>
  
  <!-- Metric 4: Workload -->
  <g transform="translate(920, 120)">
    <rect width="240" height="140" rx="16" fill="url(#metricGrad4)" opacity="0.15" stroke="url(#metricGrad4)" stroke-width="2.5" filter="url(#glowMetric)"/>
    <text x="120" y="70" font-family="'SF Pro Display', Arial" font-size="56" font-weight="700" fill="#f59e0b" text-anchor="middle">-80%</text>
    <text x="120" y="105" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb" text-anchor="middle">Manual</text>
    <text x="120" y="128" font-family="'SF Pro Display', Arial" font-size="16" fill="#94a3b8" text-anchor="middle">Workload</text>
  </g>
  
  <!-- Metric 5: Code -->
  <g transform="translate(220, 300)">
    <rect width="240" height="120" rx="16" fill="#1e293b" stroke="#334155" stroke-width="2"/>
    <text x="120" y="60" font-family="'SF Pro Display', Arial" font-size="44" font-weight="700" fill="#00d4ff" text-anchor="middle">2,249</text>
    <text x="120" y="90" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">Lines of Code</text>
    <text x="120" y="110" font-family="'SF Pro Display', Arial" font-size="12" fill="#64748b" text-anchor="middle">(parallel_tracker + ActionDetector)</text>
  </g>
  
  <!-- Metric 6: Actions -->
  <g transform="translate(490, 300)">
    <rect width="220" height="120" rx="16" fill="#1e293b" stroke="#334155" stroke-width="2"/>
    <text x="110" y="60" font-family="'SF Pro Display', Arial" font-size="48" font-weight="700" fill="#7c3aed" text-anchor="middle">11</text>
    <text x="110" y="90" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">Action Types</text>
    <text x="110" y="110" font-family="'SF Pro Display', Arial" font-size="12" fill="#64748b" text-anchor="middle">Detected</text>
  </g>
  
  <!-- Metric 7: Duration -->
  <g transform="translate(740, 300)">
    <rect width="220" height="120" rx="16" fill="#1e293b" stroke="#334155" stroke-width="2"/>
    <text x="110" y="60" font-family="'SF Pro Display', Arial" font-size="42" font-weight="700" fill="#10b981" text-anchor="middle">7 Mo.</text>
    <text x="110" y="90" font-family="'SF Pro Display', Arial" font-size="14" fill="#94a3b8" text-anchor="middle">Internship</text>
    <text x="110" y="110" font-family="'SF Pro Display', Arial" font-size="12" fill="#64748b" text-anchor="middle">April - October 2025</text>
  </g>
</svg>

---

## 🛠️ Technical Stack

### Deep Learning Frameworks
- **PyTorch 2.0** - Model training and inference
- **Ultralytics YOLOv11** - Object detection (v11m-cls, v11x)
- **TensorRT 8.6+** - Optimized inference engines
- **CUDA 11.8+** - GPU acceleration

### Computer Vision Libraries
- **OpenCV 4.8+** - Video processing, homography
- **DeepSORT** - Multi-object tracking with Re-ID
- **PaddleOCR** - Jersey number recognition
- **Tesseract 5.0** - Backup OCR engine

### Hardware
- **Training:** NVIDIA RTX 3090 (24GB VRAM)
- **Inference:** NVIDIA RTX 4060 (8GB VRAM)

---

## 👨‍💻 About This Project

**Duration:** April 2025 - October 2025 (7 months)  
**Type:** Final-Year Internship (Master's in Artificial Intelligence & Virtual Reality)  
**Institution:** Ibn Tofail University, Faculty of Sciences, Kenitra, Morocco  
**Company:** SPORTSCORE (Paris, France - Remote)

### Defense Jury
- **President:** Mr. Anass Nouri (FSK, Ibn Tofail University)
- **Examiner:** Mrs. Khadija Lekdioui (FSK, Ibn Tofail University)
- **Examiner:** Mrs. Khaoula Boukir (ENSC, Ibn Tofail University)

**Defense Date:** October 2025  
**Grade:** Très Bien (Excellent)

---

## 📧 Contact

**Author:** Hicham El Mehdi  
**Email:** mehdihicham736@gmail.com  
**LinkedIn:** [linkedin.com/in/elmehdihicham](https://linkedin.com/in/elmehdihicham)  
**GitHub:** [github.com/MehdiHCH](https://github.com/MehdiHCH)  

**Company:** [sportscore.tech](https://sportscore.tech)

---

*This project represents a significant step toward fully automated sports video analysis, combining cutting-edge AI (parallelization, deep learning, spatio-temporal reasoning) with domain expertise to deliver actionable insights for coaches, analysts, and federations.*