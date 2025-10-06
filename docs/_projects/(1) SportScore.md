---
layout: project
slug: automated-futsal-analysis
name: Automated Futsal Video Analysis (PFE)
tools: [Python, OpenCV, YOLOv11, DeepSORT, AI, Computer Vision]
image: /Portfolio/assets/img/projects/SportScore.png
description: >
  AI-based video analysis system for futsal games, developed during my final-year project at SportScore.
  The pipeline detects, classifies, and structures player actions (passes, shots, interceptions, goals) from futsal videos,
  with intelligent filtering of irrelevant frames.
external_url: /demos/#futsal-demo  permalink: /projects/futsal-analysis/
---

{% if page.external_url %}
  <p style="text-align: right;">
    <a href="{{ page.external_url | relative_url }}" class="btn btn-primary" target="_blank">Regarder la Démo 🎥</a>
  </p>
{% endif %}

## 🧠 Aperçu du Projet
Ce projet se concentre sur la **compréhension automatisée du jeu de futsal** en utilisant une pipeline de vision par ordinateur personnalisée.

---

## 🧩 Architecture du Système
Voici un diagramme simplifié du pipeline de traitement :

![System Architecture](/Portfolio/assets/img/projects/futsal_architecture.png)
---

## 🚀 Fonctionnalités Clés
- Suivi et ré-identification multi-joueurs  
- Classification d'actions avec l'apprentissage profond  

---

## 🎥 Démo
Vous pouvez regarder la démo complète en cliquant sur le bouton 👇  

👉 [**Regarder la démo vidéo**]({{ page.external_url | relative_url }}){: .btn .btn-primary target="_blank"}

---

## 🧰 Pile Technologique
---

[⬅ Retour aux Projets](/projects/){: .btn .btn-secondary }