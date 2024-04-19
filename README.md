# Bitstream-Evolution-FilterBoard
Logan Manthey Spring 2023-2024

## Purpose
This board is a simple header board to be able to mount an FPGA, Ardunio Nano Microcontroller, and as ESPOtek Labador to it. This board also includes a basic passive low pass filter which will filter measurements on the ardunio to be more accurate to what we can accurately gather it will also ensure consistency with how we are gathering measurements as well. This PCB also allows us to test fit headers for future boards to build as well. 

| ![PCBRende:r](Bitstream_Evolution_Filterboard/Images/PopulatedBoard.png) | 
|:--:| 
| *Populated PCB* |


| ![PCBRende:r](Bitstream_Evolution_Filterboard/Images/CompletedBoard.png) | 
|:--:| 
| *Unpopulated PCB* |


| ![PCBRende:r](Bitstream_Evolution_Filterboard/Images/RenderV1.png) | 
|:--:| 
| *PCB Render* |

## Filter
The filter used has a 160 ohm resistor and a 0.01 uF capacitor this gives a -3dB cutoff frequency of 99471.8394 Hz. In testing at 3.3 volts this will give us an accurate interrupt reading range on the ardunio of between 10kHz and 60Khz with only some aliasing around the 55kHz to 60Khz range. This is much better than not using as there will be aliasing anywhere above about 100kHz whereas this will simply just filter those values out. Though this is an extremly simple filter it will allow us to ensure that our measurements we are getting are in a certain measureable range while still maintaining affordability. 

| ![PCBRende:r](Bitstream_Evolution_Filterboard/Images/Bode.png) | 
|:--:| 
| *Bode Plot* |

| ![PCBRende:r](Bitstream_Evolution_Filterboard/Images/Step.png) | 
|:--:| 
| *Step Response* |

## BOM

| Part                        | Quanity |
| --------------------------- | ------- |
| 160 Ohm Resistor            | 1       |
| 0.01 uF Capacitor           | 1       |
| 10 Pin 2.54mm Female Header | 3       |
| 15 Pin 2.54 Female Header   | 2       |

