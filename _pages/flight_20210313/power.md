---
title: "Power Systems"
permalink: /flight20210313/power/
layout: single
excerpt: "Power systems for 2021-03-13 flight."
sidebar:
  nav: "flight20210313"
---


We had four power banks for the Arduinos and sensors, so each bank powered three sensors. Each power bank consisted of 3 AA Energizer lithium batteries, and were wired to the step up/step down voltage regulators to power the Arduinos.

For the cameras, we used a store-bought external USB power bank since they were effectively plug and play.

The biggest issue with power in a HAB is that the atmospheric temperature can drop below -40C during the flight, significantly reducing battery performance. We were not sure exactly how much degradation we would see, nor did we know how warm the interior of our payload would be. We ended up estimating the power we’d need at room temperature, either by measuring the current drawn or estimating based on battery usage over a given time period, and multiplied it by an arbitrarily chosen factor of 2 to 3. This ended up being sufficient for the sensors but insufficient for the camera battery packs, which had a different battery chemistry (see the [Postmortem and Takeaways - Technical Failures]({{ "/flight20210313/technicalfailures/" | relative_url }}) section for more details).
