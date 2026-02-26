# Self-Balancing-Motorcycle-Control

Embedded control design for an inverted pendulum motorcycle system, implementing full state feedback stabilisation, open-loop locomotion control, and IMU calibration on Arduino hardware.

## Key Results

- Maximum stationary balance time: **374 s (6+ minutes)**
- Stable straight-line locomotion achieved for **11 s**
- Full state-feedback controller implemented (θ, θ̇, ω)
- Digital low-pass filtering applied to IMU signals (τ = 0.2)
- Supervisory logic enforcing safety constraints:
  - Lean angle < 12°
  - Battery voltage > 3V
- Final tuned gains:
  - Kp = 64
  - Kd = 5
  - Kpw = 0.004

# Media:

## Hardware Validation

The controller was validated under nominal conditions, surface irregularities, and external disturbances to assess robustness and stability margins.

<img width="579" height="637" alt="image" src="https://github.com/user-attachments/assets/8b1bd0cc-eddb-4b6b-b1e5-9042af2afb90" />

Figure 1: Closed-loop stabilisation under nominal conditions. The state-feedback controller maintains upright equilibrium at the tuned control gains (Kp = 64, Kd = 5, Kpw = 0.004).

<img width="517" height="318" alt="image" src="https://github.com/user-attachments/assets/734ba6dd-ea52-4e6c-96f5-6e52649d2a1f" />

Figure 2: Stability validation on irregular terrain. The controller maintains balance despite surface disturbances and model uncertainty.

<img width="596" height="761" alt="image" src="https://github.com/user-attachments/assets/a98ded88-a62b-41f0-98fa-cfd3338917b2" />

Figure 3: Disturbance rejection test. External lateral impulse applied while stationary; controller successfully restores upright position.
