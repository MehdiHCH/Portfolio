---
title: RoboRangers - Voiture Autonome avec Deep Reinforcement Learning
image: /assets/img/projects/roborangers.gif
description: Système de navigation autonome utilisant ROS2, Gazebo et Deep Reinforcement Learning (TD3) pour une conduite intelligente et sécurisée dans des environnements dynamiques.
category: robotics
tags:
  - Autonomous Driving
  - ROS2
  - Gazebo
  - Deep Reinforcement Learning
  - TD3
  - LIDAR
  - Computer Vision
  - Robotics
demo: /assets/videos/roborangers_demo.mp4
date: 2024-06-15
company: Academic Project
location: Ibn Tofail University, Kenitra
duration: February 2024 - June 2024
github: https://github.com/MEHDI57-NRG/RoboRangers
---

## 🎯 Project Overview

**RoboRangers** est un projet de **voiture autonome** utilisant **Deep Reinforcement Learning (DRL)** et **ROS2** pour la navigation intelligente dans des environnements simulés. Le système intègre des capteurs LIDAR et caméras pour une perception complète, et implémente l'algorithme **TD3** (Twin Delayed Deep Deterministic Policy Gradient) pour la prise de décision autonome.

**Équipe:**
- **ALAMI AROUSSI Zineb**
- **GRICHE MOHAMMED Imrane**
- **HICHAM EL Mehdi**
- **MOUTIA Salma**

**Sous la direction de:** Pr. BOUKIR Khaoula

**Mission:** Développer un véhicule autonome capable de naviguer, éviter les obstacles et respecter les panneaux de signalisation dans un environnement dynamique.

---

## 🔍 Problem Statement

### Challenges

**Problématique:** Comment permettre à un système d'apprendre à prendre des décisions en temps réel en fonction des changements dans son environnement tout en garantissant sécurité et efficacité?

- 🚗 **Accidents routiers:** Erreurs humaines = principale cause de décès
- 🚦 **Embouteillages:** Pertes économiques et pollution
- 👥 **Accessibilité:** Mobilité limitée pour personnes âgées/handicapées
- 🌍 **Impact environnemental:** Émissions de CO2 élevées
- 🎯 **Navigation complexe:** Environnements dynamiques et imprévisibles

### Solution

Voiture autonome intégrant:
- **ROS2:** Communication inter-modules distribuée
- **Gazebo:** Simulation 3D réaliste pour tests sécurisés
- **DRL (TD3):** Apprentissage autonome par essai-erreur
- **Capteurs multi-modaux:** LIDAR + Caméras pour perception 360°

---

## 🏗️ Technical Architecture

<div align="center">

![RoboRangers Architecture](/assets/img/projects/roborangers_arch.png)

**Architecture système complète RoboRangers**

</div>

---

### 🔧 System Components

<table>
<tr>
<td width="50%" valign="top">

#### **Perception Layer**

![Sensors Integration](/assets/img/projects/roborangers_sensors.png)

**Capteurs:**
- 📹 **Caméras RGB:** Détection obstacles, panneaux
- 🔵 **LIDAR Velodyne:** Mesure distances 360°
- 📊 **Point Cloud Processing:** Données 3D temps réel
- 🎯 **Fusion sensorielle:** Perception robuste

</td>
<td width="50%" valign="top">

#### **Decision & Control**

![TD3 Algorithm](/assets/img/projects/roborangers_td3.png)

**Intelligence:**
- 🧠 **TD3 Agent:** Apprentissage par renforcement
- 🎮 **Action Selection:** Steering, accélération, freinage
- 📈 **Reward Function:** Sécurité + efficacité
- 🔄 **Continuous Learning:** Amélioration itérative

</td>
</tr>
</table>

---

