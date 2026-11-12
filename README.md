# Relux-TC
Relux-Custom-Toolchanger

[![Part of Relux-9X](https://shields.io)](https://github.com)
[![YouTube](https://shields.io)](https://youtube.com)
[![Firmware](https://shields.io)](https://klipper3d.org)

**Relux-TC** is a custom, ground-up toolchanger and multi-material extruder system engineered specifically for Klipper and high-acceleration Linear Magnetic Drives (LMD). Developed as the core toolhead architecture for the [Relux-9X](https://github.com), it is built to handle abrasive engineering composites (ABS-CF, ASA-GF) and rapid, automated filament changes.

---

## 🙏 Inspiration & Credits

This project is heavily inspired by the brilliant mechanical engineering of **dumplinglab** and the **YUDX** project. 

While following the development and participating in discussions on the YUDX Discord community, the vision emerged to adapt this rapid-docking philosophy to a completely custom Klipper architecture. **Relux-TC** is an independent, ground-up CAD redesign built from scratch to meet the specific kinematic, electronic, and multi-filament requirements of the Relux-9X production cell. Massive thanks to dumplinglab for pioneering such a clean and fast docking concept!

---

## 🛠️ What Makes Relux-TC Different?

While inspired by rapid mechanical docking principles, Relux-TC introduces several major hardware and electronic departures tailored for autonomous manufacturing:

* **HGX-Lite Extruder Gears.** Built around large-diameter, hardened steel HGX-Lite drive gears. This provides massive grip and torque for pushing abrasive carbon- and glass-fiber filaments without grinding or slipping.
* **Triple & Quad Extruder Architecture.** Engineered to support multi-filament shared-path configurations on a single toolhead. This works seamlessly alongside an external 32-spool RFID AMS matrix.
* **Dual Filament Cutter System.** Features mechanical filament cutters integrated into **both the carriage and the dock**. This ensures clean, string-free filament tips during high-speed tool swaps and automated AMS unloading cycles.
* **Custom Toolhead PCB & Pogo-Pin Interface.** Eliminates umbilical cable drag on the lightweight carbon gantry. A custom PCB integrates a spring-loaded Pogo-Pin array with outermost hardware presence loops (safety interlocks), fan tachometry, and onboard RGB status LEDs.
* **Integrated Filament Sensing.** Equipped with dedicated entry and buffer sensors to support automatic filament loading and synchronized dual-motor extrusion (`SYNC_EXTRUDER_MOTION`).
* **Native Klipper & LMD Tuning.** Designed around Klipper macros and current-limited docking routines. This protects the carbon-fiber gantry from the high instantaneous forces of a beltless Linear Magnetic Drive.

---

## 🚀 Development Roadmap

Relux-TC follows a modular, self-replicating build strategy—starting with a single active toolhead that prints the components for its own expansion.

- [x] **Concept & Architecture:** Initial CAD layout and community teaser on Discord.
- [ ] **Phase 1 (Mechanical Bench Test):** Single dock and carriage coupling test to validate alignment and Pogo-Pin contact resistance.
- [ ] **Phase 2 (Toolhead T0):** First active HGX-Lite toolhead with custom PCB and dual-cutter validation.
- [ ] **Phase 3 (Self-Replication):** Printing ABS-CF docks and housings for Toolhead T1 and running 100-cycle automated swap tests.
- [ ] **Phase 4 (Full Array):** Scaling to 9 filament toolheads plus the reserved `[TOOL_X]` slot.

---

## 📂 Repository Structure

*(Files will be uploaded as each mechanical and electronic stage is tested and documented on YouTube)*

```text
├── CAD/                 # SolidCraft STEP files, toolhead bodies, docks & cutter mechanisms
├── PCB/                 # Custom toolhead schematics, Gerber files & Pogo-Pin assignments
├── Klipper/             # Toolchange macros, cutter sequences & status LED controls
└── BOM/                 # Hardware lists (HGX-Lite gears, Pogo-Pins, magnets & bearings)
```

---

## 🤝 Follow the Build

Watch the prototyping, macro testing, and full assembly logs on **TMcTrain TechLab**:
* **YouTube:** [TMcTrain TechLab](https://youtube.com)
* **Discord:** `@TMcTrain`
