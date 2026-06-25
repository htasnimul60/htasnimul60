<div align="center">

# 👋 Hi, I'm Tasnimul Hasan

### CSE Student · Embedded Systems Developer · IoT Builder

![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![ESP8266](https://img.shields.io/badge/ESP8266-gray?style=flat-square&logo=espressif&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)

</div>

---

## 💡 About Me

I build systems where **hardware, firmware, and software work together end-to-end** — from assistive devices that help visually impaired people navigate safely, to smart EV charging infrastructure, to autonomous radar defense systems.

My projects are real, working hardware. I enjoy designing state machines, non-blocking firmware, and web dashboards that talk to physical sensors in real time.

---

## 🛠️ Tech Stack

| Area | Tools |
|------|-------|
| 💻 Languages | C, C++ |
| ⚡ Hardware | ESP32, ESP8266, Arduino Uno, RFID RC522, INA219, SIM900A GSM, HC-SR04, Servo, IR |
| 🔗 Protocols | I2C, SPI, UART, SoftwareSerial, WiFi, Bluetooth, GSM/SMS, GPS |
| 🌐 Web | HTML, CSS, ESP WebServer |

---

## 🚀 Projects

### 🦯 Smart Blind Stick — Assistive Navigation Device
> ESP32 · HC-SR04 ×3 · SIM900A GSM · NEO-6M GPS · Water Sensor

ESP32-powered walking stick for visually impaired users. Three ultrasonic sensors cover different danger zones simultaneously. Non-blocking buzzer plays distinct alert patterns per hazard type. In an emergency, holding the button for 1 second sends a **live GPS location via SMS** to a preset contact number using SIM900A.

| Sensor | Position | Detects |
|--------|----------|---------|
| HC-SR04 #1 | Chest height | Large objects (walls, people) |
| HC-SR04 #2 | Ground level | Small obstacles (curbs, bags) |
| HC-SR04 #3 | Downward | Holes, drops, missing steps |
| Water sensor | Bottom | Puddles, wet ground |

**Buzzer alerts:** Continuous → large object · 2 fast beeps → hole · 3 beeps → small object · 2 slow beeps → water  
**SOS SMS:** Button hold (1s) → `"Emergency! Help needed. Location: maps.google.com/..."`

---

### ⚡ IoT Wireless EV Charging Station
> ESP32 · RFID RC522 · INA219 · Servo Gate · WiFi Web Dashboard

Full EV charging station with RFID-controlled entry gate, real-time power monitoring, and automatic charge termination. A live web dashboard refreshes every 3 seconds with voltage, current, power, battery level, gate/relay status, and per-session cost.

**Flow:** Car detected (IR1) → Scan RFID → Gate opens (servo) → Car parks (IR2) → Gate closes → Charging starts → Auto-stop at 4.1V / <50mA → Cost displayed → Gate opens for exit

**Cost formula:** `cost (taka) = (energy_Wh / 1000) × 8 tk/kWh`  
**Dashboard:** Voltage · Current · Power · Battery % bar · RFID auth status · Cost · Session time

---

### 🎯 Tasnim Defense System — Autonomous Radar
> Arduino Uno · ESP8266 · Servo ×3 · HC-SR04 · Real-time Web UI

Arduino sweeps a servo-mounted ultrasonic sensor from 15° to 165° and streams angle + distance data to ESP8266 over SoftwareSerial every 50ms. The ESP hosts a live radar web dashboard. The web UI can send `AIM:angle` and `FIRE` commands back to Arduino — the aim servo locks onto a target and the fire servo triggers.

**Servos:** Radar (auto-sweep) · Aim (web-controlled targeting) · Fire (trigger)  
**Features:** `flipAngle()` correction for physically reversed servos, non-blocking sweep, servo detach when idle  
**Comms:** Arduino ↔ ESP8266 via SoftwareSerial 9600 baud · angle + distance stream at 50ms interval

---

## 🎯 Current Goals

- [ ] Add target-lock algorithm to the Defense System radar
- [ ] Ship Smart Blind Stick v1 — field-test ready
- [ ] Build a freelancing-ready portfolio
- [ ] Strengthen DSA fundamentals

---

## 📊 GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=htasnimul60&show_icons=true&theme=tokyonight&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=htasnimul60&layout=compact&theme=tokyonight&hide_border=true)
![GitHub Streak](https://streak-stats.demolab.com?user=htasnimul60&theme=tokyonight&hide_border=true)

</div>

---

## 📫 Connect

[![GitHub](https://img.shields.io/badge/GitHub-htasnimul60-181717?style=flat-square&logo=github)](https://github.com/htasnimul60)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Tasnimul_Hasan-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/htasnimul60/)

---

<div align="center">

*"Measure twice, solder once — then ship it."*

</div>
