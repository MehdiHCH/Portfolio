---
layout: project
title: "Automated Futsal Video Analysis (PFE chez SportScore)"
description: "Pipeline IA pour analyser vidéos futsal : détection, tracking et classification d'actions avec filtrage intelligent."
image: "/assets/img/projects/SportScore.gif"
tools: [Python, OpenCV, YOLOv8, DeepSORT]
demo_anchor: "#sportscore-demo"
category: tracking
tags:
  - Tracking
  - DeepSORT
  - Kalman Filter
  - Sports Analytics
github: https://github.com/votreusername/deepsort-tracking
date: 2024-02-10
---
## À propos du projet

Système de suivi multi-objets en temps réel pour l'analyse sportive, utilisant DeepSORT avec filtre de Kalman.

## Fonctionnalités

- Suivi de joueurs en temps réel
- Analyse de trajectoires
- Génération de heatmaps
- Statistiques de mouvement

## Stack technique

- Python
- DeepSORT
- OpenCV
- NumPy

## Résultats
# Automated Futsal Video Analysis

## Architecture du Projet
Voici le schéma complet de l'architecture (export Draw.io en PDF pour zoom interactif) :

<embed src="{{ site.baseurl }}/assets/pdfs/Figure_1_.pdf" type="application/pdf" width="100%" height="600px">

<!-- Fallback si embed foire : lien télécharge -->
<p><a href="{{ site.baseurl }}/assets/pdfs/Figure_1_.pdf" download>Télécharger le PDF</a> (si ton navigateur bloque l'embed).</p>

**Détails du flux** : Input vidéo → Preprocessing (OpenCV) → Détection YOLOv8 → Tracking DeepSORT → Classification CNN → Filtrage intelligent → Output JSON/Heatmap.

**PFE chez SportScore** : Système IA pour extraire insights automatisés des matchs futsal. Détecte joueurs/balle, tracke trajectoires, classe actions (passes, tirs, goals), filtre frames inutiles, génère heatmaps/stats.

Skills : Computer Vision, Deep Learning, temps réel (25 FPS CPU).

## Explications Techniques
- **Détection** : YOLOv8 fine-tuné (dataset 500+ frames). mAP@0.5 : 92%.
- **Tracking** : DeepSORT pour IDs persistants/occlusions.
- **Classification** : CNN ResNet pour labelliser. Accuracy : 88%.
- **Filtrage** : Optical flow OpenCV.