### 📐 ROS2 Architecture

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 700" style="background: transparent;">
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
    
    <marker id="arrowGreen" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#34d399" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="500" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="32" font-weight="700" fill="url(#blueGrad)" text-anchor="middle" filter="url(#glow)">
    ROS2 Architecture - RoboRangers
  </text>
  
  <!-- Sensor Layer -->
  <g>
    <text x="100" y="100" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#94a3b8">
      Sensor Layer
    </text>
    
    <!-- Camera Node -->
    <rect x="50" y="120" width="180" height="100" rx="10" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="140" y="155" font-size="32" text-anchor="middle">🎥</text>
    <text x="140" y="185" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Camera Node
    </text>
    <text x="140" y="205" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      /camera/image_raw
    </text>
    
    <!-- LIDAR Node -->
    <rect x="260" y="120" width="180" height="100" rx="10" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="350" y="155" font-size="32" text-anchor="middle">📡</text>
    <text x="350" y="185" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      LIDAR Node
    </text>
    <text x="350" y="205" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      /scan (720 points)
    </text>
    
    <!-- Localization Node -->
    <rect x="470" y="120" width="180" height="100" rx="10" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="560" y="155" font-size="32" text-anchor="middle">📍</text>
    <text x="560" y="185" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Localization
    </text>
    <text x="560" y="205" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      /odom, /tf
    </text>
  </g>
  
  <!-- Arrows from Sensors to Fusion -->
  <line x1="140" y1="220" x2="350" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
  <line x1="350" y1="220" x2="350" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
  <line x1="560" y1="220" x2="350" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
  
  <!-- Fusion Layer -->
  <g>
    <text x="700" y="100" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#94a3b8">
      Processing Layer
    </text>
    
    <!-- Fusion Node -->
    <rect x="220" y="300" width="260" height="110" rx="10" fill="rgba(167, 139, 250, 0.15)" stroke="url(#purpleGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="350" y="340" font-size="28" text-anchor="middle">🔄</text>
    <text x="350" y="370" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Sensor Fusion Node
    </text>
    <text x="350" y="390" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Multi-modal perception
    </text>
  </g>
  
  <!-- Arrow to DRL Agent -->
  <line x1="350" y1="410" x2="500" y2="470" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Decision Layer -->
  <g>
    <text x="750" y="320" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#94a3b8">
      Decision Layer
    </text>
    
    <!-- TD3 DRL Agent -->
    <rect x="380" y="480" width="240" height="120" rx="10" fill="rgba(251, 191, 36, 0.15)" stroke="url(#yellowGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="500" y="520" font-size="28" text-anchor="middle">🧠</text>
    <text x="500" y="550" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#fbbf24" text-anchor="middle">
      TD3 DRL Agent
    </text>
    <text x="500" y="570" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Actor-Critic Network
    </text>
    <text x="500" y="587" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Action: [steering, velocity]
    </text>
  </g>
  
  <!-- Arrow to Control Node -->
  <line x1="500" y1="600" x2="350" y2="470" stroke="#fbbf24" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Control Layer -->
  <g>
    <text x="100" y="460" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#94a3b8">
      Control Layer
    </text>
    
    <!-- Control Node -->
    <rect x="50" y="480" width="240" height="100" rx="10" fill="rgba(52, 211, 153, 0.15)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="170" y="515" font-size="28" text-anchor="middle">🎮</text>
    <text x="170" y="545" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#34d399" text-anchor="middle">
      Control Node
    </text>
    <text x="170" y="565" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      /cmd_vel publisher
    </text>
  </g>
  
  <!-- Arrow to Actuators -->
  <line x1="170" y1="580" x2="170" y2="620" stroke="#34d399" stroke-width="2.5" marker-end="url(#arrowGreen)" opacity="0.8"/>
  
  <!-- Actuator Layer -->
  <g>
    <!-- Vehicle Actuators -->
    <rect x="50" y="630" width="240" height="40" rx="8" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <text x="170" y="655" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      🚗 Vehicle Actuators
    </text>
  </g>
  
  <!-- Arrow to Gazebo -->
  <line x1="290" y1="650" x2="370" y2="650" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Simulation Environment -->
  <g>
    <rect x="380" y="620" width="240" height="60" rx="10" fill="rgba(167, 139, 250, 0.15)" stroke="url(#purpleGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="500" y="655" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#a78bfa" text-anchor="middle">
      🌍 Gazebo Simulation
    </text>
  </g>
  
  <!-- Feedback loop to sensors -->
  <path d="M 620 650 L 680 650 L 680 170 L 650 170" stroke="#a78bfa" stroke-width="2.5" fill="none" marker-end="url(#arrowBlue)" opacity="0.6" stroke-dasharray="5,5"/>
  
  <!-- Legend Box -->
  <g>
    <rect x="700" y="400" width="260" height="260" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2"/>
    <text x="830" y="430" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#60a5fa" text-anchor="middle">
      ROS2 Topics
    </text>
    
    <!-- Topics list -->
    <text x="720" y="460" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      📷 /camera/image_raw
    </text>
    <text x="735" y="478" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      sensor_msgs/Image
    </text>
    
    <text x="720" y="502" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      📡 /scan
    </text>
    <text x="735" y="520" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      sensor_msgs/LaserScan
    </text>
    
    <text x="720" y="544" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      📍 /odom
    </text>
    <text x="735" y="562" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      nav_msgs/Odometry
    </text>
    
    <text x="720" y="586" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      🎮 /cmd_vel
    </text>
    <text x="735" y="604" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#64748b">
      geometry_msgs/Twist
    </text>
    
    <text x="830" y="635" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Communication
    </text>
    <text x="720" y="655" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8">
      • Publisher-Subscriber
    </text>
  </g>
