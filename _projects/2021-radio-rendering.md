---
layout: project
title: MAE 4272 Blade Design Project
description: Advanced CAD Project
technologies: [Solidworks, MATLAB, LabView]
image: /assets/images/blade-cad.jpg
---

In MAE 4272, our team was tasked with designing and testing a small-scale wind turbine blade to maximize average power production over a given Weibull wind speed distribution centered around 5 m/s. The design was subject to several constraints, including a 6-inch blade radius, compatibility with a standard hub, operation at a constant speed near 1300 RPM, and a strict maximum torque limit of 0.035 N·m to protect the torque brake system.

We selected the E387 airfoil based on its favorable lift-to-drag ratio and manufacturability, then applied Blade Element Momentum (BEM) theory to design the blade geometry. The blade was discretized into 40 radial sections, and optimal chord and pitch distributions were calculated as functions of radius to maximize power extraction at the most probable wind speed. To enforce the torque constraint, the chord distribution was iteratively scaled until predicted torque remained below 0.035 N·m across all operating wind speeds. Structural stress calculations were performed to ensure the blade would not fail under combined aerodynamic and centrifugal loading. The final chord and pitch distributions were fit with third-order polynomials and used to generate CAD for 3D printing.

![Shaded rendering of earlier version]({{ "/assets/images/radio-machine.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

The blades were experimentally evaluated in a wind tunnel by mapping power output across wind speeds from 3.2 to 9.0 m/s. At each wind speed, torque brake voltage was incrementally increased until stall, while RPM, torque, and electrical power were recorded at steady state. The turbine began rotating at 3.2 m/s and consistently remained below the maximum allowable torque throughout testing. Experimental power curves were post-processed and integrated over the Weibull distribution to compute average power output, resulting in a measured average power of approximately 0.10 W. This value was compared against theoretical predictions and the Betz-limit-based maximum to evaluate overall blade efficiency and identify sources of performance loss.

![Photo of old radio]({{ "/assets/images/old-radio.jpg" | relative_url }}){: .inline-image-l}

I led several key technical components of the project across the design and testing phases. Early in the project, I performed the initial airfoil trade study, comparing candidate airfoils based on lift-to-drag ratio, predicted power output, and manufacturability. This analysis informed our selection of the E387 airfoil and provided the team with a strong aerodynamic baseline for optimization.

I then worked on evaluating system limits by calculating the maximum torque and stress experienced by the blade across the operating wind speed range. This included assessing aerodynamic and centrifugal loading to ensure the design remained below the 0.035 N·m torque constraint and within acceptable stress limits.

Finally, I developed the experimental testing protocol used in the wind tunnel, including system validation steps, stall-based loading procedures, and data collection sequencing. I supported post-processing of RPM, torque, and power data to generate power curves and Weibull-weighted performance metrics, enabling direct comparison between predicted and experimental blade performance.
