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
external_url: /Portfolio/demos/#futsal-demo  ---

{% if page.external_url %}
  <p style="text-align: right;">
    <a href="{{ page.external_url }}" class="btn btn-primary" target="_blank">Regarder la Démo 🎥</a>
  </p>
{% endif %}

## 🧠 Aperçu du Projet
Ce projet se concentre sur la **compréhension automatisée du jeu de futsal** à l'aide d'un pipeline de vision par ordinateur personnalisé.

Nous avons construit un **système d'analyse vidéo de bout en bout** capable de détecter, suivre et classifier les actions clés des joueurs
en utilisant des modèles d'apprentissage profond de pointe.

---

## 🧩 Architecture du Système
Voici un diagramme simplifié du pipeline de traitement :

![System Architecture](/Portfolio/assets/img/projects/futsal_architecture.png)
1. **Détection** : YOLOv11 détecte les joueurs et le ballon dans chaque image.  
2. **Suivi** : DeepSORT attribue des ID cohérents aux joueurs à travers les images.  
3. **Reconnaissance d'Action** : Un modèle CNN-LSTM classifie les actions temporelles comme les passes ou les tirs.  
4. **Structuration d'Événements** : Filtre et résume le jeu en statistiques et faits saillants significatifs.

---

## 🚀 Fonctionnalités Clés
- Suivi et ré-identification multi-joueurs  
- Sélection et filtrage intelligent des images  
- Classification d'actions avec l'apprentissage profond  
- Optimisation des performances en quasi-temps réel  

---

## 🎥 Démo
Vous pouvez regarder la démo complète en cliquant sur le bouton 👇  

👉 [**Regarder la démo vidéo**]({{ page.external_url }}){: .btn .btn-primary target="_blank"}

---

## 🧰 Pile Technologique
| Composant | Technologie |
|------------|-------------|
| Détection d'Objets | YOLOv11 |
| Suivi | DeepSORT |
| Traitement Vidéo | OpenCV |
| Framework | PyTorch |
| Visualisation | Matplotlib, Seaborn |

---

[⬅ Retour aux Projets](/projects/){: .btn .btn-secondary }