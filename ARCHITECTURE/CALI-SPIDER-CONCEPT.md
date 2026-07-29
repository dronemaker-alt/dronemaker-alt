# CALI-SPIDER ARCHITECTURE CONCEPT

## System Overview

Cali-Spider is a scalable modular robotics platform intended to evolve from desktop walker prototypes into larger autonomous hexapod field systems.

This document defines the enduring concept. Engineering choices, measurements, and test results belong in [CALI-SPIDER-PROJECT-NOTES.md](CALI-SPIDER-PROJECT-NOTES.md).

## Core Concept

### Modular Leg Architecture

Each replaceable leg subsystem may eventually provide:

- local real-time control;
- servo management;
- joint or load feedback;
- a defined mechanical mounting interface;
- a defined power and data connector;
- quick replacement and field diagnosis.

### Layered Control

The candidate control hierarchy is:

1. Local leg nodes handle deterministic joint control and immediate feedback.
2. A gait controller coordinates legs, balance, and body motion.
3. A companion computer handles navigation, perception, voice interaction, and higher-level autonomy.

ESP32, STM32, Raspberry Pi, and later AI accelerators remain candidates until requirements and bench tests assign them specific roles.

### Communications

CAN is the leading candidate for the primary distributed control bus because Cali-Spider is expected to have multiple replaceable nodes and electrically noisy actuators.

UART remains useful for short internal point-to-point links. Wi-Fi is a supervisory or payload link, not the default real-time leg-control bus.

### Sensor Systems

Candidate sensors include:

- body and leg IMUs;
- joint position, current, load, or contact feedback;
- cameras;
- lidar or time-of-flight ranging;
- ultrasonic sensing;
- environmental payload sensors.

A sensor is not part of the baseline until its purpose, location, interface, power draw, data rate, and failure response are recorded.

## Long-Term Experimental Concepts

- autonomous navigation;
- voice interaction;
- modular payload systems;
- recon-drone deployment;
- distributed robotics experiments;
- field diagnostics integration.

These remain optional capabilities and must not drive the first walking prototype.

## Development Path

1. Desktop walker: prove joint control, gait generation, and basic telemetry.
2. Modular walker: prove replaceable leg nodes, bus communications, and fault isolation.
3. Large walker: validate structure, actuator sizing, power distribution, and safe field mobility.
4. Autonomous field system: add perception, navigation, payloads, and higher-level AI.

Each stage advances only after its measurable exit criteria are recorded in the project notes.

## Research Boundary

The ManaFly 3 entry is background research. Its topology-optimization methods may inform Cali-Spider leg links and joint housings, but no geometry or performance claim becomes part of Cali-Spider without license verification and controlled comparison testing.

## Status

Active concept and prototype-evolution stage.

Legitimate engineering process translated from:

> What if we made the tiny walker terrifyingly larger?
