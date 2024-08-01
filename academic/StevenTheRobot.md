
<h1 align="center">Steven the Autonomus Robot</h1>

<h3>Introduction</h3>
This page is dedicated to my RSLK Robot project "Steven the Robot", built using Texas Instruments' Launchpad platform and the RSLK (Robotic Systems Learning Kit). This project showcases my expertise in robotics, embedded systems, and programming, highlighting my ability to integrate hardware and software for innovative solutions.

<h3>Project Overview</h3>
<ul>
  <li><b>Project Name:</b> Steven The Robot</li>
  <li><b>Class:</b> Embedded Systems</li>
  <li><b>Platform:</b> Texas Instruments Launchpad</li>
</ul>

<h3>Technical Details</h3>
<h4>Bumpers and 180-Degree Turn</h4>
One of the key features of Steven was the use of the bumpers on the front of the RSLK kit. When the bumper was triggered, Steven was programmed to make a 180-degree turn. We had to carefully mitigate bouncing in the button to ensure precise and reliable activation of this turn mechanism.

<h3>Hard and Soft Turns</h3>
Steven was designed to navigate a black line on the ground using its IR sensors. We implemented two types of turns to optimize its performance in the competition:
<ul>
  <li><b>Hard Turn:</b>When all IR sensors on one side were triggered, Steven would stop and execute a 90-degree turn. This allowed for a sharp correction when necessary.</li>
  <li><b>Soft Turn:</b>When the sensors were not centered on the line, Steven would slightly reduce the duty cycle on one of the wheels. This allowed it to continue moving forward while making minor course corrections. This approach was crucial for maintaining speed while navigating the course.</li>
</ul>

<h3>Competition Details</h3>
The competition required Steven to follow a black line on the ground until it reached the end, at which point it would touch a wall, turn around, and return to the start. Our team focused on balancing speed and accuracy, particularly through the implementation of the soft turn program. This allowed Steven to maintain a high speed with decent accuracy, which proved to be an effective strategy.

<h3>Results</h3>
Steven the Robot placed second in the competition. Our emphasis on speed and the effectiveness of the soft turn program allowed us to excel where many teams slowed down. By prioritizing speed with decent accuracy, Steven was able to complete the course efficiently and outperform many competitors.

<h3>Gallery</h3>
<h4>Photos</h4>
<p align="center"><img src= "/images/StevenTheRobot/Steven-second-place.jpg" Width=600/>
  <h5 align="center">Steven with his second place award.</h5>
<p align="center"><img src= "/images/StevenTheRobot/Steven-Award.jpg" Width=600/>
<h5 align="center">Award ceremony, my team is on the left</h5>
  
<h4>Video Demo</h4>
<video align="center" controls> <source src= "https://raw.githubusercontent.com/Trankley/Trankley.github.io/main/images/StevenTheRobot/Steven-moving.mp4" type="video/mp4">
</video>

<h3>Conclusion</h3>
Working on Steven the Robot was an incredible learning experience that combined theoretical knowledge with practical application. The project challenged us to innovate and refine our approach to embedded systems, ultimately resulting in a successful competition performance. Thank you for exploring this project with me!

