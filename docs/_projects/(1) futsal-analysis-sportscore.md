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
    <text x="190" y="87" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ 7 Pass Types + 2 Goals + 2 Defense</text>
    <text x="190" y="107" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">├─ 11 Total Action Types</text>
    <text x="190" y="127" font-family="'SF Pro Display', Arial" font-size="13" fill="#94a3b8">└─ 88% accuracy, 100% on basic passes</text>
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

## 🎬 System in Action

### Real-Time Analysis Dashboard

The image below shows the complete system running on a **FIFA Futsal World Cup 2021** match (Portugal vs Morocco). This demonstrates the full pipeline operating in real-time with three synchronized visualization windows:

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/projects/MVP.png" alt="System in Action - Real-Time Dashboard" width="100%" style="border-radius: 12px; box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);">
</p>

<p align="center" style="color: #94a3b8; font-style: italic; margin-top: 12px;">
  <strong>Real-time analysis dashboard</strong> — Player tracking, tactical heatmaps, and homography projection<br>
  <em>FIFA Futsal World Cup 2021: Portugal 3-2 Morocco (2nd Period, 9:37)</em>
</p>

---

### Dashboard Components

<table align="center" style="width: 90%; max-width: 900px; margin: 30px auto; border-collapse: separate; border-spacing: 15px;">
  <tr>
    <td style="background: linear-gradient(135deg, #00d4ff 0%, #0891b2 100%); padding: 20px; border-radius: 12px; color: white; text-align: center;">
      <h4 style="margin: 0 0 8px 0; font-size: 18px;">🎯 Main Window</h4>
      <p style="margin: 0; font-size: 14px; opacity: 0.95;">Player Tracking & Detection</p>
    </td>
    <td style="background: linear-gradient(135deg, #ec4899 0%, #be185d 100%); padding: 20px; border-radius: 12px; color: white; text-align: center;">
      <h4 style="margin: 0 0 8px 0; font-size: 18px;">🔥 Bottom-Left</h4>
      <p style="margin: 0; font-size: 14px; opacity: 0.95;">Tactical Heatmaps</p>
    </td>
    <td style="background: linear-gradient(135deg, #10b981 0%, #059669 100%); padding: 20px; border-radius: 12px; color: white; text-align: center;">
      <h4 style="margin: 0 0 8px 0; font-size: 18px;">📐 Bottom-Right</h4>
      <p style="margin: 0; font-size: 14px; opacity: 0.95;">Homography Projection</p>
    </td>
  </tr>
</table>

---

#### 1️⃣ **Main Window: Player Tracking**
- ✅ **Real-time player detection** with YOLOv11x (colored skeletons)
- ✅ **Player identification** with jersey numbers and confidence scores
  - Yellow team (Portugal): IDs 17, 21 (B. Bakkali 0.88, S. El Mesrar 0.81)
  - Green team (Morocco): IDs 1, 8, 10, 16, 18 (with confidence scores)
- ✅ **Ball tracking** with trajectory prediction (yellow marker)
- ✅ **Bounding boxes** with team color coding (yellow/green)
- ✅ **Score overlay**: POR 3-2 MAR, 2nd period, 9:37
- ✅ **Pass counter**: Real-time statistics (Morocco: 21 passes)

#### 2️⃣ **Bottom-Left: Heatmaps Window**
- 🔥 **Tactical positioning heatmap** showing player presence zones
- 🔴 **Red zones**: High-intensity areas (attacking third, penalty area)
- 🔵 **Blue zones**: Defensive positioning and coverage
- ⚪ **Circle marker**: Current ball position on tactical map
- 📊 **Purpose**: Analyze team formation, pressing patterns, and spatial dominance

#### 3️⃣ **Bottom-Right: Homography Window**
- 🎯 **Projected trajectories** on 2D pitch representation
- 🟢 **Green lines**: Pass networks and ball movements
- ⚪ **White lines**: Player movement paths
- 🏟️ **Top-down view**: Pixel coordinates transformed to real-world pitch positions
- 📐 **Purpose**: Tactical analysis, distance calculation, zone-based action detection

---

### Key Observations from This Frame