</svg>

---

## ⚙️ ROS2 & Gazebo Integration

### ROS2 (Robot Operating System 2)

**Description:**
- Framework open-source pour développement robotique
- Communication distribuée entre nœuds
- Support multi-langages (Python, C++)
- Temps-réel et fiabilité

**Architecture de Communication:**
- **Publisher-Subscriber:** Topics pour échange de données
- **Master Node:** Coordination des connexions
- **Messages standardisés:** Formats prédéfinis (sensor_msgs, geometry_msgs)

### Gazebo Simulator

**Fonctionnalités:**
- 🌍 **Environnement 3D réaliste:** Routes, obstacles, panneaux
- ⚙️ **Moteur physique:** Gravité, collisions, friction
- 🤖 **Multi-robots:** Simulations à grande échelle
- 🔗 **Intégration ROS2:** Communication seamless

**Avantages:**
- Tests sécurisés sans risque matériel
- Itérations rapides sur algorithmes
- Scénarios reproductibles

---

## 🚀 TD3 (Twin Delayed DDPG) Algorithm

### Description

**TD3** améliore DDPG (Deep Deterministic Policy Gradient) avec 3 innovations:
1. **Twin Critics:** Deux réseaux critiques pour réduire biais
2. **Delayed Policy Updates:** Maj acteur moins fréquente
3. **Target Policy Smoothing:** Bruit sur actions target

