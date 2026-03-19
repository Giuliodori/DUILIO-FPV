<p align="left">
  <img src="docs/images/logo_duilio.png" alt="Duilio logo" width="220" />
</p>

# DUILIO FPV — Limitless Remote Control

<p align="left">
  <img src="docs/images/lawn_mover_p46_4wd.png" alt="Duilio FPV platform" width="720" />
</p>

## Real-time remote control. No distance limits.

Duilio FPV enables real-time remote control of vehicles and machines from anywhere using Wi-Fi mesh and 4G/5G networks.

Built to remove physical barriers, Duilio FPV brings real-world actions into the digital space with a game-like operator experience.

---

## At a glance

| Topic | Summary |
|---|---|
| Latency | Real-time remote control designed for ultra-low delay operation |
| Connectivity | Wi-Fi mesh and 4G/5G network support |
| Control | PC operator station with live first-person visual feedback |
| Safety | Failsafe-first architecture and supervised operation |
| Telemetry | Monitoring and diagnostics-ready workflow |
| Architecture | Distributed system (PC + Raspberry Pi + STM32 real-time control) |

---

## Highlights

- Unlimited range remote control over WiFi and 4G/5G
- Ultra-low latency real-time operation
- Fully open source (GPLv3)
- Hardware-agnostic design
- Distributed architecture (PC + Raspberry Pi + STM32)
- Built-in safety and failsafe logic

---

## How the System Works

As with a videogame, the operator controls the vehicle from a PC with a gamepad while viewing the onboard camera feed in first person.

```mermaid
flowchart LR
    A["Offboard system (PC + monitor + gamepad)"]
    B["Encrypted VPN"]
    C["Onboard system (Rpi5 + camera)"]
    D["Duilio F4 (motion control)"]
    A --> B
    B --> A
    B --> C
    C --> B
    D --> C
    C --> D
```

Core flow:

1. Low-latency connection  
   Video and commands are transmitted over Wi-Fi mesh or 4G/5G, with encrypted VPN communication.

2. Remote control station (PC)  
   The operator sends driving commands and receives live audio and visual feedback.

3. Integrated safety logic  
   Automatic failsafe behavior and supervision mechanisms support safe operations.

4. Telemetry and diagnostics  
   Operational data can be monitored and logged for analysis.

---

## Core Features

- Fully open source (GPLv3), designed to be transparent, hackable, and extensible
- Hardware-agnostic system adaptable to a wide range of machines (RC, robotics, industrial)
- Distributed architecture with Raspberry Pi (high-level control) and onboard control nodes
- Hybrid connectivity (WiFi + 4G/5G) for unlimited range with automatic failover
- Real-time remote control with ultra-low latency pipeline
- Audio and video streaming for FPV operation
- Gamepad-based control interface
- Runtime flexibility:
  - Instant switching between vehicles and operators

---

## Duilio F4 — Advanced Features

- Dedicated STM32 real-time control for precise and reliable actuation
- Scalable multi-node system using robust RS-485 bus for motors and peripherals
- Multi-mode motor control:
  - Speed control (DC motors)
  - Position control (servo/actuator)
- Advanced safety system:
  - Multi-layer failsafe
  - Fail-off logic
  - Watchdog monitoring
  - Safe state fallback
- Local RC control with priority override over remote commands
- Relay outputs for external device control:
  - Lights
  - Thermal engine ignition
  - Horn
  - Auxiliary systems
- Integrated telemetry system with real-time data:
  - Battery voltage
  - Speed (km/h)
  - Temperature
  - Obstacle distance
  - Network signal quality (WiFi / 4G / 5G)
  - Real-time latency monitoring
- GPS support:
  - Live map visualization
  - Real-time position tracking
- IMU integration with feedback (including vibration on gamepad)
- Assisted driving features:
  - Straight-line stabilization
  - Basic autopilot support
- Advanced remote interface:
  - Live gauges (speed, compass, timers, vehicle info)
  - On-screen messages and diagnostics
- Media control:
  - High-resolution photo capture
  - Dynamic video resolution control from gamepad
- Full system monitoring:
  - Trip data (distance, total time, total km)
  - System status and diagnostics
- Remote logging and diagnostics (e.g. via Telegram)

---

## Why Duilio FPV

Unlike traditional RC systems, Duilio FPV is designed as a real distributed control platform:

- No distance limits
- Network-based control instead of proprietary RF
- Scalable multi-node architecture
- Support for both hobby and industrial systems
- Built for real-world applications, not just prototyping

---

## Architecture

The project is divided into:

- Onboard (Raspberry Pi)  
  Control, communication, sensors, and low-level logic  
  https://github.com/giuliodori/duilio_fpv_onboard

- Offboard (PC)  
  UI, control interface, and remote management  
  https://github.com/giuliodori/duilio_fpv_offboard

---

## Project Goal

Duilio FPV was born from a real need: enabling a person with a physical disability to mow the lawn remotely.

The vision is to remove physical barriers and bring real-world actions into the digital space — allowing anyone to operate machines, explore environments, and perform tasks from anywhere.

From this starting point, the project expands toward robotics, remote vehicles, and distributed automation systems.

---

## Status

Active development — core architecture is functional and continuously evolving.

---

## Ecosystem

- Duilio FPV → main project hub
- Onboard system → Raspberry Pi control layer
- Offboard system → PC interface and remote control
- Duilio F4 hardware → https://github.com/Giuliodori/duilio_f4

---

## Stack & Integrations

![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-C51A4A?logo=raspberrypi&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?logo=debian&logoColor=white)
![Arducam](https://img.shields.io/badge/Arducam-005BAC?logo=camera&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Windows](https://img.shields.io/badge/Windows-0078D6?logo=windows&logoColor=white)
![WireGuard](https://img.shields.io/badge/WireGuard-88171A?logo=wireguard&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?logo=webrtc&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-4A4A4A?logo=socketdotio&logoColor=white)
![DuckDNS](https://img.shields.io/badge/DuckDNS-FFCC00?logo=duckduckgo&logoColor=black)

---

## Author

Fabio Giuliodori  
Founder & Creator — Duilio FPV  

Website: https://duilio.cc  
LinkedIn: https://linkedin.com/in/fabio-giuliodori  
Email: info@duilio.cc
