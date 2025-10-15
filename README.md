# About

I am a Senior Designer with a background in complex engineering projects across various industries, including semiconductor technology, robotics, and heavy machinery. Currently, at Capgemini Engineering, I have lead the development of a robotic arm for the innovative Avatar Project. This initiative focus on 3D printing and cycloidal drive mechanisms to maximize torque and efficiency in a lightweight design.


Avatar robotics is the field of developing remotely operated robotic systems that act as a physical extension of a human, allowing the operator to see, hear, move, and interact with a distant environment in real time—often enhanced with immersive technologies like VR, AR, haptic feedback, and motion capture, so the experience feels as if the operator is physically present in the robot’s location.


It’s essentially telepresence with a body—but a body that can work in hazardous, remote, or inaccessible places.
However halfway true the devolment of this arm the project was canceled.


## About me
 Prior to this, I held key roles at ASML, where he contributed to wafer stage cooling unit concepts and transport tool solutions for EUV lithography machines, ensuring precision and durability for equipment transporting modules weighing up to 30 tons. My expertise in mechanical design extends over 34 years, with projects ranging from transport tools and robotic systems to complex prototypes for international clients.

 I am proficient in industry-standard CAD tools such as NX, Fusion360, and Inventor, and I have a track record in structural design, FEM calculations, and prototype testing. His educational foundation in Mechanical Engineering from HTS WTB(BSc) Breda.

Outside of work, I enjoys fitness, fencing, and creating 3D-printed models, alongside hands-on projects like telescope construction.


# 1.Avatar project

## Avatar Project Overview

Avatar is an innovation initiative focused on developing a remotely controlled robotic arm. It is a spin-off from an earlier project that aimed to create a full rover with an integrated robotic arm. However, due to limited resources, the original concept was never fully completed.

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


# 3.Conceptual design

I am very familair with the V-shape model that is used by module architect within asml,applied this many times myself whena transport tool was designed
I designed 3 concepts with rufly the same dimensions.
From these 3 concepts I selected what I thought was the best one and started to calculate the torque in each actuator.

<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/949067bd4e9d4df3c4edeb5e1cae1387a92257ab/1726081868763.jpg?raw=true" width="50%">

Fig 2.Concept 1 robotic arm

<img src="https://github.com/user-attachments/assets/15bef3d5-14c3-4381-bdb7-14b49f2b4f57" width="40%">

Fig 3.Concept 1 Isometric view Concept 1


<img src="https://github.com/user-attachments/assets/46a765af-63a9-4192-8b40-34f643c232e8" width="50%">


Fi 4.Isomtric view concept 1A

<img src="https://github.com/user-attachments/assets/3177454e-ddc8-4370-958f-e988ae604e2a" width="60%">


Fig 5.Isometric view concept 1 B

<img src="https://github.com/user-attachments/assets/a9ee5799-15a2-44d3-8bd4-dd58db180ff9" width="50%">

Fig 6. Concept 2 robotic arm

<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/949067bd4e9d4df3c4edeb5e1cae1387a92257ab/1726081905612.jpg?raw=true" width="50%">


Fig 7. Isometric view concept 2



<img src="https://github.com/user-attachments/assets/d814da55-9c11-4155-ac90-d8f4f311e1f7" width="50%">

Fig 8. Concept 3 robotic arm


<img src="https://github.com/user-attachments/assets/f10e2a49-f859-4eac-9361-72ef05b8d224" width="50%">


Fig 9. Concept 3 Isometric view robotic arm



# 4.Prelimenairy design review Concept 1&2&3

Dimensions for all concept are basically the same,i can change them because i use a excel sheet to play with the weights and dimensions.

##concept 1

+ Strait forward actuators are in line with eachother.
+ Depending on how i will connect the actuators with eachother,meaning a arm on one (concept 1B) side or more a fork like arm (Concept 1A)this concept looks a safe option 
+ Conservative concept
  
