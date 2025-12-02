<h1>INTRODUCTION</h1>
This lab aims to analyze the performance benefits of using a pooling system for particle systems. The lab will demonstrate the benefits and tradeoffs for a pooled particle system by displaying the cost of instantiating particle systems at runtime versus pre-loading a pooled particle system before the game begins. As this lab will show, there is some measurable improvement to performance when using a pooled system. However, performance in this lab varied due to high particle counts being rendered at once. Regardless, creating a pooling system provided a net positive effect on the performance.

<h1>SETUP</h1>
For this lab, I reused the levels from lab 6. However, many of the material used in this lab will be created from scratch. I will be using the Niagara particle system to create particles. Then, I will have two blueprints to control the particle behavior, one will control the instantiation logic (BP_NiagaraSpawner), and the other will contain the particle system itself(BP_NiagaraFX). Below, you may find the blueprint structure for BP_NiagaraSpawner:
<img width="2036" height="479" alt="image" src="https://github.com/user-attachments/assets/7f204f11-4e61-4bb8-9305-8c8a5d013169" /> <br>
<img width="1999" height="507" alt="image" src="https://github.com/user-attachments/assets/e7dd1123-fff4-459e-a8ee-b1542a038620" /><br>
<img width="2004" height="374" alt="image" src="https://github.com/user-attachments/assets/9ae8947f-a83f-4a4f-a712-bbfe18a7d488" /><br>
<img width="761" height="346" alt="image" src="https://github.com/user-attachments/assets/f7ca37de-75b9-41e4-8da9-b536151e23d6" /><br>
<img width="2222" height="591" alt="image" src="https://github.com/user-attachments/assets/e032be19-0cdd-4e62-9f77-d559287cefd3" /><br>
<img width="2129" height="569" alt="image" src="https://github.com/user-attachments/assets/93c76157-d31f-4c95-bb25-6c4faed4d6c6" /><br>
Additionally, the following attributes were added for playtesting:
<img width="575" height="391" alt="image" src="https://github.com/user-attachments/assets/989c1d4c-c021-4e17-a8bf-24e6bdfa7c55" />
The attribute value for the non-pooling and pooled setup are the same, other than the usePooling attribute, which is disabled for the non-pooling setup and enabled for the pooling setup.

<br>
Below, you may find the blueprint for BP_NiagaraFX:
<img width="1307" height="408" alt="image" src="https://github.com/user-attachments/assets/a0b0813a-7c4d-4368-83eb-cc993fc2eabc" />
<img width="652" height="395" alt="image" src="https://github.com/user-attachments/assets/3ad1c42c-470d-4d4b-b0d0-92e90fb034ae" />

<h1>VIDEO</h1>
The video illustrates how performance-intensive running hundreds of particle systems every second can be on computers. Especially when not using a pooled system, the performance drops to <10fps. Comparatively, running a pooled system may provide upwards of 30fps. However, the performance does drop down to non-pooled framerate on occasion. This frame drop likely does not display the benefits of a pooling system, but rather the cost of running many particle systems at once. It is worth mentioning that the non-pooled system could not achieve any frame rate higher than 10fps, whereas the pooled system was capable of achieving upwards of 30fps. 

You may find the video <a href = "https://github.com/JeremyRoalef/CITA_417_TPA_Foundations/releases/tag/V3.0">Here</a>, and clicking on the file named "2025-12-01.20-53-00.mkv
".
<h1>RESULTS</h1>
Here is a simple table illustrating the performance difference between the pooling and non-pooling setup:
<img width="472" height="137" alt="image" src="https://github.com/user-attachments/assets/24f15cdd-5a07-44c7-9f81-60d0fd78b139" />

