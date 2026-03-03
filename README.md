# GestureArm
Real-time gesture-controlled robotic arm simulation using on-device AI hand tracking.

## How it works
- MediaPipe Hands detects 21 hand landmarks in real time via webcam
- Hand position and finger angles are mapped to robot joint angles
- 3D arm rendered with Three.js responds instantly to gestures

## Gestures
| Gesture | Action |
|---|---|
| Move hand left/right | Base rotation |
| Move hand up/down | Elbow angle |
| Open hand | Gripper open |
| Close fist | Gripper closed |

## Built with
- MediaPipe Hands (on-device ML)
- Three.js (3D rendering)
- Vanilla JS / HTML