### Architecture

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 1100" style="background: transparent;">
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
    
    <linearGradient id="orangeGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#fb923c;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#f97316;stop-opacity:1" />
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
  <text x="400" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="30" font-weight="700" fill="url(#blueGrad)" text-anchor="middle" filter="url(#glow)">
    TD3 Agent Architecture
  </text>
  <text x="400" y="65" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" fill="#94a3b8" text-anchor="middle">
    Twin Delayed Deep Deterministic Policy Gradient
  </text>
  
  <!-- Main Container -->
  <rect x="80" y="100" width="640" height="950" rx="15" fill="rgba(30, 41, 59, 0.6)" stroke="#475569" stroke-width="2"/>
  
  <!-- Section: State Input -->
  <g>
    <rect x="110" y="130" width="580" height="100" rx="10" fill="rgba(96, 165, 250, 0.12)" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <text x="400" y="160" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="600" fill="#60a5fa" text-anchor="middle">
      State Input (s)
    </text>
    <text x="130" y="190" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8">
      • LIDAR: 720 points (360° distance scan)
    </text>
    <text x="130" y="210" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8">
      • Velocity: [v_linear, v_angular]
    </text>
  </g>
  
  <!-- Arrow down -->
  <line x1="400" y1="230" x2="400" y2="270" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Section: Actor Network -->
  <g>
    <rect x="110" y="280" width="280" height="180" rx="10" fill="rgba(167, 139, 250, 0.12)" stroke="url(#purpleGrad)" stroke-width="2" filter="url(#glow)"/>
    <circle cx="140" cy="310" r="18" fill="url(#purpleGrad)" filter="url(#glow)"/>
    <text x="140" y="318" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="700" fill="#0f172a" text-anchor="middle">μ</text>
    
    <text x="180" y="315" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#a78bfa">
      Actor Network μ<tspan font-size="14" baseline-shift="sub">θ</tspan>(s)
    </text>
    
    <text x="130" y="345" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Input: State (724 dims)
    </text>
    <text x="130" y="365" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Hidden: [512, 256, 128]
    </text>
    <text x="130" y="385" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Activation: ReLU
    </text>
    <text x="130" y="405" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Output: Action (2 dims)
    </text>
    <rect x="130" y="420" width="240" height="30" rx="5" fill="rgba(167, 139, 250, 0.2)" stroke="#a78bfa" stroke-width="1"/>
    <text x="250" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#a78bfa" text-anchor="middle">
      [steering, velocity]
    </text>
  </g>
  
  <!-- Section: Twin Critic Networks -->
  <g>
    <rect x="410" y="280" width="280" height="240" rx="10" fill="rgba(52, 211, 153, 0.12)" stroke="url(#greenGrad)" stroke-width="2" filter="url(#glow)"/>
    <circle cx="440" cy="310" r="18" fill="url(#greenGrad)" filter="url(#glow)"/>
    <text x="440" y="318" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="700" fill="#0f172a" text-anchor="middle">Q</text>
    
    <text x="480" y="315" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#34d399">
      Twin Critics Q<tspan font-size="14" baseline-shift="sub">φ1</tspan>, Q<tspan font-size="14" baseline-shift="sub">φ2</tspan>
    </text>
    
    <text x="430" y="345" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Input: State + Action
    </text>
    <text x="430" y="365" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Hidden: [512, 256]
    </text>
    <text x="430" y="385" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Output: Q-value (scalar)
    </text>
    
    <!-- Q1 box -->
    <rect x="430" y="405" width="105" height="35" rx="5" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="482.5" y="428" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#34d399" text-anchor="middle">
      Critic 1 (Q₁)
    </text>
    
    <!-- Q2 box -->
    <rect x="555" y="405" width="105" height="35" rx="5" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="607.5" y="428" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" font-weight="600" fill="#34d399" text-anchor="middle">
      Critic 2 (Q₂)
    </text>
    
    <!-- Min operation -->
    <text x="550" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#34d399" text-anchor="middle">
      Q-value = min(Q₁, Q₂)
    </text>
    <text x="550" y="490" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Reduces overestimation bias
    </text>
  </g>
  
  <!-- Arrow from Actor/Critic to Replay Buffer -->
  <line x1="400" y1="520" x2="400" y2="560" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Section: Replay Buffer -->
  <g>
    <rect x="110" y="570" width="580" height="140" rx="10" fill="rgba(251, 191, 36, 0.12)" stroke="url(#orangeGrad)" stroke-width="2" filter="url(#glow)"/>
    <circle cx="140" cy="600" r="18" fill="url(#orangeGrad)" filter="url(#glow)"/>
    <text x="140" y="608" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="700" fill="#0f172a" text-anchor="middle">D</text>
    
    <text x="180" y="605" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#fb923c">
      Replay Buffer (Experience Memory)
    </text>
    
    <text x="130" y="635" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8">
      Stores transitions: (state, action, reward, next_state, done)
    </text>
    <text x="130" y="660" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8">
      Buffer Size: 1,000,000 transitions
    </text>
    <text x="130" y="685" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8">
      Batch Sampling: 256 random samples for training
    </text>
  </g>
  
  <!-- Arrow to Training Process -->
  <line x1="400" y1="710" x2="400" y2="750" stroke="#fb923c" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.8"/>
  
  <!-- Section: Training Updates -->
  <g>
    <rect x="110" y="760" width="580" height="260" rx="10" fill="rgba(96, 165, 250, 0.12)" stroke="url(#blueGrad)" stroke-width="2" filter="url(#glow)"/>
    <text x="400" y="790" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Training Process (TD3 Innovations)
    </text>
    
    <!-- Innovation 1 -->
    <rect x="130" y="810" width="540" height="60" rx="8" fill="rgba(167, 139, 250, 0.1)" stroke="#a78bfa" stroke-width="1.5"/>
    <text x="150" y="835" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#a78bfa">
      1. Twin Delayed Updates
    </text>
    <text x="160" y="855" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Update Actor every 2 Critic updates (policy_delay=2)
    </text>
    
    <!-- Innovation 2 -->
    <rect x="130" y="885" width="540" height="60" rx="8" fill="rgba(52, 211, 153, 0.1)" stroke="#34d399" stroke-width="1.5"/>
    <text x="150" y="910" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#34d399">
      2. Target Policy Smoothing
    </text>
    <text x="160" y="930" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Add noise to target actions: ã = μ'(s') + ε, ε ~ clip(N(0, σ), -c, c)
    </text>
    
    <!-- Innovation 3 -->
    <rect x="130" y="960" width="540" height="50" rx="8" fill="rgba(251, 191, 36, 0.1)" stroke="#fb923c" stroke-width="1.5"/>
    <text x="150" y="985" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" font-weight="600" fill="#fb923c">
      3. Soft Target Updates
    </text>
    <text x="160" y="1002" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      θ' ← τθ + (1-τ)θ', φ' ← τφ + (1-τ)φ' (τ=0.005)
    </text>
  </g>
