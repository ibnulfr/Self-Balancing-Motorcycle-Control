# Self-Balancing-Motorcycle-Control

Embedded control design for an inverted pendulum motorcycle system, implementing full state feedback stabilisation, open-loop locomotion control, and IMU calibration on Arduino hardware.

## Key Results

- ⚖️ Maximum stationary balance time: **374 s (6+ minutes)**
- 🚴 Stable straight-line locomotion achieved for **11 s**
- 🧠 Full state-feedback controller implemented (θ, θ̇, ω)
- 🔎 Digital low-pass filtering applied to IMU signals (τ = 0.2)
- 🔁 Supervisory logic enforcing safety constraints:
  - Lean angle < 12°
  - Battery voltage > 3V
- ⚙️ Final tuned gains:
  - Kp = 64
  - Kd = 5
  - Kpw = 0.004
