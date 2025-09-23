---
layout: default
modal-id: 2
date: 2024-02-02
img: maxmsp.png
alt: image-alt
project-date: 2022-?
category: sound
tools: MaxMSP, Arduino (physical computing), Ableton
---

<span style="color:red"> ** I unfortunately don’t have any documentation of the final physical form of the project! I used an arduino with soil moisture sensor and photoresistor. I will rebuild it soon and post pictures! ** </span>.

<br/><br/>

Generative music from plants:: Generative Max MSP patch with arduino and node.js. The arduino sends the value from the photoresistor and soil moisture sensor to Max. The light value from the photoresistor is mapped to the gain in the mc.fffb~ object, making the water bubble sound louder as it gets darker. The soil moisture value determines the midi note of the subtractive synthesizer created with the water bubble sound. The temperature sensors did not work well, so I ended up using node.js to retrieve the temperature and humidity data from the web. Humidity determines the cutoff frequency of the water bubble synthesizer (high frequencies are less present when it is more humid). Lastly, the temperature is mapped to the value for mc.sig~.

<br/><br/>

Demo video:
<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/9Sb_fUMfHaw?si=9FM2nTtWI08dRF9i" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div>

<br/><br/>
Main Code
<br/><br/>
<img src="{{ site.baseurl }}/img/portfolio/main-code.png" alt="Main MaxMSP Code" class="center-image" width="500">


<br/><br/>
Synth Subpatch
<br/><br/>
<img src="{{ site.baseurl }}/img/portfolio/synth.png" alt="Synth subpatch" class="center-image" width="400">

<br/><br/>
Arduino Subpatch
<br/><br/>
<img src="{{ site.baseurl }}/img/portfolio/arduino.png" alt="Arduino Subpatch" class="center-image" width="400">