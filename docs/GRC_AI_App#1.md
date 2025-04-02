# GRC AI DevBoard + Robot Control App + Apps#1 


<img src="https://github.com/user-attachments/assets/e3e6825e-b6aa-4fa9-a20d-46c42cd3a039" width=40% align="left"> GRC Development Board and ready-to-use software applications to help you quickly make AI-based solutions.

This kit includes a preinstalled app:
- **Voice and tilt Robot Control**
  Ready to use with [CrowBot](https://www.elecrow.com/crowbot-bolt-programmable-smart-robot-car-steam-robot-kit.html)!


Additional Apps:
- Voice PIN
  We recommend using it with: [Crowtail Relay](https://www.elecrow.com/crowtail-relay-p-1232.html) + [Electromagnetic Lock](https://www.elecrow.com/electromagnetic-lock-p-1609.html)
- Teacher 3+


Where can it be used? 
- DIY projects
- AI\ML technologies studying
- tinyML devices development

  

---

## Preinstalled Applications
Three pre-installed proprietary applications come with the development board, offering advanced functionality out of the box:

**Robot Control**: Voice command recognition and tilt control for Arduino robots and other devices. 

**Voice PIN-Code**: Activates upon detecting a user-spoken four-digit voice PIN code.

**Teacher 3+ (English)**: AI-powered English word learning for kids 3+, recognizing their spoken words.

---

**You can utilize these pre-installed applications alongside an open-source component running on the ESP32-C3.**

While the applications are not open-source, this component provides access to their output data. It lets you control and manage them, send commands, and supply data for processing, allowing integration and customization for your specific tasks, equipment, and scenarios. 

**[Open-source software component on GitHub](https://github.com/Grovety/GRC-AI-apps/tree/main)**

---


## Applications Overview

### Robot Control
An app for controlling devices, such as robots, using voice commands and gestures like tilting a board in different directions. Both modes can be used simultaneously or separately.

> Check out our [Arduino open-source program](https://github.com/Grovety/CrowBot_GRC_program) for the [CrowBot-BOLT robot](https://www.elecrow.com/crowbot-bolt-programmable-smart-robot-car-steam-robot-kit.html), which is ready to use right out of the box!  
We designed it to showcase voice control and tilt-based movement. You can also use it as a project reference, adapt it for other robots and devices, or explore new possibilities with the CrowBot. 


**Voice Control**

Demo: https://youtu.be/RoclNdVzP7A

The application operates in constant mode listening for user commands through the built-in microphones. When it detects a command from its predefined list, the application recognizes it, announces it through the speaker on the development board, and transmits it via BLE and wired connections.
The command that is sent can be transformed into movement commands by the robot or other devices. Additionally, you can process the command using the onboard ESP32-C3 microcontroller, allowing you to convert it directly into commands for controlling the motors without the need for extra computing boards.

**Tilt Control**

Demo: https://youtu.be/FIsmTgkFIoI

The app detects the tilt of a board and translates it into commands to control a robot. Tilting forward makes the robot speed up while tilting backward slows it down, or moves it in reverse. Tilting to the sides makes it turn. The controls are intuitive and engaging, offering a fun user experience. This system can be adapted to control different types of machines. 

**For the complete description and documentation, visit: https://github.com/Grovety/GRC-AI-apps/blob/main/docs/Robot_Control_Description.md**


---

### Voice PIN
This application allows the DevBoard to function as an electronic switch that activates when a user says a pre-set voice PIN code consisting of four digits. 

It serves as a secure key to prevent unauthorized use, ensuring that the switch activates only for the authorized user who knows the correct PIN.

>Create a smart lock activated by voice PIN using the GRC AI DevBoard with App#1, [Crowtail Relay](https://www.elecrow.com/crowtail-relay-p-1232.html) + [Electromagnetic Lock](https://www.elecrow.com/electromagnetic-lock-p-1609.html)

https://youtu.be/QeatYOg01Y4 

#### Use Cases:
- Automated entry management.
- Smart home device regulating access — imagine simply saying a PIN code to control lighting, fans, and your HVAC system.
- Access to the car: voice activation for starting the engine.
- Restriction of access inside office premises.
- Personal lockers without physical keys.

#### Interfaces:
You can use UART and other interfaces to interact with the app. [Learn more](https://github.com/Grovety/GRC-AI-apps/blob/main/GRC_AI_apps_kit%231.md).

You can utilize the specified DevBoard output to control external devices, such as an electric lock latch. Alternatively, you can use the second microcontroller (ESP32-C3) to develop your methods for controlling external devices.

---

### Teacher 3+
This interactive English learning app helps kids learn through pictures, sounds, and simple math (addition and subtraction up to 20). Children say their answers aloud, and AI checks if they're correct. If they need help, they can skip or get a hint with the word and pronunciation.

#### How It Works:
- The Teacher displays pictures of various objects, plays sounds, shows numbers, and provides simple examples of addition and subtraction up to 20.
- Children not only learn new words but also memorize them through immediate communication with the toy, similar to how native speakers acquire language.
- When using the toy, children vocalize their answers, and the AI Teacher recognizes whether their responses are correct.
- If a child is unable to answer, they can skip the word by pressing the left button or request a hint by pressing the right button. This action will display the word and produce the correct pronunciation.

 <img src="https://github.com/user-attachments/assets/3ed4a5cd-e88b-4f1b-a126-9579a6f3e1a8" width=30%> <img src="https://github.com/user-attachments/assets/9bfc5516-a63d-4b90-9f44-cade02def54f" width=30%> <img src="https://github.com/user-attachments/assets/ff35d011-8c57-4abb-b24d-ef83607cba60" width=30%>


#### Summary:
- English language learning device.
- Learning words.
- Pronunciation training.
- Training through different channels:
  - Pictures.
  - Sounds.
  - Numbers in addition and subtraction examples.

#### Topics:
- Numbers (0 to 10).
- Animals.
- Nature.
- Human.
- Objects.

#### Interface:
You can use UART and other interfaces to interact with the app. [Learn more](https://github.com/Grovety/GRC-AI-apps/blob/main/GRC_AI_apps_kit%231.md).

---

## Overview

### Master Module:
- ESP32-S3

### Communication Module:
- ESP32-C3

### Connectivity:
- USB, UART to USB interface CP2102N
- Wi-Fi 802.11 b/g/n
- Bluetooth LE: Bluetooth 5, Bluetooth mesh

### Periphery:
- 2 MEMS microphones
- Accelerometer MPU-9250
- 4 buttons
- Amplifier MAX98357A
- Speaker FUET_FS_1340
- 3 RGB LEDs – SK6805
- Monochrome OLED Display 0.96" 128x64

### Ports:
- USB-C port: 5V, 500mA (min)
- 2 PIN socket: LiPo 1S - 3.7V

### Power Consumption (Average):
- 30mA

Check the full specification at the link: **[GRC tinyML DevBoard Specification](https://github.com/Grovety/GRC-AI-apps/blob/main/docs/DevBoard_Specification.md)**

---

## Links:

- [Open-source component on GitHub](https://github.com/Grovety/GRC-AI-apps/tree/main)
- [Robot Control description](https://github.com/Grovety/GRC-AI-apps/blob/main/docs/Robot_Control_Description.md)
- [Example of Robot Control Implementation Using the CrowBot-BOLT Robot](https://github.com/Grovety/CrowBot_GRC_program/tree/main)
- [GRC tinyML DevBoard Specification](https://github.com/Grovety/GRC-AI-apps/blob/main/docs/DevBoard_Specification.md)

