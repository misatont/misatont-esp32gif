# ESP32 OLED GIF Display
Display any GIFs on an OLED (SSD1306) using an ESP32 :)
Created by @misaprojects on TikTok (soon to be uploaded)

## Required Components

- ESP32
- 128x64 OLED Display (SSD1306)
- Dupont Wires

## 📌 Pin Connections

| ESP32 Pin | OLED Pin | Description |
|----------|----------|-------------|
| 3.3V     | VCC      | Power       |
| GND      | GND      | Ground      |
| GPIO 21  | SDA      | Data line   |
| GPIO 22  | SCL      | Clock line  |

## ⚙️ Setup

This project is made for simulation using the **Wokwi platform**.

###  How to run it:
1. Go to https://wokwi.com
2. Create a new ESP32 project
3. Add an SSD1306 OLED display
4. Paste the provided code
5. Click **Run**
(No physical wiring is required — everything runs in simulation)

## 🎞️ How to Create GIF Animation (ESP32 OLED Frames)

This guide explains how to convert a GIF into frames and display it on an SSD1306 OLED (128x64) using an ESP32.

---

###  Step 1 — Get a GIF
- Go to https://giphy.com  
- Search and download the GIF you want to use

---

###  Step 2 — Split into frames
- Go to https://ezgif.com/split  
- Upload your GIF  
- Click **Split to frames**  
- Download all frames  
- Resize all frames to **128 × 64 pixels**

---

###  Step 3 — Convert frames to C arrays
- Go to https://javl.github.io/image2cpp/
- Upload **one frame at a time**
- Use these settings:
  - Output: Arduino code  
  - Mode: Monochrome  
  - Size: 128 × 64  
- Click **Generate code**
- Copy the generated C array

---

### 💻 Step 4 — Add frames to your project
- Open `src/main.cpp`
- Find the section:

```cpp
// BITMAP FRAMES
const unsigned char frame1[PASTE GENERATED C ARRAY]
const unsigned char frame2[PASTE GENERATED C ARRAY]
