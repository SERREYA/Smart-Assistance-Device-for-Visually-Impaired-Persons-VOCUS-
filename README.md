# Smart Assistance Device for Visually Impaired Persons

## 📌 Project Overview
The **Smart Assistance Device for Visually Impaired Persons** is a hardware-based embedded system designed to assist visually impaired users in safe navigation, text recognition, and emergency communication.  
The system integrates **computer vision, LiDAR sensing, OCR, and audio feedback**, implemented on a **Raspberry Pi 4 Model B** platform.

---

## 🎯 Objectives
- Detect obstacles in real time
- Measure distance to nearby objects accurately
- Identify printed characters and letters using OCR
- Provide audio feedback for all system outputs
- Enable emergency communication via GSM
- Offer a portable and user-friendly wearable design

---

## 🧠 System Features
- Real-time obstacle detection using camera vision
- Accurate distance measurement using LiDAR sensor
- Optical Character Recognition (OCR) for text reading
- Audio-based feedback for navigation and text output
- Emergency SMS alert system
- Custom 3D-printed enclosure for ergonomic use

---

## 🧰 Hardware Components
- **Raspberry Pi 4 Model B**
- **Raspberry Pi Camera Module V2**
- **VL53L0X / VL53L1X LiDAR Distance Sensor**
- **SIM800L GSM Module**
- **11.1V LiPo Battery**
- **UBEC 5V / 7A Power Module**
- **LM2596 Buck Converters**
- Custom **3D-Printed Enclosure**

---

## 🔤 OCR (Character & Letter Recognition)
The device is capable of identifying **printed characters and letters** from the live camera feed using  
**:contentReference[oaicite:0]{index=0}**.

### OCR Capabilities
- Recognition of printed text, letters, and numbers
- Works with labels, signs, and documents
- Real-time image capture and processing
- OCR output converted directly to audio

---

## 🔊 Audio Feedback System
All system outputs are delivered to the user through **audio feedback**, ensuring complete accessibility without visual interaction.

### Audio Feedback Includes
- Spoken OCR text output
- Obstacle distance announcements
- Warning alerts for close objects
- System status notifications
- Emergency action confirmations

### Audio Implementation
- Python-based Text-to-Speech (TTS)
- Audio output via speaker or earphones
- Priority handling to avoid overlapping alerts

---

## 💻 Software & Tools
- **Programming Language:** Python
- **Operating System:** Raspberry Pi OS
- **Computer Vision:** OpenCV
- **OCR Engine:** Tesseract OCR
- **Text-to-Speech:** Python TTS Engine
- **Communication:** Serial (SIM800L GSM)
- **System Type:** Autonomous / Real-Time Embedded System

---

## ⚙️ System Architecture & Workflow
1. Camera captures real-time image frames
2. Image is processed for:
   - Obstacle detection
   - Text and character recognition (OCR)
3. LiDAR sensor measures distance to obstacles
4. Raspberry Pi evaluates environmental risk
5. Detected information is converted to speech
6. Audio feedback is delivered to the user
7. Emergency SMS is sent via GSM when triggered

---

## 🔌 Power Management
- 11.1V LiPo battery as the main power source
- UBEC provides regulated 5V supply for Raspberry Pi
- LM2596 buck converters regulate voltage for peripherals
- Designed for portable and long-duration operation

---

## 🛠️ Installation & Setup

### Hardware Setup
- Connect Camera Module to CSI interface
- Connect LiDAR sensor via I2C
- Connect SIM800L via UART
- Ensure correct voltage levels for GSM and sensors

### Software Setup
```bash
sudo apt update
sudo apt install tesseract-ocr python3-opencv python3-numpy
pip install pytesseract pillow pyserial
