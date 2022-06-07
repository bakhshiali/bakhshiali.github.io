---
title: "Nano/Micro Image Processing"
collection: projects
type: "Undergraduate projects"
permalink: /projects/NanoMicroImageProcessing
venue: "Tehran"
date: 2017-1-1
location: "Tehran, Iran"
---

<h2>How to image Nano/Micro-scale and process Nano/Micro Images?</h2>
<h3>Project story</h3>
<p align="justify" style="padding-left: 1em">My previous project in M.Sc nanotechnology was about image processing. In Physics Department, we made sensors by tapering technique. As my curious manner I had an idea that the system could be automatized, so I simulated the system by Catia, Proteus and etc., it was accepted with PROF. DR. SULAIMAN WADI HARUN visit and I got optical part to work on. I designed an optical system with limited instruments. Here I had pxr 800 board from Imagenation and a ccd camera. I had to process the diameter as the fiber being tapered (C++ codes). My primary results were like below. single mode optical fiber initial diameter is 125 micrometer (without jacket/coating).</p>

<figure>
  <img src="/images/projects/FiberIP1.JPG" alt="FiberIP1.JPG" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">fiber optic image processing with ccd camera</figcaption>
</figure> 

<p align="justify" style="padding-left: 1em">2nd try was with a motorized ccd and had better magnification. Here, ccd feedback wire to motor were broken and I had to design a interface with atmega 8 to control pulses as voltages was 5-12 volts. Below images show better improvements in boundary detection (Red Lines).</p>

<figure>
  <img src="/images/projects/FiberIP2.JPG" alt="FiberIP2.JPG" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">fiber optic image processing with motorized ccd camera</figcaption>
</figure> 

<p align="justify" style="padding-left: 1em">CCDs are perfect but I had low resolution as seen in above pictures, I took a canon camera with CMOS technology then connected it to my laptop and programmed it to get data. Results were fascinating, when I converted images into gray scale, lower noise were appeared and I removed noise canceling lines, respectively. Results were like below.</p>

<figure>
  <img src="/images/projects/FiberIP3.JPG" alt="FiberIP3.JPG" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">fiber optic image processing with Canon Camera (CMOS Technology)</figcaption>
</figure> 

<p align="justify" style="padding-left: 1em">Detected Boundaries were perfect, I decided to prevent background noises and lights and used white lamp far from setup, Results with same Canon Camera were like below.</p>

<figure>
  <img src="/images/projects/FiberIP4.JPG" alt="FiberIP4.JPG" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">fiber optic image processing with Canon Camera (CMOS Technology) without background noise</figcaption>
</figure> 

<p align="justify" style="padding-left: 1em">Optical fibers are transparent that makes picturing difficult. Lights, vibrations, any movements and etc. need to be canceled to get best quality. We need to get pictures in same distances to prevent any errors in scaling. Actual diameter is proportion of initial diameter and in the way to get that we have to find initial and current diameter pixels in vertical distance between optimum red boundaries. In this case we have actual diameters as tapering fibers and we could control waist diameter of sensors to enhance reproducibility and repeatability of them.</p>
