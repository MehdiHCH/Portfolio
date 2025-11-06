---
title: Azul OCR - Tifinagh Handwritten Character Recognition
image: /assets/img/projects/azul.jpeg
description: Innovative OCR system using CNN, Tesseract and PaddleOCR for Tifinagh handwritten character recognition, preserving Amazigh cultural heritage.
category: computer-vision
tags:
  - OCR
  - Tifinagh
  - CNN
  - PaddleOCR
  - Tesseract
  - Cultural Heritage
  - Deep Learning
  - Computer Vision
demo: /assets/videos/azul_ocr_demo.mp4
date: 2024-03-15
company: Academic Project
location: Ibn Tofail University, Kenitra
duration: February 2024 - June 2024
github : https://github.com/MehdiHCH/Tesseract-OCR--Handwritten-Tifinagh-Character-Recognition
---

## 🎯 Project Overview

**Azul OCR** (ⴰⵣⵓⵍ - "Hello" in Amazigh) is an innovative OCR system specialized in **Tifinagh handwritten character recognition**. The project aims to preserve and digitize Amazigh cultural heritage by developing an artificial intelligence solution capable of accurately recognizing Tifinagh handwritten characters and sentences.

**Team:**
- **Rima Daqch** - Project Manager, Tesseract OCR Developer
- **Adil Eddarif** - Tesseract OCR Developer, CNN Model Developer
- **Brahim El Aboudi** - PaddleOCR Developer, CNN Model Developer
- **El Mehdi Hicham** - PaddleOCR Developer, CNN Model Developer
- **Zineb Lahraoui** - PaddleOCR Developer, CNN Model Developer

**Supervised by:** Prof. Khadija Lekdioui

**Mission:** *"Preserving and digitizing Amazigh cultural heritage"*

---

## 🔍 Problem Statement

### Challenges

**"Tifinagh script is an essential element of Amazigh cultural heritage, but it remains underrepresented in modern technological tools."**

- 📚 **Lack of OCR tools:** No dedicated OCR solution for Tifinagh manuscripts
- 🎨 **Character complexity:** Significant variability in handwriting
- ⚠️ **Cultural risk:** Potential loss of valuable content for future generations
- 🔬 **Limited accuracy:** Existing solutions not adapted to Tifinagh specificities

### Solution

Development of **Azul OCR**, hybrid system combining:
- **Tesseract OCR** fine-tuned for Tifinagh
- **PaddleOCR** adapted for Amazigh characters
- **Custom CNN** for character recognition
- **Intuitive interface** for capture and recognition

---

## 🏗️ Technical Architecture


### 🔧 Key Components



#### **Module 1: Image Preprocessing**


**Applied techniques:**
- 🖼️ **Otsu Thresholding:** Automatic binarization
- 📐 **Resizing:** 64×64 → 128×128 pixels
- 🎨 **Filtering:** Noise reduction
- 🔄 **Augmentation:** Rotation, translation, zoom



#### **Module 2: Recognition Engines**


**Three approaches:**
- 📝 **Tesseract OCR:** Fine-tuned on AMHCD dataset
- 🎯 **PaddleOCR:** Adapted lightweight architecture
- 🧠 **Custom CNN:** Model trained from scratch
- 🔀 **Hybrid model:** Prediction fusion

---

