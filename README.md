# Self_Balance_Robot_Project_SafiSoft
Start
How are you all doing? I'm Safi from SafiSoft, and I'm here today to walk you through the process of building a self-balancing robot with Arduino Nano and controlling it with our custom Java native Android app.

PID
Before we begin building our robot, we must first explore the amazing technology that will be used in this project.
the PID Controller, also known as the Proportional Integral Derivative
The PID Controller determines how much and how quickly correction is applied by varying the amount of P,I, and D action, which is then added together to produce the controller output signal.
The PID controller is in charge of ensuring that the process stays as close to the desired value as possible despite various interruptions.

Go Back
Go back to our robot project after this quick hint about PID . We have two sections in this project, one of which is the robot head. I made this robot head to make the robot more interactive, but you can skip this part of the project because it is not important in the self balance robot project.

Components
Robot head
Now I'll describe the components that we'll need to build the robot head, but first I'll explain how it works and what functions it has.
The robot head detects the presence of an object using ultrasonic sensors on the right and left sides of the robot. If the sensor detects an object on the left or right side, it sends a signal to the Arduino controller, which moves the servo motor that holds the robot head to the Object direction.
Simultaneously, the arduino controller will send a signal to the Tow led matrix that is playing the role of the robot's eyes to change, causing the robot to look in the same direction as the object.
On the Github link, you will find the schematic and instructions for wiring all of the components together, as well as the robot head design and, of course, the robot head code.
Robot Body Self Balance
Now is the time to discuss the most important sections of this project: the self-balancing robot body and the components.
The brain of this project will be an Arduino Nano, but you can use an Arduino Uno if you prefer.
Tow DC geared motors with wheels, which we will of course use to control the robot's movement.
We will use the L298N DC motor driver to control the DC motors.
The MPU6050 gyroscope sensor is in charge of sending the robot tilt value to the Arduino controller.
We will use the HC-05 Bluetooth module to communicate with the Android App in order to receive commands and send responses.
A battery is required as a power source, but here's a little trick: you can use a power bank as a power source in this project and everything will be fine, but make sure it has at least a 5V and 2A output that will be sufficient for all components.
Because the robot body is so important, you should make it as light as possible while also ensuring proper weight distribution.
On the Github link, you will find the schematic and instructions for wiring all of the components together and of course, the self balance code
Self Balance code
Now let's take a quick look at the Self Balance code.
Include libraries can be found in the first 5 lines. Before you verify the code, make sure to include those libraries in the project. You can find all of the files and libraries you need at the Github link.
The most important part of the code is from line 48 to line 59 because this is where you can set the PID values that correspond with your robot's design and weight. You will spend a lot of time changing those numbers to get the right value. Don't give up; you'll get it.
You must set the original set point of the robot body at line 81. You can get this value by manually balancing the robot and opening the serial monitor. Don't forget to disconnect the DC motors wires to stop the robot from moving.
The Bluetooth control function can be found on line 222. When you send a command from the Android app, you can change those values to control the robot's movement direction.
Everything else you need to know about the code can be found in the Docemontation section of the GetHub link.

Android App
Let's talk about the Android app now. At the start of this project, I intended to create a small and simple app to control my robot, but since I am already an android developer, I found myself creating a more complete and comprehensive app because why not? This app will work perfectly with our robot project and you can use it for any and all projects that use a bluetooth module with Arduino to control whatever you want.
This ROBOBOY App has three ways to communicate with the Arduino Bluetooth module: voice command, rotation command, and button command.
Buttons
With the buttons command, you have four direction keys and one for the centre position, as well as six keys with press and release commands for each button, for a total of 11 keys and 22 commands, or you can simply use the terminal at any time.
Rotation
It's amazing how you can rotate your phone 360 degrees in both directions and send 18 commands at one command every 20 degrees. I don't believe it exists in any other app.
End
I hope you learned something from this video, and I want you to know that everything in this project is open source, and you can use it however you want, with the exception of the native java android app, which you can download for free from the Google Play Store, but if you want the native source code, you must contact me; you can find my email address in the description box, and don't forget to like this video and subscribe to SafiSoft Youtube Channel. have a nice code and a good bay.
