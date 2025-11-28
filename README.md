<h1>INTRODUCTION</h1>
This lab aims to explore optimization strategies within the Unreal game engine. For this lab, I will be using Unreal Engine 5. The optimizations I will be targeting are the following:
<ul>Ray Tracing</ul>
<ul>Shadow Quality</ul>
Lighting in video games the most expensive task you can give a computer. Understanding how to reduce lighting detail in your game can offer low to medium-end computers the opportunity to play your game. Thus, the lab will explore how one can reduce lighting quality in their game. The lab will illustrate how Unreal Engine offers many tools that make this process easy.

<h1>SETUP</h1>
The lab started from a blank Unreal project. Unreal provides a sample level that the lab will work in. Custom assets that I created in the past were exported into the project with two variants: The original and a high-triangle version that has been subdivided in Blender many times. A simple room was designed with some of the custom assets. Additionally, the room features 13 point lights. Point lights are the most expensive form of lighting for a scene, so they will demonstrate the optimization improvements most significantly. Under the details for each point light, the following light settings have been applied:
<img width="996" height="790" alt="image" src="https://github.com/user-attachments/assets/4c73221c-dd98-4be8-9259-fb6bf21a3939" />
These settings will apply high-quality shadows and lighting to the world.
<br><br>
The objects in the scene are using their expensive counterparts. Even though there is no visual difference between the cheap and expensive mesh models, the expensive model has significantly more triangles and, thus, will require the ray tracing in the world to work harder. Here is a statistic comparison for the one of the cheap-expensive models in the world:
<img width="649" height="958" alt="image" src="https://github.com/user-attachments/assets/8e10c4b5-d554-4fc0-8129-247f6d56393d" />
<img width="717" height="1026" alt="image" src="https://github.com/user-attachments/assets/1cd955d2-dad2-49ce-a830-9da24d489147" />
This setup will produce a high-quality scene with very poor performance. To illustrate how performance will be improved, a duplicate level was created to apply the following:
<ul>Removing ray tracing lighting</ul>
<ul>Reducing shadow quality</ul>
<ul>Replacing expensive meshes with cheaper counterparts<ul>

<h1>VIDEO</h1>
<p>
  The video illustrates how the lab optimized the world. The world has the following:
  <ul>Ray Tracing</ul>
  <ul>High-fidelity shadows</ul>
  <ul>High triangle counts for meshes</ul>
  Each of these unoptimizations causes a confounding effect on the game's performance. High triangle counts causes the ray tracing to be more expensive, and shadows, by default, are expensive to have.
<br><br>
  In the video, you will see the unoptimized world first, which has the the items listed above. Take note of the FPS in the world. Additionally, the video displays the GPU calls. You will want to focus on the following GPU statistics:
  <ul>RenderDefferedLighting</ul>
  <ul>Lights</ul>
  <ul>RayTracingDynamicGeometry</ul>
  These are the targeted systems for improvement.
<br><br>
  After showing the unoptimized world, the video will swap to the optimized world. The optimized world has:
  <ul>No ray tracing</ul>
  <ul>Reduced shadow detail</ul>
  <ul>Lower triangle counts</ul>
  Take notice to the FPS increase from the unoptimized setup. On the GPU statistics page, notice how the GPU calles for the items listed earlier no longer show up. That is because their GPU calls have been reduced significantly, and other items are calling the GPU more now.
  <br><br>
  You may find the video <a href = "https://github.com/JeremyRoalef/CITA_417_TPA_Foundations/releases/tag/V1.0">Here</a>, and clicking on the file named "2025-11-22.20-29-53.mkv
"
</p>

<h1>RESULTS</h1>
Here is a simple table illustrating the performance difference between the optimized world and unoptimized world:
<img width="2101" height="240" alt="image" src="https://github.com/user-attachments/assets/e1f7d4e1-ce5c-4e3c-a7ce-730adf448834" />
