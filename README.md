<p align="left">
  <img src="docs/images/logo_duilio.png" alt="Duilio logo" width="220" />
</p>

# DUILIO FPV - Limitless Remote Control

<p align="left">
  <img src="docs/images/campo.png" alt="Duilio FPV at work in the field" width="720" />
</p>

Real-world operation: Duilio FPV at work in the field.

## Real-time remote control. No distance limits.

Duilio FPV enables real-time remote control of vehicles and machines from anywhere using Wi-Fi or 4G/5G networks.

Built to remove physical barriers, Duilio FPV brings real-world actions into the digital space with a game-like operator experience.

## At a Glance

| Topic | Summary |
|---|---|
| Latency | Real-time remote control designed for ultra-low delay operation |
| Connectivity | Wi-Fi mesh and 4G/5G network support |
| Control | PC operator station with live first-person visual feedback |
| Safety | Failsafe-first architecture and supervised operation |
| Telemetry | Monitoring and diagnostics-ready workflow |
| Architecture | Distributed system (PC + Raspberry Pi + STM32 real-time control) |

## Highlights

- Unlimited range remote control over Wi-Fi and 4G/5G
- Ultra-low latency real-time operation
- Hardware-agnostic design
- Distributed architecture (PC + Raspberry Pi + STM32)
- Built-in safety and failsafe logic
- Optimized integration with Duilio F4 hardware

## How the System Works (Basic Features)

As with a videogame, the operator controls the vehicle from a PC with a gamepad while viewing the onboard camera feed in first person.

<p align="left">
  <img src="docs/images/simple_overview.png" alt="Basic configuration" width="720" />
</p>


Core flow:

1. Low-latency connection
   Commands and video are exchanged over Wi-Fi or 4G/5G networks.
2. Remote control station (PC)
   The operator sends commands and receives live video/audio feedback.
3. Onboard processing (Raspberry Pi)
   Handles communication, video streaming, and high-level logic.
4. Real-time control (Duilio F4)
   Executes precise motor control and safety-critical functions.

Basic feature set (Raspberry Pi-based deployment):

- Real-time audio/video streaming with ultra-low latency
- Full HD H.264 video quality with on-the-fly configuration
- Secure connectivity via WireGuard VPN
- Easy installation and configuration
- Multi-machine / multi-operator configuration
- Telemetry and remote configuration via Telegram
- GPS support for real-time position visualization
- Assisted driving autopilot
- Stopwatch / chronometer
- Temperature data
- Multi-camera support
- Audio support
- Wi-Fi / mobile network / phone tethering support
- Radio signal status visualization
- RC steer/speed support
- GPIO lights control
- GPIO horn control
- GPIO engine starter control
- GPIO engine shutdown control
- Full-resolution 4K photo capture and Telegram delivery
- Telemetry delivery via Telegram

## How the System Works (Advanced Features with Duilio F4 Board)

Additional capabilities enabled by the Duilio F4 hardware platform:

- Tachometer
- Battery data
- Instant power data
- Slope / incline data
- Distance traveled / trip data
- Power relay output for lights
- Power relay output for horn
- Power relay output for engine starter
- Power relay output for engine shutdown
- Local 4-channel RC radio control
- Integrated failsafe systems
- 7–43V power input for Raspberry Pi and auxiliaries
- Precision RC servo outputs
- PWM/DIR outputs for high-power drivers (speed and position control)
- On-the-fly speed limiter
- Support for 2 sonars with real distance visualization
- 4WD / 6WD operating modes
- RS-485 expansion for additional boards, motors, outputs, and inputs
- EMI/TVS filters and disturbance protection

## Ecosystem Repositories

### Onboard

Machine-side software, typically running on Raspberry Pi-class hardware.

- Repository: [duilio_fpv_onboard](https://github.com/giuliodori/duilio_fpv_onboard)
- Scope: communication, control, sensors, low-level logic, hardware integration

### Offboard

Operator-side software, typically running on a PC.

- Repository: [duilio_fpv_offboard](https://github.com/giuliodori/duilio_fpv_offboard)
- Scope: user interface, remote control, telemetry visualization, operator workflow

### Hardware

Reference hardware platform optimized for the ecosystem.

- Repository: [duilio_f4](https://github.com/Giuliodori/duilio_f4)
- Scope: tested electronics base for tighter integration and higher reliability

## Why Duilio FPV

Unlike traditional RC systems, Duilio FPV is designed as a real distributed control platform:

- No distance limits
- Network-based control instead of proprietary RF
- Scalable multi-node architecture
- Support for both hobby and industrial systems
- Built for real-world applications, not just prototyping

## Project Goal

Duilio FPV was born from a real need: enabling a person with a physical disability to mow the lawn remotely.

The vision is to remove physical barriers and bring real-world actions into the digital space, allowing anyone to operate machines, explore environments, and perform tasks from anywhere.

From this starting point, the project expands toward robotics, remote vehicles, and distributed automation systems.

## Repository Scope

This repository is the main Duilio FPV hub and project presentation. Most implementation code lives in the dedicated repositories above.

Choose your entry point:

1. Start from `offboard` if you want to see the operator experience and interface layer.
2. Start from `onboard` if you want to inspect machine-side logic and hardware interaction.
3. Start from `duilio_f4` if you want the reference electronics platform.

## Status

Active development - core architecture is functional and continuously evolving.

Current focus:

- reliability and failsafe validation
- telemetry quality and diagnostics
- deployment hardening for real-world operation

## Contributing

Contribution guidelines are in [CONTRIBUTING.md](CONTRIBUTING.md).

In short:

- use this repository for hub-level issues and documentation updates
- open code-specific issues and pull requests in the relevant subproject repository

## Author

Fabio Giuliodori
Founder and Creator, Duilio FPV

- Website: https://duilio.cc
- LinkedIn: https://linkedin.com/in/fabio-giuliodori
- Email: info@duilio.cc

## License

This repository is distributed under the GPL-3.0 license. See [LICENSE](LICENSE).
