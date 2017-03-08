---
layout: post
title:  "Putting a Sticker on it"
date:   2017-03-07 18:39 -0000
categories: electronics update
---

After many hours machining, wiring, and mounting, the electronics has gotten the orange seal of approval. We're CSA approved (for the syposium, atleast). That's one thing less to worry about. Here's the enclosure in in all it's magnificence: 

![Electronics Enclosure]({{ site.url }}/assets/image/enclosure-closed.jpg)
<div class="caption">Yeah, someone actually drilled all those holes</div>

Now, let's take a closer look at what's in the box. 

![Inside the enclosure]({{ site.url }}/assets/image/enclosure-inside.jpg)
<div class="caption">Inside the belly of the beast</div>

On the top right, we have our 24V, 350W power supply. On the bottom left, there's the three motor drivers, one for each of the motors. They're equipped with some oversized heat sinks (under-powered motor drivers with over-designed heat sinks even things out, right?). On the top left, we have two 24V exhaust fans that pull air out of the enclosure. 

Finally, from just under the fans, we have the Atmel board, the low-power board, and the high-power board. The low-power board has isolated amplifiers for the current sense, and opto-isolators to control the motor drivers. It uses USB power, which is completely isolated from the PSU output. The encoders and force sensor are connected to this board (circular connectors on the left). And the high-power board has the motor driver power connections and the current sense resistors. 

![Another angle]({{ site.url }}/assets/image/enclosure-open.jpg)
<div class="caption">Pretty much a photoshoot at this point</div>

At a different angle, we can see the encoder and motor connections. It was important that the connectors were circular, otherwise it becomes a lot more difficult to attach them to the enclosure. 

We had a minor hiccup last week, which resulted in some fried motor drivers. But they've been replaced, and we're ready to integrate our software with the robot (which is looking pretty damn good, by the way). This next week will be a big one.



