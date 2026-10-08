# AGISCORE 🛡️
"AI Powered Safety & Intelligence: Arduino Uno Based Multi-Hazard Safety System"

AGISCORE is a multi-hazard detection and response system built on an Arduino Uno. It monitors flame, gas/smoke, air quality, temperature and humidity in real time, and responds automatically by activating an ultrasonic mist maker and an exhaust fan, while alerting occupants through a buzzer, LEDs and an OLED display.

> Submitted in partial fulfillment of the requirements for the degree of **Bachelor of Technology in Computer Science & Engineering (AI & ML)
> ITS Engineering College, Greater Noida | Academic Year 2026–2027

---

# Problem Statement
Standard hazard detection systems are reactive: they alert people but take no immediate action to douse flames or vent toxic gas. AGISCORE combines multi-sensor detection with automatic suppression and ventilation, so the response starts without any manual delay.

# Features
- **Multi-sensor monitoring:** Flame (IR), MQ-2 (gas/smoke), MQ-135 (air quality/CO2) and DHT11 (temperature/humidity)
- **Automated dual mitigation:** Relay-driven ultrasonic mist maker and DC exhaust fan, triggered when sensor readings cross set thresholds
- **Instant local alerts:** Buzzer, status LEDs and a 0.96" OLED display showing live readings
- **Fail-safe power:** Twin 18650 Li-ion battery backup (TP4056 charging module + MT3608 boost converter)
- **Low cost and easy to build:** Uses widely available components

# Hardware Components
| Component | Purpose |
|---|---|
| Arduino Uno | Main microcontroller |
| Flame sensor (IR) | Fire detection |
| MQ-2 | Gas / smoke detection |
| MQ-135 | Air quality / CO2 |
| DHT11 | Temperature and humidity |
| 2-channel relay module | Switches mist maker and exhaust fan |
| Ultrasonic mist maker | Suppression |
| 5V DC exhaust fan | Ventilation |
| 0.96" OLED (I2C) | Live status display |
| Buzzer and LEDs | Audio / visual alerts |
| 2 × 18650 batteries, TP4056, MT3608 | Backup power supply |

# Pin Configuration (Arduino Uno)
| Device | Pin |
|---|---|
| Flame sensor | D2 |
| DHT11 | D3 |
| Relay 1 (Mist maker) | D4 |
| Relay 2 (Exhaust fan) | D5 |
| Buzzer | D8 |
| LEDs (Green / Red / Blue) | D9, D10, D11 |
| MQ-135 | A0 |
| MQ-2 | A1 |
| OLED SDA / SCL | A4 / A5 |

> Update this table if your final wiring changes.

# Project Structure
```
AGISCORE/
├── README.md
├── LICENSE
├── CONTRIBUTORS.md
├── docs/            # Synopsis, circuit diagram, report
├── hardware/        # Wiring, pin map, power circuit
├── arduino-code/    # Arduino sketches (.ino)
└── app-and-display/ # Display and dashboard work
```

## 🚀 Getting Started
1. **Clone the repository**
```bash
   git clone https://github.com/shashwat903/AGISCORE.git
   cd AGISCORE
```
2. **Install the Arduino IDE** from [arduino.cc](https://www.arduino.cc/en/software).
3. **Install the required libraries** (Sketch → Include Library → Manage Libraries):
   - DHT sensor library (Adafruit)
   - Adafruit SSD1306 and Adafruit GFX
4. **Wire the circuit** as shown in `hardware/` and the pin table above.
5. **Open the sketch** in `arduino-code/`, select **Arduino Uno** and the correct port, then click **Upload**.
6. Power the system and open the Serial Monitor at **9600 baud** to see live readings.

 Team and Roles
| Member | Role | Responsibilities |

| Shashwat Singh | Hardware & Embedded Lead | Circuit wiring, relays, mist maker and fan control, battery power system |
| Samiksha Chauhan | Sensing & Alert Logic Lead | Sensor calibration, threshold logic, buzzer/LED alert behaviour |
| Mehak | Display & Documentation Lead | OLED interface, README and report, testing records, demo |

All members share code review, testing and final presentation duties.

 Project Guide
This project is developed under the guidance of Prof. Anjali Shrivastav

Prof. Anjali Shrivastav
Faculty Member / Project Guide, Department of Computer Science & Engineering
ITS Engineering College, Greater Noida

 Future Scope
- Add an ESP8266 / ESP32 module for WiFi, so readings and alerts can go to a Blynk or Flutter mobile dashboard
- Voice alerts and an AI voice assistant using a DFPlayer Mini or an ESP32 with the Gemini API
- TinyML-based prediction of rapid temperature rise before ignition
- Data logging and an SMS / push notification system

 Applications
Smart homes, laboratories, server rooms and small industrial spaces that need early hazard containment and automatic gas venting.

 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file.

 🙏 Acknowledgements
Thanks to our project guide Prof. Anjali Shrivastav and the Department of CSE, ITS Engineering College, for their guidance and support.
