# sim-vehicle-copter-quad-x500

A **wwsim vehicle profile repo** — the reference 500 mm quad (X frame, 4S).

A simulation in [wwsim](https://sim.wws.inc) is `environment × vehicle`. This
repo is the *vehicle* half: airframe, sensors, ArduPilot params. The contract
is `docs/VEHICLES.md` in the orchestrator repo.

## Contents

| Path | Purpose |
|------|---------|
| `wwsim-vehicle.yaml` | The manifest the orchestrator reads + validates. |
| `params/copter_x500.parm` | Base ArduPilot params. |
| `params/sitl_dev.parm` | SITL quality-of-life overlay (auto-applied). |
| `params/no_gps.parm`, `params/gps_outdoor.parm` | Optional named overlays. |
| `noise/*.yaml` | Sensor-noise profiles for deterministic mode. |

## Releases

Sims pin to a **git tag**, never to `main`. Current: `v1.0.0`.

## Register it

In the wwsim dashboard → **Admin → Vehicles → Register**, point at this repo,
set `defaultRef: v1.0.0` and `allowedRefs: [v1.0.0]`, then **Validate**.