##Concept 2
+ Shorter arm at the tip but of this concept which means less bulky actuators
- Not able to validate how strong i have to make this excentric design 

##Concept 3
- To complex at this moment
- Excentric design which looks attracive but i dont have a FEM calculation tool to make sure its strong ebough

##Conclusion
Concept 1 looks the best ,later in the design i have to make a desicion if i want to use a arm on one side of go for the fork arm design



# 5.Design and building of the the first test cycliodal drive

Since the design was created in Fusion 360, I took advantage of an app called Cycloidal Drive Maker—an essential tool, as manually designing the cycloidal profiles would have been extremely complex and time-consuming.

I began by designing a prototype cycloidal drive to validate whether the generated disks from the tool would function as expected. After printing and assembling the first prototype, I quickly realized something was wrong: the drive was stuck and not rotating properly.

Upon further investigation, I identified a design flaw and revised the model, this time introducing a 2 mm eccentricity. I also discovered that the movement of the cycloidal drive could be simulated within Fusion 360, which helped me better understand and optimize the mechanism.

With the updated parameters, I reprinted the prototype, assembled the parts again, and this time the drive worked perfectly. I had considered testing it further using an Arduino for motion control, but due to limited time, I decided that validating the mechanical functionality was sufficient. With the working prototype in hand, I moved forward with designing the rest of the robotic arm.


https://github.com/user-attachments/assets/385b46bd-afdb-4a00-a8de-3286c1ac143f

Fig 10. Simulation cycliodal drive


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

Fig 11.Example calculation cycliodal drive

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

Fig 12.Example what the inside of a cycliodal drive looks like



# 6.Designing the test cycliodal drive

Designing and putting the design together i noticed that the disks didnt want to move,the teeth where also to high.So redesigned the actuator with a excenter 2 mm instad of 3 mm.


<img src="https://github.com/user-attachments/assets/dfc64668-49e9-40fc-9171-572d2105655e" width="50%">

Fig 13.Main parts cycliodal drive 

<img src="https://github.com/user-attachments/assets/26e5ef52-fad0-4e96-bf54-1770b757ffd7" width="50%">

Fig 14.Assembled cycliodal drive

<img src="https://github.com/user-attachments/assets/f37fb6e8-27d1-466f-8f21-688361ae4835" width="50%">


Fig .16 Picture test cycliodal drive


# 7.Design robotic arm

If we keep out mass inertia it s a very simple calcultion however it requires allot weight assumptions.In basic its a bending moment calculation.
If you want to design a robotic arm you want to prevent that the arm crashes if it is completly horizontal.
You start with the object the arm is holding and asume the weight of the gripper and the arm that is connected to it.
The next step is to ad the asumpted weight of the actuator and then the next arm and so on.
The next actuator needs to be more powerful to keep the complet mass in the air.
Basically you make a hand calculation in excel,excel offers the flexibility change dimensions asumpted weights so that is why its a excellent tool.


<img width="1002" height="667" alt="Image" src="https://github.com/user-attachments/assets/ed5147d6-4959-4172-8af9-844766db294a" />

Fig.17 Example calculation concept 1

# 8.Detail design
In this chapter i will show some design details of the robot arm.As stated previously i had no Fem analysis tool to me disposal so arm is probably a little bit over demensioned

<img src="https://github.com/user-attachments/assets/0e8717ec-45fc-40cb-8202-f9e677f1d54b" width="50%">

Fig .18 Isometric view robot arm 1


<img src="https://github.com/user-attachments/assets/5c414358-cd3b-4f00-8e10-6edb953b95b5" width="50%">

Fir.19 Isometric view robot arm 1

# 9.Sub system breakdown


## 9.1 short description robotic arm

## 10.Detailed description

## 10.1 function description and requirements

## 10.1 Mechanical breakdown robotic parts

The robot arm contains the following main parts


