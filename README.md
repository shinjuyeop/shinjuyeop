# Juyeop Shin

**Embedded Systems · Automotive Control · Edge AI**

Electrical & Electronic Engineering · Konkuk University

## About

I build embedded control software and the tools to test it, connecting STM32 firmware, ROS 2, and CAN actuators through hardware-in-the-loop (HIL) validation. My AI work extends from simulation and model evaluation to on-device inference and firmware integration.

Interests: embedded software, vehicle control, real-time systems, robotics, and on-device AI.

## Featured Engineering

### Autonomous Vehicle Control System — Team K.A.I.

**Control Part Lead** · Autonomous electric vehicle control and HIL validation

- Integrates a host PC with two STM32 controllers: **STM_A** handles drive, accelerator, and vehicle inputs; **STM_B** handles braking, physical E-stop inputs, and safety functions.
- Connects FreeRTOS firmware with ROS 2 Humble through micro-ROS and controls CAN-based actuators.
- Uses a React web HIL console and virtual LCD for bench validation, with attention to command timeouts, E-stop response, and fail-safe behavior.

Validation currently centers on the HIL bench; final integration checks on the vehicle remain pending.

**Built with:** C/C++ · STM32G4 · FreeRTOS · ROS 2 Humble · micro-ROS · CAN · HIL · React

[Project repository][kai-project] · Private; access required.

<!--
TODO MEDIA
File: assets/kai/vehicle.jpg
Content: Actual Team K.A.I. autonomous vehicle, preferably a clean side/front view in a driving or competition setting.
Recommended: landscape, around 16:9.
Activate after adding the file:
![Team K.A.I. autonomous electric vehicle](assets/kai/vehicle.jpg)
-->

<!--
TODO MEDIA
File: assets/kai/hil.png
Content: Full web HIL console screenshot with readable controls and bench observations.
Recommended: landscape, around 16:9; remove private identifiers before publishing.
Activate after adding the file:
![Team K.A.I. web HIL console](assets/kai/hil.png)
-->

<!--
TODO MEDIA
File: assets/kai/architecture.png
Content: Public overview of the host PC, STM_A, STM_B, actuators, and HIL bench.
Recommended: simple landscape diagram; omit internal protocols, pin maps, and implementation details.
Activate after adding the file:
![Team K.A.I. system architecture overview](assets/kai/architecture.png)
-->

<!--
TODO VIDEO
Content: Autonomous vehicle driving demo.
Use the vehicle photo as a thumbnail; replace VIDEO_URL with the supplied demo URL.
[![Watch the autonomous vehicle driving demo](assets/kai/vehicle.jpg)](VIDEO_URL)

Content: Web HIL / E-stop reaction demo.
Use the HIL screenshot as a thumbnail; replace VIDEO_URL with the supplied demo URL.
[![Watch the web HIL and E-stop demo](assets/kai/hil.png)](VIDEO_URL)
Activate each link only after its thumbnail and video URL are available.
-->

### Infineon FastReflex — Research

Early hazard detection for humanoid robots in **Unitree G1 / MuJoCo** simulation. A **PyTorch GRU** uses pelvis IMU signals to detect emerging hazards; a separate foot-sensor model provides terrain context.

The research covers reproducible evaluation, held-out experiments, and generalization across physical conditions. The baseline is supported within its original test conditions; generalization to new conditions remains unproven.

[Research repository][fastreflex-research] · [Deployment repository][fastreflex-deployment]

<!--
TODO MEDIA
File: assets/fastreflex/mujoco.png
Content: Unitree G1 in the MuJoCo viewer, with sensor or hazard visualization if readable.
Recommended: landscape, around 16:9.
Activate after adding the file:
![Unitree G1 hazard detection in MuJoCo](assets/fastreflex/mujoco.png)
-->

### Infineon FastReflex E84 — Edge Deployment

A separate deployment repository takes a frozen research model through **TFLite conversion, INT8 quantization, and Vela compilation** to the **PSoC Edge E84 / Ethos-U55**, with ModusToolbox firmware integration.

