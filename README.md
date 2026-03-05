🦾 GestureArm

> Real-time gesture-controlled robotic arm simulation using on-device AI hand tracking — no backend, no server, just your hand and a webcam.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-gesture--arm.netlify.app-00C7B7?style=for-the-badge&logo=netlify)](https://gesture-arm.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](./LICENSE)
[![Built with MediaPipe](https://img.shields.io/badge/AI-MediaPipe%20Hands-FF6F00?style=for-the-badge&logo=google)](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker)
[![Three.js](https://img.shields.io/badge/3D-Three.js-black?style=for-the-badge&logo=three.js)](https://threejs.org/)

---

## ✨ Overview

**GestureArm** lets you control a 3D robotic arm in real time using nothing but your hand in front of a webcam. MediaPipe's on-device hand tracking detects 21 hand landmarks per frame, maps them to joint angles, and Three.js renders the arm's response instantly — all running locally in the browser with zero latency from a server.

---

## 🚀 Live Demo

👉 [gesture-arm.netlify.app](https://gesture-arm.netlify.app/)

---

## 🎮 Gesture Controls

| Gesture | Robot Action |
|---|---|
| ✋ Move hand **left / right** | Base rotation |
| ☝️ Move hand **up / down** | Elbow angle |
| 🖐️ **Open hand** | Gripper opens |
| ✊ **Close fist** | Gripper closes |

---

## ⚙️ How It Works

1. **Hand Tracking** — MediaPipe Hands runs entirely on-device via your webcam, detecting 21 landmarks on your hand in real time.
2. **Gesture Mapping** — Hand position and finger angles are translated into robot joint angles (base, elbow, gripper).
3. **3D Rendering** — Three.js renders a responsive 3D robotic arm that mirrors your hand movements frame by frame.

```
Webcam → MediaPipe Hands → Joint Angle Mapping → Three.js Arm Render
```

---

## 🛠️ Tech Stack

| Technology | Role |
|---|---|
| **MediaPipe Hands** | On-device ML hand landmark detection |
| **Three.js** | 3D robotic arm rendering |
| **Vanilla JS / HTML** | Core application logic |
| **Netlify** | Deployment & hosting |

---

## 🏃 Running Locally

No build step required — this is a pure HTML/JS project.

1. **Clone the repository**
   ```bash
   git clone https://github.com/alphonsjaison/gesture-arm.git
   cd gesture-arm
   ```

2. **Serve locally** (required for webcam access)

   Using Python:
   ```bash
   python -m http.server 8080
   ```
   Or using the VS Code [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension.

3. **Open in browser**
   ```
   http://localhost:8080
   ```

4. **Allow webcam access** when prompted — the hand tracking runs entirely on your device.

> ⚠️ Webcam access requires a secure context (`localhost` or `https`). Opening `index.html` directly as a file will not work.

---

## 📁 Project Structure

```
gesture-arm/
├── index.html        # Main application (all-in-one)
├── netlify.toml      # Netlify deployment config
├── _redirects        # Netlify redirect rules
└── LICENSE           # MIT License
```

---

## 🌐 Deployment

This project is a static site and can be deployed anywhere. To deploy your own:

**Netlify (recommended):**
1. Fork the repository
2. Connect to [Netlify](https://netlify.com)
3. Deploy — no environment variables or build commands needed

**GitHub Pages:**
1. Go to **Settings → Pages**
2. Set source to the `main` branch
3. Done!

---

## 🔒 Privacy

All hand tracking is processed **entirely on your device** using MediaPipe's on-device models. No video, image, or gesture data is ever sent to a server.

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---

## 👤 Author

**Alphons Jaison**

- GitHub: [@alphonsjaison](https://github.com/alphonsjaison)

---

<p align="center">Made with ❤️ by Alphons Jaison</p>
ng gesture-arm-README.md…]()
