---
layout: default
---
## <span id="about-me">About Me</span>

Hi, I'm a computer vision researcher specializing in **3D reconstruction** and **spatial computing**, with a focus on developing practical, end-to-end systems.

My work sits at the intersection of multi-view geometry, real-time reconstruction, and interactive 3D systems, including recent directions in hybrid scene representations such as Gaussian Splatting.

During my PhD, I focused on **multi-view stereo**, exploring numerical and metaheuristic optimization techniques to address ill-posed problems in multi-view geometry. This experience continues to inform how I design reconstruction pipelines and evaluate newer representations.

More recently, I worked on <a href="/r3cap">R3CAP</a>, an open-source platform for real-time scene capture, editing, and collaboration across web and VR. The system integrates SLAM, digital twins, and multi-user 3D interaction, and was showcased at <a href="https://s2024.siggraph.org/program/labs/">SIGGRAPH 2024 Labs</a> and <a href="https://chi2025.acm.org/for-authors/interactivity">CHI 2025 Interactivity.</a>

I also work with learning-based approaches for scene understanding and 3D perception, particularly in settings where learned models and geometric methods need to work together reliably (e.g., robot perception in real-world environments).

I am particularly interested in:
<ul style="margin-top:-15px; margin-left:-1em;">
  <li>3D reconstruction, SLAM, and real-time systems</li>
  <li>Computer vision and robot perception for 3D understanding</li>
  <li>Hybrid representations bridging geometric and learned methods</li>
  <li>Spatial computing and interactive 3D tools</li>
</ul>

---

## <span id="publications">Publications</span>

<h3 style="margin-bottom:2px;font-weight:100;"><a href="https://dl.acm.org/doi/abs/10.1145/3706599.3721190">Collaborative Scene Authoring with Near Real-Time 3D Reconstruction</a> <a href="https://www.immersification.org/projects/2025/10/09/r3cap.html">[project]</a></h3>
<p style="margin:0;">Leon Foo, <b>Nirmal S. Nair</b>, Liuziyi Liu, Jeannie Su Ann Lee, Songjia Shen, Indriyati Atmosukarto, Alvin Chan, Jing Shi, Yong Joo Loh, Yih Yng Ng, Michael Chia, Chek Tien Tan<br>
<i>ACM CHI 2025 Interactivity</i></p>
<ul style="margin-left: -1.4em;">
</ul>

<h3 style="margin-bottom:2px;font-weight:100;"><a href="https://dl.acm.org/doi/abs/10.1145/3641236.3664424">demoConstruct: Democratizing Scene Construction for Digital Twins through Progressive Reconstruction</a> <a href="https://github.com/singaporetech/r3cap">[code]</a></h3>
<p style="margin:0;">Leon Foo, Chek Tien Tan, Liuziyi Liu, <b>Nirmal S. Nair</b>, Songjia Shen, Jeannie Lee<br>
<i>ACM SIGGRAPH 2024 Labs</i></p>
<ul style="margin-left: -1.4em;">
</ul>

<h3 style="margin-bottom:2px;font-weight:100;"><a href="https://doi.org/10.1109/LSP.2022.3201778">Multi-View Stereo Using Graph Cuts-Based Depth Refinement</a> <a href="https://github.com/nirmalsnair/mvs-graphcuts">[code]</a></h3>
<p style="margin:0;"><b>Nirmal S. Nair</b>, Madhu S. Nair<br>
<i>IEEE Signal Processing Letters, 2022</i></p>
<ul style="margin-left: -1.4em;">
</ul>

<h3 style="margin-bottom:2px;font-weight:100;"><a href="https://doi.org/10.1117/12.2601119">Multi-view Stereo using Cross-view Depth Map Completion and Row-column Depth Refinement</a></h3>
<p style="margin:0;"><b>Nirmal S. Nair</b>, Madhu S. Nair<br>
<i>SPIE International Conference on Digital Image Processing, ICDIP 2021</i></p>
<ul style="margin-left: -1.4em;">
</ul>

<h3 style="margin-bottom:2px;font-weight:100;"><a href="https://doi.org/10.1117/12.2587241">Scalable Multi-view Stereo using CMA-ES and Distance Transform-based Depth Map Refinement</a> <a href="https://github.com/nirmalsnair/mvs-cmaes">[code]</a></h3>
<p style="margin:0;"><b>Nirmal S. Nair</b>, Madhu S. Nair<br>
<i>SPIE International Conference on Machine Vision, ICMV 2020</i></p>
<ul style="margin-left: -1.4em;">
</ul>

