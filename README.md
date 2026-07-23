# navigation

Vehicle-agnostic **navigation & state estimation** for GT Propulsive Landers —
the "N" in GN&C. Sensor-fusion filters that estimate vehicle attitude and state,
plus the sensor simulation used to test them. Designed to plug into any GTPL
vehicle, not tied to a specific airframe.

## Contents

| Path | What it is |
|------|------------|
| `AttitudeEstimation/` | Extended Kalman Filter variants (Python + C++), plus Complementary, Madgwick, Mahony, and Fourati filters, with test benches and a Rust EKF |
| `SensorSimulation/` | Synthetic IMU/LiDAR data generation for filter validation |
| `imu_at_rest.csv` | Static IMU capture for noise/bias characterization |
| `docs/` | Legacy documentation |

## Branches

`main` is the default. `rust-ekf`, `dynamics_model`, and
`integrate-sim-and-control-loop` carry unmerged estimation work.

## Sibling GN&C libraries

[`control`](../control) · [`guidance`](../guidance) · [`simulations`](../simulations) — integrated per vehicle in [`monoprop-flight-software`](../monoprop-flight-software).