### 📊 System Workflow

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 700" style="background: transparent;">
  <defs>
    <linearGradient id="blueGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="purpleGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#a78bfa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#8b5cf6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="greenGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="yellowGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#fbbf24;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#f59e0b;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="pinkGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f472b6;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#ec4899;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <marker id="arrowBlue" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#60a5fa" />
    </marker>
    
    <marker id="arrowPurple" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#a78bfa" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="450" y="35" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="30" font-weight="700" fill="url(#blueGrad)" text-anchor="middle" filter="url(#glow)">
    Azul OCR - Complete System Workflow
  </text>
  <text x="450" y="60" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#94a3b8" text-anchor="middle">
    ⴰⵣⵓⵍ - Tifinagh Manuscript Recognition System
  </text>
  
  <!-- Input Image -->
  <g>
    <rect x="350" y="90" width="200" height="80" rx="10" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="450" y="120" font-size="32" text-anchor="middle">📸</text>
    <text x="450" y="150" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Input Image
    </text>
  </g>
  
  <!-- Arrow to Preprocessing -->
  <line x1="450" y1="170" x2="450" y2="210" stroke="#60a5fa" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Preprocessing -->
  <g>
    <rect x="350" y="220" width="200" height="70" rx="10" fill="rgba(251, 191, 36, 0.15)" stroke="url(#yellowGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="450" y="255" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Preprocessing
    </text>
    <text x="450" y="277" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Otsu + Resize + Normalize
    </text>
  </g>
  
  <!-- Arrow to Decision -->
  <line x1="450" y1="290" x2="450" y2="330" stroke="#fbbf24" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Decision Diamond -->
  <g>
    <path d="M 450 340 L 530 380 L 450 420 L 370 380 Z" fill="rgba(167, 139, 250, 0.15)" stroke="url(#purpleGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="450" y="375" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Detection
    </text>
    <text x="450" y="393" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Type?
    </text>
  </g>
  
  <!-- Left Branch: Characters -->
  <line x1="370" y1="380" x2="200" y2="380" stroke="#a78bfa" stroke-width="2.5" opacity="0.8"/>
  <line x1="200" y1="380" x2="200" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowPurple)" opacity="0.8"/>
  <text x="280" y="370" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa">
    Characters
  </text>
  
  <!-- CNN Model Box -->
  <g>
    <rect x="80" y="460" width="240" height="100" rx="10" fill="rgba(244, 114, 182, 0.15)" stroke="url(#pinkGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="200" y="490" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#f472b6" text-anchor="middle">
      CNN Model
    </text>
    <text x="200" y="515" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Custom Architecture
    </text>
    <text x="200" y="535" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      33 Tifinagh classes
    </text>
    <text x="200" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      6 Conv layers + Dropout
    </text>
  </g>
  
  <!-- CNN Stats Box -->
  <g>
    <rect x="80" y="580" width="240" height="70" rx="6" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="1.5"/>
    <text x="200" y="603" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#f472b6" text-anchor="middle">
      94.2% Accuracy ⭐
    </text>
    <text x="200" y="623" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Precision: 93.8% | Recall: 94.1%
    </text>
    <text x="200" y="640" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Best for: Isolated characters
    </text>
  </g>
  
  <!-- Middle Branch: Words/Phrases -->
  <line x1="450" y1="420" x2="450" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowPurple)" opacity="0.8"/>
  <text x="460" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa">
    Words/Phrases
  </text>
  
  <!-- Tesseract OCR Box -->
  <g>
    <rect x="350" y="460" width="200" height="100" rx="10" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="450" y="490" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Tesseract OCR
    </text>
    <text x="450" y="515" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Fine-tuned on AMHCD
    </text>
    <text x="450" y="535" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      LSTM + Language Model
    </text>
    <text x="450" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Custom training data
    </text>
  </g>
  
  <!-- Tesseract Stats Box -->
  <g>
    <rect x="350" y="580" width="200" height="70" rx="6" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="1.5"/>
    <text x="450" y="603" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#60a5fa" text-anchor="middle">
      87.5% Accuracy ⭐
    </text>
    <text x="450" y="623" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      CER: 12.5% | WER: 18.3%
    </text>
    <text x="450" y="640" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Best for: Simple layouts
    </text>
  </g>
  
  <!-- Right Branch: Text Lines -->
  <line x1="530" y1="380" x2="700" y2="380" stroke="#a78bfa" stroke-width="2.5" opacity="0.8"/>
  <line x1="700" y1="380" x2="700" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowPurple)" opacity="0.8"/>
  <text x="610" y="370" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa">
    Text Lines
  </text>
  
  <!-- PaddleOCR Box -->
  <g>
    <rect x="580" y="460" width="240" height="100" rx="10" fill="rgba(52, 211, 153, 0.15)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="700" y="490" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#34d399" text-anchor="middle">
      PaddleOCR
    </text>
    <text x="700" y="515" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      DB++ + CRNN
    </text>
    <text x="700" y="535" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      End-to-end detection
    </text>
    <text x="700" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Fine-tuned on Tifinagh
    </text>
  </g>
  
  <!-- PaddleOCR Stats Box -->
  <g>
    <rect x="580" y="580" width="240" height="70" rx="6" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="1.5"/>
    <text x="700" y="603" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#34d399" text-anchor="middle">
      89.6% Accuracy ⭐
    </text>
    <text x="700" y="623" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      CER: 10.8% | WER: 15.4%
    </text>
    <text x="700" y="640" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Best for: Complex layouts
    </text>
  </g>
  
  <!-- Hybrid Model Banner -->
  <g>
    <rect x="50" y="670" width="800" height="20" rx="5" fill="rgba(167, 139, 250, 0.2)" stroke="#a78bfa" stroke-width="1.5"/>
    <text x="450" y="684" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa" text-anchor="middle">
      🏆 Hybrid Model (Weighted Voting): 91.2% Accuracy | Best Overall Performance
    </text>
  </g>
