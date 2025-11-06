---
title: RoboRangers - Autonomous Vehicle with Deep Reinforcement Learning
image: /assets/img/projects/robo/roborangers.jpg
description: Autonomous navigation system using ROS2, Gazebo and Deep Reinforcement Learning (TD3) for intelligent and safe driving in dynamic environments.
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
date: 2024-06-15
company: Academic Project
location: Ibn Tofail University, Kenitra
duration: February 2024 - June 2024
github: https://github.com/MEHDI57-NRG/RoboRangers
---

## 🎯 Project Overview

**RoboRangers** is an **autonomous vehicle** project using **Deep Reinforcement Learning (DRL)** and **ROS2** for intelligent navigation in simulated environments. The system integrates LIDAR sensors and cameras for complete perception, and implements the **TD3** (Twin Delayed Deep Deterministic Policy Gradient) algorithm for autonomous decision-making.

**Team:**
- **ALAMI AROUSSI Zineb**
- **GRICHE MOHAMMED Imrane**
- **HICHAM EL Mehdi**
- **MOUTIA Salma**

**Under the supervision of:** Pr. BOUKIR Khaoula

**Mission:** Develop an autonomous vehicle capable of navigating, avoiding obstacles and respecting traffic signs in a dynamic environment.

---

## 🔍 Problem Statement

### Challenges

**Problem:** How to enable a system to learn real-time decision-making based on changes in its environment while ensuring safety and efficiency?

- 🚗 **Traffic accidents:** Human errors = main cause of death
- 🚦 **Traffic jams:** Economic losses and pollution
- 👥 **Accessibility:** Limited mobility for elderly/disabled people
- 🌍 **Environmental impact:** High CO2 emissions
- 🎯 **Complex navigation:** Dynamic and unpredictable environments

### Solution

Autonomous vehicle integrating:
- **ROS2:** Distributed inter-module communication
- **Gazebo:** Realistic 3D simulation for safe testing
- **DRL (TD3):** Autonomous learning through trial-and-error
- **Multi-modal sensors:** LIDAR + Cameras for 360° perception

---

## 🏗️ Technical Architecture


### 🔧 System Components
**Sensors:**
- 📹 **RGB Cameras:** Obstacle detection, signs
- 🔵 **Velodyne LIDAR:** 360° distance measurement
- 📊 **Point Cloud Processing:** Real-time 3D data
- 🎯 **Sensor Fusion:** Robust perception

**Intelligence:**
- 🧠 **TD3 Agent:** Reinforcement learning
- 🎮 **Action Selection:** Steering, acceleration, braking
- 📈 **Reward Function:** Safety + efficiency
- 🔄 **Continuous Learning:** Iterative improvement

<table>
<tr>
<td width="50%" valign="top">

<div class="component-grid">
  <div class="component-card">
    <h4>Sensors Integration </h4>
    <img src="{{ site.baseurl }}/assets/img/projects/robo/LiDAR.png" alt="Gate Shift Modules">
  </div>
</div>


</td>
<td width="50%" valign="top">

<div class="component-grid">
  <div class="component-card">
    <h4>Camera </h4>
    <img src="{{ site.baseurl }}/assets/img/projects/robo/Camera.png" alt="Camera">
  </div>
</div>

</td>
</tr>
</table>


---

