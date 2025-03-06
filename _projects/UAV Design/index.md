---
layout: post
title: Ship-Launched UAV Design
description: 
    Developing a UAV involves determining design criteria, creating and simulating a detailed computer model, and building a prototype for testing.
skills: 
  - Solidworks
  - FDM
  - CNC
  - MS Office (Excel, Word, PowerPoint)

main-image: /TrafficCone.png
---

---

## Introduction  

As part of an eight-person team, I led the control system design and analysis and played a key role in manufacturing a UAV for a two-semester capstone project. Our team placed second overall, with our main disadvantage being a slightly shorter flight time due to prioritizing weight savings over a larger battery.  

### Mission Requirements  

We were tasked with designing an sUAS with solar recharge capabilities that could launch from a 10-foot ramp, fly for at least 45 minutes, and collect weather data. The aircraft had to be under 10 lbs, achieve an optimal cruise velocity of 30 knots, and break down into components under 50 inches for transport. Our team also set additional goals, such as toolless assembly and a factor of safety of at least 2.  

## Design  

{% include image-gallery.html images="https://raw.githubusercontent.com/wyattkac/wyattkac.github.io/refs/heads/main/_projects/UAV%20Design/Drawing.png, https://raw.githubusercontent.com/wyattkac/wyattkac.github.io/refs/heads/main/_projects/UAV%20Design/CAD.png" height="400" %} The final design  

Our first semester was spent designing the aircraft. We chose a conventional fixed-wing design for its simplicity and ease of manufacturing. We simulated airfoils using XFLR5 and chose an airfoil with the highest L/D at cruise speed, sizing the wing based on the estimated aircraft weight. We optimized the fuselage size to accommodate the payload and avionics while maintaining a simple shape for easier manufacturing. The fuselage also had an aerodynamic nose and tail cone designed using CFD to minimize drag. The tail dimensions were determined using tail sizing coefficients, and stability was validated through CFD analysis. We went with a two-motor design so that we would have enough thrust to get off of the ten-foot ramp, but still have a high enough efficiency at cruise that we could fly for the required amount of time. The final aircraft consisted of four parts, each sized to stay within the fifty-inch length limit. The outer wings attached with ferrules and magnets, and the tail attached with a ferrule and a pin. These attachment points allowed for tool-free assembly. The final design incorporated carbon fiber (CF) spars for the wings and tail, foam aerodynamic surfaces, and a wooden fuselage. These materials ensured the aircraft would be lightweight, cost-effective, and easy to manufacture. At the end of the first semester, we had a design review from which only minor changes, such as switching which fasteners to use, were requested.  

## Build  

{% include image-gallery.html images="https://github.com/wyattkac/wyattkac.github.io/blob/main/_projects/UAV%20Design/TrafficCone.png?raw=true" height="400" %} A promotional image of our prototype  

The fuselage was laser-cut from plywood and glued together, simplifying manufacturing compared to a composite airframe. CF was chosen for the spars and tail boom due to its high rigidity and low weight. Hot-wire-cut blue foam was chosen for the aerodynamic shapes due to its light weight, ease of manufacture, and low cost. We used 3D printed jigs to cut the holes in the proper places, increasing precision and lowering production time. The nacelles were 3D printed from lightweight PLA, since 3D printing allowed easy manufacture of the complex shapes, and the material and design were modified to minimize weight while still maintaining strength. Most wiring was embedded into the foam and tested before applying monocoat to cover the airframe.  

## Testing  

{% include image-gallery.html images="https://raw.githubusercontent.com/wyattkac/wyattkac.github.io/refs/heads/main/_projects/UAV%20Design/Testing.jpg" height="400" %} The prototype undergoing testing  

The prototype aircraft was tested at the local model airfield and passed all required flight tests. The aircraft remained stable throughout testing, and the pilots noted that it was one of the easiest to fly, requiring only minor trimming. The flight time was shorter than calculated; however, our team anticipated this and oversized the battery accordingly, ensuring we met the flight time requirements. The only unverified requirement was maximum velocity, as time and weather constraints prevented a full-speed test. Flight data from previous tests recorded an airspeed of 38 knots, and additional testing would likely have confirmed a top speed of 40 knots.  
