---
title: "Recovery and Flight Analysis"
permalink: /flight20210313/recoveryanalysis/
layout: single
excerpt: "Recovery and flight analysis for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---

After releasing the balloon, we began driving south towards our predicted landing site. As mentioned in [Hardware - Tracking]({{ "/flight20210313/tracking/" | relative_url }}), we knew that we would probably not receive any tracking information until the balloon landed. We ended up waiting many hours beyond our estimated flight time without receiving a response, and went home for the day.

The next morning, we received an update from our GPS. The box had landed southwest of Fresno in the middle of a field and was easily recovered. 

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/flight20210313/trajectory.png)
{: .full}

Our sensors indicated a flight time of under four hours, yet we did not receive tracking until a day after launch. The payload had landed upside down, and we suspect this led to the GPS tracker failing to transmit until it got lucky with satellite positioning. See the [Postmortem and Takeaways - Technical Failures]({{ "/flight20210313/technicalfailures/" | relative_url }}) section for more details.

Final flight statistics:

| Total flight time                             | 3 hours, 22 minutes |
| Ascent time                                   | 2 hours, 56 minutes |
| Descent time                                  | 26 minutes          |
| Max altitude (estimated)                      | ~24 km              |
| Average ascent rate (estimated)               | ~2.3 m/s            |
| Total distance travelled (spherical distance) | 148 km              |

The flight was slightly shorter in length and max altitude than our target, which we attribute to overfilling of the balloon.