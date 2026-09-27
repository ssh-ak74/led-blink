#  ESP32 LED Blink

A simple **ESP32 LED blinking project** built with Arduino and PlatformIO.

This project turns an LED on and off repeatedly using an ESP32 GPIO pin.

##  Features

*  LED blinking
*  ESP32 GPIO control
*  500ms ON / 500ms OFF
*  Built with PlatformIO
*  Simple and beginner-friendly
*  MIT licensed

##  Wiring

| Component         | Connection                      |
| ----------------- | ------------------------------- |
| ESP32 GPIO 2      | 1kΩ resistor → LED long leg (+) |
| LED short leg (−) | Breadboard GND rail             |
| ESP32 GND         | Breadboard GND rail             |

```text
ESP32 GPIO 2 ── 1kΩ ──► LED (+)
                         LED (−)
                           │
ESP32 GND ──────────────── GND
```

> The resistor limits current through the LED.

##  Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ssh-ak74/led-blink.git
cd led-blink
```

### 2. Open with PlatformIO

Open the project in **VS Code with PlatformIO** installed.

### 3. Connect your ESP32

Connect the ESP32 to your computer using USB.

### 4. Upload

Run:

```bash
pio run --target upload
```

Or use the **Upload** button in PlatformIO.

##  How It Works

The ESP32 sets GPIO 2 as an output:

```cpp
pinMode(LED, OUTPUT);
```

The LED is then turned on:

```cpp
digitalWrite(LED, HIGH);
```

After 500 milliseconds, it is turned off:

```cpp
digitalWrite(LED, LOW);
```

The process repeats continuously.

##  Project Structure

```text
led-blink/
├── src/
│   └── main.cpp
├── platformio.ini
├── LICENSE
└── README.md
```

##  Hardware

* ESP32 development board
* 1× LED
* 1× 1kΩ resistor
* Breadboard
* Jumper wires
* USB cable

##  License

This project is licensed under the **MIT License**.

See [`LICENSE`](LICENSE) for details.