</svg>

---

## 🔬 Technical Deep Dive

### 1️⃣ CNN Architecture Details

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1100 650" style="background: transparent;">
  <defs>
    <linearGradient id="pinkGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f472b6;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#ec4899;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="blueGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="purpleGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#a78bfa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#8b5cf6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="greenGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <filter id="shadow">
      <feDropShadow dx="0" dy="2" stdDeviation="4" flood-opacity="0.3"/>
    </filter>
    
    <marker id="arrowhead" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#a78bfa" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="550" y="35" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="28" font-weight="700" fill="url(#pinkGradient)" text-anchor="middle">
    🧠 Custom CNN Architecture for Tifinagh Recognition
  </text>
  <text x="550" y="60" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
    6 Convolutional Layers + Dropout Regularization + 33-class Classification
  </text>
  
  <!-- Input Layer -->
  <g>
    <rect x="50" y="100" width="100" height="120" rx="8" fill="rgba(96, 165, 250, 0.2)" stroke="url(#blueGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="100" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Input Layer
    </text>
    <text x="100" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      128×128×1
    </text>
    <text x="100" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      Grayscale
    </text>
    <text x="100" y="195" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      Normalized
    </text>
    <text x="100" y="212" font-size="20" text-anchor="middle">📸</text>
  </g>
  
  <!-- Arrow -->
  <line x1="150" y1="160" x2="190" y2="160" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Conv Block 1 -->
  <g>
    <rect x="200" y="100" width="110" height="120" rx="8" fill="rgba(244, 114, 182, 0.2)" stroke="url(#pinkGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="255" y="125" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#f472b6" text-anchor="middle">
      Conv Block 1
    </text>
    <text x="255" y="147" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Conv2D (32, 3×3)
    </text>
    <text x="255" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ReLU
    </text>
    <text x="255" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      MaxPool (2×2)
    </text>
    <text x="255" y="201" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      → 64×64×32
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="310" y1="160" x2="340" y2="160" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Conv Block 2 -->
  <g>
    <rect x="350" y="100" width="110" height="120" rx="8" fill="rgba(244, 114, 182, 0.2)" stroke="url(#pinkGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="405" y="125" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#f472b6" text-anchor="middle">
      Conv Block 2
    </text>
    <text x="405" y="147" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Conv2D (64, 3×3)
    </text>
    <text x="405" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ReLU
    </text>
    <text x="405" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      MaxPool (2×2)
    </text>
    <text x="405" y="201" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      → 32×32×64
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="460" y1="160" x2="490" y2="160" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Conv Block 3 -->
  <g>
    <rect x="500" y="100" width="110" height="120" rx="8" fill="rgba(244, 114, 182, 0.2)" stroke="url(#pinkGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="555" y="125" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#f472b6" text-anchor="middle">
      Conv Block 3
    </text>
    <text x="555" y="147" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Conv2D (128, 3×3)
    </text>
    <text x="555" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ReLU
    </text>
    <text x="555" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      MaxPool (2×2)
    </text>
    <text x="555" y="201" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      → 16×16×128
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="610" y1="160" x2="640" y2="160" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Conv Block 4 -->
  <g>
    <rect x="650" y="100" width="110" height="120" rx="8" fill="rgba(244, 114, 182, 0.2)" stroke="url(#pinkGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="705" y="125" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#f472b6" text-anchor="middle">
      Conv Block 4
    </text>
    <text x="705" y="147" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Conv2D (256, 3×3)
    </text>
    <text x="705" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ReLU
    </text>
    <text x="705" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      MaxPool (2×2)
    </text>
    <text x="705" y="201" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      → 8×8×256
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="760" y1="160" x2="790" y2="160" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Conv Block 5 -->
  <g>
    <rect x="800" y="100" width="110" height="120" rx="8" fill="rgba(244, 114, 182, 0.2)" stroke="url(#pinkGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="855" y="125" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#f472b6" text-anchor="middle">
      Conv Block 5
    </text>
    <text x="855" y="147" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Conv2D (512, 3×3)
    </text>
    <text x="855" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ReLU
    </text>
    <text x="855" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      MaxPool (2×2)
    </text>
    <text x="855" y="201" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      → 4×4×512
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="910" y1="160" x2="940" y2="160" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Conv Block 6 -->
  <g>
    <rect x="950" y="100" width="110" height="120" rx="8" fill="rgba(244, 114, 182, 0.2)" stroke="url(#pinkGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="1005" y="125" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#f472b6" text-anchor="middle">
      Conv Block 6
    </text>
    <text x="1005" y="147" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Conv2D (512, 3×3)
    </text>
    <text x="1005" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ReLU
    </text>
    <text x="1005" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      MaxPool (2×2)
    </text>
    <text x="1005" y="201" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      → 2×2×512
    </text>
  </g>
  
  <!-- Vertical Arrow to Flatten -->
  <line x1="555" y1="220" x2="555" y2="270" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Flatten Layer -->
  <g>
    <rect x="450" y="280" width="210" height="60" rx="8" fill="rgba(167, 139, 250, 0.2)" stroke="url(#purpleGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="555" y="305" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Flatten Layer
    </text>
    <text x="555" y="328" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      2048 neurons (2×2×512)
    </text>
  </g>
  
  <!-- Arrow to Dense -->
  <line x1="555" y1="340" x2="555" y2="380" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Dense Layer 1 -->
  <g>
    <rect x="450" y="390" width="210" height="70" rx="8" fill="rgba(52, 211, 153, 0.2)" stroke="url(#greenGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="555" y="418" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#34d399" text-anchor="middle">
      Dense Layer 1
    </text>
    <text x="555" y="438" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      512 neurons + ReLU
    </text>
    <text x="555" y="454" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      Dropout (50%)
    </text>
  </g>
  
  <!-- Arrow to Output -->
  <line x1="555" y1="460" x2="555" y2="500" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowhead)" opacity="0.7"/>
  
  <!-- Output Layer -->
  <g>
    <rect x="450" y="510" width="210" height="80" rx="8" fill="rgba(96, 165, 250, 0.2)" stroke="url(#blueGradient)" stroke-width="2.5" filter="url(#shadow)"/>
    <text x="555" y="538" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Output Layer
    </text>
    <text x="555" y="560" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      33 neurons (classes)
    </text>
    <text x="555" y="578" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      Softmax activation
    </text>
  </g>
  
  <!-- Stats Box -->
  <g>
    <rect x="50" y="280" width="350" height="140" rx="8" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#shadow)"/>
    <text x="225" y="310" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#f472b6" text-anchor="middle">
      📊 Model Statistics
    </text>
    <text x="60" y="340" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Total Parameters: <tspan font-weight="600" fill="#34d399">~2.5M</tspan>
    </text>
    <text x="60" y="365" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Training Time: <tspan font-weight="600" fill="#60a5fa">~3 hours</tspan>
    </text>
    <text x="60" y="390" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Inference Speed: <tspan font-weight="600" fill="#fbbf24">~15ms/image</tspan>
    </text>
    <text x="60" y="415" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Accuracy: <tspan font-weight="600" fill="#f472b6">94.2%</tspan>
    </text>
  </g>
  
  <!-- Training Details Box -->
  <g>
    <rect x="700" y="280" width="350" height="140" rx="8" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#shadow)"/>
    <text x="875" y="310" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#a78bfa" text-anchor="middle">
      🎯 Training Details
    </text>
    <text x="710" y="340" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Optimizer: <tspan font-weight="600" fill="#34d399">Adam (lr=0.001)</tspan>
    </text>
    <text x="710" y="365" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Loss Function: <tspan font-weight="600" fill="#60a5fa">Categorical Crossentropy</tspan>
    </text>
    <text x="710" y="390" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Batch Size: <tspan font-weight="600" fill="#fbbf24">32</tspan>
    </text>
    <text x="710" y="415" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Epochs: <tspan font-weight="600" fill="#f472b6">50 (Early Stopping)</tspan>
    </text>
  </g>
  
  <!-- Footer Note -->
  <text x="550" y="630" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" font-style="italic" fill="#94a3b8" text-anchor="middle">
    🏆 Best performance on isolated character recognition | Trained on AMHCD dataset
  </text>
