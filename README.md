# Tritium Legacy Software & Documentation Archive

Community archive of legacy Tritium motor controller, BMS, and CAN tools — preserved for solar car teams and developers.

> [!WARNING]
> This repository contains legacy Tritium software, firmware, logs, and documentation collected over multiple years by our solar car team. It is **not official, not supported, and not endorsed by Prohelion** (who acquired Tritium). All firmware files are provided as-is with no guarantees of correctness, safety, or compatibility. **Flashing incorrect firmware can permanently damage your hardware. Use at your own risk.**

---

## Repository Structure

```
├── logs/
├── tritium-battery-management-system/
├── tritium-can-ethernet-bridge/
├── tritium-driver-controller/
└── wave-sculptor-controller/
```

---

## 📁 logs/

Historical CAN logs and vehicle data collected by our solar car team over the years.

Useful for reference data during software development, comparing telemetry values, debugging similar vehicle architectures, and understanding real-world CAN traffic patterns. If you are not part of our team, these logs may not directly apply to your system, but can still serve as helpful reference material.

---

## 🔋 tritium-battery-management-system/

Documentation and software related to the Tritium BMS.

**Includes:** PDF user manuals, datasheets, wiring references, and the legacy BMS Viewer software.

> [!NOTE]
> Some documentation may refer to different BMS revisions. Please verify compatibility yourself.

### BMS Viewer

Legacy Tritium BMS configuration and monitoring software. Use it to view CMU data, monitor pre-charge state, errors, cell balancing, SOC, and temperature extremes, as well as configure CMUs and BMS settings and manage logs.

---

## 🌐 tritium-can-ethernet-bridge/

Documentation, firmware, and software for the Tritium CAN–Ethernet bridge.

**Includes:** User Manual (PDF), Datasheet (PDF), Ethernet Interface Documentation (PDF), `IM_bridge_1_04.tab` firmware file, CAN Bridge Config, and CAN Logger.

> [!WARNING]
> It is unclear whether modifications were made to the included firmware. Verify carefully before flashing.

### CAN Bridge Config

Configures and manages the Tritium CAN–Ethernet bridge. Features include viewing bridge and local interface IPs, setting a static IP, checking protocol version, configuring the virtual bus number, changing CAN bitrate (e.g. 250 kbps vs. 500 kbps), and flashing new firmware. Bitrate configuration is especially important when MPPTs run at 250 kbps while the driver controller defaults to 500 kbps.

### CAN Logger

Monitors all CAN traffic on the vehicle network. Displays CAN IDs and raw data payloads, supports live monitoring, and can log data to file. Useful for debugging, reverse engineering, and system validation.

---

## 🕹️ tritium-driver-controller/

Documentation and tools related to the Tritium Driver Controller.

**Includes:** User Manual (PDF), Overlay (PDF), Schematic (PDF), and the DC Test executable.

### DC Test

A highly capable debugging tool that can emulate or read data from a driver controller and simulate WaveSculptor telemetry. Displays base CAN ID, setpoint velocity/RPM, setpoint current, device type, serial, mode, errors, and active switches. Telemetry simulation covers bus voltage and current, velocity/RPM, ETS temperature, and motor temperature. Ideal for bench testing and debugging vehicle control systems.

---

## ⚡ wave-sculptor-controller/

Documentation, firmware, and software related to the Tritium WaveSculptor motor controller.

**Includes:** Multiple PDFs, `VS22_release_1_11.TSF` firmware file, DRIFVLoad, and WSConfig.

> [!WARNING]
> The included firmware file has not been verified for modification. Inspect and validate before flashing. No responsibility is taken for hardware damage.

### DRIFVLoad

Tritium firmware loader used for programming Tritium CAN devices including motor controllers. Allows you to select a base CAN address, select a firmware file, and flash firmware to a CAN device.

### WSConfig

The primary tool for working with WaveSculptor motor controllers. Displays active motors, CAN errors, setpoint, bus voltage, controller power, velocity, rail voltages, and motor temperature. Supports controls configuration, phasing, parameter extraction, IM extract, telemetry monitoring, and logging.

---

## 🎯 Purpose

This archive exists to preserve legacy Tritium tooling, help solar car teams maintain older vehicles, support developers building custom vehicle software, and prevent institutional knowledge from being lost.

If this archive helps your team, consider contributing missing documentation, verified firmware, compatibility notes, or corrections.

---

## ⚖️ Legal & Responsibility Notice

All trademarks belong to their respective owners. This is a historical archive maintained by the community. No guarantees are provided. Always verify firmware integrity before flashing any hardware.
