---
layout: project
title: MAE 4272 Blade Design Project
description: Advanced CAD Project
technologies: [Autodesk Fusion, MATLAB]
image: assets/images/4272BladeDesignCADRender.png
---


As demand for clean energy grows, we need wind turbines that can reliably generate power under realistic wind conditions. In our project we designed a blade that performs well across a Weibull wind-speed distribution with k = 5 and c = 5, where most usable wind energy occurs around 4–6 m/s.
To translate that mission into hardware, we used Blade Element Momentum (BEM) theory to model how effective wind velocity, angle of attack, and bending moment change across the length of a blade. We selected a NACA 4412 cross-section for the blade due to its lift-to-drag performance and manufacturability, and used airfoil polar data at Re ≈ 50,000 to choose an operating point of α = 10°. Then we used matlab to break the blade into 20 radial segments. For each segment, we found a pitch value that would get the blade closest to the taget α value. Then we defined constraints on stress, torque, blade rotation rate, and chord length. Starting at a low RPM, the code analyzes whether the design meets the constraints and estimates the power output. This process loops, increasing the rotation rate each time until one of the constraints are no longer met. The geometry determined for the last working RPM value was the geometry that we used for CADing the blade. 
The three blades were then 3D printed and mounted on a torque break in a wind tunnel for testing. Through testing the tunnel at different torque values and wind speeds, we were able to graph power curves for multiple wind speeds. This helped us form a fit model that finds an optimal rotation rate for a given wind speed. 
My role on the team was broad, as we all enjoyed playing a role in each part, from design to data analysis. With that being said, I took a lead on designing the wind tunnel testing procedure to ensure that our testing would provide valuable data for informing a suggested operating RPM. 
![Experimental power curves obtained from testing turbine in wind tunnel at various wind speeds]({{ "/assets/images/BladeDesign4272PowerCurves.png" | relative_url }}){: class="project-image" }
