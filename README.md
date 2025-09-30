# This repository controls an RGB LED to perform synchronized lighting effects that are triggered at specific times in a selected song

## Workflow
When the button is pressed, the RGB LED begins a programmed sequence of lighting patterns.
These patterns are synchronized with the song’s rhythm and beat, creating a dynamic light show that matches the music.

## Hardware Required
- Arduino Uno R3
- DFPlayer Mini
- WS2812B
- Sound sensor

## Wiring
| DFPlayer Mini Pin    | Connects To Arduino Uno               |
| -------------------- | ------------------------------------- |
| **TX**               | Pin **10** (Uno RX)                   |
| **RX**               | Pin **11** (Uno TX)                   |
| **VCC**              | **5V**                                |
| **GND**              | **GND**                               |
| **SPK_1**, **SPK_2** | Connect to a small speaker (optional) |
| **DAC_L**, **DAC_R** | Optional for external amplifier       |

| WS2812B Pin | Connects To Arduino Uno |
| ----------- | ----------------------- |
| **DIN**     | **Pin 7**               |
| **+5V**     | **5V** (or external 5V) |
| **GND**     | **GND**                 |

| Button            | Connects To Arduino Pin | Other Side Connects To |
| ----------------- | ----------------------- | ---------------------- |
| **Play**          | **Pin 2**               | **GND**                |
| **Stop**          | **Pin 3**               | **GND**                |
| **Next**          | **Pin 4**               | **GND**                |
| **(Unknown 4th)** | **Pin 5**               | **GND**                |

## Software Requirement
| Library Name            | Description                                                          |
| ----------------------- | -------------------------------------------------------------------- |
| **FastLED**             | Controls WS2812B (NeoPixel-style) addressable LEDs                   |
| **SoftwareSerial**      | Allows serial communication on digital pins (used for DFPlayer Mini) |
| **DFRobotDFPlayerMini** | Communicates with the DFPlayer Mini MP3 module                       |

## Guidance
The most complete hardware set up in this project is the DFPlayer Mini as other hardware is good to run without any changes. You should purchase a sd card and sd card reader, those will be used to download you own prefer song (as in this project the selected song was **Tết Đong Đầy by KHOA x Kay Tran x Duck V**. 

Connect the sd card reader into your own computer, then download and store your prefer song within the sd card. Then enter sd card in DFPlayer Mini.

If you prefer to alter this project to make your own rgb led movement based on the song beat, then I suggect you to download free to access software which can differentiate beats in a song. Then change the code accordingly.


