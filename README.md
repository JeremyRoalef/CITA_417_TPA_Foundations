<h1>INTRODUCTION</h1>
<h1>INTRODUCTION</h1>
<h1>INTRODUCTION</h1>

<h1>VIDEO</h1>

<p>
  The video illustrates how the lab optimized the world. The world has the following:
  <ul>Ray Tracing</ul>
  <ul>High-fidelity shadows</ul>
  <ul>High triangle counts for meshes</ul>
  Each of these unoptimizations causes a confounding effect on the game's performance. High triangle counts causes the ray tracing to be more expensive, and shadows, by default, are expensive to have.

  In the video, you will see the unoptimized world first, which has the the items listed above. Take note of the FPS in the world. Additionally, the video displays the GPU calls. You will want to focus on the following GPU statistics:
  <ul>RenderDefferedLighting</ul>
  <ul>Lights</ul>
  <ul>RayTracingDynamicGeometry</ul>
  These are the targeted systems for improvement.

  After showing the unoptimized world, the video will swap to the optimized world. The optimized world has:
  <ul>No ray tracing</ul>
  <ul>Reduced shadow detail</ul>
  <ul>Lower triangle counts</ul>
  Take notice to the FPS increase from the unoptimized setup. On the GPU statistics page, notice how the GPU calles for the items listed earlier no longer show up. That is because their GPU calls have been reduced significantly, and other items are calling the GPU more now.
</p>


You may find the video <a href = "">Here </a>
