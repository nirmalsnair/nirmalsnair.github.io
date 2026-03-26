---
layout: default
permalink: /r3cap
---

**[Home](/) >> R3CAP**

## R3CAP

### <b>R</b>eal-time <b>3</b>D Reconstruction and <b>C</b>ollaborative <b>A</b>uthoring <b>P</b>latform

<p><b>SLAM · Gaussian Splatting · WebXR | Python · Nerfstudio · Babylon.js · MongoDB</b></p>


<iframe width="560" height="315" src="https://www.youtube.com/embed/h0eHyic-tmE?si=I32gXRK2NZIq21T0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

### Overview

<p style="margin-top:-10px;">R3CAP is an open-source system for real-time 3D reconstruction and collaborative editing that enables users to create and interact with digital twins as they are being captured.</p>

<p style="margin-top:-10px;">Unlike traditional pipelines that are offline, fragmented, and expert-driven, R3CAP provides a unified, interactive, and accessible workflow for non-expert users.</p>

<img src="assets/img/r3cap.jpg">
<br><br>

### Key Contributions

<p style="margin-top:-10px;">
<ul style="margin-left:-1em;">
    <li><b>Real-time progressive 3D reconstruction</b> with immediate visual feedback</li>
    <li><b>Collaborative multi-user editing</b> interface for web and immersive (VR) environments</li>
    <li><b>Edge-server architecture</b> for scalable processing and low-latency interaction</li>
    <li><b>User-centric design</b> supporting non-expert users with commodity hardware</li>
    <li><b>Unified end-to-end system</b> integrating capture, reconstruction, and interaction</li>
</ul>
</p>

---

### System Overview

<p style="margin-top:-10px;margin-bottom:10px;">R3CAP consists of three core components:</p>

#### 1. Capture Client (Mobile)

<ul style="margin-top:-10px;margin-left:-1em;margin-bottom:10px;">
    <li>RGB-D data acquisition using consumer devices</li>
    <li>Streams data continuously to the server</li>
    <li>Provides live feedback during scanning</li>
</ul>

#### 2. Edge Server

<ul style="margin-top:-10px;margin-left:-1em;margin-bottom:10px;">
    <li>Performs progressive reconstruction and scene updates</li>
    <li>Maintains a shared 3D representation</li>
    <li>Synchronizes updates across users</li>
</ul>

#### 3. Editing & Exploration Client

<ul style="margin-top:-10px;margin-left:-1em;">
    <li>Web-based interface with optional VR support</li>
    <li>Enables scene editing, annotation, navigation and inspection</li>
</ul>

This enables parallel workflows:<br>
capture → reconstruction → interaction (simultaneously, not sequentially)

---

### Technical Stack

<p style="margin-top:-10px;">
<ul style="margin-left:-1em;">
<li><b>Front-end</b>: Babylon.js, WebXR, Swift (iOS capture client)</li>
<li><b>Back-end</b>: Python, SLAM, Gaussian Splatting, MongoDB</li></ul>
</p>

### Key Applications

<p style="margin-top:-10px;">
<ul style="margin-left:-1em;">
<li><b>Medical Rehabilitation</b>: Virtual environments for therapy, monitoring, and assessment.</li>
<li><b>Disaster Response</b>: Rapid 3D mapping of affected areas for emergency planning.</li>
<li><b>Architectural Design</b>: Collaborative design and visualization of architectural projects.</li>
<li><b>Industrial Training</b>: Realistic, interactive training scenarios for complex procedures.</li></ul>
</p>

### Presentations

<p style="margin-top:-10px;">
<ul style="margin-left:-1em;">
    <li><b>ACM CHI 2025 <a href="https://chi2025.acm.org/for-authors/interactivity">Interactivity</a></b>:
    Showcased in Yokohama, Japan · April 26 – May 1, 2025</li>
    <li><b>ACM SIGGRAPH 2024 <a href="https://s2024.siggraph.org/program/labs/">Labs</a></b>:
    Showcased in Denver, USA · July 28 – August 1, 2024</li>
</ul>
</p>

### Resources

<p style="margin-top:-10px;">
<ul style="margin-left:-1em;">
<li><b>Project Website</b>: <a href="https://www.immersification.org/projects/2025/10/09/r3cap.html">R3CAP</a></li>
<li><b>Code Repository</b>: <a href="https://github.com/singaporetech/r3cap">singaporetech-r3cap</a></li>
<li><b>Research Lab</b>: <a href="https://www.immersification.org/">Centre for Immersification</a></li></ul>
</p>

---

### Research Impact

<p style="margin-top:-10px;">
R3CAP contributes to spatial computing by unifying real-time reconstruction, collaborative editing, and web-based deployment into a single framework. The system lowers the barrier to creating and interacting with digital twins, enabling both researchers and practitioners to adapt it across domains.
</p>

<p style="margin-top:-6px;">
The platform is currently being piloted with <a href="https://www.ttsh.com.sg/Pages/default.aspx">Tan Tock Seng Hospital</a> (TTSH), Singapore, for virtual rehabilitation workflows, highlighting its potential for translation from research to clinical practice.
</p>

---
