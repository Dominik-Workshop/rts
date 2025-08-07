# RTS - Line Follower Robot

[![License](https://img.shields.io/github/license/Dominik-Workshop/rts)](https://github.com/Dominik-Workshop/rts/blob/main/LICENSE) ![Repo Size](https://img.shields.io/github/repo-size/Dominik-Workshop/rts)
![Microcontroller](https://img.shields.io/badge/uC-ATmega32-white)

<img src="images/pictures/LF-nb.png" alt="RTS photo">

## Overview

A line follower robot built to autonomously navigate a track marked by a black line on a white surface. The goal is for the robot to complete the track as quickly as possible.

### Key Features

- **16 reflective sensors** for precise line detection
- **PD controller** for responsive steering
- **Bluetooth module** for remote control and PID parameter calibration
- **Lightweight design** at just **~70g**

## Electronics

This project features two custom-designed PCBs that are connected via a flexible flat cable (FFC):

- [**Sensor board**](/pcb/sensor_board/) - contains 16 reflective sensors for line detection

<p align="center">
  <img src="images/renders/LF_front_PCB_top.png" width=90% alt="Sensor board render top">
  <img src="images/renders/LF_front_PCB_bottom.png" width=90% alt="Sensor board render bottom">
</p>

- [**Main board**](/pcb/main_board/) - responsible for the robot's core functionalities. It integrates the microcontroller, motor drivers, bluetooth module and power management circuitry

<p align="center">
  <img src="images/renders/LF_mainboard_PCB_top.png" width=90% alt="Main board render top">
  <img src="images/renders/LF_mainboard_PCB_bottom.png" width=90% alt="Main board render bottom">
</p>

## Mechanical

The PCBs are mechanically joined with a lightweight 3D-printed connection bar. The motor and battery mounts are also 3D-printed.

### Tires

Several tire types have been tested:

- **MINI-Z Low Height Slick Tire 40° MZW39-40**: This tire provided solid grip and durability, serving as a reliable baseline for testing.
- **MINI-Z LM Wide High Grip Tire 20° MZT302-20**: This tire offered superior grip, which led to improved cornering speeds, but at the cost of durability.
- **MINI-Z RACING SLICK WIDE TYRES 20° MZW17-20B**: Initial tests showed slightly less traction, and require further testing.

## Android App

A dedicated Android app allows for remote control and tuning of the robot. Its main functions include **PID parameter calibration** and the ability to **start and stop** the robot's run.

<div align="center">
  <img src="images/screenshots/Android_app_set.jpg" width=50% alt="Android app screenshot showing PID settings.">
</div>

## Troubleshooting

<details>
<summary><b>Microcontroller doesn't program</b></summary>

Make sure that the fusebits are set as bellow:
<img src="images/screenshots/atmega_fuses.png" alt="Fuse Bits Settings">
</details>

## Used Tools

<img src="images/logos/Eagle.png" align="center" height="64" alt="Eagle logo"> &nbsp;&nbsp;
<img src="images/logos/Fusion-360.png" align="center" height="64" alt="Fusion 360 logo"> &nbsp;&nbsp;
<img src="images/logos/Platformio_vscode.png" align="center" height="64" alt="PlatformIO logo"> &nbsp;&nbsp;
<img src="images/logos/MIT_app_inventor.png" align="center" height="64" alt="MIT App Inventor logo">
