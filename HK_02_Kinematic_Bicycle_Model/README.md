<p align="right">© Documentation by T V Hari Krishna</p>
<p align="right">5 𝘮𝘪𝘯𝘶𝘵𝘦 𝘳𝘦𝘢𝘥 📚 </p> <br>

<!------ PROJECT TITLE ------>
<p align="center">
    <img src="readme_data/title.png" alt="Why we chose this project" width="1500"/>
</p> <br> <br>

<!------ WHAT ------>
<p align="center">
    <img src="readme_data/what.png" alt="Why we chose this project" width="600"/>
</p>

<p align="center"><h1>🎀 Essence of the Project</h1></p>
<p align='justify'>
The Bicycle Kinematic Model block creates a bicycle vehicle model to simulate simplified car-like vehicle dynamics, representing a vehicle with two axles defined by the length between the axles, known as the `wheel base. The vehicle's heading, theta, is defined at the center of the rear axle, where the front wheel can be steered using an angle psi. <br>
    
This kinematic approach is fundamental in <strong>autonomous driving vehicles</strong> and <strong>autonomous mobile robotics</strong>, enabling accurate motion planning and control by predicting vehicle trajectory and facilitating the implementation of advanced navigation algorithms. </p> <br> <br>

<!------ WHY ------>
<p align="center">
    <img src="readme_data/why.png" alt="What the project accomplishes" width="600"/>
</p>

<p align="center"><h1>🎯 Project Vision</h1></p>
<p style="text-align: justify;">
▸ The Bicycle Kinematic Model is pivotal in autonomous driving and robotics for precise movement planning and execution.

▸ It converts complex vehicle dynamics into a simpler model for trajectory prediction from steering commands.

▸ Essential for path planning and control, it predicts vehicle or robot future positions for smooth navigation and path adherence.

▸ Optimizes trajectories for energy-efficient routing, extending battery life and reducing energy use.

▸ Enhances safety by enabling systems to react to unexpected obstacles or changes, minimizing accident risks.
</p> <br> <br>

<!------ HOW ------>
<p align="center">
    <img src="readme_data/how.png" alt="How we implemented the project" width="600"/>
</p>

<p align="center"><h1>🪓Project Implementation</h1></p>

<p><h2>💠 Software Design & Tools </h2></p>
<p align='justify'>
The project is developed using the Robot Operating System (ROS), facilitating complex simulations and trajectory analysis. The mathematical foundation and kinematic behavior of the bicycle model are visualized through Matplotlib, with Python scripting at the core of the development. RViz provides real-time visualization of the robot model and trajectory, enhancing the analysis and debugging process.
</p>
<p>
  <!-- Ubuntu Badge -->
  <img src="https://img.shields.io/badge/Ubuntu-E95420.svg?&style=flat-square&logo=ubuntu&logoColor=white" alt="Ubuntu" style="height: 25px;"/> &nbsp;
  <!-- Linux Badge -->
  <img src="https://img.shields.io/badge/Linux-FCC624.svg?&style=flat-square&logo=linux&logoColor=black" alt="Linux" style="height: 25px;"/> &nbsp;
  <!-- VS Code Badge -->
  <img src="https://img.shields.io/badge/VS%20Code-007ACC.svg?&style=flat-square&logo=visual-studio-code&logoColor=white" alt="VS Code" style="height: 25px;"/> &nbsp;
  <!-- ROS Badge -->
  <img src="https://img.shields.io/badge/ROS-22314E.svg?&style=flat-square&logo=ros&logoColor=white" alt="ROS" style="height: 25px;"/> &nbsp;
  <!-- Python Badge -->
  <img src="https://img.shields.io/badge/Python-3776AB.svg?&style=flat-square&logo=python&logoColor=white" alt="Python" style="height: 25px;"/> &nbsp;
  <!-- Matplotlib Badge -->
  <img src="https://img.shields.io/badge/Matplotlib-FFD43B.svg?&style=flat-square&logo=python&logoColor=blue" alt="Matplotlib" style="height: 25px;"/> &nbsp;
</p> <br>

<!------ Deployment and Testing ------>
<p align="center"><h2>💠 Deployment and Testing </h2></p>
<p align='justify'>
▸ The deployment of the Bicycle Kinematic Model was conducted within a simulated environment using ROS, ensuring a controlled testing. I deployed the model on a standard Ubuntu system, with simulations facilitated by Matplotlib for trajectory visualization. The process included continuous integration practices to check for code integrity and automated tests to validate kinematic equations against predetermined inputs.
</p>

<p align='justify'>
▸ Testing consisted of a series of controlled simulations designed to challenge the model's capabilities in trajectory planning and response. Scenarios included navigating circular paths, sharp turns, and S-shaped trajectories, each requiring precise control of steering angles and velocity. The model's performance was gauged by its ability to maintain the intended path with minimal deviation and its response time to dynamic commands.
</p> <br>

<!------ Observation 1 ------>
<p align="center">
    <img src="readme_data/project_obs_1.png" alt="Why we chose this project" width="1500"/>
</p> <br>

<!------ Observation 2 ------>
<p align="center">
    <img src="readme_data/project_obs_2.png" alt="Why we chose this project" width="1500"/>
</p> <br>

<!------ Observation 3 ------>
<p align="center">
    <img src="readme_data/project_obs_3.png" alt="Why we chose this project" width="1500"/>
</p> <br>

<!------ Result and Analysis ------>
<p align="center"><h2>💠 Results & Analysis </h2></p>

<p align='justify'>
▸ The results of the Bicycle Kinematic Model were documented to demonstrate the alignment between theoretical predictions and practical observations. A series of control sequences were executed, each manipulating the model's velocity and turning rate over a set duration. The initial and final positions were recorded alongside the total distance traveled, providing a quantitative measure of the model's behavior.
</p>

<p align='justify'>
▸ For example, the <code>control sequence [1, 0.1, 5]</code> indicating a velocity of 1 unit/s, a turning rate of 0.1 rad/s, and a duration of 5 seconds resulted in a final position of <code>(-2.5586, 5.1742)</code> from the origin <code>(0,0)</code>. The model traversed a distance of approximately <code>5.77 units</code>, as calculated by the Euclidean distance formula, correlating with the model's kinematic equations.
</p>

<p align='justify'>
▸ The precision of the model was highlighted in complex maneuvers, such as a sharp turn demonstrated by the <code>control sequence [1, 0.7, 7]</code>, which yielded a significant change in position, and a minimal distance traveled when the model performed a near-instantaneous direction reversal with the <code>sequence [-0.1, 0.8]</code>. The results confirmed the model's capability to accurately predict the effects of various control inputs on the vehicle's trajectory.
</p>

<p align='justify'>
▸ The kinematic equations were validated against these practical outcomes, with each step of the computational process from determining velocity and heading change to calculating the change in position showing a high degree of accuracy. This rigorous analysis not only confirms the robustness of the Bicycle Kinematic Model for theoretical application but also demonstrates its potential for real-world implementation in autonomous vehicle navigation and robotics control systems.
</p>

<!------ Observation 4 ------>
<p align="center">
    <img src="readme_data/project_obs_4.png" alt="Why we chose this project" width="1500"/>
</p> <br>

<hr> 
<br>

<p align="center">
    <img src="readme_data/funny_endquote_autonomous_driving.png" alt="Alt text for your image" width="1500"/>
</p>




























