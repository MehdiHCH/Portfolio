---
title: Azul OCR - Reconnaissance d'Écriture Manuscrite Tifinagh
image: /assets/img/projects/azul.jpeg
description: Système OCR innovant utilisant CNN, Tesseract et PaddleOCR pour la reconnaissance de l'écriture manuscrite Tifinagh, préservant le patrimoine culturel Amazigh.
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

**Azul OCR** (ⴰⵣⵓⵍ - "Bonjour" en Amazigh) est un système OCR innovant spécialisé dans la **reconnaissance de l'écriture manuscrite Tifinagh**. Le projet vise à préserver et digitaliser le patrimoine culturel Amazigh en développant une solution d'intelligence artificielle capable de reconnaître précisément les caractères et phrases manuscrites en alphabet Tifinagh.

**Équipe:**
- **Rima Daqch** - Project Manager, Tesseract OCR Developer
- **Adil Eddarif** - Tesseract OCR Developer, CNN Model Developer
- **Brahim El Aboudi** - PaddleOCR Developer, CNN Model Developer
- **El Mehdi Hicham** - PaddleOCR Developer, CNN Model Developer
- **Zineb Lahraoui** - PaddleOCR Developer, CNN Model Developer

**Encadré par:** Prof. Khadija Lekdioui

**Mission:** *"Préserver et digitaliser le patrimoine culturel Amazigh"*

---

## 🔍 Problem Statement

### Challenges

**"L'écriture Tifinagh est un élément essentiel du patrimoine culturel Amazigh, mais elle reste sous-représentée dans les outils technologiques modernes."**

- 📚 **Manque d'outils OCR:** Aucune solution OCR dédiée aux manuscrits Tifinagh
- 🎨 **Complexité des caractères:** Variabilité importante de l'écriture manuscrite
- ⚠️ **Risque culturel:** Perte potentielle de contenus précieux pour les générations futures
- 🔬 **Précision limitée:** Solutions existantes inadaptées aux spécificités du Tifinagh

### Solution

Développement d'**Azul OCR**, système hybride combinant:
- **Tesseract OCR** fine-tuné pour le Tifinagh
- **PaddleOCR** adapté aux caractères Amazighs
- **CNN personnalisé** pour reconnaissance de caractères
- **Interface intuitive** pour capture et reconnaissance

---

## 🏗️ Technical Architecture


### 🔧 Key Components



#### **Module 1: Image Preprocessing**


**Techniques appliquées:**
- 🖼️ **Otsu Thresholding:** Binarisation automatique
- 📐 **Resizing:** 64×64 → 128×128 pixels
- 🎨 **Filtrage:** Réduction du bruit
- 🔄 **Augmentation:** Rotation, translation, zoom



#### **Module 2: Recognition Engines**


