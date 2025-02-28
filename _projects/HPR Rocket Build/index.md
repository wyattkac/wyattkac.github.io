---
layout: post
title: HPR Rocket Build
description: 
    Designing an HPR rocket requires developing an airframe that is strong, aerodynamic, and stable. To ensure high reliability, an avionics bay must be constructed with at least two different deployment mechanisms.
skills: 
  - KiCad
  - C++

main-image: /L2.jpg
---

---

## Introduction  

High power rocketry (HPR) is a hobby where enthusiasts design, build, and test advanced rockets. Due to the high propellant quantities used, certification is required. There are three certification levels:  
- L1: Motors up to 640 Newton-seconds (Ns)  
- L2: Motors up to 5120 Ns  
- L3: Motors exceeding 5120 Ns  

## L1 Certification  

For my L1, I built a [Wildman Journey 75](https://wildmanrocketry.com/products/journey-75), a fiberglass rocket known for its simplicity, durability, and included Rocksim design file for easier simulation. I successfully flew the rocket and earned my L1 certification on the first attempt.  

## L2 Certification  

### Airframe  

For my L2, I modified the Journey 75 I used for my L1 to save money. Since this rocket would use a larger motor, I needed to add an avionics bay for dual deployment recovery. The increased weight from the avionics and larger motor shifted the center of mass. Using OpenRocket, I determined that adding a 2-foot section would maintain proper stability. I modified the Rocksim file and assembled the airframe before starting work on the avionics bay.  

### Avionics  

I needed two independent deployment methods to ensure redundancy. I chose the Missile Works RRC3 for its affordability and proven reliability. Initially, I planned to use a custom-built flight computer for the second deployment method. However, since it remains untested, I decided to fly it as a payload instead. This allows me to collect flight data, helping validate its performance before integrating it into future recovery systems. The rocket is nearly complete, and I expect to launch within the next couple of months, weather permitting.  

#### Why Build a Custom Flight Computer  

I chose to design my own flight computer both to enhance functionality and to gain hands-on experience. Typical COTS avionics rely solely on a barometric pressure sensor. My design integrates a barometric pressure sensor, GPS, and accelerometer with a Kalman Filter for sensor fusion. My avionics system records raw flight data, enabling post-flight analysis to refine future designs. This project provides hands-on experience in PCB design and C++ programming, skills valuable for both industry and future personal projects.  
