---
title: How Self-Driving Cars Work
author: Atul Acharya
date: '2017-01-03'
slug: how-self-driving-cars-work
categories:
  - Self Driving Car
tags:
  - Self Driving Car
  - Autonomous Systems
---

In this post, we will look at the architecture of Self-Driving Cars (SDC) -- or Autonomous Vehicles (AV), as they are alternatively called -- and the various sub-systems that make it work. 

## Architecture 

At a high level, AVs have four critical subsystems: Sensors, Perception, Planning, and Control. These subsystems act together to perceive the environment around the AV, detect drivable parts of the road, plan a route to destination, predict behavior of other cars or pedestrians around it, plan trajectories, and finally execute the motion: drive smoothly and safely. Let's see how these systems work.

<img src="/sdc/udacity-av-subsystems.png" height=300 width=500 />
Architecture of Self-Driving Cars (pic credit: Udacity)

# Sensors

The sensor subsystem consists of various hardware sensors that gather data about the environment. These include Radar, LiDAR, GPS, Camera, and others. 

<img src="/sdc/sdc-sensors.png" height=200 width=300 />

(pic credit: Lex Fridman)

### Camera

Camera (image sensor) is perhaps the most important sensor. Typical AVs will have both front-facing and rear-facing cameras, often multiple instances of these, and might also have side-facing cameras. Cameras are used to "see" things around the AV -- roads, other vehicles, pedestrians, bikes, etc. 

Cameras have high resolution, are cheap (hence multiple units can be easily installed), can collect lot of data, therefore are useful for _deep learning_. 

However, trouble with cameras is they are:

- poor with depth perception - hence multiple sensors may be needed to stitch together to give a perception of depth
- not good in extreme weather - they essentially useless under inclement weather

### Radar

Radar are most common automotive sensors for object tracking and detection. They are cheap, do well in poor weather as well, but have low resolution.

### Lidar

Lidar (laser detector) works on the same principle as radars do, except they emit lasers at a high frequency (50-100 times/second). They offer extremely accurate depth information, a full 360 degree _view_, and have higher resolution than radars. But lidars are also extremely expensive. Typical range of lidars is ~150 meters. Lidar data is typically a _point cloud_

Lidar Point Cloud
<img src="/sdc/velo-lidar-cloud.png" width=600 height=300 />
[Source](http://velodynelidar.com/lidar/hdlpressroom/pdf/Articles/Learning%20a%20Real-Time%203D%20Point%20Cloud%20Obstacle%20Discriminator%20via%20Bootstrapping.pdf)

### GPS

GPS sensors are the common positioning sensors that give latitude, longitude (and altitude, where available) information. Since the resolution of GPS data is of the range of a few feet (10ft or 3 meters or more), vehicles typically use this information for long range planning rather than for short range.

### Others

Other sensors typically used are _ultrasonic Sonars_, which provide proximity sensing such as parking sensors, and IMUs (intertial measurement units) or gyroscopes that provide angular (pitch, yaw, roll) information.

# Perception 

The perception subsystem essentially consists of software components that take all the sensor data data, fuses them together into meaningful information, hence _Sensor Fusion_, and attempts to understand the environment around the AV.


# Planning 

The planning subsystem takes information from the perception subsystem and uses it for long-range planning (such as route planning) and short-range planning (such as which turns to take).

# Control

The control subsystem is the final system, which takes commands from the planner, and actually executes them - via acceleration/deceleration (i.e. throttle), braking, or steering. It ensures that the vehicle follows the trajectory it receives from the planning subsystem.