</svg>

---

### 2️⃣ Tesseract OCR Fine-tuning

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1100 620" style="background: transparent;">
  <defs>
    <linearGradient id="tesseractBlue" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="tesseractPurple" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#a78bfa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#8b5cf6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="tesseractGreen" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <filter id="tesseractShadow">
      <feDropShadow dx="0" dy="2" stdDeviation="4" flood-opacity="0.3"/>
    </filter>
    
    <marker id="tesseractArrow" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#a78bfa" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="550" y="35" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="28" font-weight="700" fill="url(#tesseractBlue)" text-anchor="middle">
    📝 Tesseract OCR Fine-tuning Pipeline
  </text>
  <text x="550" y="60" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
    Adapted for Tifinagh Script Recognition | LSTM-based Architecture
  </text>
  
  <!-- Step 1: Data Preparation -->
  <g>
    <rect x="50" y="100" width="220" height="110" rx="10" fill="rgba(96, 165, 250, 0.2)" stroke="url(#tesseractBlue)" stroke-width="2.5" filter="url(#tesseractShadow)"/>
    <text x="160" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#60a5fa" text-anchor="middle">
      1️⃣ Data Preparation
    </text>
    <text x="160" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • AMHCD Dataset
    </text>
    <text x="160" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Ground Truth (GT) Files
    </text>
    <text x="160" y="195" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Box Files Generation
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="270" y1="155" x2="310" y2="155" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#tesseractArrow)" opacity="0.7"/>
  
  <!-- Step 2: Training -->
  <g>
    <rect x="320" y="100" width="220" height="110" rx="10" fill="rgba(167, 139, 250, 0.2)" stroke="url(#tesseractPurple)" stroke-width="2.5" filter="url(#tesseractShadow)"/>
    <text x="430" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#a78bfa" text-anchor="middle">
      2️⃣ LSTM Training
    </text>
    <text x="430" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • 100+ iterations
    </text>
    <text x="430" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Language Model
    </text>
    <text x="430" y="195" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Character Error Rate ↓
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="540" y1="155" x2="580" y2="155" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#tesseractArrow)" opacity="0.7"/>
  
  <!-- Step 3: Evaluation -->
  <g>
    <rect x="590" y="100" width="220" height="110" rx="10" fill="rgba(52, 211, 153, 0.2)" stroke="url(#tesseractGreen)" stroke-width="2.5" filter="url(#tesseractShadow)"/>
    <text x="700" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#34d399" text-anchor="middle">
      3️⃣ Evaluation
    </text>
    <text x="700" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Test on validation set
    </text>
    <text x="700" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • CER: 12.5%
    </text>
    <text x="700" y="195" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • WER: 18.3%
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="810" y1="155" x2="850" y2="155" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#tesseractArrow)" opacity="0.7"/>
  
  <!-- Step 4: Deployment -->
  <g>
    <rect x="860" y="100" width="200" height="110" rx="10" fill="rgba(251, 191, 36, 0.2)" stroke="#fbbf24" stroke-width="2.5" filter="url(#tesseractShadow)"/>
    <text x="960" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#fbbf24" text-anchor="middle">
      4️⃣ Deployment
    </text>
    <text x="960" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Export .traineddata
    </text>
    <text x="960" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Integration in App
    </text>
    <text x="960" y="195" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      • Real-time Recognition
    </text>
  </g>
  
  <!-- Architecture Details -->
  <g>
    <rect x="50" y="240" width="1010" height="150" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#tesseractShadow)"/>
    <text x="555" y="270" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#60a5fa" text-anchor="middle">
      🏗️ Tesseract LSTM Architecture
    </text>
    
    <text x="70" y="305" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#60a5fa">Input Layer:</tspan> Variable-width image strips (H=48px)
    </text>
    <text x="70" y="330" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#a78bfa">Convolutional Layers:</tspan> 3 layers for feature extraction
    </text>
    <text x="70" y="355" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#34d399">LSTM Layers:</tspan> Bidirectional LSTM (2 layers, 256 units each)
    </text>
    <text x="70" y="380" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#fbbf24">Output Layer:</tspan> CTC (Connectionist Temporal Classification)
    </text>
  </g>
  
  <!-- Training Metrics -->
  <g>
    <rect x="50" y="410" width="320" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#tesseractShadow)"/>
    <text x="210" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#60a5fa" text-anchor="middle">
      📊 Training Metrics
    </text>
    <text x="70" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Training Images: <tspan font-weight="600" fill="#34d399">15,000+</tspan>
    </text>
    <text x="70" y="495" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Iterations: <tspan font-weight="600" fill="#60a5fa">120 epochs</tspan>
    </text>
    <text x="70" y="520" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Training Time: <tspan font-weight="600" fill="#fbbf24">~12 hours</tspan>
    </text>
    <text x="70" y="545" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Final CER: <tspan font-weight="600" fill="#f472b6">12.5%</tspan>
    </text>
    <text x="70" y="570" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      • Word Accuracy: <tspan font-weight="600" fill="#34d399">87.5%</tspan>
    </text>
  </g>
  
  <!-- Challenges & Solutions -->
  <g>
    <rect x="400" y="410" width="320" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#tesseractShadow)"/>
    <text x="560" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#a78bfa" text-anchor="middle">
      🔧 Key Optimizations
    </text>
    <text x="420" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✅ Custom Unicode mapping
    </text>
    <text x="420" y="495" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✅ Tifinagh-specific wordlists
    </text>
    <text x="420" y="520" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✅ Context-aware correction
    </text>
    <text x="420" y="545" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✅ Augmented training data
    </text>
    <text x="420" y="570" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✅ Multi-font training
    </text>
  </g>
  
  <!-- Performance Comparison -->
  <g>
    <rect x="750" y="410" width="310" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#tesseractShadow)"/>
    <text x="905" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#34d399" text-anchor="middle">
      🎯 Best Use Cases
    </text>
    <text x="770" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✓ Documents with simple layouts
    </text>
    <text x="770" y="495" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✓ Printed text recognition
    </text>
    <text x="770" y="520" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✓ Well-separated lines
    </text>
    <text x="770" y="545" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✓ High contrast images
    </text>
    <text x="770" y="570" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      ✓ Historical manuscripts
    </text>
  </g>
  
  <!-- Footer -->
  <text x="550" y="610" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" font-style="italic" fill="#94a3b8" text-anchor="middle">
    🏆 87.5% accuracy on word/phrase recognition | Ideal for structured documents
  </text>
