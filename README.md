<h1>INTRODUCTION</h1>
This lab aims to explore the effects of taking the optimization strategies from lab 5 and apply them at scale. The aim is to get a measurable performance increase to demonstrate that the optimization strategies work properly. To recap, the optimization strategies implement include level of detail and lighting quality settings.

As the video will demonstrate, the top costs for this lab is lighting. Unreal breaks these costs into many categories. The categories I will focus on are lights, rendered deferred lighting, and ray tracing geometric shadows.

<h1>SETUP</h1>
The lab started from the same levels in lab 5. Additionally, this lab introduces new objects with expensive and cheap counterparts. These new objects include:
<ul>Tables</ul>
<ul>Plates</ul>
<ul>Pillars</ul>
<ul>Maces</ul>
These assets will be used to create a larger scene with some detail.
These settings will apply high-quality shadows and lighting to the world.

<h1>VIDEO</h1>
You may find the video <a href = "">Here</a>, and clicking on the file  named "".

<h1>RESULTS</h1>
Here is a simple table illustrating the performance difference between the optimized world and unoptimized world:
<img width="1090" height="118" alt="image" src="https://github.com/user-attachments/assets/3b9e5219-58f9-4842-93fa-50d96a653301" />
You may notice that there was no perceivable difference in frame rate from the optimized and unoptimized world. The FPS value was 60 in each scenario. This is likely due to a frame rate cap set at 60 for the game. The actual time it took to render the frame, the ms category, shows that it took less time to render the optimized world (15.57ms) than the unoptimized world (16.66ms).
