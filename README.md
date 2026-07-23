# navigation

Vehicle-agnostic **navigation & state estimation** for GT Propulsive Landers —
the "N" in GN&C. Sensor-fusion filters that estimate vehicle attitude and state,
plus the sensor simulation used to test them. Designed to plug into any GTPL
vehicle, not tied to a specific airframe.

> **Provenance:** Reorganized **by function** in July 2026 from the monolithic
> [`GTPL-Testing/MonopropUAV`](https://github.com/GTPL-Testing/MonopropUAV)
> repo (was `Sensing&Controls/`). Full commit history is preserved, including the
> original feature branches that carried estimation work (e.g. `rust-ekf`,
> `dynamics_model`, `integrate-sim-and-control-loop`). See the
> [GTPL-test root README](../README.md) for the full mapping.

## Contents

| Path | What it is |
|------|------------|
| `AttitudeEstimation/` | Extended Kalman Filter variants (Python + C++), plus Complementary, Madgwick, Mahony, and Fourati filters, with test benches and a Rust EKF |
| `SensorSimulation/` | Synthetic IMU/LiDAR data generation for filter validation |
| `imu_at_rest.csv` | Static IMU capture for noise/bias characterization |
| `docs/` | Original `Sensing&Controls` README |

## Branches

Feature branches from MonopropUAV that carried unmerged navigation work were
preserved here (filtered to this repo's paths): `rust-ekf`, `dynamics_model`,
`integrate-sim-and-control-loop`. `main` is the default.

## Sibling GN&C libraries

[`control`](../control) · [`guidance`](../guidance) · [`dynamics`](../dynamics) — integrated per vehicle in [`monoprop-flight-software`](../monoprop-flight-software).