**Trois approches:**
- 📝 **Tesseract OCR:** Fine-tuné AMHCD dataset
- 🎯 **PaddleOCR:** Architecture légère adaptée
- 🧠 **CNN Custom:** Modèle entraîné from scratch
- 🔀 **Modèle hybride:** Fusion des prédictions

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
    <text x="200" y="552" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#64748b" text-anchor="middle">
      Accuracy: 94.2%
    </text>
  </g>
  
  <!-- Right Branch: Phrases -->
  <line x1="530" y1="380" x2="700" y2="380" stroke="#a78bfa" stroke-width="2.5" opacity="0.8"/>
  <line x1="700" y1="380" x2="700" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowPurple)" opacity="0.8"/>
  <text x="620" y="370" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa">
    Phrases
  </text>
  
  <!-- OCR Engines Box -->
  <g>
    <rect x="580" y="460" width="240" height="100" rx="10" fill="rgba(52, 211, 153, 0.15)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="700" y="485" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#34d399" text-anchor="middle">
      OCR Engines
    </text>
    
    <!-- Tesseract -->
    <rect x="595" y="500" width="100" height="25" rx="5" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1"/>
    <text x="645" y="518" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#34d399" text-anchor="middle">
      Tesseract
    </text>
    
    <!-- PaddleOCR -->
    <rect x="705" y="500" width="100" height="25" rx="5" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1"/>
    <text x="755" y="518" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#34d399" text-anchor="middle">
      PaddleOCR
    </text>
    
    <text x="700" y="548" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b" text-anchor="middle">
      Fine-tuned for Tifinagh
    </text>
  </g>
  
  <!-- Merge arrows to output -->
  <line x1="200" y1="560" x2="200" y2="600" stroke="#f472b6" stroke-width="2.5" opacity="0.8"/>
  <line x1="200" y1="600" x2="390" y2="600" stroke="#f472b6" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <line x1="700" y1="560" x2="700" y2="600" stroke="#34d399" stroke-width="2.5" opacity="0.8"/>
  <line x1="700" y1="600" x2="510" y2="600" stroke="#34d399" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Character Recognition Output -->
  <g>
    <rect x="400" y="580" width="100" height="40" rx="8" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <text x="450" y="605" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#60a5fa" text-anchor="middle">
      ⴰ ⵣ ⵓ ⵍ
    </text>
  </g>
  
  <!-- Arrow to final output -->
  <line x1="450" y1="620" x2="450" y2="650" stroke="#60a5fa" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Final Output -->
  <g>
    <rect x="300" y="660" width="300" height="30" rx="8" fill="rgba(52, 211, 153, 0.2)" stroke="url(#greenGrad)" stroke-width="2" filter="url(#glow)"/>
    <text x="450" y="680" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#34d399" text-anchor="middle">
      📄 Output Text (JSON/TXT/CSV)
    </text>
  </g>
  
  <!-- Performance Stats Box -->
  <g>
    <rect x="40" y="90" width="260" height="260" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2"/>
    <text x="170" y="120" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Performance Metrics
    </text>
    
    <!-- CNN Accuracy -->
    <rect x="60" y="140" width="220" height="45" rx="6" fill="rgba(244, 114, 182, 0.1)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="170" y="160" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#f472b6" text-anchor="middle">
      94.2%
    </text>
    <text x="170" y="177" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      CNN Character Recognition
    </text>
    
    <!-- Tesseract -->
    <rect x="60" y="200" width="220" height="45" rx="6" fill="rgba(52, 211, 153, 0.1)" stroke="#34d399" stroke-width="1.5"/>
    <text x="170" y="220" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      87.3%
    </text>
    <text x="170" y="237" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Tesseract Phrase Accuracy
    </text>
    
    <!-- PaddleOCR -->
    <rect x="60" y="260" width="220" height="45" rx="6" fill="rgba(52, 211, 153, 0.1)" stroke="#34d399" stroke-width="1.5"/>
    <text x="170" y="280" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      89.6%
    </text>
    <text x="170" y="297" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      PaddleOCR Phrase Accuracy
    </text>
    
    <!-- Hybrid -->
    <rect x="60" y="320" width="220" height="20" rx="5" fill="rgba(96, 165, 250, 0.2)" stroke="#60a5fa" stroke-width="1.5"/>
    <text x="170" y="334" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Hybrid Model: 91.2% ⭐
    </text>
  </g>
  
  <!-- Dataset Info Box -->
  <g>
    <rect x="600" y="90" width="260" height="260" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2"/>
    <text x="730" y="120" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Dataset & Training
    </text>
    
    <text x="620" y="150" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#fbbf24">
      AMHCD Dataset
    </text>
    <text x="620" y="170" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • 33 Tifinagh classes
    </text>
    <text x="620" y="188" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Original: 64×64×3 RGB
    </text>
    <text x="620" y="206" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Augmented: ×5 samples
    </text>
    <text x="620" y="224" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Final size: 128×128 pixels
    </text>
    
    <line x1="620" y1="240" x2="840" y2="240" stroke="#475569" stroke-width="1"/>
    
    <text x="620" y="260" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa">
      Augmentation
    </text>
    <text x="620" y="278" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Rotation: ±15°
    </text>
    <text x="620" y="296" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Translation: ±10%
    </text>
    <text x="620" y="314" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Zoom: 0.9-1.1×
    </text>
    <text x="620" y="332" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Brightness: ±20%
    </text>
  </g>
</svg>

---

## 📦 Dataset & Preprocessing

### AMHCD Dataset

**Source:** IRCAM (Institut Royal de la Culture Amazighe)  
**Collaborations:** ENCG et Laboratoire IRF-SIC, Université Ibn Zohr, Agadir

