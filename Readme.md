# 🛰️ Arduino Radar Project  

A cool Arduino radar that sweeps an ultrasonic sensor from **15° → 165° → 15°**, measures distance, and streams the data so you can watch objects appear on a live radar screen! 🌟  

---

## ✨ What It Does  
- 🔊 **Ultrasonic sensing** – Detects objects and measures their distance in real time.  
- ⚙️ **Servo scanning** – Moves back and forth like a real radar.  
- 💻 **Serial data** – Outputs `angle,distance.` so a Processing sketch can draw a sweeping radar.  

---

## 🧰 Parts You’ll Need  
- 🟦 Arduino Uno (or any compatible board)  
- 📡 HC-SR04 Ultrasonic Sensor  
- 🔄 SG90/SG92R Servo Motor  
- 🧵 Jumper wires & breadboard  
- 🔌 USB cable for power/programming  
- 🩹 **Double-sided tape or a glue gun** to secure the sensor and servo in place  

### 🔗 Wiring (Ultrasonic Sensor)

| Part | Pin on Arduino |
|------|---------------|
| HC-SR04 **Trig** | D10 |
| HC-SR04 **Echo** | D11 |
| VCC / GND | 5 V / GND |

---

## 🔌 Servo Motor Connection  ⚠️  
Follow these connections **exactly** to avoid damaging the servo motor:

| Servo Wire | Connect To |
|------------|-----------|
| 🔴 **Red**    | 5 V |
| 🟡 **Yellow** | Pin 12 |
| 🟤 **Brown**  | GND |

⚠️ **Important:** Please follow these connections carefully or you risk damaging your servo motor.

---

## 🖥️ Software  
- Arduino IDE (latest version)  
- Servo library (already included)  
- *Optional:* Processing IDE if you want the fancy radar display 💚

---

## 🚀 Quick Start  
1. Open **`radar.ino`** in the Arduino IDE.  
2. Select your board & COM port.  
3. Click **Upload**.  
4. Open the **Serial Monitor** at **9600 baud** to watch `angle,distance` readings.  
   - 👉 Run a Processing sketch to see the sweeping radar visuals.

---

## 🧩 How the Code Works  
- `setup()` – Sets pins, starts Serial, attaches the servo.  
- `loop()` – Sweeps the servo left ↔ right, grabs distance at each angle, prints the data.  
- `calculateDistance()` – Sends a trigger pulse and calculates distance in cm.  

---

## 💡 Fun Add-Ons  
- 🔔 Add a buzzer or LED for objects closer than a set distance.  
- 📶 Send data wirelessly with Bluetooth/Wi-Fi.  
- 🎨 Customize the Processing radar colors & speed.

---

## 📜 License  
MIT License – hack it, remix it, share it!  
