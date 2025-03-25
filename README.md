# Women-Safety
# Women Safety Voice-Activated Security System 

##  Project Overview
The **Women Safety Voice-Activated Security System** is a **machine learning-powered safety system** that detects **emergency voice commands, records audio & video evidence, and sends alerts** to emergency contacts. The system works **offline for voice activation** and automatically **enables the internet** to upload recorded data to a backend server once an emergency is detected.

##  Key Features
**Voice-Activated Emergency Detection** (Works Offline)  
**Automatic System Volume Increase & Alert Message**  
**Audio & Video Recording** for Evidence Collection  
**Automatic Internet Activation for Data Transfer**  
**Offline Data Storage & Auto-Upload When Online**  
**Real-time GPS Tracking & Emergency Alerts via WhatsApp/SMS**  
**User-Friendly & Works on Windows/Linux**  

---

## 🛠️ Technologies & Libraries Used

### **1️Machine Learning & Speech Recognition**
- **Pocketsphinx** → Offline **voice recognition** for detecting "Start Recording"
- **DeepSpeech / Wav2Vec2** → High-accuracy **speech-to-text conversion**
- **OpenCV** → **Real-time video recording & processing**
- **Numpy** → **Efficient data handling**
- **Librosa** → **Audio processing for speech analysis**

### **2️ IoT & System Control**
- **PyCaw** → **Automatically sets system volume to 100%**
- **OS & Platform** → **Enables WiFi automatically after voice detection**
- **Time & Threading** → **Handles multi-tasking operations smoothly**

### **3️ Networking & Backend Communication**
- **Requests** → **Uploads video & audio to the backend**
- **Twilio API** → **Sends emergency WhatsApp/SMS alerts**
- **Geopy** → **Retrieves real-time GPS location**

---

##  How It Works

### **1️ Initialization**
- The system **starts and sets the volume to 100%**.
- It then **plays an alert message** notifying that the system is active.
- **Waits for voice activation** ("Start Recording").

### **2️ Voice-Activated Recording (Offline)**
- Uses **Pocketsphinx** (offline model) to **detect emergency phrases**.
- Once it hears **"Start Recording"**, it:
  1. **Enables WiFi (if disabled)**.
  2. **Starts audio & video recording**.
  3. **Saves the recordings locally**.

### **3️ Data Transmission & Emergency Alerts**
- If the internet is available, **uploads recorded data** to the backend.
- If the internet is **not available**, stores data in a "Pending Uploads" folder.
- **When the internet is restored, automatically uploads pending files**.
- **GPS location is retrieved and sent via WhatsApp/SMS**.

---

## 🛠️ Installation & Setup

### **1️ Install Dependencies**
```sh
pip install pocketsphinx speechrecognition opencv-python numpy requests pycaw pygame geopy twilio
