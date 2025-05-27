---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! My name is Jay Rana and I am currently a Master's student at the University of Maryland College Park (UMD). I am pursuing a MS in Electrical and Computer Engineering at UMD and intend to specialize in Control, Robotics, Autonomy, and Learning (CRAL).

Below is a summary of my academic/research experience, projects, and extracurriculars. You can click on the headers at the top to learn more about each.

## Academic Experience
I graduated from UMD with a BS in Computer Engineering and a Minor in Robotics and Autonomous Systems in May of 2025. Below is a list of relevant undergraduate coursework:

- Robotics Planning and Perception
- Robotics Project Laboratory
- Capstone Design Project: Autonomous Control of Interacting Robots
- Digital Computer Design (graduate-level)
- Digital Control Systems
- Signal and System Theory
- Introduction to Artificial Intelligence

## Research Experience
I was in the [Gemstone Honors Program at UMD](https://gemstone.umd.edu/){:target="_blank"}. As part of Team Affordable Natural Disaster Relief Robotics (ANDRR), I researched, prototyped, and tested an accessible modular system that can be attached to hobby quadcopters to enable onboard computer vision for the purposes of disaster relief. Our research started in the Fall of 2022 and concluded in the Spring of 2025. We wrote a thesis and successfully defended it in front of a panel of discussants. You can learn more about our research and read our thesis [here](https://teamandrr.wordpress.com/){:target="_blank"}.

Over the summer of 2025, I plan to work with [Dr. Yiannis Aloimonos](https://scholar.google.com/citations?hl=en&user=7QmEsOwAAAAJ&view_op=list_works){:target="_blank"} and [Levi Burner](https://scholar.google.com/citations?user=BKY_uwoAAAAJ&hl=en){:target="_blank"} on computer vision research regarding optical flow.

## Projects
### DogBot
We developed a robot that can play fetch for our capstone design project. We modified a TurtleBot 3 Burger so that it could "hold" a ball in between a set of chopsticks, and attached a USB webcam to the front. We also used an Nvidia Jetson Xavier NX for performing image recognition tasks using YOLO. By running the Robot Operating System (ROS) on both devices, we were able to send camera data to the Jetson and then send velocity commands back to the TurtleBot. The Jetson performed image-based visual servoing (IBVS) based on the camera data, which enabled the TurtleBot to smoothly track objects in its field of view. After combining the subsystems together, the robot was able to track a ball, "hold" it, then track a human to return the ball to.
<video src="../images/DogBot.mov" width="320" height="240" controls></video>

### Clean Out the Closet! Robot
We developed a robot that can pick up Lego towers, avoid obstacles, and navigate between locations for our final project in our Robotics Planning and Perception class.

The goal of the project was to compete with other teams to move Lego towers from our "closet" to the "closet" of the other team while avoiding collisions. The robot we used for this project was the DJI RoboMaster EP Core, which comes with Mecanum wheels for omnidirectional movement, as well as a claw with a camera. The Python SDK for the RoboMaster provides callbacks and built-in commands for receiving camera data, measuring position from encoders and IMU readings, and sending velocity commands to the chassis. We created a robot controller that chooses the optimal action to take using a minimax tree, then runs a state machine based on that action to perform tasks such as picking up towers or moving towards a location. The controller also uses YOLO to detect towers and other robots on the field, and uses the Pupil AprilTags library to detect AprilTags which are located on randomly placed obstacles. The full system can navigate to locations on the map, pick up blocks using image-based visual servoing (IBVS), and avoid obstacles (robots and AprilTags).
<video src="../images/CMSC477 Project 3.mov" width="320" height="240" controls></video>
<video src="../images/CMSC477 Project 3 2.mov" width="320" height="240" controls></video>

### Image-Based Visual Servoing Controller
The projects above both use image-based visual servoing (IBVS), which is a control technique that aims to move an object towards a desired place in an image. Indirectly, this allows robots to move towards a target while exhibiting the same stable smoothing behavior as PID controllers. For example, in DogBot, in order to track the ball and move it in between the chopsticks, we set the desired location of the image of the ball to be in the bottom center of the image. Since the TurtleBot 3 Burger is only able to move forward/backward and pivot left/right, it must necessarily move forward and turn towards the ball in order to move the image of the ball there. I followed the control equations given in ["Visual servo control I. Basic approaches" by Chaumette and Hutchinson](https://ieeexplore.ieee.org/document/4015997){:target="_blank"} and [implemented them as a Python file](https://github.com/wolr210/IBVS_Controller){:target="_blank"}, which is published on my GitHub account. In the future, I plan on expanding the controller to include all six traditional degrees of freedom, and publishing the controller as a Python package on PyPI.

## Extracurriculars
### Gamer Symphony Orchestra
I am part of the [Gamer Symphony Orchestra (GSO) at UMD](https://umd.gamersymphony.org/index.php){:target="_blank"}. We are a full symphonic rock orchestra that arranges and plays music from video games! I serve as the cello section leader and webmaster. Here is a [link to our YouTube channel](https://www.youtube.com/c/GamerSymphonyUMD){:target="_blank"}. Below is the recording of one of my favorite arrangements.
<iframe width="560" height="315" src="https://www.youtube.com/embed/aCt4w-SBpoU?si=AVRFwneW_T1FUawN" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### The Hare
[The Hare](https://theumdhare.com/about-us/){:target="_blank"} is a satire news organization at UMD. You can read my article about how [Taco Bell planned to open a hotel near campus](https://theumdhare.com/2024/10/02/before-budget-cuts-route-1-taco-bell-had-plans-for-new-hotel/){:target="_blank"}, or my other article about how the northern lights that were visible across the United States in October 2024 were actually [caused by the spotlights of a local bar](https://theumdhare.com/2024/10/23/spotlights-from-terrapins-turf-mistaken-for-another-aurora-borealis/){:target="_blank"}.