**Caractéristiques:**
- 📊 **33 classes** de caractères Tifinagh
- 🖼️ **Format original:** 64×64×3 (RGB)
- 📈 **Augmentation:** ×5 par technique
- 🎯 **Résolution finale:** 128×128 pixels

### Preprocessing Pipeline

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 800" style="background: transparent;">
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
    
    <linearGradient id="cyanGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#22d3ee;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#06b6d4;stop-opacity:1" />
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
  </defs>
  
  <!-- Title -->
  <text x="500" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="32" font-weight="700" fill="url(#cyanGrad)" text-anchor="middle" filter="url(#glow)">
    Azul OCR - Preprocessing Pipeline
  </text>
  <text x="500" y="65" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" fill="#94a3b8" text-anchor="middle">
    ⴰⵣⵓⵍ - Tifinagh Handwriting Recognition
  </text>
  
  <!-- Input Image -->
  <g>
    <rect x="50" y="120" width="160" height="140" rx="10" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="130" y="160" font-size="40" text-anchor="middle">📝</text>
    <text x="130" y="200" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Input Image
    </text>
    <text x="130" y="225" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      64×64×3 (RGB)
    </text>
    <text x="130" y="245" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#64748b" text-anchor="middle">
      AMHCD Dataset
    </text>
  </g>
  
  <!-- Arrow 1 -->
  <line x1="210" y1="190" x2="260" y2="190" stroke="#60a5fa" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Step 1: Grayscale Conversion -->
  <g>
    <rect x="270" y="120" width="180" height="140" rx="10" fill="rgba(167, 139, 250, 0.15)" stroke="url(#purpleGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <circle cx="300" cy="150" r="18" fill="url(#purpleGrad)" filter="url(#glow)"/>
    <text x="300" y="158" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#0f172a" text-anchor="middle">1</text>
    
    <text x="360" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Grayscale
    </text>
    <text x="360" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Conversion
    </text>
    <text x="290" y="205" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      RGB → Grayscale
    </text>
    <text x="290" y="225" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      64×64×3 → 64×64×1
    </text>
    <text x="290" y="245" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      cv2.cvtColor(GRAY)
    </text>
  </g>
  
  <!-- Arrow 2 -->
  <line x1="450" y1="190" x2="500" y2="190" stroke="#a78bfa" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Step 2: Otsu Thresholding -->
  <g>
    <rect x="510" y="120" width="180" height="140" rx="10" fill="rgba(251, 191, 36, 0.15)" stroke="url(#yellowGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <circle cx="540" cy="150" r="18" fill="url(#yellowGrad)" filter="url(#glow)"/>
    <text x="540" y="158" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#0f172a" text-anchor="middle">2</text>
    
    <text x="600" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Otsu
    </text>
    <text x="600" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Thresholding
    </text>
    <text x="530" y="205" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      Automatic binarization
    </text>
    <text x="530" y="225" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      Grayscale → Binary
    </text>
    <text x="530" y="245" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      cv2.threshold(OTSU)
    </text>
  </g>
  
  <!-- Arrow 3 -->
  <line x1="690" y1="190" x2="740" y2="190" stroke="#fbbf24" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Step 3: Gaussian Filtering -->
  <g>
    <rect x="750" y="120" width="180" height="140" rx="10" fill="rgba(34, 211, 238, 0.15)" stroke="url(#cyanGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <circle cx="780" cy="150" r="18" fill="url(#cyanGrad)" filter="url(#glow)"/>
    <text x="780" y="158" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#0f172a" text-anchor="middle">3</text>
    
    <text x="840" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#22d3ee" text-anchor="middle">
      Gaussian
    </text>
    <text x="840" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#22d3ee" text-anchor="middle">
      Filtering
    </text>
    <text x="770" y="205" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      Noise reduction
    </text>
    <text x="770" y="225" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      Kernel: 5×5
    </text>
    <text x="770" y="245" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      cv2.GaussianBlur()
    </text>
  </g>
  
  <!-- Arrow down from center -->
  <line x1="500" y1="260" x2="500" y2="320" stroke="#22d3ee" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Step 4: Resizing -->
  <g>
    <rect x="380" y="330" width="240" height="140" rx="10" fill="rgba(52, 211, 153, 0.15)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <circle cx="410" cy="360" r="18" fill="url(#greenGrad)" filter="url(#glow)"/>
    <text x="410" y="368" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#0f172a" text-anchor="middle">4</text>
    
    <text x="500" y="365" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#34d399" text-anchor="middle">
      Resizing (Upscaling)
    </text>
    <text x="400" y="400" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      64×64 → 128×128 pixels
    </text>
    <text x="400" y="423" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Preserve fine details
    </text>
    <text x="400" y="446" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#64748b">
      cv2.resize(INTER_CUBIC)
    </text>
  </g>
  
  <!-- Arrow down -->
  <line x1="500" y1="470" x2="500" y2="530" stroke="#34d399" stroke-width="3" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Step 5: Normalization & Augmentation -->
  <g>
    <rect x="210" y="540" width="580" height="180" rx="10" fill="rgba(167, 139, 250, 0.15)" stroke="url(#purpleGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <circle cx="240" cy="570" r="18" fill="url(#purpleGrad)" filter="url(#glow)"/>
    <text x="240" y="578" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#0f172a" text-anchor="middle">5</text>
    
    <text x="500" y="575" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="19" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Normalization & Data Augmentation
    </text>
    
    <!-- Normalization -->
    <rect x="230" y="600" width="250" height="100" rx="8" fill="rgba(167, 139, 250, 0.2)" stroke="#a78bfa" stroke-width="1.5"/>
    <text x="355" y="625" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Normalization
    </text>
    <text x="245" y="650" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Pixel values: [0, 255] → [0, 1]
    </text>
    <text x="245" y="670" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Mean subtraction
    </text>
    <text x="245" y="690" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Standard deviation scaling
    </text>
    
    <!-- Augmentation -->
    <rect x="510" y="600" width="260" height="100" rx="8" fill="rgba(167, 139, 250, 0.2)" stroke="#a78bfa" stroke-width="1.5"/>
    <text x="640" y="625" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Augmentation (×5)
    </text>
    <text x="525" y="650" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Rotation: ±15°
    </text>
    <text x="525" y="670" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Translation: ±10%
    </text>
    <text x="525" y="690" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Zoom: 0.9-1.1×, Brightness: ±20%
    </text>
  </g>
  
  <!-- Arrow to output -->
  <line x1="500" y1="720" x2="500" y2="750" stroke="#a78bfa" stroke-width="3" opacity="0.8"/>
  
  <!-- Output: Ready for Training -->
  <g>
    <rect x="340" y="750" width="320" height="35" rx="8" fill="rgba(52, 211, 153, 0.2)" stroke="url(#greenGrad)" stroke-width="2" filter="url(#glow)"/>
    <text x="500" y="773" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#34d399" text-anchor="middle">
      ✅ Ready for Model Training (128×128×1)
    </text>
  </g>
</svg>

## 🚀 Model Architecture

### Custom CNN Model

**Architecture:**
```
Input (128×128×1)
    ↓
Conv2D (32 filters) + ReLU + MaxPool
    ↓
Conv2D (64 filters) + ReLU + MaxPool
    ↓
Conv2D (128 filters) + ReLU + MaxPool
    ↓
Flatten + Dense(256) + Dropout(0.5)
    ↓
Dense(33) + Softmax
```

**Hyperparamètres:**
- Optimizer: Adam (lr=0.001)
- Loss: Categorical Crossentropy
- Batch Size: 32
- Epochs: 50

### Tesseract Fine-Tuning

- **Baseline:** Tesseract 4.0 pré-entraîné
- **Fine-tuning:** AMHCD dataset (2000+ samples)
- **Language:** `tif` (Tifinagh custom traineddata)

### PaddleOCR Adaptation

- **Architecture:** Lightweight PP-OCRv3
- **Detection:** DB++ (Differentiable Binarization)
- **Recognition:** CRNN fine-tuné sur Tifinagh

---

## 📊 Results & Performance

### Character Recognition (CNN)

| Métrique | Score |
|----------|-------|
| **Accuracy** | 94.2% |
| **Precision** | 93.8% |
| **Recall** | 94.5% |
| **F1-Score** | 94.1% |

### Phrase Recognition

| Modèle | Accuracy | CER* | WER** |
|--------|----------|------|-------|
| **Tesseract** | 87.3% | 12.5% | 18.2% |
| **PaddleOCR** | 89.6% | 10.8% | 15.4% |
| **Hybrid*** | 91.2% | 9.1% | 13.7% |


### Performance Comparison

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1100 650" style="background: transparent;">
  <defs>
    <linearGradient id="pinkGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f472b6;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#ec4899;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="blueGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="greenGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Title -->
  <text x="550" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="30" font-weight="700" fill="url(#pinkGrad)" text-anchor="middle" filter="url(#glow)">
    Azul OCR - Recognition Models Comparison
  </text>
  
  <!-- Model 1: Custom CNN -->
  <g>
    <rect x="50" y="80" width="320" height="520" rx="12" fill="rgba(244, 114, 182, 0.12)" stroke="url(#pinkGrad)" stroke-width="2.5" filter="url(#glow)"/>
    
    <text x="210" y="115" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="600" fill="#f472b6" text-anchor="middle">
      Custom CNN
    </text>
    <text x="210" y="138" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
      Character Recognition
    </text>
    
    <!-- Architecture layers -->
    <rect x="70" y="160" width="280" height="35" rx="6" fill="rgba(244, 114, 182, 0.2)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="210" y="183" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#f472b6" text-anchor="middle">
      Input: 128×128×1
    </text>
    
    <text x="210" y="210" font-size="16" fill="#f472b6">↓</text>
    
    <rect x="70" y="220" width="280" height="35" rx="6" fill="rgba(244, 114, 182, 0.2)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="210" y="243" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#f472b6" text-anchor="middle">
      Conv2D(32) + ReLU + MaxPool
    </text>
    
    <text x="210" y="270" font-size="16" fill="#f472b6">↓</text>
    
    <rect x="70" y="280" width="280" height="35" rx="6" fill="rgba(244, 114, 182, 0.2)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="210" y="303" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#f472b6" text-anchor="middle">
      Conv2D(64) + ReLU + MaxPool
    </text>
    
    <text x="210" y="330" font-size="16" fill="#f472b6">↓</text>
    
    <rect x="70" y="340" width="280" height="35" rx="6" fill="rgba(244, 114, 182, 0.2)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="210" y="363" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#f472b6" text-anchor="middle">
      Conv2D(128) + ReLU + MaxPool
    </text>
    
    <text x="210" y="390" font-size="16" fill="#f472b6">↓</text>
    
    <rect x="70" y="400" width="280" height="35" rx="6" fill="rgba(244, 114, 182, 0.2)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="210" y="423" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#f472b6" text-anchor="middle">
      Flatten + Dense(256) + Dropout(0.5)
    </text>
    
    <text x="210" y="450" font-size="16" fill="#f472b6">↓</text>
    
    <rect x="70" y="460" width="280" height="35" rx="6" fill="rgba(244, 114, 182, 0.2)" stroke="#f472b6" stroke-width="1.5"/>
    <text x="210" y="483" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#f472b6" text-anchor="middle">
      Output: Dense(33) + Softmax
    </text>
    
    <!-- Stats -->
    <rect x="70" y="515" width="280" height="70" rx="6" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="1.5"/>
    <text x="210" y="538" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#f472b6" text-anchor="middle">
      94.2% Accuracy
    </text>
    <text x="210" y="558" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Training: 50 epochs
    </text>
    <text x="210" y="575" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Optimizer: Adam (lr=0.001)
    </text>
  </g>
  
  <!-- Model 2: Tesseract OCR -->
  <g>
    <rect x="390" y="80" width="320" height="520" rx="12" fill="rgba(96, 165, 250, 0.12)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    
    <text x="550" y="115" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Tesseract OCR
    </text>
    <text x="550" y="138" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
      Phrase Recognition
    </text>
    
    <!-- Architecture components -->
    <rect x="410" y="160" width="280" height="45" rx="6" fill="rgba(96, 165, 250, 0.2)" stroke="#60a5fa" stroke-width="1.5"/>
    <text x="550" y="178" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#60a5fa" text-anchor="middle">
      Tesseract 4.0 Engine
    </text>
    <text x="550" y="196" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      LSTM-based recognition
    </text>
    
    <text x="550" y="220" font-size="16" fill="#60a5fa">↓</text>
    
    <rect x="410" y="235" width="280" height="45" rx="6" fill="rgba(96, 165, 250, 0.2)" stroke="#60a5fa" stroke-width="1.5"/>
    <text x="550" y="253" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#60a5fa" text-anchor="middle">
      Fine-tuning
    </text>
    <text x="550" y="271" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      AMHCD Dataset (2000+ samples)
    </text>
    
    <text x="550" y="295" font-size="16" fill="#60a5fa">↓</text>
    
    <rect x="410" y="310" width="280" height="45" rx="6" fill="rgba(96, 165, 250, 0.2)" stroke="#60a5fa" stroke-width="1.5"/>
    <text x="550" y="328" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#60a5fa" text-anchor="middle">
      Custom Language Model
    </text>
    <text x="550" y="346" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      .traineddata file for Tifinagh
    </text>
    
    <text x="550" y="370" font-size="16" fill="#60a5fa">↓</text>
    
    <rect x="410" y="385" width="280" height="45" rx="6" fill="rgba(96, 165, 250, 0.2)" stroke="#60a5fa" stroke-width="1.5"/>
    <text x="550" y="403" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#60a5fa" text-anchor="middle">
      Text Detection + Recognition
    </text>
    <text x="550" y="421" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      Word & line segmentation
    </text>
    
    <text x="550" y="445" font-size="16" fill="#60a5fa">↓</text>
    
    <rect x="410" y="460" width="280" height="35" rx="6" fill="rgba(96, 165, 250, 0.2)" stroke="#60a5fa" stroke-width="1.5"/>
    <text x="550" y="483" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#60a5fa" text-anchor="middle">
      Output: Text strings
    </text>
    
    <!-- Stats -->
    <rect x="410" y="515" width="280" height="70" rx="6" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="1.5"/>
    <text x="550" y="538" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#60a5fa" text-anchor="middle">
      87.3% Accuracy
    </text>
    <text x="550" y="558" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      CER: 12.5% | WER: 18.2%
    </text>
    <text x="550" y="575" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Best for: Longer phrases
    </text>
  </g>
  
  <!-- Model 3: PaddleOCR -->
  <g>
    <rect x="730" y="80" width="320" height="520" rx="12" fill="rgba(52, 211, 153, 0.12)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    
    <text x="890" y="115" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="600" fill="#34d399" text-anchor="middle">
      PaddleOCR
    </text>
    <text x="890" y="138" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
      Phrase Recognition
    </text>
    
    <!-- Architecture components -->
    <rect x="750" y="160" width="280" height="45" rx="6" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="890" y="178" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#34d399" text-anchor="middle">
      PP-OCRv3 Architecture
    </text>
    <text x="890" y="196" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      Lightweight & efficient
    </text>
    
    <text x="890" y="220" font-size="16" fill="#34d399">↓</text>
    
    <rect x="750" y="235" width="280" height="45" rx="6" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="890" y="253" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#34d399" text-anchor="middle">
      Text Detection
    </text>
    <text x="890" y="271" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      DB++ (Differentiable Binarization)
    </text>
    
    <text x="890" y="295" font-size="16" fill="#34d399">↓</text>
    
    <rect x="750" y="310" width="280" height="45" rx="6" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="890" y="328" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#34d399" text-anchor="middle">
      Text Recognition
    </text>
    <text x="890" y="346" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      CRNN fine-tuned on Tifinagh
    </text>
    
    <text x="890" y="370" font-size="16" fill="#34d399">↓</text>
    
    <rect x="750" y="385" width="280" height="45" rx="6" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="890" y="403" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#34d399" text-anchor="middle">
      Post-processing
    </text>
    <text x="890" y="421" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      Language model correction
    </text>
    
    <text x="890" y="445" font-size="16" fill="#34d399">↓</text>
    
    <rect x="750" y="460" width="280" height="35" rx="6" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="890" y="483" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#34d399" text-anchor="middle">
      Output: Structured text + boxes
    </text>
    
    <!-- Stats -->
    <rect x="750" y="515" width="280" height="70" rx="6" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="1.5"/>
    <text x="890" y="538" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="700" fill="#34d399" text-anchor="middle">
      89.6% Accuracy ⭐
    </text>
    <text x="890" y="558" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      CER: 10.8% | WER: 15.4%
    </text>
    <text x="890" y="575" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Best for: Complex layouts
    </text>
  </g>
  
  <!-- Hybrid Model Banner -->
  <g>
    <rect x="150" y="620" width="800" height="20" rx="5" fill="rgba(167, 139, 250, 0.2)" stroke="#a78bfa" stroke-width="1.5"/>
    <text x="550" y="634" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa" text-anchor="middle">
      🏆 Hybrid Model (Weighted Voting): 91.2% Accuracy | Best Overall Performance
    </text>
  </g>
</svg>

---

## 💻 User Interface

### Features

✅ **Upload Image:** Support PNG, JPG, JPEG  
✅ **Take Picture:** Capture directe via webcam  
✅ **Real-time Recognition:** Résultats instantanés  
✅ **Copy Output:** Copie du texte reconnu  
✅ **Multi-format Export:** TXT, JSON, CSV  

### Interface Screenshots

**Interface utilisateur intuitive d'Azul OCR**

<div class="component-grid">
  <div class="component-card">
    <h4>Azul Interface</h4>
    <img src="{{ site.baseurl }}/assets/img/projects/azul_interface.jpeg" alt="Gate Shift Modules">
</div>
</div>
---

## 🛠️ Challenges & Solutions

### Challenge 1: Variabilité de l'Écriture Manuscrite

**Problème:** Grande diversité de styles d'écriture  
**Solution:** 
- Augmentation intensive (×5)
- Modèle hybride (fusion de 3 approches)
- Fine-tuning sur données réelles

### Challenge 2: Dataset Limité

**Problème:** Peu de données annotées disponibles  
**Solution:**
- Collaboration avec IRCAM
- Data augmentation aggressive
- Transfer learning depuis modèles pré-entraînés

### Challenge 3: Reconnaissance de Phrases

**Problème:** Segmentation difficile entre mots  
**Solution:**
- Utilisation de PaddleOCR pour détection
- Post-processing avec règles linguistiques
- Correction contextuelle

---

## 💼 Impact & Value

### For Cultural Heritage

✅ **Préservation numérique** de manuscrits anciens  
✅ **Accessibilité** des textes Amazighs à tous  
✅ **Éducation** facilitée pour les nouvelles générations  
✅ **Recherche** académique sur la culture Amazigh  

### For Institutions

✅ **Digitalisation rapide** des archives  
✅ **Indexation automatique** de documents  
✅ **Recherche textuelle** dans corpus numériques  
✅ **Coûts réduits** vs annotation manuelle  

---

## 🔮 Future Improvements

**Short-Term:**
- Améliorer précision sur phrases complexes (>95%)
- Support de variantes régionales du Tifinagh
- API REST pour intégration externe

**Long-Term:**
- Application mobile (iOS/Android)
- Reconnaissance de textes historiques dégradés
- Extension à d'autres alphabets africains
- OCR multilingue (Tifinagh + Latin + Arabe)

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
3. **AMHCD Dataset** - IRCAM & Université Ibn Zohr
4. **Otsu Thresholding** - IEEE Trans. SMC (1979)

---

## 📧 Contact

**Team Lead:** Rima Daqch  
**Technical Lead:** El Mehdi Hicham  
**Email:** mehdihicham736@gmail.com  
**LinkedIn:** [linkedin.com/in/elmehdihicham](https://linkedin.com/in/elmehdihicham)  
**GitHub:** [github.com/MehdiHCH](https://github.com/MehdiHCH)

**Supervisor:** Prof. Khadija Lekdioui  
**Institution:** Faculté des Sciences, Ibn Tofail University

---

## 🏆 Achievements

✅ **94.2% Accuracy** sur reconnaissance de caractères  
✅ **91.2% Accuracy** sur reconnaissance de phrases (hybride)  
✅ **Premier OCR Tifinagh** open-source au Maroc  
✅ **Collaboration institutionnelle** avec IRCAM  
✅ **Interface intuitive** testée par 50+ utilisateurs  

---

*"Chaque manuscrit oublié est une voix de l'humanité réduite au silence."*  
*ⵛⴰⵇⴰ ⵎⴰⵏⵓⵙⵖⵔⵉⵜ ⵓⴱⵍⵉⵎ ⴻⵙⵜ ⵓⵏⴻ ⵓⵡⵏⴰⵙ ⴷⴻ ⵍⵓⵎⵍⵉⵏⵏⵉⵏ ⵔⴻⵙⵓⵉⵜⴰ ⵓⵢ ⵙⵉⵍⵓⵏⵉⵛ*

*Azul OCR - L'IA au service du patrimoine culturel Amazigh*