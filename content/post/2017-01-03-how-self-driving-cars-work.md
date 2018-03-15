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

Architecture of Self-Driving Cars
<img src="/sdc/udacity-av-subsystems.png" height=400 width=600 />

(pic credit: Udacity)

# Sensors

The sensor subsystem consists of various hardware sensors that gather data about the environment. These include Radar, LiDAR, GPS, Camera, and others. 

<img src="/sdc/sdc-sensors.png" height=300 width=400 />

(pic credit: Lex Fridman)

### Camera

Camera (image sensor) is perhaps the most important sensor. Typical AVs will have both front-facing and rear-facing cameras, often multiple instances of these, and might also have side-facing cameras. Cameras are used to "see" things around the AV -- roads, other vehicles, pedestrians, bikes, etc. 

Cameras have high resolution, are cheap (hence multiple units can be easily installed), can collect lot of data, therefore are useful for _deep learning_. 

However, trouble with cameras is they are:

- poor with depth perception - hence multiple sensors may be needed to stitch together to give a perception of depth
- not good in extreme weather - they essentially useless under inclement weather

### Radar

Radars are the most common automotive sensors for object tracking and detection. They are cheap, do well in poor weather as well, but have low resolution, though at 100-150m range.

### Lidar

Lidar (laser detector) works on the same principle as radars do, except they emit lasers at a high frequency (50-100 times/second). They offer extremely accurate depth information, a full 360 degree _view_, and have higher resolution than radars. But lidars are also extremely expensive. Typical range of lidars is ~150 meters. Lidar data is typically a _point cloud_ of information.

Lidar Point Cloud
<img src="/sdc/velo-lidar-cloud.png" width=600 height=300 /> <br />
[Source](http://velodynelidar.com/lidar/hdlpressroom/pdf/Articles/Learning%20a%20Real-Time%203D%20Point%20Cloud%20Obstacle%20Discriminator%20via%20Bootstrapping.pdf)

### GPS

GPS sensors are the common positioning sensors that give latitude, longitude (and altitude, where available) information. Since the resolution of GPS data is of the range of a few feet (10ft or 3 meters or more), vehicles typically use this information for long range planning rather than for short range.

### Others

Other sensors typically used are _ultrasonic Sonars_, which provide proximity sensing such as parking sensors, and IMUs (intertial measurement units) or gyroscopes that provide angular (pitch, yaw, roll) information.

# Perception 

The perception subsystem essentially consists of software components that take all the sensor data data, fuse them together into meaningful, structured information, via _Sensor Fusion_, and attempt to understand the environment around the AV. 

Broadly speaking, perception can be divided into two key components: **localization** and **detection**.

**Localization** This system uses data from mainly from GPS and maps (and possibly other sensors) to determine the vehicle's precise location. This forms the basis for other, later functions.

**Detection** This system uses data from camera, lidar, radar and other sensors for key functionality such as _lane detection_, _vehicle detection_, _traffic light detection and classification_, _obstacle detection_, _object detection and tracking_, _free space detection_, and more.


# Planning 

The planning subsystem takes information from the perception subsystem and uses it for long-range planning (such as route planning) and short-range planning (such as which turns to take). There are four key planning functions.

### Route Planning
The route planner performs high-level, coarse plans about the path the vehicle should take between two points on a map, e.g. the highways and roads to take. This is similar to the navigation system on most vehicles.

### Prediction
The prediction component predicts the behavior of _other vehicles, obstacles, pedestrians_ on the road in the vicinity of the AV. It uses probabilistic models to make educated guesses about their next positions and future trajectories. All this is done so that the AV can safely maneuver itself around themm

### Behavior Planning
The behavior planner then uses information from the predictor, and sensor fusion data, to plan its own behavior, such as keeping in the existing lane, or to change lanes (to the right/left), or brake at traffic light, or accelerate as needed.

### Trajectory Planning
The trajectory planner takes the behavior planner's immediate planned behavior, and generates multiple (dozens or hundreds) trajectories, all the while while keeping track of user comfort (e.g. smooth acceleration/decelration, no sudden jerky movements), road rules (e.g. speed limits, etc.), vehicle dynamics (e.g. body weight, load, etc.), and determines the exact trajectory to take. This trajectory is passed on to the control subsystem to execute as a set of commands.

# Control

The control subsystem is the final system, which takes commands from the planner, and actually executes them - via acceleration/deceleration (i.e. throttle), braking, or steering. It ensures that the vehicle follows the trajectory it receives from the planning subsystem.



