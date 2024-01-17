
# Overview: 

This document elaborates the hardware and software configurations for using Autoware for autonomous driving. Hence, it will serve as a guideline to select hardware and software components to build autonomous vehicles. However, this document is NOT prepared as neither step-by-step instructions nor Q&A books, which will be provided as a reference link if available. 

# Design Overview: 

![Meta Chart for LeoDrive RoboTaxi Design](LeoTaxi_Meta.png)
![Tech Chart for LeoDrive RoboTaxi Design](LeoTaxi_Tech.png)


# Who should read: 
One is interested in building autonomous cars for taxi service and looking for a place to start with. 

# References and Resources: 
- Complete LeoDrive RoboTaxi design documents: [link](https://leodrive.atlassian.net/wiki/spaces/MD/pages/97583105/Overview+of+Reference+Design)
- Feature list of LeoDrive RoboTaxi: [link](https://leodrive.atlassian.net/wiki/spaces/MD/pages/104071185/Autonomous+Driving+Feature+List)

# Contributors: [complete list](https://f1tenth.readthedocs.io/en/foxy_test/support/acknowledgment.html#contributors)
## Core Developers
- Mert Çolak

## Contributors
- (To be added.)

# Community Outreach
- (To be added.)

# Targeted Use Cases

| Use Cases: | Education | Racing | PoC | Open AD Kit | Commercial Services/Production |
|:--------: | :--------:| :---------: | :---------: |:---------: | :---------: |
|F1Tenth | <input type="checkbox" checked />  | <input type="checkbox" checked />  | <input type="checkbox" disabled  />  | <input type="checkbox" disabled  />  | <input type="checkbox" checked /> | 

# ODD

| ODD | Cargo | Bus | RoboTaxi | Low Speed (Utility) Vehicle | Delivery Robot |
|:--------: | :--------:| :---------: | :---------: |:---------: | :---------: |
| LeoDrive RoboTaxi | <input type="checkbox" disabled  />  | <input type="checkbox" disabled />  | <input type="checkbox" checked />  | <input type="checkbox" disabled  />  | <input type="checkbox" disabled  />  | 

# Automation Level:
| Automation Level | 0 | 1 | 2 | 3 | 4 | 5 |
|:--------: | :--------:| :---------: | :---------: |:---------: | :---------: | :---------: |
| LeoDrive RoboTaxi | <input type="checkbox" checked  />  |  <input type="checkbox" checked  />  | <input type="checkbox" checked />  | <input type="checkbox" checked  /> | <input type="checkbox" checked  />  | <input type="checkbox" disabled  />  | 


# System Architecture

The Robo-Taxi Reference Design is designed to offer efficient, safe, and convenient urban transportation solutions. The project enables passengers to hail a robotaxi via a mobile application, upon which the Fleet Management System dispatches an available autonomous vehicle to the passenger's location.

![LeoTaxi.png](LeoTaxi.png)

# Hardware Configuration
## Chassis:
-  Traxxas Slash 4x4 Premium: [link to purchase](https://www.amainhobbies.com/traxxas-slash-4x4-ultimate-rtr-4wd-short-course-truck-orange-tra68077-4-orng/p858530)
- VESC Speed Controllers: # VESC 6 MK III
  
![LeoTaxi_SysArchitecture.png](LeoTaxi_SysArchitecture.png)

## Sensors:
- Lidar: choose one
	- Hokuyo UTM-30LX
	- Hokuyo 10LX
- Camera (optional):
	- ZED 2
	- Intel Real Sense
  
![[LeoTaxi_Sensors.png]]

## Computing Platforms:
- NVIDIA Jetson Xavier NX
- USB Hub (4 ports)
- (DEPRECATED) NVIDIA Jetson TX2

![LeoTaxi_SysArchitecture.png](LeoTaxi_SysArchitecture.png)

# Software Configuration 
- Software on the car:
	- Operating System: Linux 20.04
	- ROS: [ROS2 galactic](https://docs.ros.org/en/galactic/Installation/Ubuntu-Install-Debians.html)
	- GPU Driver: nVidia: JetPack 5.1.1 (rev. 1)
	- [Autoware](https://github.com/autowarefoundation/autoware.git)
	- SLAM Toolbox to create and edit map: ros-galactic-slam-toolbox
- Tools: 
	- Simulator: [f1tenth simulator](https://f1tenth.readthedocs.io/en/foxy_test/going_forward/simulator/index.html)
	- VESC Tool for motor control: [link](https://vesc-project.com/vesc_tool)
	- Version Control tool: [vcstool](https://github.com/dirk-thomas/vcstool)

![LeoTaxi_Software.png](LeoTaxi_Software.png)
