---
layout: project
title: MAE 4272 Blade Design Project
description: Advanced CAD Project
technologies: [Solidworks, MATLAB, LabView]
image: /assets/images/blade-cad.jpg
---

In MAE 4272, our team was tasked with designing and testing a wind turbine blade to maximize average power production over a given Weibull wind speed distribution centered around 5 m/s. The design had several constraints: a 6-inch blade radius maximum, maximum RPM of 3500, and a maximum torque brake limit of 0.035 N·m.

The design process took several weeks. First, we started with the airfoil selection tradeoff where we selected the **E387 airfoil** based on its favorable lift-to-drag ratio and manufacturability. Our models used **Blade Element Momentum theory** to design the blade geometry. The blade was discretized into 40 radial sections, and optimal chord and pitch distributions were calculated as functions of radius to maximize power extraction. The chord distribution was iteratively scaled until predicted torque remained below 0.035 N·m across all operating wind speeds. Structural stress calculations were performed to ensure the blade would not fail under combined aerodynamic loading. The final chord and pitch distributions were fit with third-order polynomials and used to generate CAD for 3D printing in **Solidworks**.

![Actual picture of the blades]({{ "/assets/images/blade-photo.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

The testing process took an hour. Our goal was to map a sweep of power output across wind speeds in the Weibull distribution. At each wind speed, torque brake voltage was incrementally increased until stall, while RPM, torque, and power were all recorded at each increment from LabView. The turbine began rotating at 3.2 m/s and consistently remained below the maximum allowable torque throughout testing. We maxed out at 9 m/s as the torque brake reached its limit of 12V. Experimental power curves were post-processed and integrated over the Weibull distribution to compute average power output, resulting in a measured average power of approximately 0.10 W. This value was compared against theoretical predictions and the Betz-limit-based maximum to evaluate overall blade efficiency and identify sources of performance loss.

![Power curves from wind tunnel testing]({{ "/assets/images/blade-powercurves.jpg" | relative_url }}){: .inline-image-r style="width: 420px;"}

I led several key technical components of the project across the design and testing phases. Early in the project, I performed the initial airfoil trade study, comparing candidate airfoils based on lift-to-drag ratio, predicted power output, and manufacturability. This analysis informed our selection of the E387 airfoil and provided the team with a strong aerodynamic baseline for optimization.

I then worked on evaluating system limits by calculating the maximum torque and stress experienced by the blade across the operating wind speed range. This included assessing aerodynamic and centrifugal loading to ensure the design remained below the 0.035 N·m torque constraint and within acceptable stress limits.

Finally, I developed the experimental testing protocol used in the wind tunnel, including system validation steps, stall-based loading procedures, and data collection sequencing. I supported post-processing of RPM, torque, and power data to generate power curves and Weibull-weighted performance metrics, enabling direct comparison between predicted and experimental blade performance.