Research model → conversion / quantization → NPU deployment → firmware → HIL → runtime validation

Recorded board runs include Hazard and Terrain inference on the U55, sensor replay, and a live MuJoCo bridge. This is an engineering prototype: numerical parity and loss-free high-rate HIL remain unresolved, and real-robot validation is still outstanding.

[Deployment repository][fastreflex-deployment] · [HIL and runtime validation report][fastreflex-validation]

<!--
TODO MEDIA
File: assets/fastreflex/e84.jpg
Content: Actual PSoC Edge E84 board or HIL setup, with the board and connections clearly visible.
Recommended: landscape, around 16:9.
Activate after adding the file:
![PSoC Edge E84 inference and HIL setup](assets/fastreflex/e84.jpg)
-->

<!--
TODO VIDEO
Content: FastReflex MuJoCo + E84 inference demo.
Use the MuJoCo screenshot as a thumbnail; replace VIDEO_URL with the supplied demo URL.
[![Watch the MuJoCo and E84 inference demo](assets/fastreflex/mujoco.png)](VIDEO_URL)
Activate only after the thumbnail and video URL are available.
-->

## Side Projects

Small applications I built for everyday use with friends.

- **[ohnochoo][ohnochoo]** — A mobile-first music recommendation app where friends share songs, vote, and leave ratings. Built with React, TypeScript, Supabase Realtime, PWA installation, and Web Push on Vercel.
- **[whomadethis][whomadethis]** — A shared map of restaurants friends have visited, with ratings, reviews, photos, and visit records. Built with React, TypeScript, NAVER Maps, and Supabase, deployed on Vercel.

<!--
TODO MEDIA
File: assets/side-projects/ohnochoo.png
Content: Representative music recommendation and voting screen; use demo data or obtain consent for visible user content.
Recommended: one readable mobile or desktop screenshot.
Activate after adding the file:
![ohnochoo music recommendations and voting](assets/side-projects/ohnochoo.png)
-->

<!--
TODO MEDIA
File: assets/side-projects/whomadethis.png
Content: Representative restaurant map and review screen; use demo data or obtain consent for visible user content.
Recommended: one readable mobile or desktop screenshot.
Activate after adding the file:
![whomadethis shared restaurant map](assets/side-projects/whomadethis.png)
-->

## Tech Stack

**Embedded:** C · C++ · STM32G4 · FreeRTOS · CAN · UART

**Robotics & Vehicle:** ROS 2 · micro-ROS · HIL · MuJoCo

**Edge AI:** Python · PyTorch · TensorFlow Lite · INT8 quantization · Vela · Ethos-U55 · PSoC Edge E84

**Tools & Applications:** Linux · Git · ModusToolbox · React · TypeScript · Supabase

## Experience / Highlights

- **Control leadership:** Control Part Lead at Team K.A.I., working across vehicle control firmware, host software, and bench tools.
- **System validation:** HIL scenarios, E-stop and timeout behavior, sensor replay, and host-to-target numerical comparisons.
- **Research to hardware:** Separate model evaluation from deployment engineering, with frozen model handoffs and documented runtime results.

## Contact

[GitHub · @shinjuyeop](https://github.com/shinjuyeop)

<!-- TODO: Add LinkedIn -->
<!-- TODO: Add public contact email -->

<!--
Maintenance: Project summaries checked against repository READMEs on 2026-09-10.
Name, education, and Control Part Lead role supplied by the profile owner.
TODO: When a public K.A.I. showcase is available, update kai-project below
and remove the "Private; access required" note above.
-->

[kai-project]: https://github.com/TeamKAI-DL/Control
[fastreflex-research]: https://github.com/shinjuyeop/Infineon_FastReflex
[fastreflex-deployment]: https://github.com/shinjuyeop/Infineon_FastReflex_E84
[fastreflex-validation]: https://github.com/shinjuyeop/Infineon_FastReflex_E84/blob/main/reports/e84_hil_runtime_validation.md
[ohnochoo]: https://github.com/shinjuyeop/ohnochoo
[whomadethis]: https://github.com/shinjuyeop/whomadethis