</svg>
### State Space

| Composant | Description | Dimension |
|-----------|-------------|-----------|
| **LIDAR** | Distances obstacles 360° | 720 points |
| **Velocity** | Vitesse linéaire/angulaire | 2 |
| **Goal** | Distance/angle vers objectif | 2 |
| **Total** | État complet | 724 |

### Action Space

| Action | Range | Description |
|--------|-------|-------------|
| **Steering** | [-1, 1] | Angle de rotation |
| **Velocity** | [0, 1] | Vitesse linéaire |

### Reward Function

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 600" style="background: transparent;">
  <defs>
    <linearGradient id="greenGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="redGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f87171;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#ef4444;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="yellowGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#fbbf24;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#f59e0b;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="blueGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
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
  <text x="500" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="30" font-weight="700" fill="url(#blueGrad)" text-anchor="middle" filter="url(#glow)">
    TD3 Reward Function Design
  </text>
  <text x="500" y="65" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#94a3b8" text-anchor="middle">
    Reinforcement Learning for Autonomous Navigation
  </text>
  
  <!-- Central Formula Box -->
  <g>
    <rect x="150" y="100" width="700" height="80" rx="12" fill="rgba(96, 165, 250, 0.15)" stroke="url(#blueGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="500" y="130" font-family="'Courier New', monospace" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Reward = distance_progress × w₁ - collision_penalty × w₂
    </text>
    <text x="500" y="155" font-family="'Courier New', monospace" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      - path_deviation × w₃ + goal_bonus × w₄
    </text>
  </g>
  
  <!-- Component 1: Distance Progress (Positive) -->
  <g>
    <rect x="70" y="220" width="200" height="320" rx="10" fill="rgba(52, 211, 153, 0.15)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="170" y="250" font-size="28" text-anchor="middle">✅</text>
    <text x="170" y="280" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#34d399" text-anchor="middle">
      Distance Progress
    </text>
    
    <rect x="90" y="300" width="160" height="50" rx="8" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="170" y="323" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      +0.1 to +1.0
    </text>
    <text x="170" y="342" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      per step
    </text>
    
    <text x="90" y="375" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Formula:
    </text>
    <text x="90" y="395" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      Δd = d_prev - d_current
    </text>
    <text x="90" y="413" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      reward += Δd × w₁
    </text>
    
    <text x="90" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₁ = 1.0
    </text>
    
    <text x="90" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#34d399">
      Encourages:
    </text>
    <text x="95" y="488" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Forward movement
    </text>
    <text x="95" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Goal-oriented behavior
    </text>
    <text x="95" y="522" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Efficient navigation
    </text>
  </g>
  
  <!-- Component 2: Collision Penalty (Negative) -->
  <g>
    <rect x="290" y="220" width="200" height="320" rx="10" fill="rgba(248, 113, 113, 0.15)" stroke="url(#redGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="390" y="250" font-size="28" text-anchor="middle">❌</text>
    <text x="390" y="280" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#f87171" text-anchor="middle">
      Collision Penalty
    </text>
    
    <rect x="310" y="300" width="160" height="50" rx="8" fill="rgba(248, 113, 113, 0.2)" stroke="#f87171" stroke-width="1.5"/>
    <text x="390" y="323" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#f87171" text-anchor="middle">
      -100
    </text>
    <text x="390" y="342" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      episode ends
    </text>
    
    <text x="310" y="375" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Trigger:
    </text>
    <text x="310" y="395" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      if LIDAR_min &lt; 0.3m:
    </text>
    <text x="310" y="413" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
        reward = -100
    </text>
    
    <text x="310" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₂ = 1.0
    </text>
    
    <text x="310" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#f87171">
      Discourages:
    </text>
    <text x="315" y="488" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Obstacle collisions
    </text>
    <text x="315" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Reckless behavior
    </text>
    <text x="315" y="522" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Dangerous actions
    </text>
  </g>
  
  <!-- Component 3: Path Deviation (Negative) -->
  <g>
    <rect x="510" y="220" width="200" height="320" rx="10" fill="rgba(251, 191, 36, 0.15)" stroke="url(#yellowGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="610" y="250" font-size="28" text-anchor="middle">⚠️</text>
    <text x="610" y="280" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Path Deviation
    </text>
    
    <rect x="530" y="300" width="160" height="50" rx="8" fill="rgba(251, 191, 36, 0.2)" stroke="#fbbf24" stroke-width="1.5"/>
    <text x="610" y="323" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#fbbf24" text-anchor="middle">
      -0.01 to -0.5
    </text>
    <text x="610" y="342" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      per step
    </text>
    
    <text x="530" y="375" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Formula:
    </text>
    <text x="530" y="395" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      angle_error = |θ_goal|
    </text>
    <text x="530" y="413" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      penalty = angle × w₃
    </text>
    
    <text x="530" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₃ = 0.5
    </text>
    
    <text x="530" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#fbbf24">
      Penalizes:
    </text>
    <text x="535" y="488" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Wrong direction
    </text>
    <text x="535" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Circular movement
    </text>
    <text x="535" y="522" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Inefficient paths
    </text>
  </g>
  
  <!-- Component 4: Goal Bonus (Positive) -->
  <g>
    <rect x="730" y="220" width="200" height="320" rx="10" fill="rgba(52, 211, 153, 0.15)" stroke="url(#greenGrad)" stroke-width="2.5" filter="url(#glow)"/>
    <text x="830" y="250" font-size="28" text-anchor="middle">🎯</text>
    <text x="830" y="280" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="17" font-weight="600" fill="#34d399" text-anchor="middle">
      Goal Reached
    </text>
    
    <rect x="750" y="300" width="160" height="50" rx="8" fill="rgba(52, 211, 153, 0.2)" stroke="#34d399" stroke-width="1.5"/>
    <text x="830" y="323" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      +100
    </text>
    <text x="830" y="342" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      episode success
    </text>
    
    <text x="750" y="375" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Trigger:
    </text>
    <text x="750" y="395" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      if distance &lt; 0.5m:
    </text>
    <text x="750" y="413" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
        reward = +100
    </text>
    
    <text x="750" y="440" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₄ = 1.0
    </text>
    
    <text x="750" y="470" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#34d399">
      Rewards:
    </text>
    <text x="755" y="488" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Task completion
    </text>
    <text x="755" y="505" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Successful navigation
    </text>
    <text x="755" y="522" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Episode success
    </text>
  </g>
  
  <!-- Summary Box -->
  <g>
    <rect x="150" y="560" width="700" height="30" rx="8" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="1.5"/>
    <text x="500" y="582" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Typical Episode Reward Range: -100 (collision) to +100 (goal reached) | Average: +5 to +20 per successful step
    </text>
  </g>
