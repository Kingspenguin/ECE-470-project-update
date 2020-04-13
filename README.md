# ECE-470-project-update
Group Members: Jianhan Ma (jianhan3) Boyang Zhou (Boyangz3)
This repository is for the ECE 470 Robotics Project. In this project we planned to simuate a "cleaner" robot whic will clean the desk by sorting multiple kinds of stuffs on a messy desk and placing them to their reset areas. The simulation will be based on Coppelia 4.0.0.

Project 1 Update:
1. We have succesfully implemented a simulation of a UR5 robot arm. As the robot arm needs to detect and verify different kinds of stuffs (e.g. pens, cups, books,etc), we fixed a kinect camera on the gripper.
2. We successfully make the robtarm move according to our command, and the camera works well.
3. The camera returns two images: One is the real world image, the other is the depth image of the RGB graph, which can relect the distance form the object to the camera.
3. For now the control of the robot arm is through the keyboard:
    Q/W: Rotation of Joint 1
    A/S: Rotation of Joint 2
    Z/X: Rotation of Joint 3
    E/R: Rotation of Joint 4
    D/F: Rotation of Joint 5
    C/V: Rotation of Joint 6
    Y/T: Open/Close of RG2 (gripper)
    P:Exit the program
    L:Reset 
    Space: Save the image obtained by the camera. Path: /saveImg
4. To run the program, lauch the remoteApi in Coppelia 4.0.0.by running update.ttt, and run the code in Update1.py
Project 2 Update:
1. We have implemented the algorithm to obtain the forward kinematics. Two dummies will be created based on the things we get.
2. To run the program, lauch the remoteApi in Coppelia 4.0.0.by running update.ttt, and run the code in Update2.py
 
Project 3 Update:
In this update, we make some small modules for our final project.
1.	Inverse Kinematics
We develop the inverse kinematics algorithm to calculate the theta list to get to the desired location (by the translation matrix) with the DH parameter of UR5
2.	Color block detection 
We develop a scene to try out the camera detection. We use a single visual sensor to catch picture of the environment and use the opencv library of python to filter out the green block and create an outline for that object.
3. Reconstruct the 3D axis location based on the depth graph precepted by the camera
In this update, we achieved the goal of deriving the location of certain pixels from the depth image that the camera embedded on the robot arm returns. This part serves as a support to the color detection mode. In our project, after the camera distinguish the next object that the robot arm needs to fetch by their colors, a depth image of this object is created. The location of this object is also determined by its depth image, so that the robot arm would know where to fetch this object.