</svg>

---

### 3️⃣ PaddleOCR Integration Pipeline

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1100 650" style="background: transparent;">
  <defs>
    <linearGradient id="paddleGreen" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="paddleBlue" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="paddlePurple" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#a78bfa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#8b5cf6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="paddleYellow" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#fbbf24;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#f59e0b;stop-opacity:1" />
    </linearGradient>
    
    <filter id="paddleShadow">
      <feDropShadow dx="0" dy="2" stdDeviation="4" flood-opacity="0.3"/>
    </filter>
    
    <marker id="paddleArrow" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#34d399" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="550" y="35" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="28" font-weight="700" fill="url(#paddleGreen)" text-anchor="middle">
    🎯 PaddleOCR Complete Pipeline
  </text>
  <text x="550" y="60" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
    DB++ Text Detection + CRNN Recognition | End-to-End Tifinagh OCR
  </text>
  
  <!-- Input Image -->
  <g>
    <rect x="50" y="100" width="180" height="90" rx="8" fill="rgba(96, 165, 250, 0.2)" stroke="url(#paddleBlue)" stroke-width="2.5" filter="url(#paddleShadow)"/>
    <text x="140" y="135" font-size="28" text-anchor="middle">📄</text>
    <text x="140" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Input Image
    </text>
    <text x="140" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      Tifinagh Text
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="230" y1="145" x2="270" y2="145" stroke="#34d399" stroke-width="2.5" marker-end="url(#paddleArrow)" opacity="0.7"/>
  
  <!-- Text Detection (DB++) -->
  <g>
    <rect x="280" y="100" width="200" height="90" rx="8" fill="rgba(52, 211, 153, 0.2)" stroke="url(#paddleGreen)" stroke-width="2.5" filter="url(#paddleShadow)"/>
    <text x="380" y="128" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#34d399" text-anchor="middle">
      Text Detection
    </text>
    <text x="380" y="148" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      DB++ Algorithm
    </text>
    <text x="380" y="166" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Differentiable Binarization
    </text>
    <text x="380" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      ResNet50 Backbone
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="480" y1="145" x2="520" y2="145" stroke="#34d399" stroke-width="2.5" marker-end="url(#paddleArrow)" opacity="0.7"/>
  
  <!-- Text Boxes -->
  <g>
    <rect x="530" y="100" width="180" height="90" rx="8" fill="rgba(251, 191, 36, 0.2)" stroke="url(#paddleYellow)" stroke-width="2.5" filter="url(#paddleShadow)"/>
    <text x="620" y="135" font-size="28" text-anchor="middle">📦</text>
    <text x="620" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Bounding Boxes
    </text>
    <text x="620" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#cbd5e1" text-anchor="middle">
      Polygons (x,y coords)
    </text>
  </g>
  
  <!-- Arrow -->
  <line x1="710" y1="145" x2="750" y2="145" stroke="#34d399" stroke-width="2.5" marker-end="url(#paddleArrow)" opacity="0.7"/>
  
  <!-- Text Recognition (CRNN) -->
  <g>
    <rect x="760" y="100" width="280" height="90" rx="8" fill="rgba(167, 139, 250, 0.2)" stroke="url(#paddlePurple)" stroke-width="2.5" filter="url(#paddleShadow)"/>
    <text x="900" y="128" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Text Recognition
    </text>
    <text x="900" y="148" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1" text-anchor="middle">
      CRNN Architecture
    </text>
    <text x="900" y="166" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      CNN + BiLSTM + CTC
    </text>
    <text x="900" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Fine-tuned on Tifinagh
    </text>
  </g>
  
  <!-- Output -->
  <g>
    <rect x="900" y="220" width="140" height="70" rx="8" fill="rgba(34, 211, 153, 0.3)" stroke="url(#paddleGreen)" stroke-width="2.5" filter="url(#paddleShadow)"/>
    <text x="970" y="250" font-size="24" text-anchor="middle">✅</text>
    <text x="970" y="275" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#34d399" text-anchor="middle">
      Final Output
    </text>
  </g>
  
  <!-- Arrow down -->
  <line x1="900" y1="190" x2="900" y2="210" stroke="#34d399" stroke-width="2.5" opacity="0" />
  <line x1="970" y1="190" x2="970" y2="210" stroke="#34d399" stroke-width="2.5" marker-end="url(#paddleArrow)" opacity="0.7"/>
  
  <!-- DB++ Architecture Details -->
  <g>
    <rect x="50" y="230" width="400" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#paddleShadow)"/>
    <text x="250" y="260" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      🔍 DB++ Text Detection
    </text>
    
    <text x="70" y="290" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#34d399">Backbone:</tspan> ResNet50 (Pretrained)
    </text>
    <text x="70" y="313" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#60a5fa">Feature Pyramid:</tspan> FPN for multi-scale
    </text>
    <text x="70" y="336" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#a78bfa">Head:</tspan> Probability + Threshold maps
    </text>
    <text x="70" y="359" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#fbbf24">Output:</tspan> Polygon coordinates (x,y)
    </text>
    <text x="70" y="382" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#f472b6">Performance:</tspan> 95.3% detection rate
    </text>
  </g>
  
  <!-- CRNN Architecture Details -->
  <g>
    <rect x="470" y="230" width="400" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#paddleShadow)"/>
    <text x="670" y="260" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#a78bfa" text-anchor="middle">
      📝 CRNN Text Recognition
    </text>
    
    <text x="490" y="290" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#60a5fa">CNN:</tspan> 7 convolutional layers
    </text>
    <text x="490" y="313" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#a78bfa">RNN:</tspan> 2 BiLSTM layers (256 units)
    </text>
    <text x="490" y="336" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#34d399">CTC:</tspan> Connectionist Temporal Classification
    </text>
    <text x="490" y="359" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#fbbf24">Vocabulary:</tspan> 33 Tifinagh characters
    </text>
    <text x="490" y="382" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#cbd5e1">
      <tspan font-weight="600" fill="#f472b6">Accuracy:</tspan> 89.6% on test set
    </text>
  </g>
  
  <!-- Training Process -->
  <g>
    <rect x="50" y="440" width="500" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#paddleShadow)"/>
    <text x="300" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#60a5fa" text-anchor="middle">
      🎓 Fine-tuning Process
    </text>
    
    <g>
      <text x="70" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#34d399">
        Detection Model:
      </text>
      <text x="85" y="528" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Pretrained: ICDAR2015 dataset
      </text>
      <text x="85" y="548" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Fine-tuned: 5000 Tifinagh images
      </text>
      <text x="85" y="568" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Epochs: 300 (early stopping)
      </text>
      <text x="85" y="588" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Learning rate: 0.001 → 0.0001
      </text>
    </g>
    
    <g>
      <text x="310" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#a78bfa">
        Recognition Model:
      </text>
      <text x="325" y="528" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Pretrained: Multi-language CRNN
      </text>
      <text x="325" y="548" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Fine-tuned: AMHCD dataset
      </text>
      <text x="325" y="568" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Epochs: 200 with augmentation
      </text>
      <text x="325" y="588" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        • Batch size: 256
      </text>
    </g>
  </g>
  
  <!-- Performance Metrics -->
  <g>
    <rect x="580" y="440" width="490" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#paddleShadow)"/>
    <text x="825" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      📊 Performance Metrics
    </text>
    
    <text x="600" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#34d399">Detection Precision:</tspan> 95.3%
    </text>
    <text x="600" y="530" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#60a5fa">Detection Recall:</tspan> 92.7%
    </text>
    <text x="600" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#a78bfa">Recognition Accuracy:</tspan> 89.6%
    </text>
    <text x="600" y="580" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#fbbf24">Character Error Rate:</tspan> 10.8%
    </text>
    <text x="600" y="605" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#cbd5e1">
      <tspan font-weight="600" fill="#f472b6">Inference Speed:</tspan> ~45ms/image
    </text>
  </g>
  
  <!-- Footer -->
  <text x="550" y="640" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" font-style="italic" fill="#94a3b8" text-anchor="middle">
    🏆 Best performance on complex layouts and multi-line text | End-to-end pipeline
  </text>
