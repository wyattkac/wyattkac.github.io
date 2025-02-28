---
layout: post
title: UAV Design
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

As part of an eight-person team, we worked over two semesters to design and build a drone for a simulated Navy contract. Our team placed second, mostly due to a slightly reduced flight time compared to the winning team. However, our aircraft was over a pound lighter than the winning team's, and with only a battery change, could have outperformed theirs in flight time.  

### Mission Requirements  

With a budget of five hundred dollars, we were tasked with designing an sUAS with solar recharge capabilities that would launch off a ten-foot ramp and gather weather data for at least forty-five minutes. The drone was required to have a maximum weight of 10 lbs, an optimal cruise velocity of 30 knots, and must disassemble into components no longer than fifty inches for storage. Our team decided that the drone should also have a toolless assembly and should be stable with a factor of safety of at least two.  

## Design  

{% include image-gallery.html images="Drawing.png, images/Drawing.png" height="400" %} The final design  

Our first semester was spent designing the aircraft. We chose a traditional design for its simplicity and ease of manufacturing. We chose the airfoil to maximize L/D at cruise speed, and sized the wing according to the approximate weight of the final aircraft. We optimized the fuselage size so that our payload and avionics would comfortably fit, and we went with a simple shape for ease of manufacturing. The tail sizing was based on tail sizing coefficients, and stability was checked using CFD. We went with a two-motor design so that we would have enough thrust to get off of the ten-foot ramp, but still have a high enough efficiency at cruise that we could fly for the required amount of time. The final aircraft consisted of four parts, each sized to stay within the fifty-inch length limit. The outer wings attached with ferrules and magnets, and the tail attached with a ferrule and a pin. These attachment points ensured the design would not require tools to assemble. The final design used carbon fiber (CF) wing and tail spars, foam aerodynamic surfaces, and a wooden fuselage. These materials ensured the aircraft would be lightweight, cost-effective, and easy to manufacture. At the end of the first semester, we had a design review from which only minor changes were requested.  

## Build  

The fuselage was laser-cut from plywood and glued together. CF spars and the CF tail boom connection point were glued to the fuselage, along with hot-wire-cut blue foam for the aerodynamic shapes. We used 3D printed jigs to cut the holes in the proper places, and 3D printed nacelles to mount the engines to. The nacelles were 3D printed from lightweight PLA, and optimized in shape to minimize weight and maximize printability. Most wiring was embedded into the foam, and all surfaces were monocoated to minimize drag. As a final step, the autopilot and payload were mounted and checked to ensure all control surfaces and systems were working properly.  

## Testing  

The prototype aircraft was tested at the local model airfield, and passed all required flight tests. The aircraft remained stable throughout testing, and the pilots noted that it was one of the easiest to fly. The flight time was shorter than calculated; however our team expected this and oversized the battery accordingly, so we still met the flight time requirements. The only requirement we were unable to verify was the maximum velocity, as we could only test up to 38 knots instead of 40 due to time and weather constraints.  
