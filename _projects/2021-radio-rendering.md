---
layout: project
title: MAE 4272 Blade Design Project
description: Advanced CAD Project
technologies: [Solidworks, MATLAB, LabView]
image: /assets/images/blade-cad.jpg
---

In MAE 4272, our team designed and experimentally tested a small-scale wind turbine blade to maximize average power output over a **Weibull wind speed distribution** centered at 5 m/s. The design was constrained by a 6-inch maximum blade radius, a maximum operating speed of 3500 RPM, and a torque brake limit of 0.035 N·m, which governed both the aerodynamic design and experimental testing envelope.

The blade geometry was developed using **Blade Element Momentum theory** and optimized for a **target operating speed of 1300 RPM**. After completing an airfoil trade study, we selected the **E387 airfoil** based on lift-to-drag performance and manufacturability. The blade was **discretized into 40 radial sections**, and optimal **chord and pitch distributions were calculated as functions of radius** to maximize power extraction at 5 m/s in **MATLAB**. To satisfy system limits, the chord distribution was iteratively scaled until the maximum predicted torque remained **below 0.035 N·m across all wind speeds**. Structural analysis accounting for aerodynamic bending and centrifugal loading identified the maximum combined stress at the blade root of 31 MPa, which remained below the material yield limit with a factor of safety of 1.42. Final chord and pitch profiles were fit with **third-order polynomials** and used to generate the CAD in **SolidWorks**.

![Actual picture of the blades]({{ "/assets/images/blade-photo.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

Experimental testing was conducted in a wind tunnel at 15 Hz to map power output across wind speeds from **0 to 9.0 m/s**. At each wind speed, the torque brake voltage was incrementally increased until stall while **RPM, torque, and power** were recorded using **LabVIEW**. After stall, the torque brake was reset to 0 V, the wind speed was increased to the next operating point, and the procedure was repeated. The turbine began rotating at 3.2 m/s and remained below the 0.035 N·m torque limit throughout testing. At **9.0 m/s**, the torque brake reached its **12 V** limit before stall occurred. Measured power curves were post-processed in **MATLAB and Excel** and integrated over the Weibull distribution, yielding an **average measured power of approximately 0.10 W**. These results were compared against theoretical predictions and the **Betz-limit-based maximum power** to evaluate blade efficiency and identify sources of performance loss.

![Power curves from wind tunnel testing]({{ "/assets/images/blade-powercurves.jpg" | relative_url }}){: .inline-image-l style="width: 420px;"}

I led several key technical components of the project across both design and testing phases. I performed the initial **airfoil trade study**, establishing the aerodynamic baseline that guided blade optimization. I also **computed maximum torque and blade stress** under combined aerodynamic and centrifugal loading to ensure compliance with system constraints. Finally, I developed the **wind tunnel testing protocol**, including validation procedures, stall-based loading sequences, and data collection methodology, and supported post-processing of experimental data to generate power curves and Weibull-weighted performance metrics.
