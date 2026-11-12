# \# motor-position-controller

# DC motor position control on an STM32G431, with the controller designed from a model identified from my own measurements.

# 

# \*\*Status:\*\* Phase 1, Step 1 (modelling and simulation). No hardware results yet.

# 

# \## Phase 1 definition of done

# \- \[ ] Identified model: R, L, Kt, Ke, J, b, Coulomb friction/deadzone fitted from my own experiments; fit error on held-out data

# \- \[ ] Model-based controller: design method stated, predicted gain/phase margins reported

# \- \[ ] Predicted vs. measured step responses at ≥2 sizes, including one that saturates the actuator (anti-windup shown)

# \- \[ ] Disturbance test with recovery compared against model prediction

# \- \[ ] Kalman vs. finite-difference velocity on the same run, noise covariances justified

# \- \[ ] Model-vs-reality section explaining every gap (friction, backlash, quantization, loop timing)

# 

# \## Hardware

# Pololu #4751 37D gearmotor (18.75:1, 1200 CPR at output) · DRV8874 driver · NUCLEO-G431RB

# 

# \## Environment

# `conda env create -f environment.lock.yml` reproduces the exact versions used.

# 

# Third-party drivers (STM32 HAL/CMSIS) keep their original licenses.

