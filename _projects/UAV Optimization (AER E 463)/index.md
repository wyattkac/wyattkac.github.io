---
layout: post
title: Multidisciplinary UAV Optimization
description: 
    Carrying out a UAV optimization involves picking a problem to optimize, selecting variables to use, choosing software with an API capable of performing the necessary calculations, and developing a program that systematically adjusts inputs until the solution converges, ensuring an efficient and effective design.
skills: 
  - Python
  - Git

main-image: /Drone.png
---

---

## Introduction  
Leading a two-person team, we developed a Python program that reduced a UAV's drag by 15% when compared to the initial design, while maintaining radar cross-section (RCS) by varying the geometry. This results in significant fuel savings, leaving more room for payloads or a longer flight time. I focused on designing the geometry modification loop, which adjusted airfoil shape, wing parameters, and tail sizing, and the aerodynamic analysis, which was used to find lift, drag, and stability.  

## Technical Approach  

{% include image-gallery.html images="https://raw.githubusercontent.com/wyattkac/wyattkac.github.io/refs/heads/main/_projects/UAV%20Optimization%20(AER%20E%20463)/Flow.jpg" height="400"%} Structure Design Matrix

### Literature Review  
We began by completing a literature review of similar projects. This gave us an idea of what had been done before, and helped shape our optimization approach.  

### Methodology  
We chose to use Python, as there were Python libraries or APIs for everything we needed to do. Our final project used openMDAO, OpenVSP, and RadarSimPy to calculate all needed values.  

The structure design matrix (above) visually represents the optimization process. We start with any geometry, and feed it into openVSP, which creates a mesh. Since the Reynolds number (Re) depends on both size and velocity, we use the geometry specifications to calculate Re given the speed of the aircraft. VSPAero takes this information and calculates the lift (Cl) and drag (Cd) of the aircraft. Using the CG from OpenVSP and the CP from VSPAero, we compute the static margin to assess the stability of the aircraft. The mesh from OpenVSP is then used by RadarSimPy to give us the RCS of the aircraft. The algorithm iterates through geometry modifications until convergence.  

#### Geometry  

We allowed the program to create any four-digit NACA airfoil by varying camber, the location of camber, and thickness of the airfoil. The program also adjusted the wing size, angle of incidence, and location. To simplify the problem, the program adjusted tail sizing based on airfoil position. We validated stability by calculating the static margin in each iteration, ensuring the tail surfaces were properly sized. With more time, tail sizing could have been an independent variable, but this would have exponentially increased computation time. The optimization already required 500 iterations over 26 hours to converge. Lacking a defined gradient, we could not use a gradient-based solver, which significantly increased computation time.  

#### Constraints and Objective Function  

We wanted to optimize RCS and the lift to drag ratio (L/D), as L/D defines the efficiency of the aircraft. Since our solver minimizes the objective function, we took the inverse of L/D (D/L) to ensure proper optimization. We then scaled D/L and RCS to comparable weights and combined them into a single objective function. To maintain feasibility, we constrained both the coefficient of lift and static margin, ensuring sufficient lift and stability.  