</svg>

---

## 💻 User Interface

### Features

✅ **Upload Image:** Support PNG, JPG, JPEG  
✅ **Take Picture:** Direct capture via webcam  
✅ **Real-time Recognition:** Instant results  
✅ **Copy Output:** Copy recognized text  
✅ **Multi-format Export:** TXT, JSON, CSV  

### Interface Screenshots

**Azul OCR intuitive user interface**

<div class="component-grid">
  <div class="component-card">
    <h4>Azul Interface</h4>
    <img src="{{ site.baseurl }}/assets/img/projects/azul_interface.jpeg" alt="Gate Shift Modules">
</div>
</div>
---

## 🛠️ Challenges & Solutions

### Challenge 1: Handwriting Variability

**Problem:** Great diversity of writing styles  
**Solution:** 
- Intensive augmentation (×5)
- Hybrid model (fusion of 3 approaches)
- Fine-tuning on real data

### Challenge 2: Limited Dataset

**Problem:** Few annotated data available  
**Solution:**
- Collaboration with IRCAM
- Aggressive data augmentation
- Transfer learning from pre-trained models

### Challenge 3: Sentence Recognition

**Problem:** Difficult word segmentation  
**Solution:**
- Use of PaddleOCR for detection
- Post-processing with linguistic rules
- Contextual correction

