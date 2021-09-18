---
title: "CCD Array (spectrometer)"
collection: projects
type: "Undergraduate projects"
permalink: /projects/CCD
venue: "Tabriz"
date: 2017-1-1
location: "Tabriz, Iran"
---

CCD array setup

A charge-coupled device (CCD) is a device for the movement of electrical charge, usually from within the device to an area where the charge can be manipulated, for example conversion into a digital value. This is achieved by “shifting” the signals between stages within the device one at a time. CCDs move charge between capacitive bins in the device, with the shift allowing for the transfer of charge between bins.

![TCD1304AP.jpg](/images/projects/TCD1304AP.jpg)
tcd1304ap

In recent years CCD has become a major technology for digital imaging. In a CCD image sensor, pixels are represented by p-dopedmetal-oxide-semiconductors (MOS) capacitors. These capacitors are biased above the threshold for inversion when image acquisition begins, allowing the conversion of incoming photons into electron charges at the semiconductor-oxide interface; the CCD is then used to read out these charges. Although CCDs are not the only technology to allow for light detection, CCD image sensors are widely used in professional, medical, and scientific applications where high-quality image data are required. In applications with less exacting quality demands, such as consumer and professional digital cameras, active pixel sensors, also known as complementary metal-oxide-semiconductors (CMOS) are generally used; the large quality advantage CCDs enjoyed early on has narrowed over time.

Basics of operation
In a CCD for capturing images, there is a photoactive region (an epitaxial layer of silicon), and a transmission region made out of a shift register (the CCD, properly speaking).

An image is projected through a lens onto the capacitor array (the photoactive region), causing each capacitor to accumulate an electric charge proportional to the light intensity at that location. A one-dimensional array, used in line-scan cameras, captures a single slice of the image, whereas a two-dimensional array, used in video and still cameras, captures a two-dimensional picture corresponding to the scene projected onto the focal plane of the sensor. Once the array has been exposed to the image, a control circuit causes each capacitor to transfer its contents to its neighbor (operating as a shift register). The last capacitor in the array dumps its charge into a charge amplifier, which converts the charge into a voltage. By repeating this process, the controlling circuit converts the entire contents of the array in the semiconductor to a sequence of voltages. In a digital device, these voltages are then sampled, digitized, and usually stored in memory; in an analog device (such as an analog video camera), they are processed into a continuous analog signal (e.g. by feeding the output of the charge amplifier into a low-pass filter), which is then processed and fed out to other circuits for transmission, recording, or other processing.

![CCD_charge_transfer_animation.gif](/images/projects/CCD_charge_transfer_animation.gif)  
The charge packets (electrons, blue) are collected in potential wells (yellow) created by applying positive voltage at the gate electrodes (G). Applying positive voltage to the gate electrode in the correct sequence transfers the charge packets.
Architecture
1) Frame transfer CCD
The frame transfer CCD imager was the first imaging structure proposed for CCD Imaging by Michael Tompsett at Bell Laboratories. A frame transfer CCD is a specialized CCD, often used in astronomy and some professional video cameras, designed for high exposure efficiency and correctness.

The normal functioning of a CCD, astronomical or otherwise, can be divided into two phases: exposure and readout. During the first phase, the CCD passively collects incoming photons, storing electrons in its cells. After the exposure time is passed, the cells are read out one line at a time. During the readout phase, cells are shifted down the entire area of the CCD. While they are shifted, they continue to collect light. Thus, if the shifting is not fast enough, errors can result from light that falls on a cell holding charge during the transfer. These errors are referred to as “vertical smear” and cause a strong light source to create a vertical line above and below its exact location. In addition, the CCD cannot be used to collect light while it is being read out. Unfortunately, a faster shifting requires a faster readout, and a faster readout can introduce errors in the cell charge measurement, leading to a higher noise level.

A frame transfer CCD solves both problems: it has a shielded, not light sensitive, area containing as many cells as the area exposed to light. Typically, this area is covered by a reflective material such as aluminium. When the exposure time is up, the cells are transferred very rapidly to the hidden area. Here, safe from any incoming light, cells can be read out at any speed one deems necessary to correctly measure the cells’ charge. At the same time, the exposed part of the CCD is collecting light again, so no delay occurs between successive exposures.

