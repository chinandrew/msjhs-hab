---
title: "Launch"
permalink: /flight20210313/sensordevelopment/
layout: single
excerpt: "Sensor development for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---

For the sensor development, students self organized into groups of three. Participation was voluntary, and those that volunteered were exempt from a separate assignment that was run concurrently. While 12 sensors would allow for 36 students, we ended up with 39 interested students, so we had one group work on a duplicate GPS sensor to accommodate.

Sensors were given to a parent volunteer to hold for distribution. Students would contact the parent beforehand to schedule a pick up date, and would document their retrieval of the sensor on a Google Sheet. We had duplicates of every sensor so the students could have and work on one copy while we developed the flight hardware independently. It also gave us redundancy in case a sensor broke or we failed to recover the first launch.

The student timeline was as follows:

| February 5, 2021         | Groups formed, sensors available for pickup.             |
| February 15, 2021        | Additional sensor-specific office hours between 10AM-3PM |
| February 16 and 17, 2021 | Short oral progress report in class                      |
| February 22, 2021        | Assignment due                                           |


To make the assignment more than just coding, we requested an additional writeup. This writeup would describe their hardware and software, and required explaining their design and doing research into their sensors to learn how they worked. Our intention was to show that software engineering goes beyond just solving programming problems, and involves users, devices, and interacting with real world scenarios.

We also debated how specific the code requirements should be. For example, to what extent should we specify the output file format? How many edge cases should we make them aware of? We had independently programmed and tested each sensor ourselves, and had run into some common issues ourselves. While we wanted to give students the freedom to make design decisions, we also wanted to ensure a successful flight. In the end, we tried to specify requirements that we thought would be robust against failure, while not providing too much detail into how to achieve them. Our hope was that the requirements, student testing, and our own testing would catch any issues.

Ultimately, students were given the following instructions:  

> 1. Data logging code (ino file) - This is the code that will run on the Arduino. You are free to use any libraries for the sensors or Arduino to complete this. Code most conform to the following requirements:  
>
>     a. On loss of power, all data up to the past minute must not be lost.  
>
>     b. If the SD card runs out of storage, all data up to the past minute must not be lost.  
>
>     c. If the SD card is removed during operation, all data up to the past minute must not be lost.  
>
>     d. There must be visual indication that the sensor is successfully capturing and storing the data.  
>
>     e. Data must be captured at <=1s intervals.  
>
>     f. If you are also computing a derived value from the raw sensor value (e.g. calculating altitude from the barometric pressure), you must retain the raw sensor data as well.  
>
>     e. Each data point must be timestamped with the number of milliseconds since bootup with the millis() function, as well as a timestamp using the on board real time clock.  
>
>     h. Data must be stored as one or multiple text files on the SD card.  
>
>     i. All software must run automatically on power up with no human intervention.  
>
>     j. Data logging to SD card must continue to function when the device loses power and regains power.  
> 2. Documentation/writeup (pdf) - This documents how your sensor works and the design decisions you made to develop it. There should be three sections:     
>
>     a. User Guide: How does your Arduino visually indicate that it’s working? What is the output data format? How often is data captured?  
>
>     b. Development/Design Process: How did you decide on the various choices relating to the user experience in (2a) and the requirements in (1)? How did you test that the requirements in (1) were met?   
>
>     c. Hardware Overview: Do some research and write a short description of how the sensor measures the quantity of interest and how it communicates that measurement to the Arduino.  
> 3. Test data (txt file) - Using your sensor, capture measurements from three different environments to show different readings. For example, putting a temperature sensor outdoors, in a refrigerator, and by a heating vent. These can be three separate captures or a single continuous movement between the environments. Please specify the details in your submission.  

In order to support the students, we set up a Discord chat room for students to ask questions, and also hosted a full day office hours session a week before the due date. Both of these were utilized by multiple groups.

We tested each group’s code upon submission, powering the sensors with the same batteries as we would use on flight day and verifying the SD cards captured data successfully. These tests were in addition to the dry run described in [Flight and Recovery - Preflight Testing and Dry Run]({{ "/flight20210313/testingdryrun/" | relative_url }})

For most groups, we ended up having to make minor modifications to the code to make it work. These modifications were minor enough that we didn’t feel the need to have students revise them. For example, removing a `while(!Serial)` statement since the battery powered Arduinos would never connect to the serial monitor (but students testing with the Arduino connected to their computer with the serial monitor open would not notice). All changes were documented for students to review afterwards. More discussion on how we could have given clearer instructions can be found in [Postmortem and Takeaways - Student Activities]({{ "/flight20210313/studentactivitytakeaways/" | relative_url }}) section.