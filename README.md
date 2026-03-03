# India Space Lab: Winter Internship Project Portfolio

This repository contains the projects completed during the **Winter Internship** at **India Space Lab**, focusing on Advanced Drone Technology and CanSat Avionics.

---

## 1. Advanced Drone Technology: Cessna 210 Recreation

**Objective:** To model a complete fixed-wing aircraft, the Cessna 210 (NASA Variant), using geometric parameterization in OpenVSP.

### Modeling Process

The model was constructed by analyzing 3-view 2D blueprints to create an accurate 3D digital representation.

* **Wing Design:** Utilized a default NACA airfoil with a span of exactly **36.748 ft**. The wing was translated along the Z-axis to achieve the signature high-wing configuration.


* **Fuselage:** Modeled with an overall length of **24.580 ft**. The XSec Editor was used to flatten the aircraft's belly and match the nose curvature.


* **Empennage:** The horizontal tail (12.990 ft span) and vertical tail (2.94 ft height) were created using scaled and rotated wing geometries.



### Project Screenshots

---

## 2. CanSat Dual Redundant System

**Objective:** Design a fail-safe, dual-redundant avionics architecture and mechanical structure for a CanSat aerospace module.

### Avionics Architecture

The system utilizes two completely independent control paths on a single PCB to ensure mission-critical fault tolerance.

* **MCU Isolation:** MCU-1 (Primary) and MCU-2 (Secondary) share no control pins.


* **Sensor Redundancy:** Each MCU operates on a separate I²C bus with independent altimeters and IMUs.


* **Power Management:** A 5V regulator powers the servos to prevent mechanical current spikes from causing logic brownouts in the MCUs, which are powered by a distinct 3.3V path.



### Mechanical Integration

* **Redundant Actuation:** Two independent servos are mounted to a single parachute latch; either servo alone can release the parachute.


* **PCB Layout:** Components are grouped spatially (Primary on top, Secondary on bottom) to prevent data trace interference.



### System Verification Checklist

* [x] Single PCB Construction 


* [x] Simultaneous Power to both MCUs 


* [x] Zero sensor/servo sharing 



---

## Tools Used

* **OpenVSP:** Geometric aircraft modeling.


* **EasyEDA/KiCad:** PCB Schematic and Layout design.


* **CAD Software:** Mechanical structure and latch mechanism design.


