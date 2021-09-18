---
title: "Nano/Micro Image Processing"
collection: projects
type: "Undergraduate projects"
permalink: /projects/NanoMicroImageProcessing
venue: "Tehran"
date: 2017-1-1
location: "Tehran, Iran"
---

Nano/Micro Image Processing

My previous project in M.Sc nanotechnology was about image processing. In Physics Department, we made sensors by tapering technique. As my curious manner I had an idea that the system must be automatized and I simulate the system by Catia, Proteus and etc., it wasn’t accepted til PROF. DR. SULAIMAN WADI HARUN came to laboratory and told us what I tried before. They accept and I got optical part to work on.

I designed an optical system but when they told me we have only limited instruments, I shocked. Here I had pxr 800 board from Imagenation and a ccd camera. I had to process the diameter as tapering the fiber, decided to code in python but finally I had to turn them into C++ codes. My primary results were like below. Fiber initial diameter is 125 micrometer.

![FiberIP1.JPG](/images/projects/FiberIP1.JPG)
fiber optic image processing with ccd camera

2nd try was with a motorized ccd and had better magnification. Here, ccd feedback wire to motor were broken and I had to design a interface with atmega 8 to control pulses as voltages was 5-12 volts. Below images show better improvements in boundary detection (Red Lines).

![FiberIP2.jpg](/images/projects/FiberIP2.jpg)
fiber optic image processing with motorized ccd camera

CCDs are perfect but I had low resolution as seen in above pictures, I took a canon camera with CMOS technology then connected it to my laptop and programmed it to get data. Results were fascinating, when I converted images into gray scale, lower noise were appeared and I removed noise canceling lines, respectively. Results were like below.

![FiberIP3.JPG](/images/projects/FiberIP3.JPG)
fiber optic image processing with Canon Camera (CMOS Technology)

Detected Boundaries were perfect, I decided to prevent background noises and lights and used white lamp far from setup, Results with same Canon Camera were like below.

![FiberIP4.JPG](/images/projects/FiberIP4.JPG)
fiber optic image processing with Canon Camera (CMOS Technology) without background noise

Optical fibers are transparent that makes picturing difficult. Lights, vibrations, any movements and etc. need to be canceled to get best quality. We need to get pictures in same distances to prevent any errors in scaling. Actual diameter is proportion of initial diameter and in the way to get that we have to find initial and current diameter pixels in vertical distance between optimum red boundaries. In this case we have actual diameters as tapering fibers and we could control waist diameter of sensors to enhance reproducibility and repeatability of them.
