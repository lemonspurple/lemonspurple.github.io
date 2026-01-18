---
layout: page
title: STM Guide
permalink: /stm/
---


<details>
  <summary><strong>Bill of Materials (BOM)</strong></summary>
<ul>
<li>Legend:</li>
<li>* Cheaper in bulk / sets.</li>
<li>𐤲 Often breaks. Consider buying more.</li>
<li>▭ SMD Component.</li>
</ul>
<ul>
<li><h2>Controller:</h2></li>
<li>LED 𐤲*</li>
<li>2x Red LED (5mm)</li>
<li>1x Red LED (3mm)</li>
<li>3x Yellow LED (3mm)</li>
<li>1x Green LED (3mm)</li>
</ul>
<ul>
<li>Chips</li>
<li>2x TL072 by Texas Instruments 𐤲</li>
<li>1x ESP32-DevKitC (WROOM-32 by Espressif Systems)</li>
<li>3x DAC 2 Click by Mikroe</li>
<li>1x ADC 8 Click by Mikroe</li>
</ul>
<ul>
<li>Screw Terminals (2,54mm) *</li>
<li>1x 5 Connectors</li>
<li>1x 3 Connectors</li>
<li>3x 2 Connectors</li>
</ul>
<ul>
<li>Single-row male pin headers 𐤲*</li>
<li>1x 4 Pin</li>
<li>3x 1 Pin</li>
</ul>
<ul>
<li>Jumper Cables 𐤲*</li>
<li>20-30 Female to Male</li>
</ul><ul>
<li>Resistors 𐤲*</li>
<li>17x 3k3 Ω</li>
<li>9x 220 Ω</li>
<li>1x 1k6 Ω</li>
</ul><ul>
<li>Capacitor 𐤲*</li>
<li>6x 4n7F</li>
<li>4x 100n</li>
</ul><ul>
<li>Diode 𐤲</li>
<li>2x N5819</li>
</ul><ul>
<li>Various</li>
<li>1x USB to TTL Converter (Has to support PL2303, Version TA not PL2303 HXA)</li>
<li>1x Micro-USB Cable for ESP32</li>
</ul><ul>
<li><h2>Tunneling Amp</h2></li>
<li>1x ADA4637-1ARZ-ND 𐤲</li>
<li>1x Resistor RC1206JR-07100ML 𐤲 ▭</li>
<li>1x Shielding BMI-S-201-F ▭</li>
<li>2x Ceramics Capacitor 47nF 𐤲 ▭</li>
<li>2x Ceramics Capacitor 1µF 𐤲 ▭</li>
<li>2x Condensator (Polarized) 4,7 µF/35V (for example TAJ 6032 4,7/35) 𐤲 ▭</li>
</ul><ul>
<li><h2>Mechanics</h2></li>
<li>1x KC1-T/M - Kinematic, SM1-Threaded, 30 mm-Cage-Compatible Mount for Ø1" Optic</li>
<li>1x ER2-P4 - Cage Assembly Rod, 2" Long, Ø6 mm, 4 Pack</li>
<li>1x SP05/M - 30 mm to 16 mm Cage Adapter Plate, Metric</li>
<li>(You have to order through Thorlabs)</li>
</ul><ul>
<li><h2>Scannerhead</h2></li>
<li>Multiple Piezo-Disks (20mm) 𐤲𐤲</li>
<li>5 Gold Pins 𐤲</li>
<li>Conductive Silver Lacquer</li>
<li>Silverwire (prone to oxidation) or Platin-Iridium Wire (expensive)</li>
<li>Insulated enamelled copper wire (Ø 0.1 mm)</li>
</ul><ul>
<li><h2>Batteries</h2></li>
<li>2x 10x AA Battery Holder</li>
<li>1x 1x AA Battery Holder</li>
<li>21x AA Batteries</li>
</ul><ul>
<li><h2>PCB</h2></li>
<li>Controller Board</li>
<li>github.com/PeterDirnhofer/KiCad_RTM_Adapterboard_v3_0</li>
<li>Tunnelling Amp Board</li>
<li>github.com/PeterDirnhofer/Tunnelling-Amp-20</li>
</ul><ul>
<li><h2>Probes</h2></li>
<li>Microscope Cover Glass Slides</li>
<li>Brass Stamping Blank Round (Ø10mm, 0,4mm)*</li>
<li>Blu-Ray Disk and/or</li>
<li>Gold leaf and/or</li>
<li>Graphene</li>
</ul><ul>
<li><h2>Vibration Insulation</h2></li>
<li>Sponges</li>
<li>Rubber Mats</li>
<li>Washing Machine Insulation Mats</li>
<li>Bubble Wrap</li>
</ul><ul>
<li><h2>Tools</h2></li>
<li>Multimeter</li>
<li>Soldering Iron + Flux + Soldering Wick + Soldering Tip Cleaning Wire</li>
<li>Third Hand (With rubber covered clamps)</li>
<li>Wirecutter </li>
<li>Wirestripper</li>
<li>Precision Screwdriver Set Repair Tool Kit</li>
<li>Pliers (Probably part of the Repair</li> Tool Kit already)</li>
<li>Needle-nose pliers</li>
<li>Scalpel</li>
</ul><ul>
<li><h2>Glues</h2></li>
<li>Fixogum</li>
<li>Two-part epoxy adhesive by J-B Weld</li>
<li>Superglue</li>
<li>Duct Tape</li>
</ul><ul>
<li><h2>Screws</h2></li>
<li>4x M5 Tapping Screws</li>
<li>4x M5 Nuts</li>
<li>8x M5 Washers 𐤲</li>
<li>2x Washers to pin the piezo disk inbetween (17x30x3mm / M16)</li>
</ul>



</details>
<details>
<summary><strong>Credits / Sources / Thanks</strong></summary>
<ul>
<li><h2>Credits / Sources</h2></li>
<li>Piezo STM based on John Alexander and Dan Berard</li>
<li>Tunneling-Amp based on Jost Herkenhoff design</li>
<li>Final KiCad for Tunneling-Amp Controller-Board, Software by Peter Dirnhofer</li>
</ul><ul>
<li><h2>Additional Thanks</h2></li>
<li>Chaos Computer Club Cologne for lending me standing drill.</li>
<li>Kadse from CCCC for instructions on how to thread screws.</li>
<li>Lennart Grawe for additional knowledge transfer.</li>
</ul>
</details>