</svg>

**Composantes:**
- ✅ **Progression:** Récompense pour avancement vers objectif
- ❌ **Collisions:** Pénalité élevée (-100)
- 📏 **Trajectoire:** Pénalité pour déviation
- 🎯 **Objectif atteint:** Bonus important (+100)

---

## 🛠️ Implementation Details

### Project Structure

```
RoboRangers/
├── src/
│   └── td3/
│       ├── models/              # URDF robot descriptions
│       │   └── velodyne_description/
│       ├── launch/              # ROS2 launch files
│       │   └── launch_sim.launch.py
│       ├── scripts/             # Python implementations
│       │   ├── train_velodyne_node.py
│       │   ├── test_velodyne_node.py
│       │   ├── replay_buffer.py
│       │   └── td3_algorithm.py
│       ├── pytorch_models/      # Trained models
│       │   ├── td3_velodyne_actor.pth
│       │   └── td3_velodyne_critic.pth
│       └── worlds/              # Gazebo simulation worlds
└── package.xml
```

### Training Configuration

**Hyperparamètres TD3:**
```python
config = {
    'actor_lr': 3e-4,
    'critic_lr': 3e-4,
    'gamma': 0.99,           # Discount factor
    'tau': 0.005,            # Target network update rate
    'policy_noise': 0.2,
    'noise_clip': 0.5,
    'policy_delay': 2,       # Actor update frequency
    'buffer_size': 1e6,
    'batch_size': 256
}
```

