---
layout: default
permalink: /multi-view-stereo
---

**[Home](/) >> Multi-View Stereo Reconstruction**

## Multi-View Stereo Reconstruction

### Graph Cuts-Based Depth Refinement for Dense 3D Reconstruction

<p><b>3D Reconstruction · Depth Estimation · Graph Cuts | Python · PyGMO · PyMaxflow</b></p>

<p style="margin-top:-10px;">
This project presents a depth map-based multi-view stereo (MVS) pipeline for reconstructing dense 3D geometry from calibrated images. The key idea is to refine depth maps for all pixels in an image simultaneously using a graph-cuts formulation, enabling global reasoning in low-texture regions where local methods often fail.
</p>

<p style="margin-top:-6px;">
Published in <i>IEEE Signal Processing Letters</i>, 2022.<br>
<a href="https://doi.org/10.1109/LSP.2022.3201778">https://doi.org/10.1109/LSP.2022.3201778</a>
</p>

<b>Code:</b> <a href="https://github.com/nirmalsnair/mvs-graphcuts">https://github.com/nirmalsnair/mvs-graphcuts</a>

---

<div class="sketchfab-embed-wrapper"> <iframe title="Middlebury TempleRing (IEEE SPL-2022)" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share width="640" height="480" src="https://sketchfab.com/models/ed66481b8f3f4b2d8ca991731ac3e4bb/embed?autospin=1&dnt=1"> </iframe> </div>

<div class="sketchfab-embed-wrapper"> <iframe title="Middlebury DinoRing (IEEE SPL-2022)" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share width="640" height="480" src="https://sketchfab.com/models/7fc184241cd14a46bfd9a9d4464827f0/embed?autospin=1&dnt=1"> </iframe> </div>

---

### Overview

<p style="margin-top:-10px;">
Multi-view stereo is fundamentally an ill-posed inverse problem: the system must recover 3D structure from a set of 2D calibrated views. In practice, depth estimation becomes especially difficult in homogeneous or weakly textured regions, where photo-consistency alone does not provide a strong enough signal to infer the correct depth.
</p>

<p style="margin-top:-10px;">
We address this by combining coarse global depth search with graph cuts-based depth refinement. Instead of optimizing only a subset of pixels, the method refines depths for the entire image jointly, allowing smoothness priors and global information to guide ambiguous regions while preserving discontinuities at object boundaries.
</p>

---

### Key Contributions

<ul style="margin-top:-10px;margin-left:-1em;">
    <li>Coarse-to-fine pipeline combining global search and discrete optimization.</li>
    <li>3D grid graph formulation with offset vertices for depth refinement.</li>
    <li>Joint optimization of all pixels during refinement rather than processing only subsets.</li>
    <li>Improved reconstruction in homogeneous regions where local matching cues are weak or ambiguous.</li>
</ul>

---

### Method

<img src="assets/img/mvsgc-pipeline.webp" alt="Reconstructed Dino model from the multi-view stereo project" style="margin-top:10px;margin-bottom:10px;max-width:600px;width:100%;">

<p style="margin-bottom:10px;">The pipeline follows a coarse-to-fine strategy, combining global search with graph-based optimization.</p>

#### 1. Coarse Depth Estimation

<ul style="margin-top:-10px;margin-left:-1em;margin-bottom:20px;">
    <li>Initial per-pixel depths are estimated on downscaled input images by maximizing ZNCC-based photo-consistency using Particle Swarm Optimization (PSO).</li>
    <li>Coarse depth maps are checked for cross-view consistency, removing unreliable estimates.</li>
    <li>Missing values are filled using cross-view depth map completion.</li>
</ul>

<!-- This stage provides a reliable initial estimate of depth. -->

#### 2. Graph Cuts-Based Depth Refinement