<img src="https://github.com/user-attachments/assets/0e8717ec-45fc-40cb-8202-f9e677f1d54b" width="50%">
<link rel="stylesheet" href="https://unpkg.com/balloon-css/balloon.min.css">

<button aria-label="This is a tooltip!" data-balloon-pos="up">Hover me!</button>

Fig .20 Isometric view robot arm 1

## 11. Concept and design gripper

## 11.1 Specs gripper

### 11.11 Materials:

Constructed from affordable 3D printed materials (preferably PLA or ABS).


### 11.12. Actuation:

The with of the fripper should be around 70 mm or wider

### 11.13. Payload Capacity:

The arm should be capable of lifting objects between 0.5 kg and 2 kg.

### 11.14. Servo:
The servo should be a cheap dynamixel sero


### 11.2 Design gripper 1(linked motion concept)

Concept of a robot gripper using watt's linkage.
A Watt's linkage is a type of mechanical linkage invented by James Watt in which the central moving point of the linkage is constrained to travel a nearly straight path. Watt's described the linkage in his patent specification of 1784 for the Watt steam engine.


https://github.com/user-attachments/assets/9dd68d49-2878-4e4b-aa79-ac6d7ac4ef8b

Fig. 20 Watt'slinkage concept

https://github.com/user-attachments/assets/5a6c02ba-0414-4e3a-beb3-4614a49d757a

Fig. 21 Detail design of the Watt's linkage concept

Validating gripper 1:

+interresting construction where a rotating movement is translate into a rotating movement
-Complex rob mechanisme
-Complex rod mechanisme to put together
-Rod mechanism to thin not strong enough to hold 2 kg

Conclusion:initial i had allot of trust in this design, its a very ellegant design but this design is simply not strong enough

### 11 .3 Design Gripper 2
This is a more complex design where i use a teeth belly and several rollers make this design possible

<img src="https://github.com/user-attachments/assets/b0a10f32-6bb1-4b08-ae71-41240b69c768" style="width:50%;" />

<img src="https://github.com/user-attachments/assets/f084d6e4-8ddd-46fe-94fd-e01ff84b33e3" style="width:50%;" />

Fig. 22 Isometric view Gripper 2


I have a little bit trust in this design i still have to assemble it but at this moment this design looks good

Validating gripper 2
+Robust
+Design is straight forward
-Teeth belly goes straight true basis gripper jaws
-Not clear yet if it is easy to assemble


### 11.4 Design Gripper 3

<img src="https://github.com/user-attachments/assets/1c08f562-f09a-4771-8bc2-a34c0dabd6c8" style="width:50%;" />

Fig. 23  Isomtric view Gripper 2 motor is stickingout true one of the side pannels

Validating Gripper 3
+Straight forward design
+Simple
+minimum parts
-Not sure how strong this design will be

### 11.5 Conclusion

All these designes have there Plus and minus pionts
Fot time being i will progress with design of gripper 2,if its not working or not strong enough i have go back to drawing board

## 12. Quick connection


Because i want that its possible to connect diverend styles of grippers to the robot arm i started out investigating what a quick connection would look like
I got inspired by a cobra buckle ,the simplisity of the cobra buckle design is attractive but real life use will determain if this design is strong enough

<img src="https://github.com/user-attachments/assets/b8252a2c-76bd-4562-b8d1-c59c368930a3" style="width:50%;" />

Fig. 24  Isomtric view cobra buckle inspired design

<img src="https://github.com/user-attachments/assets/d818356e-51b6-4a9a-bc0f-586ceb663e0e" style="width:50%;" />

Fig. 25  View Quick connect cobra buckle inspired design

<img src="https://github.com/user-attachments/assets/fd5ea9cc-1941-4fb8-9e8d-a5bee9eaea62" style="width:50%;" />

<img src="https://github.com/user-attachments/assets/5a7df17f-ee65-44b4-8197-eea878051503" style="width:50%;" />

Fig. 26  Isometric view of robot arm with gripper 2

