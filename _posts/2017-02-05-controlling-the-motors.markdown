---
layout: post
title:  "Controlling the Motors"
date:   2017-02-05 22:00 -0000
categories: controls update
---

With the mechanical design and manufacturing well underway, it's time to take a closer look at the task of controlling the robot. We are driving our Matsushita GMX-8MC045A DC motors using the L298 drivers from ST, which will convert our low-power PWM signals from our microcontroller to high-power voltages to the motor.

The microcontroller we are using is an [Atmel SAM-E70](http://www.atmel.com/tools/ATSAME70-XPLD.aspx) (ARM) microcontroller with built-in USB, ADC, DAC, and PWM peripherals, as well as a monstrous clock speed of 150 MHz. We're borrowing the [SLIP](https://en.wikipedia.org/wiki/Serial_Line_Internet_Protocol) encoding idea for our USB communication's high-level packet format, for communicating with serial over USB between our microcontroller and the computer. On the computer side, we have built a python interface for sending commands to the robot and reading/plotting its responses.

Since our motors have an appreciable amount of non-linear friction effects, we specified a controller with a feedforward friction compensator model, with a cascade P-PI feedback controller.

![alt text]({{ site.url }}/assets/image/blockdiagram.png "Block diagram of the controller")
<div class="caption">Tentative motor position controller design</div>

Initial results on the unassembled robot have been promising, and we have been seeing 40-degree step response with no overshoot of less than one second settling time.

![alt text]({{ site.url }}/assets/image/step.png "40 degree step response")
<div class="caption">No overshoot, taking roughly 0.7 seconds to settle at less than 1 degree error</div>

Further characterization and tuning should yield continued improvements on the bandwidth of the system. I can't want to test it out on the fully-assembled hardware!