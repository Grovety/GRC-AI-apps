# GRC-AI-apps - Robot Control

[Description of GRC_AI_RoborControl (App#1)](https://github.com/Grovety/GRC-AI-apps/blob/main/docs/GRC_AI_App%231.md)

[DevBoard Specification](https://github.com/Grovety/GRC-AI-apps/blob/main/docs/DevBoard_Specification.md)

[Robot Control Description](https://github.com/Grovety/GRC-AI-apps/blob/main/docs/Robot_Control_Description.md)



# An example application demonstrating communication between ESP32S3 and ESP32C3

1. This example shows how to set up a console application on the ESP32C3 to control the ESP32S3 using the UART interface.
    - Type `help` to display the supported commands.
    - By default, all messages received from the ESP32S3 are sent using the [BLE](https://github.com/Grovety/GRC-AI-apps/blob/main/BLE.md). All possible messages are described in [GRC_AI_apps_kit#1.md](https://github.com/Grovety/GRC-AI-apps/blob/main/GRC_AI_apps_kit%231.md) and [GRC_AI_apps_kit#2.md](https://github.com/Grovety/GRC-AI-apps/blob/main/GRC_AI_apps_kit%232.md).

2. The UART communication protocol described [here](https://github.com/Grovety/GRC-AI-apps/blob/main/GRC_protocol.md).

3. UART parameters:

| Parameter           | Value                                |
| ------------------- | ------------------------------------ |
| UART TX pin         | GPIO_NUM_21                          |
| UART RX pin         | GPIO_NUM_20                          |
| UART NUM            | UART_NUM_1                           |

# Build instructions

ESP-IDF version: v5.2.1

## Supported devices

- GRC Devboard esp32c3

## Configure the project

```bash
idf.py menuconfig
```

## Build, Flash and Run

Build the project and flash it to the board:

```
idf.py -p PORT build flash monitor
```

(Replace PORT with the name of the serial port to use)
___________

Also, you can use binaries from https://github.com/Grovety/GRC-AI-apps/tree/main/firmware

Use https://github.com/Grovety/GRC-AI-apps/blob/main/firmware/flash_tool.zip to flash the board.
