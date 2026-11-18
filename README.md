
# AI-Based Campus Waste Management System

## Overview

The **AI-Based Campus Waste Management System** is an intelligent robotic waste collection system developed to improve campus cleanliness through the integration of Artificial Intelligence, Computer Vision, Robotics, Embedded Systems, and IoT.

The system detects waste objects such as **bottles and wrappers** using a YOLOv8-based object detection model, calculates their positions in the camera frame, and guides a mobile robot toward the detected waste. The robot uses autonomous navigation, obstacle detection, and a robotic arm to collect waste and deposit it into a smart dustbin.

This project was completed as an academic final-year project and its research work was published in **IEEE**.

---

## Objectives

- Develop an AI-based system for real-time waste detection.
- Detect waste objects such as bottles and wrappers.
- Calculate the position of detected objects using computer vision.
- Enable autonomous robot navigation toward detected waste.
- Implement robotic arm-based pick-and-place operations.
- Integrate embedded systems for robot control.
- Monitor smart dustbin fill levels using IoT.
- Reduce manual intervention in waste collection.

---

## System Architecture

The system integrates the following components:

1. **Mobile Application** – Captures live camera frames and communicates with the processing server.
2. **AI-Based Detection** – Uses YOLOv8 to identify bottles and wrappers.
3. **Server-Side Processing** – Processes image frames and calculates the coordinates of detected waste.
4. **Bluetooth Communication** – Transmits detection coordinates to the Arduino Mega.
5. **Embedded Controller** – Controls robot navigation and robotic arm operations.
6. **Autonomous Robot** – Navigates toward waste using motor control and ultrasonic sensing.
7. **Robotic Arm** – Performs waste pickup and placement into the bin.
8. **IoT Smart Dustbin** – Monitors the bin's fill level.

---

## Working Principle

1. The mobile application captures live video using the smartphone camera.
2. Individual frames are transmitted to the server for processing.
3. The YOLOv8 model detects waste objects such as bottles and wrappers.
4. Bounding boxes are generated around detected objects.
5. The center coordinates of the detected bounding boxes are calculated.
6. The coordinates are transmitted to the mobile application.
7. The mobile application sends the information to the Arduino Mega through Bluetooth.
8. The Arduino Mega controls the robot's motors to navigate toward the waste.
9. Ultrasonic sensors assist with distance measurement and obstacle detection.
10. The robotic arm picks up the waste and deposits it into the smart dustbin.

---

## AI Model

The waste detection system was developed using **YOLOv8** from Ultralytics.

### Detection Classes

- Bottle
- Wrapper

### Dataset

A custom dataset was created and annotated using Roboflow.

| Dataset Split | Bottles | Wrappers | Total |
|---|---:|---:|---:|
| Training | 2,572 | 2,115 | 4,687 |
| Validation | 735 | 604 | 1,339 |
| Testing | 368 | 303 | 671 |
| **Total** | **3,675** | **3,022** | **6,697** |

### Model Training

Multiple YOLOv8 variants were trained and evaluated:

- YOLOv8s
- YOLOv8m
- YOLOv8l

Training was performed using Kaggle GPU resources with different image sizes, batch sizes, and learning rates.

### Best Model Performance

The best-performing configuration was:

| Parameter | Value |
|---|---|
| Model | YOLOv8l |
| Image Size | 960 × 960 |
| Batch Size | 4 |
| Learning Rate | 0.01 |
| mAP@0.5 | **89.8%** |
| Precision | **88.1%** |
| Recall | **86.1%** |

---

## Software Technologies

- Python
- YOLOv8
- Ultralytics
- OpenCV
- Flutter
- Dart
- FastAPI
- WebSocket
- Roboflow
- Kaggle
- ngrok

---

## Hardware Components

- Arduino Mega
- HC-05 Bluetooth Module
- Four Geared DC Motors
- Motor Driver
- Ultrasonic Sensor
- Robotic Arm
- Two Servo Motors
- 3D-Printed End Effector
- Steel Robot Chassis
- 12V Lithium-Ion Battery
- Smartphone Camera
- IoT-Enabled Smart Dustbin

---

## Embedded Systems and Robotics

The Arduino Mega acts as the central controller for the robot.

Its responsibilities include:

- Receiving waste coordinates through Bluetooth.
- Controlling the four geared DC motors.
- Implementing robot movement and navigation logic.
- Coordinating the robotic arm.
- Controlling servo motors for pick-and-place operations.
- Using ultrasonic sensing for distance measurement and obstacle detection.

The four motors are divided into two groups to control the robot's rotational and directional movement.

---

## Results

The developed system was tested in campus environments, including cafeteria areas and open yards.

The system successfully demonstrated:

- Real-time detection of bottles and wrappers.
- Bounding-box generation and waste coordinate calculation.
- Communication between the mobile application, server, and Arduino Mega.
- Autonomous robot movement toward detected waste.
- Obstacle detection using ultrasonic sensing.
- Waste pickup using a robotic arm.
- Placement of collected waste into the smart dustbin.

---

## Research Publication

This project was developed as an academic final-year project and the research work was published in IEEE.

**Research Paper Title:**

*Design and Testing of an AI-based Campus Waste Management System*

The research presents the integration of AI-based waste detection, autonomous robotic navigation, pick-and-place operations, and IoT-based smart dustbin monitoring.

The research paper is included in this repository for reference.

---

## Future Improvements

- Improve robotic arm flexibility with additional degrees of freedom.
- Expand the waste detection dataset to include more waste categories.
- Improve navigation accuracy using depth cameras or LiDAR.
- Implement advanced path planning.
- Explore multi-robot waste collection.
- Integrate cloud-based analytics for waste monitoring.
- Improve the system for deployment in larger environments.

---

## Repository Contents

- Research Paper
- Project Documentation
- Source Code
- AI Model Implementation
- Computer Vision Modules
- Robot Control Logic
- Embedded Systems Implementation

---

## Authors

**Vivek**

Mechatronics Engineering  
Mangalore Institute of Technology and Engineering (MITE)

Final-Year Academic Project

---

## Keywords

Artificial Intelligence, Waste Management, YOLOv8, Computer Vision, Robotics, Embedded Systems, Arduino, Autonomous Navigation, IoT, Smart Dustbin, Pick-and-Place Robot, Smart Cities
