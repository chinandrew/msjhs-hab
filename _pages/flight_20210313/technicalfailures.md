---
title: "Technical Failures"
permalink: /flight20210313/technicalfailures/
layout: single
excerpt: "Technical failures for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---

We had a number of technical failures during our launch. They are presented below in no particular order.

1. GPS inconsistencies  

    a. The GPS tracker did not successfully send out a tracking ping until the day after the balloon landed. We suspect this was due to the payload landing upside down, which hinders the SPOT’s ability to transmit to a satellite. **Resolution**: We plan on flying redundant transmission systems, such as cell or LoRa, as well as design a system that will either increase the chances the GPS tracker lands face up, or a gimbal-like system so it faces up regardless of the payload orientation.   

    b. While we set the GPS to transmit every 2.5 minutes, we discovered that this was not the case in practice. We received multiple transmissions we were walking around the launch site with the container, but as soon as we launched the balloon all transmissions stopped. Even after recovering the payload, we noticed that transmissions were inconsistent when driving the payload around. This is still under investigation.  

2. Power failures  

    a. Despite a 3x margin on battery capacity for the cameras, both battery packs failed during the flight, likely due to the extreme temperatures. The battery chemistry for USB power banks is different from the lithium AAs used for the sensors, and is more susceptible to low temperatures. Though we originally had the idea of including an internal temperature sensor, we ended up not flying one since it wasn’t measuring an external atmospheric property, and we didn’t realize the batteries would fail. **Resolution**: We will switch all power systems over the lithium AAs for the next flight. We will also include an internal temperature sensor to learn how cold the batteries get.   

3. Sensor failures  

    a. The GPS sensor failed to record valid location and altitude values. It successfully wrote to the card for the whole flight, but only wrote blank values (i.e. did not connect to a satellite). We had checked that both the Arduino was capturing data and the GPS module was active, but we either misinterpreted the GPS module light, or there was some other interference going on (e.g. iron in the handwarmers accidently covered the GPS module). **Resolution**: This is twofold. The first is improved code and processes to verify that the GPS is logging. For example, the sensor was programmed to blink when writing to the SD card, regardless of if it was writing valid of invalid values. Second, we will fly a redundant GPS as part of failure (1).

    b. The barometric altimeter failed halfway through the ascent for unknown reasons. Other sensors connected to the same power source operated without issues for the duration of the flight. The values that were recorded were also noisier than values obtained from the other pressure sensor, shown in the picture below). This is still under investigation.  

    ![alt]({{ site.url }}{{ site.baseurl }}/assets/images/flight20210313/alti_thb_pressure_compare.jpg)
    {: .full}
    
    c. One group of sensors attached to the same battery pack reset at the end of the flight. This was apparent from the timestamps resetting. Two of the three sensors recovered and continued to record data with the reset timestamps, while a third did not. We estimate that the reset occurred seconds before landing, so there was little effect on post launch analysis. Why the sensors reset and why one of them did not recover is unknown, though we suspect it was related to the power systems.

    d. While not a sensor failure, one thing we did not realize was that many of the sensors would be highly temperature dependent, and thus provide inaccurate readings. For example, the light sensor (a photoresistor) and the load cell both exhibited trends suggesting they were affected by temperature. The plot of the load cell's 6 second moving average, light sensor, and temperature, all normalized between 0 and 1, is shown below. **Resolution**: Either fly sensors that are less affected by temperature (such as a photodiode instead of a photoresistor), or try to correct for the variation (such as comparing measurements when the temperatures are the same, which can occur due to the to the temperature inversion).	

    ![alt]({{ site.url }}{{ site.baseurl }}/assets/images/flight20210313/temp_dependence.jpg)
    {: .full}
    
    e. The ozone sensor SD card was returned corrupted and we were unable to read any data from it. We were unable to determine the root cause, and the data was lost.  

4. Camera failures  

    a. In the last 30 minutes of video recording, the action camera started to have weird artifacting where every few seconds a frame would glitch. It is unclear if this was due to the temperature or power loss. An example is shown below.

    ![alt]({{ site.url }}{{ site.baseurl }}/assets/images/flight20210313/camfail.png)
    {: .full}
    

In hindsight, we could have done a better job defining where we needed redundancy. Our initial planning had accounted for some of this, such as flying two altimeters, which unfortunately both failed in some way). However, we soon realized that not having GPS and altitude data was a large blow, and we should have flown an extra GPS as a backup. Similarly, having the GPS tracker nearly fail to transmit due to landing orientation was a huge risk, since recovery of the payload is a prerequisite for all further work. We had assumed that since we had good luck in the past with the SPOT trackers and they were built for commercial use, we wouldn’t have to worry much about their reliability. Though it ended up working, it was a bit less reliable than we’d like, and more emphasis will be placed on payload recovery in future launches.

There were a few unexpected results that in hindsight were obvious, such as the UV sensor showing a strong oscillating pattern as the box spun towards and away from the sun. This ended up being quite an interesting dataset to play around with and correlate against gyroscope and magnetometer measurements. Since nothing failed and we got interesting analyses from this, it was not considered a failure.
