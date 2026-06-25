<div align="center">

<table>
<tr>
<td width="65%">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,100:2c5364&height=200&section=header&text=Tasnimul%20Hasan&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Embedded%20Systems%20%7C%20IoT%20Builder&descAlignY=58&descSize=18" width="100%"/>

</td>
<td width="35%">

<img src="https://raw.githubusercontent.com/devSouvik/devSouvik/master/gif/Coding.gif" width="100%"/>

</td>
</tr>
</table>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&duration=3000&pause=1000&color=00E5FF&center=true&vCenter=true&width=600&lines=Building+real+hardware%2C+not+just+code;ESP32+%2B+Arduino+%2B+Sensors+%2B+Servos;Smart+Blind+Stick+%7C+EV+Charging+%7C+Radar" alt="Typing SVG" />
</a>

<br><br>

🔭 **Currently building:** Smart Blind Stick v1 &nbsp;|&nbsp; 🌱 **Learning:** Advanced DSA &nbsp;|&nbsp; ⚡ **Powered by:** ESP32 + curiosity

<br>

![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white)
![ESP8266](https://img.shields.io/badge/ESP8266-000000?style=for-the-badge&logo=espressif&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)

</div>

<br>

## 💡 About Me

I build systems where **hardware, firmware, and software work together end-to-end** — from assistive devices that help visually impaired people navigate safely, to smart EV charging infrastructure, to autonomous radar defense systems.

My projects are real, working hardware. I enjoy designing state machines, non-blocking firmware, and web dashboards that talk to physical sensors in real time.

<br>

## 🛠️ Tech Stack

<div align="center">

![C++](https://img.shields.io/badge/-C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=white)
![Arduino](https://img.shields.io/badge/-Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![ESP32](https://img.shields.io/badge/-ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

</div>

| Category | Stack |
|---|---|
| **Microcontrollers** | ESP32 · ESP8266 · Arduino Uno |
| **Sensors & Modules** | RFID RC522 · INA219 · SIM900A GSM · HC-SR04 Ultrasonic · NEO-6M GPS |
| **Actuators** | Servo Motors · Relay Modules |
| **Protocols** | I2C · SPI · UART · SoftwareSerial · WiFi · Bluetooth · GSM/SMS |
| **Web** | HTML · CSS · ESP WebServer (live dashboards) |

<br>

## 🚀 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### 🦯 Smart Blind Stick
![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)

**ESP32 · HC-SR04 ×3 · SIM900A · GPS**

Assistive navigation device for visually impaired users. Three ultrasonic sensors monitor chest-height, ground-level, and downward zones simultaneously. Distinct buzzer patterns signal different hazards. Emergency button triggers an **SOS SMS with live GPS location**.

`Multi-zone sensing` `GSM/SMS alerts` `Non-blocking firmware`

</td>
<td width="50%" valign="top">

### ⚡ IoT EV Charging Station
![Status](https://img.shields.io/badge/Status-Completed-blue?style=flat-square)

**ESP32 · RFID · INA219 · Servo**

Automated EV charging station with RFID-gated entry, real-time power monitoring, and auto-stop charging logic. Live web dashboard shows voltage, current, cost, and gate status — refreshing every 3 seconds.

`State machine design` `Power monitoring` `Live web dashboard`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🎯 Autonomous Defense Radar
![Status](https://img.shields.io/badge/Status-Completed-blue?style=flat-square)

**Arduino · ESP8266 · Servo ×3**

Radar-style ultrasonic scanner that streams live angle/distance data to a web dashboard. Operator can send aim and fire commands back to the Arduino in real time over serial.

`Dual-MCU comms` `Real-time control` `Servo calibration`

</td>
<td width="50%" valign="top">

<br>

*More projects coming soon — currently prototyping new sensor integrations.*

</td>
</tr>
</table>

<details>
<summary><b>📋 Click for detailed specs on each project</b></summary>
<br>

**🦯 Smart Blind Stick**

| Sensor | Position | Detects |
|--------|----------|---------|
| HC-SR04 #1 | Chest height | Large objects (walls, people) |
| HC-SR04 #2 | Ground level | Small obstacles (curbs, bags) |
| HC-SR04 #3 | Downward | Holes, drops, missing steps |
| Water sensor | Bottom | Puddles, wet ground |

Buzzer alerts → Continuous: large object · 2 fast beeps: hole · 3 beeps: small object · 2 slow beeps: water
SOS → Hold button 1s → SMS with Google Maps link via SIM900A

---

**⚡ IoT EV Charging Station**

Flow: Car detected (IR1) → Scan RFID → Gate opens → Car parks (IR2) → Gate closes → Charging starts → Auto-stop at 4.1V / <50mA → Cost shown → Gate opens for exit

Cost formula: `cost (taka) = (energy_Wh / 1000) × 8 tk/kWh`
Dashboard: Voltage · Current · Power · Battery % · RFID status · Cost · Session time

---

**🎯 Autonomous Defense Radar**

Arduino sweeps a servo-mounted ultrasonic sensor (15°–165°) and streams angle + distance to ESP8266 every 50ms via SoftwareSerial. ESP hosts a live radar web UI that can send `AIM:angle` and `FIRE` commands back.

Servos: Radar (auto-sweep) · Aim (web-controlled) · Fire (trigger)
Comms: Arduino ↔ ESP8266 @ 9600 baud

</details>

<br>

## 🎯 Current Goals

- 🔭 Add target-lock algorithm to the Defense Radar
- 🦯 Ship Smart Blind Stick v1 — field-test ready
- 💼 Build a freelancing-ready portfolio
- 📚 Strengthen DSA fundamentals

<br>

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=htasnimul60&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117" width="48%"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=htasnimul60&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117" width="35%"/>

<img src="https://streak-stats.demolab.com?user=htasnimul60&theme=tokyonight&hide_border=true&background=0D1117" width="90%"/>

</div>

<br>

## 🏆 GitHub Trophies

<div align="center">

<img src="https://github-profile-trophy.vercel.app/?username=htasnimul60&theme=tokyonight&no-frame=true&no-bg=false&margin-w=8&row=1&column=6" width="100%"/>

</div>

<br>

## 📫 Connect With Me

<div align="center">

<a href="https://github.com/htasnimul60"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/htasnimul60/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:htasnimul60@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>

</div>

<br>

<div align="center">

*"Measure twice, solder once — then ship it."*

<img src="https://komarev.com/ghpvc/?username=htasnimul60&style=flat-square&color=00E5FF&label=Profile+Views"/>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=100&section=footer" width="100%"/>
