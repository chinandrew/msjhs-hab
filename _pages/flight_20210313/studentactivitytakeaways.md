---
title: "Student Activity Takeaways"
permalink: /flight20210313/studentactivitytakeaways/
layout: single
excerpt: "Takeaways for students activities for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---


For data analysis, many of the questions assigned to students ended up being ones we hadn’t previously thought about but ended up fitting the “simple and accessible, yet still engaging” criteria. This was due to a combination of flying interesting sensors without a specific question in mind, and also having to explore and create new assignments if certain sensors failed. The analyses we did could have been extended significantly, both in the number of variables explored as well as the complexity of the analyses. As mentioned in the [Student Activites - Data Analysis]({{ "/flight20210313/dataanalysis/" | relative_url }})  section, we conducted a number of analyses that were unfortunately cut from the assignment due to time or complexity constraints.

Additional opportunities for data analysis related learning include the following:  
- Additional analyses questions as mentioned above, including many of our original questions that were excluded.  
- Data smoothing and signal processing techniques (moving averages, convolutions, polynomial fitting).  
- Estimating integrals and derivatives from the data.  
- Further instruction on data science tools like Python or R.  
- Data visualization activities.  
- String parsing to structure raw data to CSV.  

For sensor development, there were a few improvements we could have made to minimize revisions and help students succeed.  
- Have students test the Arduinos as soon as they receive them. Many students did not do this until the weekend before the assignment was due, and so debugging the connection took time away from working on code.  
- Have students include any external libraries they used. Forgetting this was just an oversight on our part.  
- We requested the students submit a file of example data, but did not make it clear that this file should have been recorded data from the SD card. Many groups used output from the serial monitor, and as a result missed bugs that occurred when writing to the SD card.  
- The data capture intervals should have been specified more clearly. We only mandated that sensors captured data every 1 second or more frequently, and received code that recorded data at multiple different intervals. While not a real technical problem (which was why we didn’t specify originally), it would be simpler for everyone using the data if it was all recorded at the same interval.  

Our ideas for extensions to sensor development mostly revolve around increasing the complexity of the programs or the requirements, such as synchronized timing or more robust failure prevention.

For payload construction, COVID prevented us from involving students as much as we’d like. We personally found it challenging and entertaining, and believe it would be excellent for students to participate in for future years. Learning opportunities include the following:  
- Circuit design for power systems and sensors.  
- Calibration of sensors. We internally proposed a number of methods for achieving reference concentrations of gases like CO2, and believe it could be an interesting chemistry assignment.  
- Implementation of redundant tracking measures. There is both an electronics side of this, such as the construction and programming of LoRa transmitters and receivers, but also a mechanical side related to mounting antennas and modules so they are in the right orientation during and after the flight (for example, putting the SPOT tracker on a gimbal so it always faces the sky).  
- Engineering of the payload container, such as mounting points and internal heating. For example, we discussed using a custom built styrofoam box to our exact proportions, but didn’t do it due to time constraints.  
- More generally, we believe it is useful for students to be invested in the success of the launch, and that this is more easily done if they help create the launch container, flight hardware, and plan the launch themselves.  
