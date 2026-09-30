# Automotive-Power-Window-Control-System-Using-MATLAB-Simulink

## Overview

This project models and simulates an automotive power window control system driven by a DC motor using MATLAB/Simulink. The system implements UP, DOWN, and STOP operations while enforcing upper and lower travel limits to ensure safe window movement.

## Objectives

- Model the electrical and mechanical dynamics of a DC motor.
- Implement UP, DOWN, and STOP window control logic.
- Enforce upper and lower travel limits for safe operation.
- Simulate window position, speed, and motor behavior.
- Analyze system performance using MATLAB and Simulink.

---

## System Features

 UP window movement control

 DOWN window movement control

 STOP operation

 Upper travel limit protection

 Lower travel limit protection

 DC motor mathematical modeling

 Position tracking and monitoring

 Simulation-based testing and validation

---

## System Architecture


![Simulink Model](Results/Simulink_Model.png)

![Simulation Output](Results/Output_Waveform.png)

### Inputs

- UP Switch
- DOWN Switch

### Control Logic

The control logic determines the motor direction based on user input and window position.

| Condition | Action |
|------------|----------|
| UP pressed and Position < Upper Limit | Move Up |
| DOWN pressed and Position > Lower Limit | Move Down |
| Both switches OFF | Stop |
| Upper Limit Reached | Stop |
| Lower Limit Reached | Stop |

---

## DC Motor Mathematical Model

The power window is driven using a DC motor model consisting of electrical and mechanical subsystems.

### Electrical Equation

\[
V = L \frac{di}{dt} + Ri + K_b \omega
\]

Where:

- V = Applied Voltage
- L = Armature Inductance
- R = Armature Resistance
- i = Armature Current
- Kb = Back EMF Constant
- ω = Angular Velocity

---

### Mechanical Equation

\[
J \frac{d\omega}{dt} + b\omega = K_t i
\]

Where:

- J = Rotor Inertia
- b = Viscous Friction Coefficient
- Kt = Torque Constant
- i = Armature Current

---

### Position Calculation

Motor position is obtained by integrating angular velocity.

\[
\theta = \int \omega dt
\]

Where:

- θ = Angular Position
- ω = Angular Velocity

---

## Simulink Model Components

The Simulink model contains the following subsystems:

### Control Logic
Implements UP, DOWN, and STOP commands based on switch inputs and position limits.

### Electrical Dynamics
Computes motor current using armature circuit equations.

### Mechanical Dynamics
Calculates motor speed using torque and inertia relationships.

### Position Calculation
Integrates angular velocity to determine window position.

### Limit Detection
Prevents window movement beyond predefined upper and lower limits.

### Monitoring
Scopes are used to visualize motor position and system response.

---

## Simulation Results

The simulation successfully demonstrates:

- Smooth upward window movement.
- Smooth downward window movement.
- Automatic stopping at upper travel limit.
- Automatic stopping at lower travel limit.
- Stable control operation without exceeding travel boundaries.

---

## Project Workflow

1. User presses UP switch.
2. Controller checks upper limit.
3. DC motor rotates in forward direction.
4. Window position increases.
5. Motor stops automatically at upper limit.

Similarly:

1. User presses DOWN switch.
2. Controller checks lower limit.
3. DC motor rotates in reverse direction.
4. Window position decreases.
5. Motor stops automatically at lower limit.

---

## Tools and Software

- MATLAB
- Simulink

---

## Skills Demonstrated

- MATLAB Programming
- Simulink Modeling
- DC Motor Modeling
- Control Systems
- Mathematical Modeling
- Dynamic System Simulation
- Automotive Control Systems

---

## Future Enhancements

- One-Touch Automatic Window Operation
- Anti-Pinch Obstacle Detection
- PWM-Based Speed Control
- Current Monitoring and Protection
- Embedded Implementation using STM32
- Embedded Implementation using ESP32
- Real-Time Hardware Testing

---
df
## Project Outcomes

- Successfully modeled an automotive power window system using MATLAB/Simulink.
- Implemented safe UP, DOWN, and STOP control logic.
- Simulated DC motor electrical and mechanical dynamics.
- Verified window position control with travel limit protection.
- Gained practical experience in control system design and automotive actuator modeling.

---

## Author

### Guni Reddy Charan Kumar Reddy

B.Tech – Electronics and Communication Engineering

Embedded Systems | IoT | MATLAB/Simulink | STM32 | FreeRTOS


---
