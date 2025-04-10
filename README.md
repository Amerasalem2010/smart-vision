---

# 🔐 RFID Access Control System with LCD and Servo

This Arduino project is a simple RFID-based access control system that reads RFID card data using an *MFRC522 RFID module, displays messages on a **16x2 I2C LCD, and controls a **servo motor* to simulate a door opening or closing.

---

## 📦 Components Used

- Arduino Uno (or compatible board)
- MFRC522 RFID Reader
- RFID Tag/Card
- 16x2 I2C LCD Display
- Servo Motor
- Jumper Wires
- Breadboard (optional)
- Power Supply (USB or battery)

---

## 🔧 How It Works

1. The system initializes the RFID reader, LCD, and servo motor.
2. It displays a message: Scan Your Card...
3. When a card is scanned:
   - The UID is read and compared to the pre-set authorized ID.
   - If matched, it prints ACCESS GRANTED!, opens the servo (simulated door), and shows the UID.
   - If not matched, it prints ACCESS DENIED! and shows the UID.
4. After a short delay, it resets and waits for the next card scan.

---

## 🧠 Code Highlights

- *Authorized UID:* My_ID = "3363C51A" → Replace this with your actual card UID.
- *LCD Address:* 0x27 → Ensure this matches your LCD's I2C address.
- *Servo Control:* Pin 6 controls the servo angle for open (90°) and close (0°).

---

## 📂 Libraries Required

Install the following libraries in the Arduino IDE:
- MFRC522 by GithubCommunity
- LiquidCrystal_I2C by Frank de Brabander (or equivalent)
- Servo by Arduino

---

## 📝 Setup Instructions

1. Connect your components as per the wiring diagram:
   - RFID SDA → Pin 10  
   - RFID RST → Pin 9  
   - Servo Signal → Pin 6  
   - LCD SCL → A5, SDA → A4 (for Uno)

2. Upload the code to your Arduino board.
3. Open Serial Monitor to debug (optional).
4. Scan a card and observe the LCD and servo motor actions.

---

## 📌 Notes

- Servo angles (0 and 90) can be adjusted depending on your setup.
- You can store multiple UIDs for multiple users by modifying the code.
- Make sure your servo has enough power — using external power might be needed.

---

## 🎯 Applications

- Smart door lock
- Student attendance system
- Time-in/time-out tracker
- Entry control for rooms, labs, or lockers

---
