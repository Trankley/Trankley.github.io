<h1>Detailed Hover DR1 Documentation</h1>

<h3>About</h3>
This documentation contains the contents of the final-deliverable my team presented for our Capstone Design project. We placed <a href="https://www.linkedin.com/posts/eceutdallas_youbelonghere-utd-stem-ugcPost-7154169550811398144-j8RZ?utm_source=share&utm_medium=member_desktop">1st place</a> in the ECE department competeing against fellow CE/EE majors at the University of Texas at Dallas.


<h1>Reactive Audio Hoverboard</h1>
<h4>UTDesign Fall 2023</h4>
<h4>UTDesign Team 1792</h4>
<ul>
  <li>Trankley Mahler</li>
  <li>Jimmy Tran</li>
  <li>Jonathan Abshiro</li>
  <li>Kevin Mikhaiel</li>
  <li>Tate Froh</li>
  <li>William Lim</li>
</ul>
<h4>Faculty Advisor:</h4>
Dr. Leo Estevez
<h4>Instructor:</h4>
Dr. Marco Tacca

<h2>Abstract</h2>
The team designed and built a market-ready kit, marketed as the HoverDR1 Learning Module, that allows consumers to convert their hoverboard devices into learning platforms using off the shelf parts and a provided instruction guide. The kit is powered by an Arduino Uno, and controls the movement of the hoverboard based on the audio frequencies detected by the module. The kit includes the aforementioned Arduino Uno, as well as a microphone module, a motor, a casing, a mounting solution, an emergency stop mechanism, and a motor relay. This device allows parents to teach their kids the basics of engineering, STEM, and software development using a guided, but expandable, learning platform.

<h2>TABLE OF CONTENTS</h2>

<ol>
  <li>Introduction</li>
  <li>Review of Conceptual and Preliminary Design</li>
  <ol>
    <li>Problem Analysis</li>
    <ol>
      <li>Summary of Specifications</li>
      <li>Main Features of Design Problem</li>
      <li>Technical Approach</li>
    </ol>
    <li>Decision Analysis</li>
    <ol>
      <li>Solution Alternatives</li>
      <li>Effectiveness Criteria</li>
      <li>Decision Analysis</li>
    </ol>
  </ol>
  <li>Basic Solution Description</li>
  <ol>
    <li>Subsystem 1 (Motor Controls)</li>
    <li>Subsystem 2 (FFT)</li>
    <li>Subsystem 3 (Chassis)</li>
  </ol>
  <li>Performance Optimization and Design of System Components</li>
  <ol>
    <li>Design Criteria</li>
    <ol>
      <li>Subsystem 1 (Motor Controls)</li>
      <li>Subsystem 2 (FFT)</li>
      <li>Subsystem 3 (Chassis)</li>
    </ol>
    <li>Components</li>
    <ol>
      <li>Subsystem 1 (H-Bridge and 30RPM Motor)</li>
      <li>Subsystem 2 (KY-038 arduinoFFT functions)</li>
      <li>Subsystem 3 (Material Choices)</li>
    </ol>
    <li>Fabrication/Assembly Process</li>
    <ol>
      <li>Subsystem 1</li>
      <li>Subsystem 2</li>
      <li>Subsystem 3</li>
    </ol>
    <li>Performance Evaluation</li>
    <ol>
      <li>Metric 1: Frequency identification and adjustment</li>
      <li>Metric 2: Universality</li>
    </ol>
  </ol>
  <li>Testing Procedure</li>
  <ol>
    <li>Metric 1</li>
    <li>Metric 2</li>
  </ol>
  <li>Project Implementation/Operation and Assessment</li>
  <ol>
    <li>Overview of Final Implementation</li>
    <li>Operational Test Results</li>
    <li>Evaluation of Results Relative to Design Criteria</li>
    <li>Kickstarter</li>
  </ol>
  <li>Conclusion, Overview of Work Statement</li>
  <li>Future Work Recommendations</li>
  <li>Other Issues</li>
  <ol>
    <li>Ethics</li>
    <ol>
      <li>Issue 1(Safety Stop Feature)</li>
      <li>Issue 2(Operational Manual)</li>
      <li>Issue 3(Warnings in Quickstart Guide)</li>
      <li>Issue 4(Backer Confidentiality)</li>
    </ol>
    <li>Operating Instructions</li>
    <ol>
      <li>Setup</li>
      <li>Mode 1 operation</li>
      <li>Mode 2 operation</li>
    </ol>
  </ol>
  <li>Cost Estimate</li>
  <ol>
    <li>Materials and Construction</li>
    <li>Estimate of Design Cost</li>
  </ol>
  <li>Project Management Summary</li>
  <ol>
    <li>Tasks Completed</li>
    <li>Tasks Pending Completion</li>
    <li>Time Allocated</li>
    <li>Facilities Used</li>
    <li>Personnel</li>
  </ol>
  <li>Appendices</li>
  <ol>
    <li>Bibliography</li>
    <li>Quickstart Guide</li>
    <li>Design Schedule</li>
    <li>Construction Schedule</li>
    <li>Equipment List and Cost Breakdown</li>
    <ol>
      <li>Subsystem 1</li>
      <li>Subsystem 2</li>
      <li>Subsystem 3</li>
    </ol>
    <li>Design Drawings</li>
    <ol>
      <li>Phase 1</li>
      <li>Phase 2</li>
      <li>Phase 3</li>
      <li>Other Part Designs</li>
    </ol>
    <li>Code</li>
  </ol>