The disadvantage of such a CCD is the higher cost: the cell area is basically doubled, and more complex control electronics are needed.

2) Intensified charge-coupled device
An intensified charge-coupled device (ICCD) is a CCD that is optically connected to an image intensifier that is mounted in front of the CCD.

An image intensifier includes three functional elements: a photocathode, a micro-channel plate (MCP) and a phosphor screen. These three elements are mounted one close behind the other in the mentioned sequence. The photons which are coming from the light source fall onto the photocathode, thereby generating photoelectrons. The photoelectrons are accelerated towards the MCP by an electrical control voltage, applied between photocathode and MCP. The electrons are multiplied inside of the MCP and thereafter accelerated towards the phosphor screen. The phosphor screen finally converts the multiplied electrons back to photons which are guided to the CCD by a fiber optic or a lens.

An image intensifier inherently includes a shutter functionality: If the control voltage between the photocathode and the MCP is reversed, the emitted photoelectrons are not accelerated towards the MCP but return to the photocathode. Thus, no electrons are multiplied and emitted by the MCP, no electrons are going to the phosphor screen and no light is emitted from the image intensifier. In this case no light falls onto the CCD, which means that the shutter is closed. The process of reversing the control voltage at the photocathode is called gating and therefore ICCDs are also called gateable CCD cameras.

Besides the extremely high sensitivity of ICCD cameras, which enable single photon detection, the gateability is one of the major advantages of the ICCD over the EMCCD cameras. The highest performing ICCD cameras enable shutter times as short as 200 picoseconds.

ICCD cameras are in general somewhat higher in price than EMCCD cameras because they need the expensive image intensifier. On the other hand, EMCCD cameras need a cooling system to cool the EMCCD chip down to temperatures around 170 K. This cooling system adds additional costs to the EMCCD camera and often yields heavy condensation problems in the application.

ICCDs are used in night vision devices and in various scientific applications.

3) Electron-multiplying CCD
An electron-multiplying CCD (EMCCD, also known as an L3Vision CCD, a product commercialized by e2v Ltd., GB, L3CCD or Impactron CCD, a now-discontinued product offered in the past by Texas Instruments) is a charge-coupled device in which a gain register is placed between the shift register and the output amplifier. The gain register is split up into a large number of stages. In each stage, the electrons are multiplied by impact ionization in a similar way to an avalanche diode. The gain probability at every stage of the register is small (P < 2%), but as the number of elements is large (N > 500), the overall gain can be very high

g = (1 + P)^N
,with single input electrons giving many thousands of output electrons. Reading a signal from a CCD gives a noise background, typically a few electrons. In an EMCCD, this noise is superimposed on many thousands of electrons rather than a single electron; the devices’ primary advantage is thus their negligible readout noise. It is to be noted that the use of avalanche breakdown for amplification of photo charges had already been described in the U.S. Patent 3,761,744 in 1973 by George E. Smith/Bell Telephone Laboratories.

EMCCDs show a similar sensitivity to intensified CCDs (ICCDs). However, as with ICCDs, the gain that is applied in the gain register is stochastic and the exact gain that has been applied to a pixel’s charge is impossible to know. At high gains (> 30), this uncertainty has the same effect on the signal-to-noise ratio (SNR) as halving the quantum efficiency (QE) with respect to operation with a gain of unity. However, at very low light levels (where the quantum efficiency is most important), it can be assumed that a pixel either contains an electron — or not. This removes the noise associated with the stochastic multiplication at the risk of counting multiple electrons in the same pixel as a single electron. To avoid multiple counts in one pixel due to coincident photons in this mode of operation, high frame rates are essential.

Because of the lower costs and better resolution, EMCCDs are capable of replacing ICCDs in many applications. ICCDs still have the advantage that they can be gated very fast and thus are useful in applications like range-gated imaging. EMCCD cameras indispensably need a cooling system — using either thermoelectric cooling or liquid nitrogen — to cool the chip down to temperatures in the range of −65 to −95 °C (−85 to −139 °F). This cooling system unfortunately adds additional costs to the EMCCD imaging system and may yield condensation problems in the application. However, high-end EMCCD cameras are equipped with a permanent hermetic vacuum system confining the chip to avoid condensation issues.

