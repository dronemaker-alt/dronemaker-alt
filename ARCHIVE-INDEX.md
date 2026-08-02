# Archive Index

## Lab Archive Structure

This repository and associated storage systems are organized into multiple tiers.

The goal is long-term preservation of:

- Embedded-systems knowledge
- Flight-firmware ecosystems
- Robotics research
- Avionics concepts
- Fabrication workflows
- Reverse-engineering data
- Engineering history

## Storage Tiers

### Active Development

The high-speed working environment for current projects, firmware repositories, CAD files, experiments, and documentation.

Examples include Cali-Spider, the P4 handheld, CyberSkull, and DroneMesh. Active work in this repository is indexed through [projects](projects/), [architecture](ARCHITECTURE/), and [lab notes](LAB-NOTES/).

### Mirror Repositories

Offline mirrors preserve critical source repositories, commit history, and access if an upstream project disappears.

Mirror clones use:

```bash
git clone --mirror
```

Outside-project references and their verification status are indexed in the [research archive](research_archive/).

### Engineering Archive

Long-term preserved knowledge, including PDFs, schematics, BOMs, board photos, firmware releases, pinouts, teardown notes, and recovered hardware.

Physical and legacy hardware records belong in the [Recovered Technology Archive](RECOVERED-TECHNOLOGY-ARCHIVE/).

### Media Archive

Visual engineering history, including bench photos, prototypes, wiring diagrams, screenshots, architecture diagrams, and project progression.

### Cold Storage

Offline backup storage for disaster recovery, archive preservation, and long-term redundancy. Important archives should exist in more than one physical location.

## Current Archive Goals

### Flight Systems

- INAV
- ArduPilot
- PX4
- Betaflight
- Paparazzi

### Embedded Systems

- ESP32
- STM32
- Display systems
- Telemetry systems

### Robotics

- Distributed control
- Modular robotics
- Sensor fusion
- Autonomous navigation

### Space Systems

- CubeSat frameworks
- NASA cFS
- OpenSatKit

## Long-Term Objective

Create a resilient engineering knowledge archive capable of surviving disappearing repositories, dead forums, lost documentation, link rot, obsolete hardware, and fragmented ecosystems.

The archive should remain useful for experimentation, learning, reverse engineering, firmware analysis, autonomous-systems research, and future hardware development.

## Engineering Principle

Preserve first. Organize second. Understand continuously.
