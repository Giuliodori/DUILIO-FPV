# DUILIO FPV — Limitless Remote Control

> Real-time remote control. No distance limits.

Duilio FPV enables ultra-low-latency remote driving and machine operation from anywhere, using Wi-Fi mesh and 4G/5G connectivity.

Built to remove physical barriers, Duilio FPV brings real-world actions into the digital space with a game-like operator experience and industrial-grade control logic.

### At a glance

| Topic | Summary |
|---|---|
| Latency | Real-time remote control designed for ultra-low delay operation |
| Connectivity | Wi-Fi mesh and 4G/5G network support |
| Control | PC operator station with live first-person visual feedback |
| Safety | Failsafe-first architecture and supervised operation |
| Telemetry | Monitoring and diagnostics-ready workflow |

---

## Key Features

- **Ultra-low latency control**  
  Real-time responsiveness for precise driving and operation.

- **Unlimited range**  
  Operate from virtually anywhere through Wi-Fi mesh and 4G/5G networks.

- **High-quality communication**  
  Smooth control and robust video streaming for long-distance operation.

- **Modular architecture**  
  Separate onboard (Raspberry Pi) and offboard (PC) components.

- **Hardware-agnostic design**  
  Supports multiple motor control methods (PWM, step/dir, analog, and more).

- **Safety and reliability**  
  Designed with failsafe-first principles for real-world operation.

---

## How the System Works

As with a videogame, the operator controls the vehicle from a PC with a gamepad while viewing the onboard camera feed in first person.

```mermaid
flowchart LR
    A[Operator PC + Gamepad] --> B[Encrypted VPN over Wi-Fi mesh or 4G/5G]
    B --> C[Onboard Control System (Raspberry Pi)]
    C --> D[Vehicle Actuation + Camera Feedback]
    D --> A
    C --> E[Telemetry & Diagnostics]
    E --> A
```

Core flow:

1. **Low-latency connection**  
   Video and commands are transmitted over Wi-Fi mesh or 4G/5G, with encrypted VPN communication.
2. **Remote control station (PC)**  
   The operator sends driving commands and receives live visual feedback.
3. **Integrated safety logic**  
   Automatic failsafe behavior and supervision mechanisms support safe operations.
4. **Telemetry and diagnostics**  
   Operational data can be monitored and logged for analysis.

---

## Architecture

The project is divided into:

- **Onboard (Raspberry Pi)**  
  Control, communication, sensors, and low-level logic  
  https://github.com/giuliodori/duilio_fpv_onboard

- **Offboard (PC)**  
  UI, control interface, and remote management  
  https://github.com/giuliodori/duilio_fpv_offboard

---

## Project Goal

Duilio FPV was born from a real need: enabling a person with a physical disability to mow the lawn remotely.

The vision is simple but powerful — bringing physical actions into the digital world, so anyone can operate machines and perform real tasks from anywhere.

From this starting point, the possibilities expand to robotics, remote vehicles, automation, and many other real-world applications.

---

## Status

Work in progress — core architecture is under active development.

---

## Ecosystem

- **Duilio FPV** → main project hub
- **Onboard system** → Raspberry Pi control layer
- **Offboard system** → PC interface and remote control
- **[Duilio F4 hardware](https://github.com/Giuliodori/duilio_f4)** → optimized hardware platform

---

## Author

**Fabio Giuliodori**  
Founder & Creator — Duilio FPV  
Building real-world remote control systems without limits

🌐 Website: https://duilio.cc  
🔗 LinkedIn: https://linkedin.com/in/fabio-giuliodori  
✉️ Email: info@duilio.cc