### 📐 ROS2 Architecture
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 720" style="background: transparent;">
  <!-- ==================== DEFINITIONS ==================== -->
  <defs>
    <!-- Gradients -->
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
    
    <!-- Filters -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <!-- Arrow Markers -->
    <marker id="arrowBlue" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#60a5fa" />
    </marker>
    
    <marker id="arrowGreen" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#34d399" />
    </marker>
  </defs>
  
  <!-- ==================== TITLE ==================== -->
  <g id="title">
    <text x="500" y="40" 
          font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
          font-size="32" 
          font-weight="700" 
          fill="url(#blueGrad)" 
          text-anchor="middle" 
          filter="url(#glow)">
      ROS2 Architecture - RoboRangers
    </text>
  </g>
  
  <!-- ==================== SENSOR LAYER ==================== -->
  <g id="sensor-layer">
    <!-- Layer Title -->
    <text x="100" y="100" 
          font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
          font-size="18" 
          font-weight="600" 
          fill="#94a3b8">
      Sensor Layer
    </text>
    
    <!-- Camera Node -->
    <g id="camera-node">
      <rect x="50" y="120" width="180" height="100" rx="10" 
            fill="rgba(96, 165, 250, 0.15)" 
            stroke="url(#blueGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="140" y="155" font-size="32" text-anchor="middle">🎥</text>
      <text x="140" y="185" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#60a5fa" 
            text-anchor="middle">
        Camera Node
      </text>
      <text x="140" y="205" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        /camera/image_raw
      </text>
    </g>
    
    <!-- LIDAR Node -->
    <g id="lidar-node">
      <rect x="260" y="120" width="180" height="100" rx="10" 
            fill="rgba(96, 165, 250, 0.15)" 
            stroke="url(#blueGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="350" y="155" font-size="32" text-anchor="middle">📡</text>
      <text x="350" y="185" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#60a5fa" 
            text-anchor="middle">
        LIDAR Node
      </text>
      <text x="350" y="205" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        /scan (720 points)
      </text>
    </g>
    
    <!-- Localization Node -->
    <g id="localization-node">
      <rect x="470" y="120" width="180" height="100" rx="10" 
            fill="rgba(96, 165, 250, 0.15)" 
            stroke="url(#blueGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="560" y="155" font-size="32" text-anchor="middle">📍</text>
      <text x="560" y="185" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#60a5fa" 
            text-anchor="middle">
        Localization
      </text>
      <text x="560" y="205" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        /odom, /amcl_pose
      </text>
    </g>
    
    <!-- IMU Node -->
    <g id="imu-node">
      <rect x="680" y="120" width="180" height="100" rx="10" 
            fill="rgba(96, 165, 250, 0.15)" 
            stroke="url(#blueGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="770" y="155" font-size="32" text-anchor="middle">🧭</text>
      <text x="770" y="185" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#60a5fa" 
            text-anchor="middle">
        IMU Node
      </text>
      <text x="770" y="205" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        /imu/data
      </text>
    </g>
  </g>
  
  <!-- ==================== PERCEPTION LAYER ==================== -->
  <g id="perception-layer">
    <!-- Layer Title -->
    <text x="100" y="270" 
          font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
          font-size="18" 
          font-weight="600" 
          fill="#94a3b8">
      Perception Layer
    </text>
    
    <!-- Obstacle Detection -->
    <g id="obstacle-detection">
      <rect x="50" y="290" width="200" height="90" rx="10" 
            fill="rgba(167, 139, 250, 0.15)" 
            stroke="url(#purpleGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="150" y="320" font-size="28" text-anchor="middle">🚧</text>
      <text x="150" y="345" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#a78bfa" 
            text-anchor="middle">
        Obstacle Detection
      </text>
      <text x="150" y="365" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        LIDAR + Vision
      </text>
    </g>
    
    <!-- Sign Detection -->
    <g id="sign-detection">
      <rect x="280" y="290" width="200" height="90" rx="10" 
            fill="rgba(167, 139, 250, 0.15)" 
            stroke="url(#purpleGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="380" y="320" font-size="28" text-anchor="middle">🚦</text>
      <text x="380" y="345" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#a78bfa" 
            text-anchor="middle">
        Sign Detection
      </text>
      <text x="380" y="365" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        CNN Classification
      </text>
    </g>
    
    <!-- Sensor Fusion -->
    <g id="sensor-fusion">
      <rect x="510" y="290" width="350" height="90" rx="10" 
            fill="rgba(167, 139, 250, 0.15)" 
            stroke="url(#purpleGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="685" y="320" font-size="28" text-anchor="middle">🔀</text>
      <text x="685" y="345" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="16" 
            font-weight="600" 
            fill="#a78bfa" 
            text-anchor="middle">
        Sensor Fusion Node
      </text>
      <text x="685" y="365" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="12" 
            fill="#94a3b8" 
            text-anchor="middle">
        Multi-modal integration (LIDAR + Camera + IMU)
      </text>
    </g>
  </g>
  
  <!-- ==================== DECISION LAYER ==================== -->
  <g id="decision-layer">
    <!-- Layer Title -->
    <text x="100" y="430" 
          font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
          font-size="18" 
          font-weight="600" 
          fill="#94a3b8">
      Decision Layer
    </text>
    
    <!-- TD3 Agent -->
    <g id="td3-agent">
      <rect x="50" y="450" width="400" height="100" rx="10" 
            fill="rgba(52, 211, 153, 0.15)" 
            stroke="url(#greenGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="250" y="485" font-size="32" text-anchor="middle">🧠</text>
      <text x="250" y="515" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="18" 
            font-weight="600" 
            fill="#34d399" 
            text-anchor="middle">
        TD3 Agent (Deep RL)
      </text>
      <text x="250" y="535" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="13" 
            fill="#94a3b8" 
            text-anchor="middle">
        State → Actor-Critic Networks → Actions
      </text>
    </g>
    
    <!-- Path Planner -->
    <g id="path-planner">
      <rect x="480" y="450" width="380" height="100" rx="10" 
            fill="rgba(52, 211, 153, 0.15)" 
            stroke="url(#greenGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="670" y="485" font-size="32" text-anchor="middle">🗺️</text>
      <text x="670" y="515" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="18" 
            font-weight="600" 
            fill="#34d399" 
            text-anchor="middle">
        Path Planning Node
      </text>
      <text x="670" y="535" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="13" 
            fill="#94a3b8" 
            text-anchor="middle">
        Global: A* | Local: DWA (Dynamic Window Approach)
      </text>
    </g>
  </g>
  
  <!-- ==================== CONTROL LAYER ==================== -->
  <g id="control-layer">
    <!-- Layer Title -->
    <text x="100" y="600" 
          font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
          font-size="18" 
          font-weight="600" 
          fill="#94a3b8">
      Control Layer
    </text>
    
    <!-- Control Node -->
    <g id="control-node">
      <rect x="50" y="620" width="810" height="80" rx="10" 
            fill="rgba(251, 191, 36, 0.15)" 
            stroke="url(#yellowGrad)" 
            stroke-width="2.5" 
            filter="url(#glow)"/>
      <text x="455" y="655" font-size="28" text-anchor="middle">🎮</text>
      <text x="455" y="680" 
            font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" 
            font-size="17" 
            font-weight="600" 
            fill="#fbbf24" 
            text-anchor="middle">
        Vehicle Control Node → /cmd_vel (linear, angular velocity)
      </text>
    </g>
  </g>
  
  <!-- ==================== ARROWS ==================== -->
  <g id="arrows">
    <!-- Sensor → Perception -->
    <line x1="140" y1="220" x2="140" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    <line x1="350" y1="220" x2="350" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    <line x1="560" y1="220" x2="560" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    <line x1="770" y1="220" x2="770" y2="290" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    
    <!-- Perception → Decision -->
    <line x1="150" y1="380" x2="200" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    <line x1="380" y1="380" x2="300" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    <line x1="685" y1="380" x2="600" y2="450" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#arrowBlue)" opacity="0.7"/>
    
    <!-- Decision → Control -->
    <line x1="250" y1="550" x2="300" y2="620" stroke="#34d399" stroke-width="2.5" marker-end="url(#arrowGreen)" opacity="0.7"/>
    <line x1="670" y1="550" x2="620" y2="620" stroke="#34d399" stroke-width="2.5" marker-end="url(#arrowGreen)" opacity="0.7"/>
  </g>