---

## 💼 Impact & Value

### For Cultural Heritage

✅ **Digital preservation** of ancient manuscripts  
✅ **Accessibility** of Amazigh texts to all  
✅ **Facilitated education** for new generations  
✅ **Academic research** on Amazigh culture  

### For Institutions

✅ **Rapid digitization** of archives  
✅ **Automatic indexing** of documents  
✅ **Text search** in digital corpus  
✅ **Reduced costs** vs manual annotation  

---

## 🔮 Future Improvements

**Short-Term:**
- Improve accuracy on complex sentences (>95%)
- Support for regional Tifinagh variants
- REST API for external integration

**Long-Term:**
- Mobile application (iOS/Android)
- Recognition of degraded historical texts
- Extension to other African alphabets
- Multilingual OCR (Tifinagh + Latin + Arabic)

---

## 🛠️ Technical Stack

**Deep Learning:** TensorFlow, Keras, PyTorch  
**OCR Engines:** Tesseract 4.0, PaddleOCR  
**Computer Vision:** OpenCV, scikit-image  
**Frontend:** React.js, HTML5, CSS3  
**Backend:** Flask, FastAPI  
**Deployment:** Docker, Heroku

---

## 🎓 Skills Developed

- **OCR Development:** Fine-tuning Tesseract/PaddleOCR
- **CNN Architecture:** Custom model design
- **Image Processing:** Otsu, filtering, augmentation
- **Team Collaboration:** 5-person agile team
- **Cultural Awareness:** Amazigh heritage preservation