**Training Process:**
- Episodes: 1000+
- Max steps per episode: 500
- Training time: ~48h on RTX 4060

---

## 📊 Functionalities Achieved

### ✅ Core Features

| Fonctionnalité | Status | Description |
|----------------|--------|-------------|
| **Navigation Autonome** | ✅ | Suivi de trajectoire prédéfinie |
| **Détection Obstacles** | ✅ | LIDAR + Caméras en temps réel |
| **Évitement Collisions** | ✅ | Réaction dynamique aux obstacles |
| **Reconnaissance Panneaux** | 🟡 | Détection basique implémentée |
| **DRL Integration** | 🟡 | TD3 partiellement intégré |

### 🎥 Visual Results

<div align="center">

![RoboRangers in Action](/assets/img/projects/roborangers_demo.png)

**Voiture autonome naviguant avec détection d'obstacles (cônes + piétons)**

</div>

**LIDAR Visualization:**
- Lignes bleues: Rayons LIDAR
- Centre rouge: Position capteur
- Obstacles détectés en temps réel

---

## 🛠️ Challenges & Solutions

### Challenge 1: Intégration DRL

**Problème:** Difficultés environnementales ROS2-Gazebo-TD3  
**Status:** Partiellement résolu  
**Solution appliquée:**
- Séparation des modules (perception / décision / contrôle)
- Tests unitaires indépendants
- Fallback sur contrôle réactif simple

