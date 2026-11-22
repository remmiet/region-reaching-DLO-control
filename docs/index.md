---
layout: default
title: "Region-Reaching Control for Deformable Linear Objects (DLO) Manipulation"
---

## Abstract
In industrial automation, operational efficiency has been increasingly enhanced by robotic manipulation. While rigid object manipulation has matured as a research subject, rigidity cannot be guaranteed in many advanced applications. Consequently, interaction with soft and deformable materials is increasingly required by modern robots. Deformable Linear Objects (DLOs) represent a significant sub-category in this domain, encompassing materials such as surgical threads, ropes and cables. In cable assembly, cables are required to be deformed to meet specific task requirements. Current research in this field relies on strict setpoint targets and the usage of advanced control methods to deform the high-dimensional continuum. In most literature, assumption that the target shape is achievable and stable is often required. In practice, goal validation is highly impractical for dynamic applications, and when invalidated planned targets are pursued, instability is frequently induced, as enforcing precision across the continuum causes conflicting inter-feature constraints. In most cases, high precision across the entire continuum is also rarely necessary. The region-reaching concept has provided target flexibility in other robotic applications; however, its application to the high-dimensional continuum of DLOs remains unexplored. Consequently, a Region-Reaching Control (RRC) framework for DLOs is developed.

---

## Simulation
The simulations below demonstrate how our region-reaching controller overcomes a core limitation of setpoint tracking. While forcing every point to an exact coordinate causes severe instability, introducing regional tolerances allows our controller to stably achieve the desired shape in both 2D and 3D.
### 2D Simulation
<table>
  <tr>
    <td width="50%" align="center">
      <video width="100%" controls>
        <source src="videos/sim 2d ours case 98 - edited.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <p><b>Our Controller</b></p>
    </td>
    <td width="50%" align="center">
      <video width="100%" controls>
        <source src="videos/sim 2d tro case 98 - edited.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <p><b>Setpoint controller</b></p>
    </td>
  </tr>
</table>
### 3D Simulation
<table>
  <tr>
    <td width="50%" align="center">
      <video id="vid1" width="100%" controls>
        <source src="videos/sim 3d our - edited.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <p><b>Our Controller</b></p>
    </td>
    <td width="50%" align="center">
      <video width="100%" controls>
        <source src="videos/sim 3d tro - edited.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <p><b>Setpoint controller</b></p>
    </td>
  </tr>
</table>

<script>
  const v1 = document.getElementById('vid1');
  v1.defaultPlaybackRate = 3.0;
  v1.playbackRate = 3.0;
</script>

<style>
  video {
    width: 100%;
    aspect-ratio: 16 / 9;
    object-fit: contain;
    background-color: black;
  }
  video::-webkit-media-controls-current-time-display,
  video::-webkit-media-controls-time-remaining-display {
    display: none;
  }
</style>


## Real-World Experiments
An example of our controller in real-world experiments. 
<video width="100%" controls>
  <source src="videos/real-world experiment 1.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<video width="100%" controls>
  <source src="videos/application_compressed.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<!--
---

## Results & Experiments
* **Experiment 1:** Description of what was tested.
* **Experiment 2:** Key findings and performance metrics.

---

## Citation
If you have a preprint or published paper, provide the BibTeX:

```bibtex
@article{yourname2026title,
  title={Your Paper Title},
  author={Your Name and Co-Author},
  journal={Journal or Conference Name},
  year={2026}
}
-->