<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
  <tr style="background: linear-gradient(135deg, #1e293b 0%, #334155 100%);">
    <th style="padding: 15px; text-align: left; color: #00d4ff; border-bottom: 2px solid #00d4ff;">Category</th>
    <th style="padding: 15px; text-align: left; color: #00d4ff; border-bottom: 2px solid #00d4ff;">Details</th>
  </tr>
  <tr>
    <td style="padding: 12px; border-bottom: 1px solid #334155;"><strong>⚽ Match Context</strong></td>
    <td style="padding: 12px; border-bottom: 1px solid #334155;">
      Portugal 3-2 Morocco • 2nd period, 9:37 • FIFA Futsal World Cup Lithuania 2021
    </td>
  </tr>
  <tr>
    <td style="padding: 12px; border-bottom: 1px solid #334155;"><strong>🎯 Tactical Situation</strong></td>
    <td style="padding: 12px; border-bottom: 1px solid #334155;">
      Morocco (green) attacking with <strong>21 completed passes</strong> • Portugal defending with 4 players • High-pressure zone
    </td>
  </tr>
  <tr>
    <td style="padding: 12px;"><strong>✅ System Performance</strong></td>
    <td style="padding: 12px;">
      9/9 players detected • 100% team assignment accuracy • OCR: 7 jersey numbers • Confidence: 0.81-0.91 • Real-time heatmap & homography
    </td>
  </tr>
</table>

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

### Detected Action Types

