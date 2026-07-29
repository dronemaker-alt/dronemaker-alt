# Cali-Spider Project Notes

## Purpose

This is the working engineering record for Cali-Spider. It separates selected architecture, unresolved trades, outside research, experiments, and measured results.

## Current Baseline

### Mission

Develop a modular hexapod platform that can grow from a desktop gait demonstrator into a repairable autonomous field robot.

### Control Hierarchy

Provisional architecture:

- local leg nodes: deterministic joint control, feedback collection, and fault reporting;
- gait controller: leg coordination, body pose, stability, and motion commands;
- companion computer: navigation, perception, logging, voice interface, and mission logic.

No processor is assigned permanently until timing, I/O, power, and software requirements are measured.

### Communications

- Primary candidate: CAN for distributed leg and body nodes.
- Secondary: UART for short point-to-point internal links.
- Supervisory/payload: Wi-Fi or another radio link.
- Open questions: bus speed, message ownership, update rates, termination, connector, fault containment, and degraded-mode behavior.

### Mechanical Modularity

Each leg module needs a documented:

- mechanical datum and bolt pattern;
- joint count and range of motion;
- actuator and reduction requirements;
- power connector and pinout;
- communications connector and pinout;
- replacement procedure;
- calibration and node-identification method.

## Reusable Research

### ManaFly 3

Classification: outside background research, not a design baseline.

Potentially reusable:

- topology-optimization workflow;
- mass-efficient printed links;
- motor or actuator mounting concepts;
- landing-foot geometry;
- lightweight electronics enclosures.

Not reusable without verification:

- complete 3-inch unibody layout;
- claimed cost;
- claimed strength or crash behavior;
- CAD whose license has not been checked;
- print settings presented without controlled test data.

## Planned Experiment: Printed Leg-Link Comparison

### Objective

Determine whether topology optimization provides a useful Cali-Spider leg link rather than merely producing an impressively organic-looking way to break plastic.

### Controls

- identical material batch;
- identical layer height and nozzle;
- identical print orientation;
- equal target mass or clearly normalized results;
- same joint-interface hardware;
- at least three specimens per configuration when material permits.

### Record

- CAD revision and source;
- material and drying history;
- slicer profile and infill;
- specimen mass;
- print time;
- dimensional error;
- bending stiffness;
- joint pullout load;
- impact or drop result;
- failure location and mode;
- photographs before and after testing.

### Decision Rule

Adopt topology-optimized geometry only if it improves a stated structural requirement without unacceptable printing, inspection, repair, or repeatability penalties.

## Prototype Stages and Exit Criteria

### Stage 1 — Desktop Walker

- command each joint predictably;
- demonstrate repeatable standing and basic gait;
- stream joint state and faults;
- log power use and control-loop timing;
- recover cleanly from an emergency stop.

### Stage 2 — Modular Walker

- replace one leg without rewiring the whole robot;
- identify and calibrate a replacement node;
- demonstrate CAN communication under actuator load;
- isolate a failed or disconnected leg node;
- document connector, pinout, and module procedure.

### Stage 3 — Large Walker

- validate actuator torque and thermal margins;
- validate leg and body structure using measured loads;
- document power distribution, protection, and runtime;
- demonstrate controlled operation on representative farm terrain;
- record transport, service, and field-recovery requirements.

### Stage 4 — Autonomous Field System

- add perception and localization;
- demonstrate bounded autonomous navigation;
- define payload interfaces;
- integrate voice and mission logic without placing safety-critical joint control on the AI layer.

## Engineering Note Backlog

Create these focused notes as decisions mature:

- `CALI-SPIDER-SYSTEM-ARCHITECTURE.md`
- `CALI-SPIDER-LEG-MODULE.md`
- `CALI-SPIDER-CONTROL-AND-GAIT.md`
- `CALI-SPIDER-CAN-PROTOCOL.md`
- `CALI-SPIDER-POWER-BUDGET.md`
- `CALI-SPIDER-SENSOR-PAYLOAD-MAP.md`
- `CALI-SPIDER-PROTOTYPE-TEST-LOG.md`

Avoid creating empty documents merely to admire the folder structure. Create each note when it has a decision, interface, calculation, or measurement to preserve.

## Immediate Next Decisions

- [ ] Define desktop prototype joint count and geometry.
- [ ] Inventory available actuators, controllers, sensors, and power hardware.
- [ ] Select the first local-node and gait-controller candidates for bench testing.
- [ ] Draft a provisional CAN message and wiring plan.
- [ ] Define the first leg-link specimen dimensions and load test.
- [ ] Verify the ManaFly source files and license.