</svg>

**Key Topics:**
- `/camera/image_raw` → RGB images
- `/scan` → LIDAR data (720 points)
- `/odom` → Odometry
- `/cmd_vel` → Velocity commands
- `/obstacle_detected` → Obstacle alerts
- `/traffic_sign` → Detected signs

---

## 🎓 TD3 Algorithm Explained

### Twin Delayed DDPG (TD3)

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1100 680" style="background: transparent;">
  <defs>
    <linearGradient id="td3Blue" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#60a5fa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="td3Purple" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#a78bfa;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#8b5cf6;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="td3Green" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="td3Yellow" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#fbbf24;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#f59e0b;stop-opacity:1" />
    </linearGradient>
    
    <filter id="td3Shadow">
      <feDropShadow dx="0" dy="2" stdDeviation="4" flood-opacity="0.3"/>
    </filter>
    
    <marker id="td3Arrow" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#a78bfa" />
    </marker>
  </defs>
  
  <!-- Title -->
  <text x="550" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="32" font-weight="700" fill="url(#td3Blue)" text-anchor="middle">
    TD3 Algorithm Architecture
  </text>
  <text x="550" y="65" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="15" fill="#94a3b8" text-anchor="middle">
    Twin Delayed Deep Deterministic Policy Gradient for Continuous Control
  </text>
  
  <!-- Environment -->
  <g>
    <rect x="50" y="120" width="200" height="100" rx="10" fill="rgba(96, 165, 250, 0.2)" stroke="url(#td3Blue)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="150" y="160" font-size="36" text-anchor="middle">🌍</text>
    <text x="150" y="195" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Environment
    </text>
    <text x="150" y="213" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Gazebo Simulation
    </text>
  </g>
  
  <!-- State -->
  <g>
    <rect x="300" y="120" width="150" height="100" rx="10" fill="rgba(251, 191, 36, 0.2)" stroke="url(#td3Yellow)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="375" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#fbbf24" text-anchor="middle">
      State (s)
    </text>
    <text x="375" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      • LIDAR (180 pts)
    </text>
    <text x="375" y="192" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      • Position (x,y,θ)
    </text>
    <text x="375" y="209" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      • Goal distance
    </text>
  </g>
  
  <!-- Actor Network -->
  <g>
    <rect x="500" y="100" width="240" height="140" rx="10" fill="rgba(167, 139, 250, 0.2)" stroke="url(#td3Purple)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="620" y="135" font-size="28" text-anchor="middle">🎭</text>
    <text x="620" y="165" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Actor Network π(s)
    </text>
    <text x="620" y="187" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      FC1(256) → ReLU
    </text>
    <text x="620" y="204" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      FC2(256) → ReLU
    </text>
    <text x="620" y="221" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      FC3(2) → Tanh
    </text>
  </g>
  
  <!-- Action -->
  <g>
    <rect x="790" y="120" width="150" height="100" rx="10" fill="rgba(251, 191, 36, 0.2)" stroke="url(#td3Yellow)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="865" y="155" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#fbbf24" text-anchor="middle">
      Action (a)
    </text>
    <text x="865" y="175" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      • Linear vel
    </text>
    <text x="865" y="192" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      • Angular vel
    </text>
    <text x="865" y="209" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8" text-anchor="middle">
      Range: [-1, 1]
    </text>
  </g>
  
  <!-- Twin Critic Networks -->
  <g>
    <rect x="380" y="290" width="340" height="160" rx="10" fill="rgba(52, 211, 153, 0.2)" stroke="url(#td3Green)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="550" y="325" font-size="28" text-anchor="middle">🎯🎯</text>
    <text x="550" y="355" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="18" font-weight="600" fill="#34d399" text-anchor="middle">
      Twin Critic Networks Q₁(s,a) & Q₂(s,a)
    </text>
    <text x="550" y="380" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Critic 1: FC(256)→ReLU→FC(256)→ReLU→FC(1)
    </text>
    <text x="550" y="400" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8" text-anchor="middle">
      Critic 2: FC(256)→ReLU→FC(256)→ReLU→FC(1)
    </text>
    <text x="550" y="425" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#34d399" text-anchor="middle">
      Output: Q-values (expected cumulative reward)
    </text>
  </g>
  
  <!-- Replay Buffer -->
  <g>
    <rect x="50" y="290" width="280" height="90" rx="10" fill="rgba(96, 165, 250, 0.2)" stroke="url(#td3Blue)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="190" y="325" font-size="28" text-anchor="middle">💾</text>
    <text x="190" y="355" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa" text-anchor="middle">
      Replay Buffer
    </text>
    <text x="190" y="373" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Store: (s, a, r, s', done) | Size: 1M
    </text>
  </g>
  
  <!-- Target Networks -->
  <g>
    <rect x="770" y="290" width="280" height="160" rx="10" fill="rgba(167, 139, 250, 0.2)" stroke="url(#td3Purple)" stroke-width="2.5" filter="url(#td3Shadow)"/>
    <text x="910" y="325" font-size="28" text-anchor="middle">🎯</text>
    <text x="910" y="355" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Target Networks
    </text>
    <text x="910" y="378" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      π'(s) - Target Actor
    </text>
    <text x="910" y="398" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Q₁'(s,a) - Target Critic 1
    </text>
    <text x="910" y="418" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" fill="#94a3b8" text-anchor="middle">
      Q₂'(s,a) - Target Critic 2
    </text>
    <text x="910" y="438" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" font-style="italic" fill="#64748b" text-anchor="middle">
      Soft update: τ = 0.005
    </text>
  </g>
  
  <!-- TD3 Key Innovations Box -->
  <g>
    <rect x="50" y="490" width="1000" height="170" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#td3Shadow)"/>
    <text x="550" y="520" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="22" font-weight="700" fill="#a78bfa" text-anchor="middle">
      🔑 TD3 Key Innovations vs DDPG
    </text>
    
    <g>
      <text x="70" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#34d399">
        1️⃣ Twin Critics:
      </text>
      <text x="85" y="577" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        Use min(Q₁, Q₂) to reduce overestimation bias
      </text>
      <text x="85" y="595" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        More stable and accurate Q-value estimates
      </text>
    </g>
    
    <g>
      <text x="380" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#60a5fa">
        2️⃣ Delayed Policy Updates:
      </text>
      <text x="395" y="577" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        Update actor every 2 critic updates
      </text>
      <text x="395" y="595" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        Reduces policy errors from bad Q-values
      </text>
    </g>
    
    <g>
      <text x="720" y="555" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="16" font-weight="600" fill="#fbbf24">
        3️⃣ Target Policy Smoothing:
      </text>
      <text x="735" y="577" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        Add noise to target actions
      </text>
      <text x="735" y="595" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#cbd5e1">
        Smooths Q-function for robustness
      </text>
    </g>
    
    <rect x="70" y="615" width="960" height="30" rx="5" fill="rgba(167, 139, 250, 0.2)" stroke="#a78bfa" stroke-width="1.5"/>
    <text x="550" y="635" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" font-weight="600" fill="#a78bfa" text-anchor="middle">
      Result: More stable training, better sample efficiency, superior performance in continuous control tasks
    </text>
  </g>
  
  <!-- Arrows -->
  <line x1="250" y1="170" x2="295" y2="170" stroke="#60a5fa" stroke-width="2.5" marker-end="url(#td3Arrow)" opacity="0.7"/>
  <line x1="450" y1="170" x2="495" y2="170" stroke="#a78bfa" stroke-width="2.5" marker-end="url(#td3Arrow)" opacity="0.7"/>
  <line x1="740" y1="170" x2="785" y2="170" stroke="#fbbf24" stroke-width="2.5" marker-end="url(#td3Arrow)" opacity="0.7"/>
  <line x1="865" y1="220" x2="865" y2="260" stroke="#34d399" stroke-width="2.5" opacity="0.7"/>
  <line x1="865" y1="260" x2="150" y2="260" stroke="#34d399" stroke-width="2.5" opacity="0.7"/>
  <line x1="150" y1="260" x2="150" y2="220" stroke="#34d399" stroke-width="2.5" marker-end="url(#td3Arrow)" opacity="0.7"/>
</svg>

**TD3 Components:**
- 🎭 **Actor:** Learns optimal policy π(s)
- 🎯 **Twin Critics:** Q₁(s,a) & Q₂(s,a) for stable learning
- 💾 **Replay Buffer:** Experience replay for sample efficiency
- 🔄 **Target Networks:** Slowly updated for stability

**Key Features:**
- ✅ Continuous action space (steering, velocity)
- ✅ Reduced overestimation bias
- ✅ Delayed policy updates
- ✅ Target policy smoothing

---

## 🎯 Reward Function Design

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 600" style="background: transparent;">
  <defs>
    <linearGradient id="rewardGreen" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#34d399;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10b981;stop-opacity:1" />
    </linearGradient>
    
    <linearGradient id="rewardRed" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#f87171;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#ef4444;stop-opacity:1" />
    </linearGradient>
    
    <filter id="rewardShadow">
      <feDropShadow dx="0" dy="2" stdDeviation="4" flood-opacity="0.3"/>
    </filter>
  </defs>
  
  <!-- Title -->
  <text x="500" y="40" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="30" font-weight="700" fill="url(#rewardGreen)" text-anchor="middle">
    Reward Function Components
  </text>
  <text x="500" y="65" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="14" fill="#94a3b8" text-anchor="middle">
    Multi-objective reward shaping for safe and efficient navigation
  </text>
  
  <!-- Component 1: Progress Reward -->
  <g>
    <rect x="50" y="100" width="420" height="170" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#rewardShadow)"/>
    <text x="260" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      1️⃣ Progress Reward (R_progress)
    </text>
    
    <text x="70" y="160" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Formula:
    </text>
    <text x="70" y="180" font-family="'Courier New', monospace" font-size="12" fill="#64748b">
      R_progress = -Δd × 10
    </text>
    <text x="70" y="200" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      where Δd = d(t) - d(t-1)
    </text>
    
    <text x="70" y="225" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₁ = 10.0
    </text>
    
    <text x="70" y="255" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#34d399">
      Rewards:
    </text>
    <text x="75" y="272" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Moving closer to goal
    </text>
  </g>
  
  <!-- Component 2: Collision Penalty -->
  <g>
    <rect x="530" y="100" width="420" height="170" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#rewardShadow)"/>
    <text x="740" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#f87171" text-anchor="middle">
      2️⃣ Collision Penalty (R_collision)
    </text>
    
    <text x="550" y="160" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Trigger:
    </text>
    <text x="550" y="180" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      if min(LIDAR) &lt; 0.3m:
    </text>
    <text x="550" y="198" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
          reward = -100
    </text>
    
    <text x="550" y="225" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₂ = 1.0
    </text>
    
    <text x="550" y="255" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#f87171">
      Penalties:
    </text>
    <text x="555" y="272" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Collision with obstacles
    </text>
  </g>
  
  <!-- Component 3: Trajectory Penalty -->
  <g>
    <rect x="50" y="300" width="420" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#rewardShadow)"/>
    <text x="260" y="330" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#fbbf24" text-anchor="middle">
      3️⃣ Trajectory Penalty (R_trajectory)
    </text>
    
    <text x="70" y="360" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Formula:
    </text>
    <text x="70" y="380" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      R_trajectory = -|heading_error| × 0.5
    </text>
    <text x="70" y="398" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      heading_error = θ_goal - θ_robot
    </text>
    
    <text x="70" y="425" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Weight: w₃ = 0.5
    </text>
    
    <text x="70" y="455" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="12" font-weight="600" fill="#fbbf24">
      Penalties:
    </text>
    <text x="75" y="472" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="11" fill="#94a3b8">
      • Deviating from optimal path
    </text>
  </g>
  
  <!-- Component 4: Goal Reward -->
  <g>
    <rect x="530" y="300" width="420" height="180" rx="10" fill="rgba(30, 41, 59, 0.8)" stroke="#475569" stroke-width="2" filter="url(#rewardShadow)"/>
    <text x="740" y="330" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="20" font-weight="700" fill="#34d399" text-anchor="middle">
      4️⃣ Goal Reward (R_goal)
    </text>
    
    <text x="550" y="360" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif" font-size="13" fill="#94a3b8">
      Formula:
    </text>
    <text x="550" y="380" font-family="'Courier New', monospace" font-size="11" fill="#64748b">
      R_goal = +200
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

**Components:**
- ✅ **Progress:** Reward for advancement towards goal
- ❌ **Collisions:** High penalty (-100)
- 📏 **Trajectory:** Penalty for deviation
- 🎯 **Goal reached:** Large bonus (+100)

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

**TD3 Hyperparameters:**
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

| Functionality | Status | Description |
|----------------|--------|-------------|
| **Autonomous Navigation** | ✅ | Predefined trajectory following |
| **Obstacle Detection** | ✅ | LIDAR + Cameras in real-time |
| **Collision Avoidance** | ✅ | Dynamic reaction to obstacles |
| **Sign Recognition** | 🟡 | Basic detection implemented |
| **DRL Integration** | 🟡 | TD3 partially integrated |

### 🎥 Visual Results

<div class="component-grid">
  <div class="component-card">
    <img src="{{ site.baseurl }}/assets/img/projects/robo/last.png" >
</div>
</div>

**LIDAR Visualization:**
- Blue lines: LIDAR rays
- Red center: Sensor position
- Real-time obstacle detection

---

## 🛠️ Challenges & Solutions

### Challenge 1: DRL Integration

**Problem:** Environmental difficulties ROS2-Gazebo-TD3  
**Status:** Partially resolved  
**Applied solution:**
- Module separation (perception / decision / control)
- Independent unit tests
- Fallback to simple reactive control

### Challenge 2: LIDAR Processing

**Problem:** High data volume (720 points @ 10Hz)  
**Solution:**
- Intelligent downsampling (720→180 points)
- Distance filtering (ROI: 0.5m - 10m)
- GPU processing for point cloud

### Challenge 3: Sim-to-Real Gap

**Problem:** Simulation ≠ Reality (physics, sensors)  
**Future solution:**
- Domain randomization (friction, lighting)
- Sensor noise injection
- Sim2Real transfer learning

---

## 💼 Impact & Value

### For Transportation

✅ **Accident reduction:** -90% human errors  
✅ **Traffic fluidity:** Trajectory optimization  
✅ **Accessibility:** Mobility for all  
✅ **Environment:** -30% CO2 emissions  

### For Research

✅ **Open-source platform** for DRL robotics  
✅ **Benchmark** ROS2 + Gazebo + TD3  
✅ **Reproducibility** via simulation  
✅ **Extensibility** to other mobile robots  

---

## 🔮 Future Improvements

**Short-Term:**
- Complete TD3 integration
- Improve sign recognition (CNN)
- Multi-agent scenarios (multiple vehicles)

**Long-Term:**
- Deployment on physical robot (TurtleBot3)
- Real-world testing with real sensors
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
**Institution:** Faculty of Sciences, Ibn Tofail University

---

## 🏆 Achievements

✅ **Autonomous navigation** functional in Gazebo  
✅ **Obstacle detection** real-time (LIDAR + Cameras)  
✅ **ROS2 architecture** modular and extensible  
✅ **TD3 Agent** partially integrated  
✅ **Open-source** on GitHub for the community  

---

*Autonomous driving system combining modern robotics (ROS2), realistic simulation (Gazebo) and artificial intelligence (Deep RL) for safe and efficient mobility.*