# Drone Libre

*Engineering should be documented, repairable, reusable, and free to learn from.*

Drone Libre is an open-hardware engineering initiative focused on robotics, embedded systems, reusable power electronics, and unmanned aircraft.

The goal is not simply to build drones. It is to produce well-documented engineering projects that others can study, reproduce, improve, and repair.

## Engineering Philosophy

Engineering knowledge should never become tribal knowledge.

Every project should include:

- Design rationale
- Schematics
- Bill of Materials (BOM)
- Manufacturing notes
- Test procedures
- Validation results
- Revision history
- Lessons learned

**If it isn't documented, it isn't finished.**

## Current Focus

- Open ESP32 flight systems
- Modular ESC development
- Printable drone airframes
- Reverse engineering reusable USB-C power modules
- Embedded robotics
- Engineering test fixtures
- Sustainable electronics reuse

See the [full engineering roadmap](ROADMAP.md) for planned phases and longer-term work.

## Repository Map

This repository separates active Drone Libre engineering from outside research and long-term preservation.

### Active Engineering

- [`projects/`](projects/) — project notebooks, hardware development, firmware work, and test results.
- [`ARCHITECTURE/`](ARCHITECTURE/) — requirements, subsystem boundaries, interfaces, assumptions, and planned validation.
- [`LAB-NOTES/`](LAB-NOTES/) — dated experiments, measurements, failures, observations, and bench results.
- [`FIELD-MANUALS/`](FIELD-MANUALS/) — repeatable bring-up, test, fabrication, and lab procedures.
- [`research/`](research/) — Drone Libre-originated design studies that may become active projects.

### Research and Preservation

- [`research_archive/`](research_archive/) — structured references to outside projects and concepts. Entries progress from **source note** to **research reference**, **mirror**, and **tested reference**.
- [`RECOVERED-TECHNOLOGY-ARCHIVE/`](RECOVERED-TECHNOLOGY-ARCHIVE/) — salvaged, obsolete, unidentified, or repairable hardware and its reverse-engineering record.
- [`ARCHIVE-INDEX.md`](ARCHIVE-INDEX.md) — preservation strategy for active development, repository mirrors, engineering records, media, and cold storage.
- [DronLibre Rescue Logs](https://github.com/dronemaker-alt/DronLibre-Rescue-Logs) — active drone rescue, teardown, hardware-discovery, and recovery records.
- [AERIS-10 Mirror](https://github.com/dronemaker-alt/AERIS-10-Mirror) — preserved PLFM phased-array radar research reference; not a validated Drone Libre hardware baseline.

New outside research entries should start with the [mirror-entry template](research_archive/MIRROR_TEMPLATE.md). Record attribution, version, license status, preserved files, verification status, and test results.

Document what was observed, separate claims from verified results, and turn useful ideas into measurable experiments.

## Sustainable Engineering

One discarded electronic device can become an educational engineering platform.

Current work includes repurposing USB-C rechargeable vape power modules for:

- ESP32 projects
- Raspberry Pi systems
- Robotics
- Drone power

Reuse before recycling.

## Guiding Principles

- Open Hardware
- Open Documentation
- Repairability
- Reuse Before Recycling
- Measure Before Assuming
- Test Before Trusting
- Build. Document. Test. Share.

## Safety Philosophy

Engineering should improve lives—not put them at unnecessary risk.

Drone Libre work may involve lithium-ion batteries, high-current electronics, rotating machinery, fabrication equipment, RF systems, and embedded hardware. Safety is part of the design and validation process from the beginning.

Core rules:

- Inspect before powering.
- Measure before assuming.
- Test before trusting.
- Document before repeating.
- Replace questionable components rather than risking failure.

Recovered lithium-ion cells remain **unverified** until inspection and measured charge/discharge testing establish their condition. Detailed procedures belong in the [field manuals](FIELD-MANUALS/).

Engineering is about curiosity, but good engineering is also about responsibility.