The low-light capabilities of EMCCDs find use in astronomy and biomedical research, among other fields. In particular, their low noise at high readout speeds makes them very useful for a variety of astronomical applications involving low light sources and transient events such as lucky imaging of faint stars, high speed photon counting photometry, Fabry-Pérot spectroscopy and high-resolution spectroscopy. More recently, these types of CCDs have broken into the field of biomedical research in low-light applications including small animal imaging, single-molecule imaging, Raman spectroscopy, super resolution microscopy as well as a wide variety of modern fluorescence microscopy techniques thanks to greater SNR in low-light conditions in comparison with traditional CCDs and ICCDs.

In terms of noise, commercial EMCCD cameras typically have clock-induced charge (CIC) and dark current (dependent on the extent of cooling) that together lead to an effective readout noise ranging from 0.01 to 1 electrons per pixel read. However, recent improvements in EMCCD technology have led to a new generation of cameras capable of producing significantly less CIC, higher charge transfer efficiency and an EM gain 5 times higher than what was previously available. These advances in low-light detection lead to an effective total background noise of 0.001 electrons per pixel read, a noise floor unmatched by any other low-light imaging device.

Color cameras
Digital color cameras generally use a Bayer mask over the CCD. Each square of four pixels has one filtered red, one blue, and two green (the human eye is more sensitive to green than either red or blue). The result of this is that luminance information is collected at every pixel, but the color resolution is lower than the luminance resolution.

Better color separation can be reached by three-CCD devices (3CCD) and a dichroic beam splitter prism, that splits the image into red, green and blue components. Each of the three CCDs is arranged to respond to a particular color. Many professional video camcorders, and some semi-professional camcorders, use this technique, although developments in competing CMOS technology have made CMOS sensors, both with beam-splitters and bayer filters, increasingly popular in high-end video and digital cinema cameras. Another advantage of 3CCD over a Bayer mask device is higher quantum efficiency (and therefore higher light sensitivity for a given aperture size). This is because in a 3CCD device most of the light entering the aperture is captured by a sensor, while a Bayer mask absorbs a high proportion (about 2/3) of the light falling on each CCD pixel.

For still scenes, for instance in microscopy, the resolution of a Bayer mask device can be enhanced by microscanning technology. During the process of color co-site sampling, several frames of the scene are produced. Between acquisitions, the sensor is moved in pixel dimensions, so that each point in the visual field is acquired consecutively by elements of the mask that are sensitive to the red, green and blue components of its color. Eventually every pixel in the image has been scanned at least once in each color and the resolution of the three channels become equivalent (the resolutions of red and blue channels are quadrupled while the green channel is doubled).

![SONY_ICX024AK_10A_1988_494kpix_CCD.jpg](/images/projects/SONY_ICX024AK_10A_1988_494kpix_CCD.jpg)
Sony 2/3″ CCD ICX024AK 10A 494496 (816*606) pixels CCD removed from Sony CCD-V88E video camera from 1988, with Yellow, Green and Cyan vertical stripe filter

Arduino 8-bit Spectrograph project
The goal of this project is to make the electronics for a spectrograph using an ATmega1284P running Arduino code and a TCD1304AP linear array CCD. The digitization is 8-bit.

An Arduino can’t really keep up with a CCD using the internal analog to digital converter, but with an external 8-bit half-flash ADC it is no problem at all. The ADC is the TI ADC0820, which can digitize up to 666k samples per second. The working sample rate works out to be a hair over 111kSPS using the code below. The 3694 pixel frame takes around 32mS to read and digitize, and around 4 seconds to download.

Microcontroller
The Arduino Uno can’t pull off a 3694 pixel buffer. It just doesn’t have enough RAM. That leaves either the Arduino Mega2560 with just 4kB or a standalone ATmega1284 with 16kB RAM. It is a whole lot easier, and cheaper, to embed a 40-pin IC into a project than it is an Arduino Mega2560, so I went with the ATmega1284. When using the Arduino Mega2560 the compiler will complain about not having enough RAM, but it will still run. The same goes for the ATmega644.

