# About

I am a Senior Designer with a background in complex engineering projects across various industries, including semiconductor technology, robotics, and heavy machinery. Currently, at Capgemini Engineering, I lead the development of a robotic arm for the innovative Arvatar Project. This initiative focuses on remote-controlled robotics, leveraging 3D printing and cycloidal drive mechanisms to maximize torque and efficiency in a lightweight design.

 Prior to this, I held key roles at ASML, where he contributed to wafer stage cooling unit concepts and transport tool solutions for EUV lithography machines, ensuring precision and durability for equipment transporting modules weighing up to 30 tons. My expertise in mechanical design extends over 34 years, with projects ranging from transport tools and robotic systems to complex prototypes for international clients.

 I am proficient in industry-standard CAD tools such as NX, Fusion360, and Inventor, and I have a track record in structural design, FEM calculations, and prototype testing. His educational foundation in Mechanical Engineering from HTS WTB(BSc) Breda.

Outside of work, I enjoys fitness, fencing, and creating 3D-printed models, alongside hands-on projects like telescope construction.


# 1.Arvatar project

Arvatar Project Summary

Arvatar is an innovation project focused on developing a remotely controlled robotic system. It is a spin-off from an earlier project that aimed to build a rover with an integrated robotic arm. Due to limited manpower, that project was never fully realized.

The current version of Arvatar takes a more focused approach, concentrating solely on the development of a robotic arm. The arm will be constructed using 3D-printed components and low-cost stepper motors to keep the design affordable and accessible.

To address the torque limitations of stepper motors, each joint of the arm will incorporate cycloidal drives, enabling it to lift objects weighing between 0.5 and 2 kg. The design aims to maintain full functionality even at a reach of over 1 meter, making the system practical for a wide range of remote manipulation tasks.


<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/4f23e76be507385357aeccc5363b5b43af4e9b93/1720725839099.jpeg?raw=true" width="50%">

Fig.1 concept of rover with robotic arm




# 2.Specs of the robot arm

The specs for the robot arm are fairly simply.
The robot arm should be build out of cheap 3D printed material(pla or ABS).
The should be build consiting out of cheap cloed loop stepper motors.
The robot arm Should be strong enough to pick up between 0.5 and 2 kg.
The robot arm should concsist out of actuators with a minimum backslash.
The robot arm should be around 1.5 to 2 m long.
The robot arm should controlled with haptic gloves or toggles.


# 2.Conceptual design

I am very familair with the V-shape model that is used by module architect within asml,applied this many times myself whena transport tool was designed
I designed 3 concepts with rufly the same dimensions.
From these 3 concepts I selected what I thought was the best one and started to calculate the torque in each actuator.

<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/949067bd4e9d4df3c4edeb5e1cae1387a92257ab/1726081868763.jpg?raw=true" width="50%">

Fig 2.Concept 1 robotic arm


<img src="https://github.com/jurgen975/Robotics.portfolio.jeisinga/blob/949067bd4e9d4df3c4edeb5e1cae1387a92257ab/1726081905612.jpg?raw=true" width="50%">


Fig 3. Concept 2 robotic arm


# 3.Design and building of the the first test cycliodal drive

Because the design was made in fusion 360 I could use a app thats calles cycliodal drive maker else it would be almost impossible the the design the cycliodal drives that where used.
I started with the design of a prototype cycliodal drive to validate if the disks that where designed with cycliodal drive maker would work.
I build the prototype cycliodal drive but i came apperent to me that that something in the design had gone wrong because it was not working the cycliodal drives where stuck.
So i designed it again with a excenter of 2 mm and i also found out that you can simulated the movement of the cycliodal dive.
I redesigned protype cycliodal drive and printed it again then put all the parts together again and it was working perfectly.
I also wanted to test it with using a arduino but i was not sure hoe much time i had this project to me it was enought that prototype was working hence i continued with the design of the arm.




https://github.com/user-attachments/assets/4130cd9a-da22-4778-a9e9-22f2ee336a4f

Fig 4. Motion link study cycliodal drive

Why a cycliodal drive?
How a Cycloidal Drive Works
A cycloidal drive is a high-torque, low-backlash gear system often used in robotics. It converts high-speed motor input into low-speed, high-torque output through a unique motion.

⚙️ Key Parts
Input shaft with an eccentric cam

Cycloidal disc with lobes

Fixed outer ring with pins

Output rollers connected to the shaft

🚀 How It Works
The motor spins the input shaft.

The eccentric cam makes the cycloidal disc "wobble" (orbit).

The lobed disc engages with more pins than it has lobes (e.g. 20 lobes, 21 pins).

This causes the disc to slowly rotate backwards.

Output rollers capture this motion and rotate the output shaft at reduced speed.