## 13 Concepts to make vision possible

## 14 Haptic Glove

The question is do i need a hand shaped size haptic glove for picking up objects or are toggles sufficient for what i need?

Short answer: ## It depends on what you need the gripper to do.
Toggles (buttons/switches/joysticks) are often perfectly fine for simple pick-and-place or single–degree open/close tasks. A hand-shaped glove (with finger tracking and/or force feedback) becomes worth it when you need dexterity, natural teleoperation, or better operator embodiment and situational awareness.



## 14.1 When toggles are enough

-Use simple toggles when most of these are true:

-Gripper only needs open / close (maybe a couple presets like half-close).

-Tasks are repetitive pick-and-place, bin picking, or coarse positioning.

-Speed, robustness, low cost and reliability matter more than finesse.

-Operators don’t need to feel or finely control individual fingers.

-You want a compact, easy-to-certify control interface (industrial settings).

-Advantages: cheap, robust, low training, easy safety integration, low latency.

-When a hand-shaped haptic glove is better

## 14.2 Choose a glove if any of these apply:

-You need independent finger control or in-hand manipulation (reorienting, rolling, pivoting).

-You want natural teleoperation — operators perform better when the control maps to their own hand motion.

-Tasks require graded force/pressure control or delicate handling (fragile objects).

-You need better situational awareness / embodiment (e.g., remote surgery, service robots, telepresence).

-You want to record human demonstrations for imitation learning.

-Advantages: intuitive control, higher dexterity, better operator acceptance for complex tasks.

## 14.3 Important distinctions about gloves

-Tracking-only gloves (flex sensors/IMUs/cameras): good for mapping finger positions to a multi-finger gripper. No force feedback — operator won’t “feel” contact.

-Haptic/force-feedback gloves or exoskeletons: can render contact forces (more complex, heavier, costly). Useful if you need force sensation or bilateral control.

-EMG gloves/sensors: can detect muscle intent — useful where motion tracking is hard but adds calibration complexity.

## 14.4 Practical hybrid options (often best)

Toggle + mode switch: simple toggles for gross motion + a glove or joystick mode for fine dexterity.

Preset grasps + a single degree trigger: provide 3–5 presets (pinch, wide, hook) selected with a button and refined with a single slider/rotary.

Thumb + index tracking only: cheaper partial glove that delivers most pinch-based control.

## 14.5 Control & mapping tips (regardless of interface)

-Use scaling: map large human motions to small gripper motions for precision.

-Provide deadbands and hysteresis to avoid jitter from sensors.

-Offer grip force limits and compliance (software impedance) for safety.

-Implement quick presets and one-button emergency stop.

-Keep latency < 50 ms for teleoperation feel (lower is better).

-Provide visual or audio feedback if there’s no haptic feedback.

## 14.6 Cost / complexity tradeoffs

-Toggles: low cost, easy to maintain, industrial-ready.

-Full haptic glove with force feedback: high cost, heavier, more maintenance, but much better for fine tasks and training/recording.

## 14.7 Recommendation (practical)

-If your gripper performs basic open/close or a few grasp types → start with toggles + presets. It’s simpler and often adequate.

-If you aim for dexterous manipulation, natural teleoperation, or demonstration collection for learning → invest in a glove (start with a tracking glove; add force feedback later if needed).

-Consider a hybrid: toggles for everyday ops and a glove mode for special tasks.

## 14.8 Conclusion
The gripper design could change,and i could ad a hand shaped design to the robot arm so for now and i will stick with the hand shaped designfor the reasons mentioned in chapter 14.2

## 15. Design haptic gloves

I will use a open source haptic glove design because i am out of my depth when it comes to electronics and designing a haptic glove.
The haptic glove designed by lucasVRTech gloves are a very good choice.

![Image](https://github.com/user-attachments/assets/e1257526-060a-4251-bac8-7dcaada4202b)

Fig. 27 Open source haptic glove

















