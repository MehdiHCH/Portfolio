---
layout: page
title: About
permalink: /about/
weight: 3
---

<style>
/* ============================================
   INTRO SECTION
   ============================================ */
.about-intro {
  background: linear-gradient(135deg, rgba(88, 166, 255, 0.1), rgba(35, 134, 54, 0.1));
  border-left: 4px solid #58a6ff;
  padding: 2rem;
  border-radius: 12px;
  margin-bottom: 3rem;
}

.about-intro h1 {
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
  background: linear-gradient(135deg, #58a6ff, #238636);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.about-intro p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #e6edf3;
  margin-bottom: 1rem;
}

.about-intro strong {
  color: #58a6ff;
  font-weight: 600;
}

/* ============================================
   SECTION DIVIDER
   ============================================ */
.section-divider {
  height: 2px;
  background: linear-gradient(90deg, transparent, rgba(88, 166, 255, 0.5), transparent);
  margin: 3rem 0;
}

/* ============================================
   SKILLS SECTION
   ============================================ */
.skills-section-header {
  text-align: center;
  margin-bottom: 3rem;
}

.skills-section-header h2 {
  font-size: 2.5rem;
  background: linear-gradient(135deg, #58a6ff, #238636);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 0.5rem;
}

.skills-section-header p {
  color: #9ba3b4;
  font-size: 1.1rem;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.skills-category {
  background: linear-gradient(135deg, rgba(30, 30, 47, 0.9), rgba(45, 27, 105, 0.7));
  border: 1px solid rgba(88, 166, 255, 0.2);
  border-radius: 20px;
  padding: 2rem;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
}

.skills-category::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, #58a6ff, #238636, #ffc107, #e91e63);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.skills-category:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 40px rgba(88, 166, 255, 0.25);
  border-color: rgba(88, 166, 255, 0.5);
}

.skills-category:hover::before {
  opacity: 1;
}

.skills-category h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #58a6ff;
  margin-bottom: 1.5rem;
}

.skill-item {
  margin-bottom: 1.5rem;
  position: relative;
}

.skill-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.5rem;
}

.skill-name {
  font-size: 1rem;
  font-weight: 600;
  color: #e6edf3;
  transition: color 0.3s ease;
}

.skill-item:hover .skill-name {
  color: #58a6ff;
}

.skill-percentage {
  font-size: 0.95rem;
  font-weight: 700;
  color: #58a6ff;
  background: rgba(88, 166, 255, 0.15);
  padding: 0.2rem 0.6rem;
  border-radius: 12px;
  min-width: 50px;
  text-align: center;
}

.skill-bar-container {
  width: 100%;
  height: 10px;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 10px;
  overflow: hidden;
  position: relative;
  box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.3);
}

.skill-bar {
  height: 100%;
  border-radius: 10px;
  position: relative;
  transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 0 10px rgba(88, 166, 255, 0.5);
  transform: scaleX(0);
  transform-origin: left;
  animation: fillBar 1.2s ease-out forwards;
}

@keyframes fillBar {
  to { transform: scaleX(1); }
}

.skill-item:nth-child(1) .skill-bar { animation-delay: 0.1s; }
.skill-item:nth-child(2) .skill-bar { animation-delay: 0.2s; }
.skill-item:nth-child(3) .skill-bar { animation-delay: 0.3s; }
.skill-item:nth-child(4) .skill-bar { animation-delay: 0.4s; }
.skill-item:nth-child(5) .skill-bar { animation-delay: 0.5s; }
.skill-item:nth-child(6) .skill-bar { animation-delay: 0.6s; }

