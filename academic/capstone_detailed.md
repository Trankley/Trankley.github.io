<h1>Detailed Hover DR1 Documentation</h1>

<h3>Reactive Audio Hoverboard</h3>

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

<h2>About</h2>
This documentation contains the contents of the final-deliverable my team presented for our Capstone Design project. We placed <a href="https://www.linkedin.com/posts/eceutdallas_youbelonghere-utd-stem-ugcPost-7154169550811398144-j8RZ?utm_source=share&utm_medium=member_desktop">1st place</a> in the ECE department competeing against fellow CE/EE majors at the University of Texas at Dallas.

<h2>Team and Team Structure</h2>
<ul>
  <li><b>Trankley Mahler</b>: Project Lead</li>
  <li><b>Tate Froh</b>: Head of Chassis Design</li>
  <li><b>Kevin Mikhaiel</b>: Point of Contact</li>
  <li><b>William Lim</b>: Embedded Systems, Audio Processing </li>
  <li><b>Jimmy Tran</b>: Motor Controls</li>
  <li><b>Jonathan Abshiro</b>: Head of fundraising</li>
</ul>

<h2>Problem Statement</h2>

The Hover DR1 was developed to solve the challenge of making STEM education engaging and accessible for students. Traditional teaching methods often struggle to capture attention or provide practical applications for core engineering and computer science concepts. The audio-reactive hoverboard bridges this gap by transforming abstract principles into a tangible, interactive experience that allows students to customize and control settings directly. It fosters creativity and teamwork through collaborative experimentation, making it easier for students to grasp difficult concepts while having fun. By providing a hands-on platform that turns theory into practice, the Hover DR1 inspires the next generation of engineers and scientists through an accessible, immersive learning environment.

<h2>Design Constraints</h2>