<h3 style="margin-bottom:2px;font-weight:100;"><a href="https://link.springer.com/article/10.1007/s00138-020-01077-2">On Evolutionary Computation Techniques for Multi-view Triangulation</a></h3>
<p style="margin:0;"><b>Nirmal S. Nair</b>, Madhu S. Nair<br>
<i>Machine Vision and Applications, Springer, 2020</i></p>
<ul style="margin-left: -1.4em;">
</ul>

---

## <span id="projects">Projects</span>

<!-- <div class="card">
  <h3>R3CAP</h3>
  <i>(<b>R</b>eal-time <b>3</b>D Reconstruction and <b>C</b>ollaborative <b>A</b>uthoring <b>P</b>latform)</i>
  <p><b>SLAM · Gaussian Splatting · WebXR</b></p>
  <ul style="margin-top:5px;">
    An open-source platform for real-time 3D capture and collaborative scene authoring. Combines SLAM-based geometry with explicit radiance field representations (e.g., 3D Gaussian Splatting) for interactive visualization and editing.
  </ul>
  <a href="/r3cap"><span class="card-link-spanner"></span></a>
</div> -->

<!-- <div class="card">
  <h3>Multi-View Stereo Reconstruction</h3>
  <p><b>3D Reconstruction, Computer Vision, Graph Cuts, Metaheuristic Optimization | Python, COLMAP, MATLAB</b></p>
  <ul style="margin-top:5px;">
    <li>A depth map-based multi-view stereo method using metaheuristics and graph cuts for depth estimation and refinement.</li>
    <li>Published in IEEE Signal Processing Letters 2022.</li>
  </ul>
  <a href="/multi-view-stereo"><span class="card-link-spanner"></span></a>
</div> -->

<!--
  Custom project card with left-side media preview.
  Safe to undo: remove this block to revert to text-only project cards.
-->
<div class="card project-card">
  <img class="project-card-media" src="/assets/img/r3cap_card.webp" alt="R3CAP preview">
  <div class="project-card-body">
    <h3>R3CAP</h3>
    <p><b>SLAM · Gaussian Splatting · WebXR</b></p>
    <ul style="margin-top:5px;">
      An open-source platform for real-time 3D capture and collaborative scene authoring. Combines SLAM-based geometry with explicit radiance field representations (e.g., 3D Gaussian Splatting) for interactive visualization and editing.
    </ul>
  </div>
  <a href="/r3cap"><span class="card-link-spanner"></span></a>
</div>

<div class="card project-card">
  <img class="project-card-media" src="/assets/img/mvsgc_card.webp" alt="R3CAP preview">
  <div class="project-card-body">
    <h3>Multi-View Stereo Reconstruction</h3>
    <p><b>Depth Estimation · Graph Cuts · Metaheuristics</b></p>
    <ul style="margin-top:5px;">
      A multi-view stereo framework that combines metaheuristic optimization and graph cuts to produce accurate, consistent depth maps, with improved robustness to occlusions and low-texture regions.
    </ul>
  </div>
  <a href="/r3cap"><span class="card-link-spanner"></span></a>
</div>
<!-- End custom project card with media preview. -->

---

## <span id="research-experience">Research Experience</span>

<h3 style="margin-bottom:0px;">Research Fellow</h3>
<p style="margin:0;"><b>Centre for Immersification, Singapore Institute of Technology</b> (2023 - 2025)<br>
</p>
<ul style="margin-top:5px; margin-left:-1em;">
  <li>Developed real-time 3D capture and digital twin systems, integrating SLAM, depth sensing, and interactive web/VR tools.</li>
  <li>Worked on interactive systems including a 3D vision-based telepresence system (<i>RoboArm</i>), focusing on real-time performance and usability.</li>
</ul>

<h3 style="margin-bottom:0px;">PhD Researcher</h3>
<p style="margin:0;"><b>Department of Computer Science, University of Kerala</b> (2015 - 2022)<br>
</p>
<ul style="margin-top:5px; margin-left:-1em;">
  <li>Conducted research in multi-view stereo, developing depth map-based methods to improve scalability, reconstruction accuracy, and robustness to occlusions and untextured regions.</li>
  <li>Investigated metaheuristic optimization for improving solutions in multi-view stereo and triangulation.</li>
</ul>

---