<img src="assets/img/mvsgc-graph.webp" alt="Graph formulation of depth refinement" style="max-width:400px;width:100%;">
<p style="margin-top:-10px;margin-bottom:30px;"><i>Graph structure for depth refinement of a 4×2 image with depth-levels d = 5 and vertices offset to account for different initial depths. The source partition S and sink partition T are denoted by blue and red nodes, respectively. The s−t cut edges are denoted by dashed lines.</i></p>

<ul style="margin-top:-10px;margin-left:-1em;margin-bottom:20px;">
    <li>Coarse depth maps are upscaled to the original resolution and used as initialization.</li>
    <li>A 3D grid graph is constructed over discretized depth levels for each pixel.</li>
    <li>Vertices are offset along the depth axis based on initial coarse depths.</li>
    <li>Edge capacities encode the photo-consistency and smoothness terms of the refinement energy.</li>
    <li>Refined depth maps are obtained via the minimum <i>s-t</i> cut using the Boykov-Kolmogorov max-flow/min-cut algorithm.</li>
</ul>

<!-- This enables global optimization over all pixels simultaneously. -->

#### 3. Fusion and Surface Reconstruction

<ul style="margin-top:-10px;margin-left:-1em;">
    <li>Refined depth maps are projected into 3D to form a dense point cloud.</li>
    <li>A watertight mesh is generated using Poisson surface reconstruction.</li>
</ul>

<p style="margin-top:10px;">
This design makes it possible to use global information during refinement without incurring the full cost of unconstrained high-dimensional optimization.
</p>

---

### Implementation

<p style="margin-top:-10px;">
<ul style="margin-left:-1em;">
    <li style="margin-bottom:5px;"><b>Language</b>: Python</li>
    <li><b>Core libraries</b>:
        <ul style="margin-left:-1em;margin-bottom:5px;">
            <li>NumPy, SciPy, OpenCV</li>
            <li>PyGMO (evolutionary computation for coarse depth search)</li>
            <li>PyMaxflow (graph cut optimization)</li>
            <li>Numba (JIT acceleration)</li>
            <li>Multiprocessing (parallel execution)</li>
        </ul>
    </li>
    <li><b>Additional tools</b>: 
        <ul style="margin-left:-1em;">
            <li>MVE (depth map visualization and point cloud generation)</li>
            <li>Open3D (3D visualization)</li>
            <li>Poisson Surface Reconstruction (mesh generation from point clouds)</li>
        </ul>
    </li>
</ul>
</p>

---

### Results

<p style="margin-top:-10px;">
The method was evaluated on standard indoor and outdoor datasets:

<ul style="margin-top:-10px;margin-left:-1em;">
    <li>Middlebury <b>TempleRing</b> (48 views, 640x480)</li>
    <li>Middlebury <b>DinoRing</b> (48 views, 640x480)</li>
    <li>EPFL <b>Fountain-P11</b> (11 views, 3072x2048)</li>
    <li>DTU <b>Skull</b> (49 views, 1600x1200)</li>
</ul>
</p>

<p style="margin-top:-10px;">
Key observations:
<ul style="margin-top:-10px;margin-left:-1em;">
    <li>High completeness with minimal holes and outliers</li>
    <li>Strong performance in low-textured regions</li>
    <li>Robust to occlusions, lighting variations, and limited viewpoints</li>
</ul>
</p>

<img src="assets/img/mvsgc-skull.webp" alt="Reconstructed Skull model" style="max-width:600px;width:100%;">
<p style="margin-top:-20px;"><i>Input images, graph cut-refined depth maps, and reconstructed 3D model for the DTU Skull dataset.</i></p>

---

### Publication

<p style="margin-top:-10px;">
<b>Nirmal S. Nair</b> and <b>Madhu S. Nair</b>, "Multi-View Stereo Using Graph Cuts-Based Depth Refinement," <i>IEEE Signal Processing Letters</i>, vol. 29, pp. 1903-1907, 2022.
</p>

<p style="margin-top:-6px;">
This work shows how graph cut optimization can be applied to dense multi-view stereo refinement, enabling practical global optimization and improving reconstruction quality in ambiguous regions.
</p>

---