Analog to Digital Converter
The ADC0820 ADC has + and – reference inputs designed to set the range of the ADC. In this way you can zone in on the used portion of the input range, keeping full resolution. The apparent noise increases as you trim the range down, though, since it becomes a larger part of the digital range.

Linear Array CCD
The CCD is a Toshiba TCD1304AP 3648 pixel linear CCD sensor which requires only a single supply voltage. The sensor is driven by the microcontroller, and the analog output is buffered by a transistor and inverted and amplified by an op-amp before being digitized by the ADC0820.

![spectrograph-1284.png](/images/projects/spectrograph-1284.png)
schematic board

oftware
Use the MightyCore boards manager plugin by MCUdude. The board will be ATmega1284 and the variant will be the 1284 or the 1284P, depending on which one you have. Pinout is “standard” and the frequency is 16MHz. You can add the MightyCore boards to the boards manager by adding the following url to the “Additional Boards Manager URLs” textbox in Arduino preferences.

Then just open the Boards Manager under Tools->Board->Boards Manager and go to the bottom to install the MightyCore boards. The selection of boards will increase considerably to include all of the ATmegaxx4 chips, ATmega16/32, and ATmega8535. Additional programmers will appear, too, and you should use one of them with the MightyCore.

You will need an AVR programmer to burn the Arduino bootloader into the ATmega1284.

The source code for the linear CCD application is very carefully crafted in places to maintain the phase relationship between all of the CCD clocks and stay true to the specification. It takes a logic analyzer to measure the results of any code changes in the “readLine()” function.

1) TCD1304Ap datasheet
2) ATmega 1284p datasheet
3) python code
4) Arduino code
5) MightyCore
6) Calibration
To calibrate, start by setting the VR2 pot so that the voltage on pin 12 of the ADC0820 is close to 5.0V. Set VR3 such that the voltage on pin 11 of the ADC0820 is 0V. Then cover the CCD with electrical tape in a room with dimmed lighting. The tape will come off without damaging the CCD. Adjust pot VR1 to get the lowest voltage you can get on pin 1 of the ADC0820. Adjust it back up so that the voltage just begins to rise. It may be anywhere from 0.65V to 0.75V. That adjusts the lowest signal to be just measurable by the ADC. Remove the electrical tape, but keep it handy. We’ll use it again. Cover the CCD with a dark cloth under dimmed room lighting so the CCD just barely saturates (a scope helps) and adjust the 2kΩ VR2 Vref(+) pot and readout a frame. Adjust until the digital value is 255, and then back off a little to 253 – 255. Then cover the CCD using the electrical tape, and adjust the 10k VR3 Vref(-) pot so the lowest digital reading just hits 1 or 2 ADU. You must adjust the pots in that order because they interact with each other. That is by design. The maximum voltage you can put on Vref(-) is the voltage on Vref(+), and the minimum is ground, so changing Vref(+) changes the range of Vref(-).

![TCD1304-Sampler.png](/images/projects/TCD1304-Sampler.png)
python Output  

A few lines up from the end of the python code is a line:  
app = Application(master=root, port=”/dev/tty.usbserial-00000000″, exposure=50)  
It should match your serial port. If you are using Windows, change that to:  
app = Application(master=root, port=”COM3″, exposure=50)  

Make it match the serial port you are using. When you run the program it draws a graph of the CCD output, but also makes a file in the program directory named ‘ccd.csv’. That file can be imported into a spreadsheet application for further processing.
The commands are:

Sample – Read the CCD and put the trace on the screen.  
Clear – Clear all traces from the screen.  
Quit – End the program (you need to do this to keep from generating an error on exit).  
Samples – How many scans to average together (removes noise).  
Exposure – An integer value from 1 to 1000. The milliseconds to expose.  
Baseline – Makes a zero second exposure to subtract from other exposures.  
notes : Be careful to keep the digital and analog wiring away from each other where possible. Use 0.1µF bypass capacitors at every Vcc connection. Keep all of the digital wires as short as practical to keep them from radiating more than necessary. Be especially careful when routing the Mclk and SH signals near analog areas.  