---

## 📚 Key References

1. **Tesseract OCR** - Google Open Source
2. **PaddleOCR** - PaddlePaddle Team
3. **AMHCD Dataset** - IRCAM & Ibn Zohr University
4. **Otsu Thresholding** - IEEE Trans. SMC (1979)

---

## 📧 Contact

**Team Lead:** Rima Daqch  
**Technical Lead:** El Mehdi Hicham  
**Email:** mehdihicham736@gmail.com  
**LinkedIn:** [linkedin.com/in/elmehdihicham](https://linkedin.com/in/elmehdihicham)  
**GitHub:** [github.com/MehdiHCH](https://github.com/MehdiHCH)

**Supervisor:** Prof. Khadija Lekdioui  
**Institution:** Faculty of Sciences, Ibn Tofail University

---

## 🏆 Achievements

✅ **94.2% Accuracy** on character recognition  
✅ **91.2% Accuracy** on sentence recognition (hybrid)  
✅ **First Tifinagh OCR** open-source in Morocco  
✅ **Institutional collaboration** with IRCAM  
✅ **Intuitive interface** tested by 50+ users  

---

*"Every forgotten manuscript is a voice of humanity silenced."*  
*ⵛⴰⵇⴰ ⵎⴰⵏⵓⵙⵖⵔⵉⵜ ⵓⴱⵍⵉⵎ ⴻⵙⵜ ⵓⵏⴻ ⵓⵡⵏⴰⵙ ⴷⴻ ⵍⵓⵎⵍⵉⵏⵏⵉⵏ ⵔⴻⵙⵓⵉⵜⴰ ⵓⵢ ⵙⵉⵍⵓⵏⵉⵛ*

*Azul OCR - AI in service of Amazigh cultural heritage*