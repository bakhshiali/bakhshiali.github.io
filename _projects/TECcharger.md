---
title: "TEC charger"
collection: projects
type: "Undergraduate projects"
permalink: /projects/TECcharger
venue: "Tabriz"
date: 2014-1-1
location: "Tabriz, Iran"
toc: true
toc_sticky: true
---

<h2>TEC</h2>

<p align="justify" style="padding-left: 1em">Thermoelectric cooling uses the Peltier effect to create a heat flux between the junction of two different types of materials. A Peltier cooler, heater, or thermoelectric heat pump is a solid-state active heat pump which transfers heat from one side of the device to the other, with consumption of electrical energy, depending on the direction of the current. Such an instrument is also called a Peltier device, Peltier heat pump, solid state refrigerator, or thermoelectric cooler (TEC). It can be used either for heating or for cooling, although in practice the main application is cooling. It can also be used as a temperature controller that either heats or cools.</p>

<figure>
  <img src="/images/projects/Thermoelectric-cooling.png" alt="Thermoelectric-cooling.png" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">Thermoelectric cooling</figcaption>
</figure> 

<p align="justify" style="padding-left: 1em">Energy given by temperature difference  = Seebeck coefficient * grad(Temperature)<br><br>

By making fire we are able to charge a smartphone.<br><br>

circuit elements : 1) TEC     2) Regulator 7805    3) Female USB     4) Heatsink</p>

<p align="justify" style="padding-left: 1em">Notes :<br><br>

1) regulator 7805 gives +5v DC between two common ground and output pins. if the regulator is located far from the power supply filter for more accurate voltage range , two capacitors needed between ground and another two pins.<br><br>

2) heatsink must be able to transfer the heat needed from TEC, Low heat results in low energy convert then this would damage regulator or device and excess heat might damage TEC. So for deep control of this effects we would need feedback in our circuit.<br><br>

3) be careful with fire!<br><br>

TEC numbers indicate it’s features as size and current that shown in below image.</p>

<figure>
  <img src="/images/projects/tec-info.png" alt="tec-info.png" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">TEC info</figcaption>
</figure> 