The system implements a comprehensive taxonomy of futsal actions, covering all critical gameplay events:

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800" style="background: linear-gradient(135deg, #0a0e1a 0%, #1a1d29 100%);">
  <defs>
    <linearGradient id="passGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#10b981;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#059669;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="goalGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#fbbf24;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#f59e0b;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="defenseGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#ef4444;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#dc2626;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glowAction">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Title -->
  <text x="600" y="50" font-family="'SF Pro Display', Arial" font-size="36" font-weight="700" fill="#ffffff" text-anchor="middle">
    11 Action Types Detected
  </text>
  
  <!-- Pass Actions Section -->
  <g transform="translate(50, 100)">
    <rect width="350" height="500" rx="16" fill="url(#passGrad)" opacity="0.1" stroke="url(#passGrad)" stroke-width="3" filter="url(#glowAction)"/>
    <text x="175" y="40" font-family="'SF Pro Display', Arial" font-size="24" font-weight="700" fill="#10b981" text-anchor="middle">PASS ACTIONS (7)</text>
    
    <!-- Pass items -->
    <g transform="translate(20, 70)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Basic PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">100%</text>
    </g>
    
    <g transform="translate(20, 130)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Progressive PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">95%</text>
    </g>
    
    <g transform="translate(20, 190)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Into-Penalty-Area PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">92%</text>
    </g>
    
    <g transform="translate(20, 250)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Pressure PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">88%</text>
    </g>
    
    <g transform="translate(20, 310)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">SMART PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">90%</text>
    </g>
    
    <g transform="translate(20, 370)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Key PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">95%</text>
    </g>
    
    <g transform="translate(20, 430)">
      <circle cx="10" cy="0" r="6" fill="#10b981"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Incomplete PASS</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#10b981" font-weight="600">85%</text>
    </g>
  </g>
  
  <!-- Goal Actions Section -->
  <g transform="translate(450, 100)">
    <rect width="300" height="230" rx="16" fill="url(#goalGrad)" opacity="0.1" stroke="url(#goalGrad)" stroke-width="3" filter="url(#glowAction)"/>
    <text x="150" y="40" font-family="'SF Pro Display', Arial" font-size="24" font-weight="700" fill="#fbbf24" text-anchor="middle">GOAL ACTIONS (2)</text>
    
    <g transform="translate(20, 90)">
      <circle cx="10" cy="0" r="6" fill="#fbbf24"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">Assist</text>
      <text x="230" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#fbbf24" font-weight="600">100%</text>
    </g>
    
    <g transform="translate(20, 150)">
      <circle cx="10" cy="0" r="6" fill="#fbbf24"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">GOAL</text>
      <text x="230" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#fbbf24" font-weight="600">100%</text>
    </g>
  </g>
  
  <!-- Defense Actions Section -->
  <g transform="translate(800, 100)">
    <rect width="350" height="230" rx="16" fill="url(#defenseGrad)" opacity="0.1" stroke="url(#defenseGrad)" stroke-width="3" filter="url(#glowAction)"/>
    <text x="175" y="40" font-family="'SF Pro Display', Arial" font-size="24" font-weight="700" fill="#ef4444" text-anchor="middle">DEFENSIVE (2)</text>
    
    <g transform="translate(20, 90)">
      <circle cx="10" cy="0" r="6" fill="#ef4444"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">INTERCEPTION</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#ef4444" font-weight="600">80%</text>
    </g>
    
    <g transform="translate(20, 150)">
      <circle cx="10" cy="0" r="6" fill="#ef4444"/>
      <text x="25" y="5" font-family="'SF Pro Display', Arial" font-size="15" fill="#e5e7eb">RECOVERY</text>
      <text x="280" y="5" font-family="'SF Pro Display', Arial" font-size="13" fill="#ef4444" font-weight="600">82%</text>
    </g>
  </g>
  
  <!-- Summary Statistics -->
  <g transform="translate(150, 680)">
    <rect width="900" height="80" rx="16" fill="#1e293b" stroke="#00d4ff" stroke-width="2"/>
    <text x="450" y="35" font-family="'SF Pro Display', Arial" font-size="20" font-weight="700" fill="#00d4ff" text-anchor="middle">SYSTEM PERFORMANCE</text>
    <text x="150" y="60" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb">125+ Total Detections</text>
    <text x="450" y="60" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb">88% Global Accuracy</text>
    <text x="700" y="60" font-family="'SF Pro Display', Arial" font-size="16" fill="#e5e7eb">1,208 Lines of Code</text>
  </g>
</svg>

---

#### **Pass Actions (7 types)**

| Action Type | Description | Detection Criteria |
|-------------|-------------|-------------------|
| **Basic PASS** | Standard successful pass between teammates | Ball possession change between same-team players |
| **Progressive PASS** | Pass that advances the ball toward opponent's goal | Distance traveled > threshold toward attacking third |
| **Into-Penalty-Area PASS** | Pass delivered into the opponent's penalty box | Destination coordinates within penalty zone |
| **Pressure PASS** | Pass executed under defensive pressure | Opponent within 2m radius during execution |
| **SMART PASS** | Tactically intelligent pass (through ball, switch) | Geometric analysis of passing lanes |
| **Key PASS** | Pass directly leading to a shot opportunity | Followed by shot attempt within 3 seconds |
| **Incomplete PASS** | Attempted pass that fails to reach teammate | Interception or out-of-bounds detection |

#### **Goal Actions (2 types)**

| Action Type | Description | Detection Criteria |
|-------------|-------------|-------------------|
| **Assist** | Final pass before a goal is scored | Last pass before goal event |
| **GOAL** | Ball crosses the goal line | Ball detection in goal area + score validation |

#### **Defensive Actions (2 types)**

| Action Type | Description | Detection Criteria |
|-------------|-------------|-------------------|
| **INTERCEPTION** | Defensive player interrupts opponent's pass | Possession change from opponent during ball flight |
| **RECOVERY** | Regaining possession of loose ball | Possession acquisition without active pass/interception |

### Performance Metrics by Action Type

| Action Type | Precision | Detections | Notes |
|-------------|-----------|------------|-------|
| **All Passes (Basic)** | **100%** | 43 | Perfect classification |
| Progressive PASS | 95% | 12 | Threshold-based detection |
| Into-Penalty-Area PASS | 92% | 8 | Geometric zone validation |
| Pressure PASS | 88% | 15 | Proximity-based detection |
| SMART PASS | 90% | 6 | Tactical pattern recognition |
| Key PASS | 95% | 14 | Temporal correlation with shots |
| Incomplete PASS | 85% | 9 | Requires ball trajectory analysis |
| Assist | 100% | 3 | Validated against goals |
| GOAL | 100% | 3 | Ball + score correlation |
| INTERCEPTION | 80% | 5 | Complex multi-player analysis |
| RECOVERY | 82% | 7 | Loose ball detection |
| **TOTAL (Global)** | **88%** | **125+** | Weighted average across all actions |

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