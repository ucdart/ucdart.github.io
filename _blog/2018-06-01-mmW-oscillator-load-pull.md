---
layout: post
title: "High-Efficiency mmW/THz Oscillator Design (1)"
date: 2018-06-01
category: blog
---
The extremely large bandwidth available at the millimeter-wave (mmW) and terahertz (THz) frequency bands has interesting potentials for a variety of applications such as high-data rate communications, high precision sensing (radar), and low-cost spectroscopy. The technology scaling of silicon integrated circuits, primarily driven by the desire to have faster and lower-power CPUs, has resulted in extremely fast transistors. This naturally motivated many researcher to look at design techniques for creating silicon IC based mmW/THz systems with the hope that the cost of these systems could be significantly lowered with the massive economy of scale of silicon IC manufacturing.

Among the many challenges of designing at extremely high frequencies, high-efficiency signal generation is one of the most critical ones. The following chart shows a review of recent works in this area. You will see that signal up to 1 THz can be generated. It's quite impressive how fast the silicon transistors (CMOS and SiGe HBT) are.

You will probably notice that the power efficiency at higher frequencies is quite low. If we do power combining to achieve higher output power, then we will most likely hit a thermal brick wall at some point. How can one improve the power efficiency of signal generation at mmW/THz frequencies? What's the upper bound of the efficiency? Our graduate students, Hao Wang and Jingjun Chen, took a stab at this problem.

Turns out that people have been thinking about this problem from very early on. In 1968, Vehovec documented in his book a method for optimizing the output power of a transistor oscillator circuit. He formulated the problem in terms of the complex voltage gain across the transistor. Shown in the following figure, a transistor oscillator is considered as a combination of an active device and a passive feedback network. The ratio between the voltage at the output and the input port of the active device is defined as the voltage gain. In the steady state, we use phasors to represent the voltages and therefore the voltage gain is complex.
