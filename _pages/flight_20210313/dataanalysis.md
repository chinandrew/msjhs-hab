---
title: "Launch"
permalink: /flight20210313/dataanalysis/
layout: single
excerpt: "Data analysis for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---
The data analysis assignment was not finalized until after we had recovered the payload, since we weren’t sure what we’d get back and what was feasible to do. 

Upon receiving the data, we structured and began analyzing the data to answer our predetermined questions as well as explore new ideas. This analysis was done primarily in Python. We couldn’t expect students to be familiar with Python and other popular analysis tools since AP CS teachers with Java, so we stuck to basic questions that could be answered in Excel. Despite this limitation, there were many results and challenges we encountered when doing basic plots that ended up being quite interesting. Most of the final questions ended up not being things that we had originally thought of. For example, determining the length of ascent and descent through any of the sensors turned out to be a fun and important exercise.

Each student group had come up with their own file formats, and we structured all of the data files into Comma Separated Values (CSV) files for the students instead of having them parse it. While parsing the strings to structure the data could have been an interesting assignment, we wanted to emphasize the analysis. 

Students were given the following questions along with the cleaned data and a data dictionary describing what each column of data represented for each file.
> 1. Plot temperature and pressure for the whole flight. Compute the minimum and maximum observed values during the flight for both.  
> 2. How long was the ascent? How long was the descent?  
> 3. Using data from the sensors, what orientation did the box land in?  
> 4. Plot all the MQ9 gas data. Do you notice anything strange?  
> 5. Plot the light sensor data. What might explain what you see (Hint: temperature)?  
> 6. Plot the UV data as a function of time. What might explain what you see? Are there any other sensors you could use to verify your hypothesis (Hint:  magnetometer)?  
> 7. (Optional challenge) Estimate the balloon burst altitude.  
> 8. Plot another set of data that was not already plotted above. Is there anything interesting the data might be telling you?   
> 9. Propose a new measurement or experiment for the second launch.  

In addition to the assignment, we also presented to each period with a small data cleaning and analysis activity using modern data science tools. This involved structuring a student data file into CSV format, plotting the data, and applying a moving average to reduce noise. It was primarily done in Python, with replication done in R and Excel for demonstration. We knew that it wasn’t possible to teach students new tools in only one period, so our goal was just to expose them to the tools and offer follow up resources if there was interest.



We discovered a number of extensions and additional learning opportunities when doing this analysis, and we spent many hours looking at questions that did not make the final cut for the assignment. Further discussion is in the [Postmortem and Takeaways - Student Activities]({{ "/flight20210313/studentactivitytakeaways/" | relative_url }}) section. 

To download the data and see examples of the analyses conducted, see the [Data]({{ "/flight20210313/data/" | relative_url }}) page.