### Challenge 2: LIDAR Processing

**Problème:** Volume de données élevé (720 points @ 10Hz)  
**Solution:**
- Downsampling intelligent (720→180 points)
- Filtrage par distance (ROI: 0.5m - 10m)
- Processing GPU pour point cloud

### Challenge 3: Sim-to-Real Gap

**Problème:** Simulation ≠ Réalité (physique, capteurs)  
**Solution future:**
- Domain randomization (friction, lighting)
- Sensor noise injection
- Sim2Real transfer learning

---

## 💼 Impact & Value

### For Transportation

✅ **Réduction accidents:** -90% erreurs humaines  
✅ **Fluidité trafic:** Optimisation trajectoires  
✅ **Accessibilité:** Mobilité pour tous  
✅ **Environnement:** -30% émissions CO2  

### For Research

✅ **Plateforme open-source** pour DRL robotique  
✅ **Benchmark** ROS2 + Gazebo + TD3  
✅ **Reproductibilité** via simulation  
✅ **Extensibilité** à autres robots mobiles  

---

## 🔮 Future Improvements

**Short-Term:**
- Finaliser intégration TD3 complète
- Améliorer reconnaissance panneaux (CNN)
- Multi-agent scenarios (plusieurs véhicules)

**Long-Term:**
- Deployment sur robot physique (TurtleBot3)
- Real-world testing avec capteurs réels
- V2V Communication (Vehicle-to-Vehicle)
- End-to-end learning (pixels → actions)

---

## 🛠️ Technical Stack

**Robotics:** ROS2 Humble, Gazebo 11  
**Deep Learning:** PyTorch, Stable-Baselines3  
**Sensors:** Velodyne LIDAR, RGB Cameras  
**Languages:** Python 3.10, C++  
**Tools:** Rviz, rqt, TensorBoard  
**Hardware:** NVIDIA RTX 4060, AMD Ryzen 7

---

## 🎓 Skills Developed

- **ROS2 Mastery:** Nodes, Topics, Services, Launch files
- **Reinforcement Learning:** TD3, DDPG, Actor-Critic
- **Sensor Fusion:** LIDAR + Camera integration
- **Robotics Simulation:** Gazebo worlds, URDF modeling
- **Autonomous Systems:** Path planning, obstacle avoidance

---

## 📚 Key References

1. **TD3 Algorithm** (Fujimoto et al., 2018) - ICML
2. **ROS2 Documentation** - Open Robotics
3. **Gazebo Simulator** - OSRF
4. **Deep Reinforcement Learning** (Sutton & Barto, 2018)

---

## 📧 Contact

**Team Lead:** El Mehdi Hicham  
**Email:** mehdihicham736@gmail.com  
**GitHub:** [github.com/MEHDI57-NRG/RoboRangers](https://github.com/MEHDI57-NRG/RoboRangers)  
**LinkedIn:** [linkedin.com/in/elmehdihicham](https://linkedin.com/in/elmehdihicham)

**Team Members:**
- ALAMI AROUSSI Zineb
- GRICHE MOHAMMED Imrane
- MOUTIA Salma

**Supervisor:** Pr. BOUKIR Khaoula  
**Institution:** Faculté des Sciences, Ibn Tofail University

---

## 🏆 Achievements

✅ **Navigation autonome** fonctionnelle dans Gazebo  
✅ **Détection obstacles** temps réel (LIDAR + Caméras)  
✅ **Architecture ROS2** modulaire et extensible  
✅ **TD3 Agent** partiellement intégré  
✅ **Open-source** sur GitHub pour la communauté  

---

*Système de conduite autonome combinant robotique moderne (ROS2), simulation réaliste (Gazebo) et intelligence artificielle (Deep RL) pour une mobilité sûre et efficace.*