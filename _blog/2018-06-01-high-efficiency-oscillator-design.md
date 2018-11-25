---
layout: post
title: "High-Efficiency mmW/THz Oscillator Designs - 1: Introduction"
date: 2018-06-01 16:16:01 -0600
category: news
published: true
---

The extremely large bandwidth available at the millimeter-wave (mmW) and terahertz (THz) frequency bands has interesting potentials for a variety of applications such as high-data rate communications, high precision sensing (radar), and low-cost spectroscopy. The technology scaling of silicon integrated circuits, primarily driven by the desire to have faster and lower-power CPUs, has resulted in extremely fast transistors. For example, the maximum achievable Fmax can go well beyond 300 GHz in a 65-nm CMOS process. This naturally motivated many researchers to look at design techniques for creating silicon IC based mmW/THz systems with the hope that the cost of these systems could be significantly lowered with the massive economy of scale of silicon IC manufacturing.

<!--more-->

Among the many challenges of designing at extremely high frequencies, high-efficiency signal generation is one of the most critical. The following chart shows a review of recent works in this area. You will see that signal up to 1 THz can be generated! As impressive as it is, you will probably notice that the output power and dc-to-RF power efficiency at higher frequencies are both quite low. One can probably argue that higher output power can be achieved by power combining. However, with such low efficiency, we will most likely hit a thermal brick wall at some point as we pack more and more of these signal sources together.

![Literature Survey](high-efficiency-oscillator/survey.png)

How can one improve the power efficiency of signal generation at mmW/THz frequencies? What's the upper bound of the output power and efficiency for a given active device when it's used in an oscillator? My graduate students, Hao Wang and Jingjun Chen, and I have been thinking about these questions for a couple of years and in this series of posts, we'll try to document our thoughts and findings along the way. With a number of academic publications in print and under review (see the [Publications](/research/publications)), a purpose of this series of blogs is to provide additional details that was inappropriate (or deemed too fundamental by the reviewers) for an academic paper.

### References

**[Wang2018]** Hao Wang, Jingjun Chen, James T.S. Do, Hooman Rashtian, Xiaoguang Liu, "High-Efficiency Millimeter-wave Single-ended and Differential Fundamental Oscillators in CMOS," IEEE Journal of Solid State Circuits, vol. 53, no. 8, pp. 2151-2163, Aug, 2018.