</ol>

<h2>Acknowledgements</h2>
We would like to thank the following people for their guidance and help with the project:
<ul>
  <li>Professor Leo Estevez</li>
  <li>Professor Marco Tacca</li>
</ul>



<h2>1. Introduction</h2>
The RAH team at UTD has developed the HoverDR1 attachment designed to allow control of a hoverboard through the use of auditory stimuli. The purpose of the document is to provide the methodology for verifying the requirements (as stated in the Functional Specification) have been satisfied by the current design. <br><br>
The attachment is mounted on top of the hoverboard and controls it by mimicking the way it would be controlled normally. The system consists of a chassis and a shaft that runs across the hoverboard, both the chassis and shaft are strapped down to the left and right plates on the hoverboard to mimic someone stepping on it. The chassis holds all of the components of the design, the arduino, motor, motor controller, and microphone. The system is powered by one external battery that is also weight-biasing the hoverboard forward. When the system is on, if the microphone detects one of two predetermined frequencies, the arduino will send a signal to the motor controller, which will rotate the motor’s shaft left or right according to the frequency detected. The motor movement will rotate the hoverboard axis and cause it to turn.<br><br>
We have designed the arduino code to interface the microphone and motor controller, we have also designed the mechanical function and chassis of the attachment. The off-shelf components are the arduino, battery, microphone, motor, motor controller, and various fixtures(screws, washers, etc).

<h2>2. Review of Conceptual and Preliminary Design</h2>
<ol>
  <li>Problem Analysis</li>
  <ol>
    <li>Summary of Specifications:</li>
    The attachment will lay on top of the hoverboard and be completely independent of the hoverboard. Meaning that the attachment will be able to be compatible with various hoverboards. The attachment should be able to obtain frequencies and utilize them as commands to control the hoverboard that it is on. These commands consist of, turning left, right, forward, and stopping.
    <li>Main Features of Design Problem</li>
    <ul>
      <li>Device Development</li>
      <ul>
        <li>An electromechanical attachment to a Hoverboard which leverages the Bluetooth Audio integrated in the Hoverboard to control its movements.</li>
        <li>The component cost of this attachment should be less than $50. (A hoverboard will be provided to the team for development and testing.)</li>
        <li>An existing downloadable audio app should be used to control the Hoverboard.</li>
        <li>The Hoverboard DR1 attachment may be prototyped with an off the shelf EVM which enables audio sensing and motor control.</li>
      </ul>
      <li>Hover DR1 Crowdfunding</li>
      <ul>
        <li>1st Month: Order Relevant EVMs and Prototype an Audio Controller</li>
        <li>2nd Month: Test to have first Proof of Concept and Stage for Campaign(file Provisional Patent)</li>
        <li>3rd Month: Launch Campaign and Report on progress towards making lower cost integrated solutions available to the public with daily posts to the campaign.</li>
        <li>4th Month: Continued posts on progress towards working boards and posts on how multiple units are being produced and tested.</li>
        <li>5th Month: Shipping Units to Backers</li>
        <li>6th Month: Preparation/Presentation of Project Results at UTD</li>
      </ul>
    </ul>
    <li>Technical Approach</li>
    Due to the nature of our unique project, we were split into two main teams to execute effectively. These teams were Development and Marketing, while we all helped  on both parts of this project, we had people focus mainly on one or the other.
    <ol>
      <li>Deveopment:</li>
      <br>The development team consisted of Trankley, Tate, William, and Jimmy. This group was in charge of the physical development of the prototypes and the coding of the device itself. This team would meet to experiment with new hardware ideas that would improve the overall performance of the device while minimizing the cost to keep it under that $50 price point.<br><br>
      <li>Marketing</li>
      <br>The marketing team consisted of Jonathan and Kevin. This group would meet with Leo and discuss the strategy for the Kickstarter. They also would go to engineering conventions such as Texas BEST, to show them the device and get feedback from middle school and high school students.<br>
    </ol>
    <br>Even though we were split into these groups, it is important to note that all group members contributed significantly to both sides of the project.
  </ol>
  <li>Decision Analysis</li>
  <ol>
    <li>Solution Alternatives</li>
    <ul>
      <li>A device that functions similarly to the Hover DR1 could be created using a remote 
        control car. However, the decision to use a hoverboard was based on the concept that
        many people have hoverboards laying around their house that they do not use anymore, 
        and that hoverboards have a “cool” factor that gets people interested.</li>
      <li>Again, a device that could compare to the Hover DR1 could be created using remote 
        controls based on radio frequencies, rather than audible sound, however, the decision
        to make it operate solely on sound would add uniqueness and the ability for the
        hoverboard to dance to music in theory.</li>
      <li>Designing and using a custom PCB to contain our device on one board was considered.
        This would allow the Hover DR1 to have a significantly smaller form and be simpler to
        install. The decision to use premade devices, such as the arduino and motor 
        controller was made based on the modular nature of the device. We wanted the device 
        to be approachable by anyone who wanted to add their own modules or functions to it,
        this adds to the educational aspect of the project.</li>
      <li>Another device that was considered to be used as our main board is a Teensy USB 
        development board. This is much smaller than the Arduino Uno but lacks the same 
        modularity and accessibility that our educational platform demands. </li>
    </ul>

  </ol>
</ol>
