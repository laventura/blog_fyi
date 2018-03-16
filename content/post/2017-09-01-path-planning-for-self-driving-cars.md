---
title: Path Planning for Self-Driving Cars - Bosch Challenge
author: Atul Acharya
date: '2017-09-01'
slug: path-planning-for-self-driving-cars
categories:
  - Self Driving Car
tags:
  - Self Driving Car
  - Autonomous Systems
  - Path Planning
  - Robotics
---

## Introduction

Late in summer 2017, Bosch, one of the leaders in automotive components, threw a challenge to Udacity learners.

<img src="/sdc/pp-bosch1.png" width=600 />

The aim of the challenge was to have a (simulated) car drive itself autonomously along a 7-mile highway loop, in traffic, without colliding with other vehicles on the road. The autonomous vehicle (called the _ego car_) should observe all the rules of the road:

- Drive at max speed 50 miles/hour
- Automatically accelerate/slow down, brake, as needed to avoid collisions
- Observe lane change rules - e.g. change lanes smoothly
- Should not cross into incoming traffic
- Max acceleration: 10 m/s^2 - to maintain passenger comfort
- Max jerk: 10 m/s^3 (rate of change of acceleration) - to maintain passenger comfort
- Drive at least ~5 miles without any _violations_

## Summary

My self-driving car successfully completed the [Bosch Path Planning challenge](https://www.udacity.com/bosch-challenge), and was one of the top 25 entries, from among hundreds of entries. 👍🚗🍾

[<img src="/sdc/pp-bosch2.png" width=600 />](https://www.youtube.com/watch?v=oVQDk5aBwvI&feature=youtu.be)
Here's the [Youtube video](https://www.youtube.com/watch?v=oVQDk5aBwvI&feature=youtu.be). Best way is to watch it at 2x speed.

## Approach