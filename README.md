# About

I am a Senior Designer with a background in complex engineering projects across various industries, including semiconductor technology, robotics, and heavy machinery. Currently, at Capgemini Engineering, I lead the development of a robotic arm for the innovative Arvatar Project. This initiative focuses on remote-controlled robotics, leveraging 3D printing and cycloidal drive mechanisms to maximize torque and efficiency in a lightweight design.

 Prior to this, I held key roles at ASML, where he contributed to wafer stage cooling unit concepts and transport tool solutions for EUV lithography machines, ensuring precision and durability for equipment transporting modules weighing up to 30 tons. My expertise in mechanical design extends over 34 years, with projects ranging from transport tools and robotic systems to complex prototypes for international clients.

 I am proficient in industry-standard CAD tools such as NX, Fusion360, and Inventor, and I have a track record in structural design, FEM calculations, and prototype testing. His educational foundation in Mechanical Engineering from HTS WTB(BSc) Breda.

Outside of work, I enjoys fitness, fencing, and creating 3D-printed models, alongside hands-on projects like telescope construction.


# 1.Arvatar project

## Arvatar Project Overview

Arvatar is an innovation initiative focused on developing a remotely controlled robotic arm. It is a spin-off from an earlier project that aimed to create a full rover with an integrated robotic arm. However, due to limited resources, the original concept was never fully completed.

The current version of Arvatar takes a more streamlined approach by concentrating exclusively on the robotic arm. The design prioritizes accessibility and affordability, utilizing 3D-printed components and low-cost closed-loop stepper motors.

To overcome the torque limitations typically associated with stepper motors, each joint is equipped with a cycloidal drive. This allows the arm to lift loads ranging from 0.5 to 2 kg, even at an extended reach of over 1 meter. The result is a practical and robust system well-suited for a variety of remote manipulation tasks.

<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/4f23e76be507385357aeccc5363b5b43af4e9b93/1720725839099.jpeg?raw=true" width="50%">

Fig.1 concept of rover with robotic arm




# 2.Specs of the robot arm

## Robot Arm Specifications

### 1. Structure & Materials:

Constructed from affordable 3D printed materials (preferably PLA or ABS).

Modular design for ease of printing, maintenance, and upgrades.

### 2. Actuation:

Equipped with budget-friendly closed-loop stepper motors to ensure positional feedback and improved control.

Actuators should exhibit minimal backlash to allow for precise and smooth motion.

### 3. Payload Capacity:

The arm should be capable of lifting objects between 0.5 kg and 2 kg.

### 4. Reach:

The total length of the robotic arm should be in the range of 1.5 to 2 meters, enabling extended reach for a variety of tasks.

### 5. Control Interface:

The robot arm should be operable via haptic gloves or joystick/toggle input, enabling intuitive and responsive control.

Would you like help drafting a concept design sketch or selecting suitable stepper motors and structural profiles for this build?


# 2.Conceptual design

I am very familair with the V-shape model that is used by module architect within asml,applied this many times myself whena transport tool was designed
I designed 3 concepts with rufly the same dimensions.
From these 3 concepts I selected what I thought was the best one and started to calculate the torque in each actuator.

<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/949067bd4e9d4df3c4edeb5e1cae1387a92257ab/1726081868763.jpg?raw=true" width="50%">

Fig 2.Concept 1 robotic arm


<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/949067bd4e9d4df3c4edeb5e1cae1387a92257ab/1726081905612.jpg?raw=true" width="50%">


Fig 3. Concept 2 robotic arm


# 3.Design and building of the the first test cycliodal drive

Since the design was created in Fusion 360, I took advantage of an app called Cycloidal Drive Maker—an essential tool, as manually designing the cycloidal profiles would have been extremely complex and time-consuming.

I began by designing a prototype cycloidal drive to validate whether the generated disks from the tool would function as expected. After printing and assembling the first prototype, I quickly realized something was wrong: the drive was stuck and not rotating properly.

Upon further investigation, I identified a design flaw and revised the model, this time introducing a 2 mm eccentricity. I also discovered that the movement of the cycloidal drive could be simulated within Fusion 360, which helped me better understand and optimize the mechanism.

With the updated parameters, I reprinted the prototype, assembled the parts again, and this time the drive worked perfectly. I had considered testing it further using an Arduino for motion control, but due to limited time, I decided that validating the mechanical functionality was sufficient. With the working prototype in hand, I moved forward with designing the rest of the robotic arm.



https://github.com/user-attachments/assets/e3d53fab-cc14-4aac-9171-1f78f3b8339a



Fig 4. Simulation cycliodal drive

# Why a cycliodal drive?

First of all i have looked at a view options but desided on a cycliodal drive because:

A cycloidal drive is a high-torque, low-backlash gear system often used in robotics. It converts high-speed motor input into low-speed, high-torque output through a unique motion.

# Key Parts
Input shaft with an eccentric cam

Cycloidal disc with lobes

Fixed outer ring with pins

Output rollers connected to the shaft

# How It Works
The motor spins the input shaft.

The eccentric cam makes the cycloidal disc "wobble" (orbit).

The lobed disc engages with more pins than it has lobes (e.g. 20 lobes, 21 pins).

This causes the disc to slowly rotate backwards.

Output rollers capture this motion and rotate the output shaft at reduced speed.

<img width="657" height="217" alt="Image" src="https://github.com/user-attachments/assets/f16e909e-68e4-43ca-890e-f990fa1c578f" />

Fig 5.Example calculation cycliodal drive

### Pros
High torque

Low backlash

Compact

Shock-resistant

### Cons
Complex design

Needs lubrication

Slight vibration


[https://github.com/user-attachments/assets/511e2779-7a20-463b-a285-b157359c101a](https://github.com/user-attachments/assets/e5a3a993-a326-40e4-997c-080fe3b2d893)

Fig 6.Example what the inside of a cycliodal drive looks like



# 4 Design robotic arm

If we keep out mass inertia it s a very simple calcultion however it requires allot weight assumptions.In basic its a bending moment calculation.
If you want to design a robotic arm you want to prevent that the arm crashes if it is completly horizontal.
You start with the object the arm is holding and asume the weight of the gripper and the arm that is connected to it.
The next step is to ad the asumpted weight of the actuator and then the next arm and so on.
The next actuator needs to be more powerful to keep the complet mass in the air.
Basically you make a hand calculation in excel,excel offers the flexibility change dimensions asumpted weights so that is why its a excellent tool.
















