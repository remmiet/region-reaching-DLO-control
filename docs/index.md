---
layout: default
title: "Region-Reaching Control for Deformable Linear Objects (DLO) Manipulation"
---

## Abstract
While modern robotics has made significant progress in rigid object manipulation, controlling Deformable Linear Objects (DLOs) remains challenging due to their infinite-dimensional configuration spaces and highly non-linear dynamics. Existing control paradigms rely primarily on setpoint targets; however, because points along a DLO are physically coupled, enforcing an exact geometric configuration frequently leads to excessive actuation effort, internal stress accumulation, and severe instability near singularities. Furthermore, these methods assume that the target shape is statically stable and physically achievable, necessitating prior goal validation that is often impractical in real-world environments. In practice, rigid setpoint accuracy is rarely required---achieving a generalized shape is typically sufficient, and when precision is necessary, it is generally restricted to specific feature points. A regional control paradigm naturally satisfies these practical requirements while overcoming the structural limitations of setpoint tracking. To bridge the gap between classical control formulations and real-world task demands, this work introduces a Region-Reaching Controller for DLO manipulation.

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
An example of our controller in real-world experiments. More examples including applications-based experiments will be inlcuded in the future.
<video width="100%" controls>
  <source src="videos/real-world experiment 1.mp4" type="video/mp4">
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
