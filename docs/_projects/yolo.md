---
title: Object Detection with YOLOv11
image: /assets/images/projects/yolo-preview.jpg
description: Real-time multi-class object detection using fine-tuned YOLOv11 for improved accuracy.
category: computer-vision
tags:
  - YOLOv11
  - Computer Vision
  - PyTorch
  - Deep Learning
github: https://github.com/votreusername/yolo-project
demo: https://votre-demo.com
date: 2024-01-15
---

## Vue d'ensemble

Ce projet implémente la détection d'objets en temps réel avec YOLOv11, fine-tuné sur un dataset personnalisé pour une meilleure précision dans des scénarios spécifiques.

## Caractéristiques principales

- Détection en temps réel à 60+ FPS
- Entraînement sur dataset personnalisé avec 15 classes d'objets
- Intégration avec flux vidéo et webcams
- Inférence optimisée avec export ONNX

## Implémentation technique

Le modèle a été entraîné avec PyTorch sur un dataset de 10 000+ images annotées...

## Résultats

Atteint 92% mAP@0.5 sur le set de validation, surpassant significativement le modèle baseline YOLOv8...

## Technologies utilisées

- Python 3.10
- PyTorch 2.0
- OpenCV
- Ultralytics YOLOv11