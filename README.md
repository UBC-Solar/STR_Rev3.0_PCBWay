# UBC Solar x [**PCBWay**](https://www.pcbway.com/) Sponsorship for Steering Wheel Showcase!
> Below are all the PCBs UBC Solar has sponsored with [**PCBWay**](https://www.pcbway.com/). 
> * ⭐ [**PCBWay**](https://www.pcbway.com/) provides reliable PCB manufacturing and assembly services, offering a wide range of cost-effective options for rapid prototyping and small-volume production. 
> * 🌟 [**PCBWay**](https://www.pcbway.com/) kindly supported all these project with manufacturing and design review! Please visit their site if you need PCB manufacturing or assembly services. 
> * ⭐ There are lots of options for low-cost prototyping and small series production. 
> * 🌟 Their 24/7 support for payments and for reviewing makes our teams production scale rapdiy!
# Author: Hardy Wang (Power and Signals)
# Acknowledgement 
A huge thank you to [**PCBWay**](https://www.pcbway.com/) for the  manufacturing of our Steering Wheel board. Their support has been invaluable in converting our project into a reliable component for our newest fourth generation solar car. PCBWay provides high-quality PCB manufacturing and assembly services that are excellent for rapid prototyping and custom engineering projects.
# 2D Front Side View:
<img width="1041" height="974" alt="image" src="https://github.com/user-attachments/assets/2f0a1e5c-a6fd-4142-b0b7-197e708d14e9" />
Figure 1: 2D frontside layout view

# 3D Front Side View:
<img width="1088" height="995" alt="image" src="https://github.com/user-attachments/assets/b6559db6-0d04-4c98-84bc-a36738e71ed0" />
Figure 2: 3D frontside layout of the board design 

# 3D Back Side View:
<img width="1256" height="1023" alt="image" src="https://github.com/user-attachments/assets/43f3b53c-82be-4edd-97c4-f1adec99207e" />
Figure 3: 3D backside layout view

# Front Side:
<img width="2005" height="1785" alt="IMG_2633" src="https://github.com/user-attachments/assets/94b5df92-0b18-44ee-8592-80035a9744cb" />
Figure 4: image highlighting all of the board's soldered on components

# Overview:
The Steering Wheel Board serves as the primary interface between the driver and the solar car’s control systems. It is centrally mounted within the steering wheel frame, providing intuitive and immediate access to critical vehicle functions.
The board communicates with other vehicle subsystems via I2C, CAN, and UART protocols, enabling reliable control and real-time feedback.

**Key Features** 
> * **Push-To-Talk:** To allow the driver to talk to the pit 
> * **HORN:** To engage the horn of the car
> * **Cruise Control:** To set a constant speed for the car and increment and decrement said speed 
> * **Regen:** To turn on and off the regenerative breaking feature in the car (converts the kinetic energy of the car back into electricity)
> * **Speedometer:** display the acvtive speed of the car 
> * **CAN Bus Termination:** Optional on-board split-termination of CAN

# Design Choices:
The Steering Wheel Board utilizes an STM32 microcontroller (STM32F103RCT6) to interface between the driver and the vehicle’s control systems. Through it's data processing and communication capabilites, the STM32 enables reliable control and monitoring of significant vehicle functions while maintaining robust communication across the car’s network.
> * Accounts driver inputs including Push-to-Talk, horn activation, cruise control, and regenerative braking through durable, egronomically chosen components and component placement designed to have a racing car feel 
> * Implements opto-isolation for high-noise and RF signals, protecting all sensitive components and ensuring robust operation in electrically noisy environment
> * Utilizes the LM66200DRLR ideal diode power switching controller to seamlessly switch between JTAG-based power (for embedded flashing/debugging) and the vehicle’s 12V supply, ensuring seemless power switch and operation 
> * All input signals are processed through low-pass filters, reducing noise and switch bounce to provide clean, stable readings to the STM32 
> * Integrates the AS1115-BSST LED driver for the hex display speedometer, offering a compact solution with high speed multiplexing, constant current control, and simplified STM32 interfacing via I2C communication 

# Design Goals & Requirements
The Steering Wheel Revision 3.0 was designed with robustness, reliability and driver/mechanical satisfaction in mind, specifcally considering:
> * **Intuative layout And Component Choice:** All component choices and placement is designed to withstand large amount of blunt force and for the driver to easily reach any frequently-used input without lifting their hand
> * **Board Dimensioning:** Through consistent communication with the Vechile dynamics team of Solar, the boards shaping staisfies all mechanical requirements / maximization for driver feel
> * **Minimizing Electromagnetic Inference:** Proper measures to isolate high-noise signals and protect sensitve signals, such as through the use of optoisolation 

# Future Improvments
The Steering Wheel can see improvements through adding more features such as intergrating the driver display, being able to detect the battery level of the supplement battery (power all low voltage boards) and communicate it to the driver display and possilbly hand controlled acceleration on the board. Furthermore, Electromagnetic interferance can be minimized even more by increasing the board layers from 2 to 4 layers.