/* Couleurs par niveau de compétence */
.skill-bar[data-level="expert"] {
  background: linear-gradient(90deg, #e91e63, #f06292);
  box-shadow: 0 0 10px rgba(233, 30, 99, 0.5);
}

.skill-bar[data-level="advanced"] {
  background: linear-gradient(90deg, #58a6ff, #2196f3);
  box-shadow: 0 0 10px rgba(88, 166, 255, 0.5);
}

.skill-bar[data-level="intermediate"] {
  background: linear-gradient(90deg, #238636, #4caf50);
  box-shadow: 0 0 10px rgba(35, 134, 54, 0.5);
}

.skill-bar[data-level="beginner"] {
  background: linear-gradient(90deg, #ffc107, #ffeb3b);
  box-shadow: 0 0 10px rgba(255, 193, 7, 0.5);
}

/* ============================================
   OBJECTIVE SECTION
   ============================================ */
.objective-section {
  background: linear-gradient(135deg, rgba(35, 134, 54, 0.15), rgba(88, 166, 255, 0.1));
  border: 2px solid rgba(88, 166, 255, 0.3);
  border-radius: 16px;
  padding: 2.5rem;
  margin-top: 3rem;
  text-align: center;
}

.objective-section h2 {
  font-size: 2rem;
  color: #58a6ff;
  margin-bottom: 1rem;
}

.objective-section p {
  font-size: 1.15rem;
  line-height: 1.8;
  color: #e6edf3;
  max-width: 800px;
  margin: 0 auto 1.5rem;
}

.cta-button {
  display: inline-block;
  background: linear-gradient(135deg, #58a6ff, #238636);
  color: white;
  padding: 1rem 2rem;
  border-radius: 10px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(88, 166, 255, 0.3);
  margin-top: 1rem;
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(88, 166, 255, 0.4);
  color: white;
}

/* ============================================
   RESPONSIVE
   ============================================ */
@media (max-width: 768px) {
  .about-intro h1 {
    font-size: 2rem;
  }
  
  .about-intro {
    padding: 1.5rem;
  }
  
  .skills-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .skills-category {
    padding: 1.5rem;
  }
  
  .skills-category h3 {
    font-size: 1.3rem;
  }
  
  .skill-name {
    font-size: 0.9rem;
  }
  
  .objective-section {
    padding: 1.5rem;
  }
  
  .skills-section-header h2 {
    font-size: 2rem;
  }
}
</style>

<div class="about-intro">
  <h1>About Me</h1>
  
  <p>
    Hi there 👋 I'm <strong>{{ site.author.name }}</strong>, an <strong>Artificial Intelligence Engineer</strong> passionate about <strong>Computer Vision</strong>, <strong>Deep Learning</strong>, and the application of AI in <strong>sports performance and analytics</strong>.
  </p>

  <p>
    During my recent projects, I built complete video analysis systems for sports — combining <strong>object detection (YOLOv8/11)</strong>, <strong>multi-player tracking (DeepSORT / ReID)</strong>, <strong>jersey number OCR</strong>, and <strong>top-down projection</strong> for tactical insights.
  </p>

  <p>
    I also explore <strong>OCR modeling (CRNN, Vision Transformers)</strong>, <strong>event detection</strong>, and <strong>synthetic data generation</strong> to improve model robustness in real-world scenarios.
  </p>
</div>

<div class="section-divider"></div>

<div class="skills-section">
  <div class="skills-section-header">
    <h2>💼 Technical Skills</h2>
    <p>My expertise across AI, Computer Vision, and Software Engineering</p>
  </div>
  
  <div class="skills-grid">
    {% include about/skills.html title="Programming & AI" source=site.data.Programming-AI %}
    {% include about/skills.html title="Computer Vision & Robotics" source=site.data.ComputerVision-Robotics %}
    {% include about/skills.html title="Generative AI & NLP" source=site.data.GenerativeAI-NLP %}
    {% include about/skills.html title="Cloud & Infrastructure" source=site.data.Cloud-Infrastructure %}
    {% include about/skills.html title="Networking & Databases" source=site.data.Networking-Databases %}
    {% include about/skills.html title="Leadership & Collaboration" source=site.data.Leadership-Collaboration %}
    {% include about/skills.html title="Languages" source=site.data.Languages %}
  </div>
</div>

<div class="section-divider"></div>

<div class="row">
  <h2 style="text-align: center; color: #58a6ff; font-size: 2rem; margin-bottom: 2rem;">📚 Experience & Education</h2>
  {% include about/timeline.html %}
</div>

<div class="section-divider"></div>

<div class="objective-section">
  <h2>🎯 Career Objective</h2>
  <p>
    My goal is to design and deploy intelligent vision-based systems that combine <strong>AI research</strong>, <strong>video analytics</strong>, and <strong>sports performance optimization</strong>.
  </p>
  <p>
    I am currently seeking a <strong>Computer Vision / AI Engineer opportunity</strong>, where I can contribute to innovative, real-world applications that push the boundaries of what's possible with AI.
  </p>
  <a href="{{ site.baseurl }}/projects/" class="cta-button">
    🚀 View My Projects
  </a>
</div>