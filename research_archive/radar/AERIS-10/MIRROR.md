# AERIS-10 / PLFM Radar Mirror Reference

## Archive Status

**Mirror reference** — a separate full repository mirror exists and is linked below. Provenance is captured, but the hardware has not been built or independently validated by Drone Libre, and the declared licenses require file-level verification.

## Source

- Project: AERIS-10 / PLFM_RADAR
- Upstream creator: Nawfal Motii
- Upstream repository: https://github.com/NawfalMotii79/PLFM_RADAR
- Drone Libre mirror: https://github.com/dronemaker-alt/AERIS-10-Mirror
- Mirror snapshot reviewed: `c80508c7b62487f905fc3968c86ecb79a7b1aa2c`
- Date reviewed: 2026-07-29
- Upstream status declared in README: Alpha / work in progress
- Hardware license declared in README: CERN-OHL-P v2
- Software and firmware license declared in README: MIT
- License verification status: incomplete; the mirror root did not expose the referenced `LICENSE` file during review

## Summary

AERIS-10 is presented upstream as a modular, open-source 10.5 GHz pulse linear-frequency-modulated phased-array radar. The repository contains hardware, FPGA, STM32, host-software, simulation, and documentation work for two proposed range classes.

The repository is substantial enough to preserve as an engineering reference, but upstream range, power, beam-steering, and processing claims must remain labeled as project claims until hardware configuration and test evidence are independently reviewed.

## Relevance to Drone Libre

Potentially reusable engineering methods include:

- Radar subsystem partitioning across RF, FPGA, MCU, host software, and power management.
- Pulse-compression, Doppler, MTI, CFAR, and target-display software architecture.
- FPGA and MCU regression-test organization.
- GPS/IMU-assisted target-coordinate handling.
- Rugged ground-station display and control concepts.
- Phased-array documentation, bring-up, and safety-interlock patterns.

This is primarily a ground-station awareness and research reference. It is not a current Drone Libre airframe payload baseline.

## Files Preserved

The complete working tree is maintained in the separate [AERIS-10 Mirror](https://github.com/dronemaker-alt/AERIS-10-Mirror). This command-center entry intentionally stores provenance and evaluation status rather than duplicating the full radar repository.

## Verification Status

- [x] Upstream repository identified.
- [x] Separate Drone Libre mirror identified.
- [x] Mirror snapshot commit recorded.
- [x] Upstream architecture and declared status summarized.
- [ ] Recover or add the complete license texts to the mirror.
- [ ] Map hardware and software files to their applicable licenses.
- [ ] Compare the mirror against the current upstream repository.
- [ ] Identify stale simulations, generated artifacts, and unverified specifications.
- [ ] Review RF exposure, power, thermal, and regulatory assumptions before hardware work.
- [ ] Independently reproduce the software/FPGA test suite.
- [ ] Record physical build and measured performance if hardware is constructed.

## Next Steps

1. Restore and verify the CERN-OHL-P and MIT license texts in the mirror.
2. Generate an upstream-to-mirror commit comparison.
3. Create a subsystem inventory covering RF boards, FPGA, STM32, GUI, simulations, and mechanical files.
4. Separate reusable ground-station software concepts from high-cost radar hardware.
5. Promote this entry to **tested reference** only after reproducible tests or measured hardware results exist.

## Rights Note

Do not infer redistribution rights from README badges alone. Confirm the actual license text and its scope before distributing hardware files, modified board designs, firmware, or packaged mirror releases.
