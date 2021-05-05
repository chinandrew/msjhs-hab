---
title: "Microcontrollers"
permalink: /flight20210313/microcontrollers/
layout: single
excerpt: "Microcontrollers for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---

Arduinos were used due to their vibrant ecosystem of sensors, active maker community, and approachability for new programmers. Each group was assigned one sensor and one arduino, as opposed to multiple groups being assigned a sensor to run off the same arduino. This meant students did not have to focus on integrating their code with another group (not a bad exercise, just complexity we didn’t want to introduce the first time around), and if any single group’s sensor code failures would not affect another group.

Arduino MKR Zero’s were chosen for their integrated micro SD card reader and small form factor. One downside is they run at 3.3V, while many sensors are 5V. This meant voltage dividers were required for some sensors, as well as appropriate corrections to the sensor readouts.

For brevity, “sensors” will generally refer to both the sensor and the Arduino pairing in this document.
