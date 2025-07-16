# 🚨 EMS - Emergency Alert System App

EMS is a real-time mobile emergency alert system built using **React Native**. It enables users to send SOS alerts, receive suspicious activity notifications, and monitor their surroundings using integrated CCTV + AI technology.

---

## 📱 Features

### 🔐 Authentication
- Email/password signup & login using Firebase Authentication
- Stores user profile (name, address, emergency contact) in Firebase Realtime Database

### 🆘 SOS Alert via Volume Key
- Long press `Volume Down` key triggers an SOS alert
- Sends emergency message & location via WhatsApp
- Alert also notifies emergency contact using FCM

### 🛰️ Real-Time Location Sharing
- On SOS, shares user’s location using a WhatsApp link (`https://maps.google.com/?q=lat,long`)

### 🎥 Suspicious Activity Detection (YOLOv8)
- Integrated with YOLOv8 model to detect anomalies:
  - Person with a gun
  - Climbing over walls
  - Masked individuals
  - Lock breaking
  - Falling down
- Notifications sent using Flask/Node.js backend via FCM to mobile app

### 🔔 Local Notifications
- Uses `react-native-push-notification` to show alerts in the notification tray

### 📷 IP Camera Integration
- IP camera feeds are added by user and monitored using backend
- Users can view footage and receive real-time alerts on detection

### 📂 Alert History & Video Playback
- App includes a screen showing recent detection events
- Video playback of detected anomalies available in app

---

## 🔧 Tech Stack

| Tech                     | Description                           |
|--------------------------|---------------------------------------|
| React Native             | Cross-platform mobile app             |
| Firebase Auth/Database   | User authentication & data storage    |
| Firebase Cloud Messaging | Real-time notifications               |
| YOLOv8                   | AI-based activity detection           |
| Flask / Node.js          | Backend for ML detection & notifications |
| RTSP / IP Camera         | Real-time camera integration          |
| WhatsApp API (intent)    | Sharing location via message          |
| Android Studio           | Android build & debug tool            |

---

## 🗂️ Folder Structure

```bash
EMS-App/
├── screens/
│   ├── LoginScreen.js
│   ├── SignupScreen.js
│   ├── HomeScreen.js
│   ├── AddCameraScreen.js
│   ├── AlertsScreen.js
├── firebase/
│   └── firebaseConfig.js
├── utils/
│   └── LocalNotification.js
├── App.js
└── ...
```

## UI 

This UI design was created as an initial concept at the early stage of the project. It represents the ideal user interface and experience we aimed to build for the EMS application.

However, please note that we were not able to fully implement this design in the final product due to:

Limited development resources

Technical and operational constraints

Platform-specific restrictions

While this file remains part of the repo for reference and documentation purposes, the final implementation may differ significantly from this design.
<img width="1897" height="810" alt="Screenshot 2025-07-16 132707" src="https://github.com/user-attachments/assets/495c6415-2efb-4601-a419-cb280d9aa323" />

<img width="1517" height="802" alt="Screenshot 2025-07-16 132754" src="https://github.com/user-attachments/assets/9b2b3d3e-4947-4a47-bf81-7aae4058d712" />
<img width="1543" height="795" alt="Screenshot 2025-07-16 132826" src="https://github.com/user-attachments/assets/f1a852ca-de1f-44bb-8d08-37e7af0681cd" />

