---
title: "Sensors"
permalink: /flight20210313/sensors/
layout: single
excerpt: "Sensors for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---

Twelve sensors were flown in the payload. Some sensors were part of experiments we knew we wanted to measure, such as the tropopause via the temperature inversion, or contained telemetry we wanted to capture, such as GPS and altitude. Additionally, some sensors were flown simply because we were curious what they would read or how well they would work, such as the UV and magnetometer sensors.

Experiments and activities we had in mind included the following:
- Determine the altitude of the tropopause and observe the temperature inversion.  
- Determine CO2 and Ozone concentration with altitude.  
- Estimate the altitude using measurements other than the altimeter and GPS.  
- Compare the GPS and barometric altimeter readings.  
- Try to measure the change in the force of gravity at the top of the flight, which would be approximately 1% less. This would be accomplished by measuring the weight of the payload during the flight and correcting for upwards acceleration using the inertial measurement unit.  
- Recreate the flight using the inertial measurement unit.  
- Measure the diameter of the earth based on still photos.  

Some considerations when considering sensors:
- Federal regulations prohibits export of commercial GPS from functioning over 60,000 ft when travelling faster than 1,000 knots. As such, most commercially available GPS receivers will meet this regulation, and many GPS sensors stop functioning only based on the 60,000 ft requirement, so make sure any GPS sensor you fly does not do this and instead checks for both speed and altitude. NOTE: This GPS sensor is separate from our tracking GPS, which is only used for recovery of the payload after landing and not in flight telemetry (so any restricted functionality at altitude acceptable).   
- Temperature and altitude were important measurements to get, so we had redundant sensors. In addition to a temperature/humidity/pressure sensor and a GPS sensor, we also had a barometric altimeter that measured temperature.  
- Calibration of gas sensors can be difficult and require putting the sensor in multiple reference concentrations of the target gas. We were unsure how to do this, and decided due to time constraints to use default values for calibration constants and figure out more accurate corrections after the launch. It turned out that even without calibration, just looking at the relative changes in the sensor readings was informative, though proper calibration is still on our minds and may even make for interesting student activities (see [Postmortem and Takeaways - Student Activities]({{ "/flight20210313/studentactivitytakeaways/" | relative_url }})).  
- Failure to capture data was a very real possibility (and welcomed in some ways, since we considered that part of the learning process for students). We wanted to have enough data such that even if multiple failed, we would be able to conduct meaningful analyses.  

Each sensor would record a timestamp and measurement and write to an SD card. We did not technically synchronize the sensor timing for simplicity. Most of the sensor values would not change quickly (e.g. temperature and pressure), and so we figured a few second difference as we powered them on sequentially would not matter. Additionally, we could synchronize them after the fact by analyzing and offsetting the timestamps appropriately. Recording intervals varied from a maximum of 1 second to a minimum of 50 milliseconds.

For more information on what requirements were provided to students to program the sensors, see the [Student Activities - Sensor Development]({{ "/flight20210313/sensordevelopment/" | relative_url }}) section. For more on the analyses that came from the data, see the [Student Activities - Data Analyses]({{ "/flight20210313/dataanalyses/" | relative_url }}) section.