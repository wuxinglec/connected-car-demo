﻿# Connected Car Demo
I created this project to demonstrate the use of [Project Flogo](http://flogo.io) as IoT Gateway. 
The use case I had in mind was to add the advantage of having a connected car that would use central knowlegde of certain conditions on the road like fog, accidents, and sun glare to enhance the notion of the driver keeping a safe distance.
The on-board Car Safety System measures the actual distance to the car in front and determines the safety state; Too Close, Safe or Optimal. It is also capable of making the car keep optimal distance.
The IoT Gateway receives distance and safety state from the Car Safety System and passes this on to the Central Logic.
The Central Logic can also receive conditional information from the frontend GUI and pass on a related safety factor back to the IoT Gateway on the car to actually tell the car to take more distance.

The setup consists of a couple of parts:

 - The [Car Safety System](car-safety-system/) based on a NodeMCU v3.0 ESP-12 Board
 - An on-board [IoT Gateway](iot-gateway/) running Project Flogo on a [C.H.I.P. computer](https://getchip.com/pages/chip)
 - Bring it all together on a standard 4-wheel [robot car](robot-car)
 - [Central Logic](central-logic/) using Project Flogo and a Redis Keystore
 - A [frontend GUI](frontend-gui/) based on [Dizmo](https://www.dizmo.com/)