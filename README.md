# Drone Project — Hackathon Submission  
**Use-case:** Medical Supply Delivery in Disaster-hit Areas  

## 🚑 Elevator Pitch
When disasters strike, roads are blocked and victims cannot access critical medicines. Our **autonomous drone platform** delivers **medical kits** directly to affected areas with **precision drop mechanism** and **real-time tracking**, ensuring **life-saving aid reaches faster** than ground relief.

## 🌍 Problem
- Earthquakes, floods, and cyclones destroy transport routes.  
- Relief teams often face **delays of hours to days** in delivering medicines.  
- Existing drones are expensive, hard to operate, and lack medical payload integration.  

## 💡 Our Solution
An **affordable drone system** with:  
- Payload box for **2–5 kg medical supplies**.  
- **Autonomous navigation** with GPS waypoints.  
- **Emergency drop-release mechanism** for safe kit delivery.  
- **Dashboard monitoring** for mission tracking & confirmation.  
- Works in **low network zones** (MAVLink telemetry + optional LTE/Satellite).  

## 📂 Repo Structure

## 🛠️ Hardware Components
- Drone frame (450–550 mm quadcopter)  
- Flight controller (Pixhawk / Matek F405) with PX4/ArduPilot firmware  
- Companion computer (Raspberry Pi 4 / Jetson Nano)  
- Payload box: lightweight (3D-printed / acrylic) with **servo-based lock-and-drop release**  
- GPS + Compass for autonomous navigation  
- Camera (for delivery confirmation photos + future AI victim detection)  
- Telemetry radio (MAVLink) + optional LTE/Satellite module for remote zones  
- 4S LiPo battery (3000–5000 mAh)  
- Future-ready add-ons:  
  - **Swarm communication module** (multi-drone missions)  
  - **Temperature-controlled payload box** (for vaccines/insulin)  
  - **Obstacle detection sensors** (LiDAR / stereo vision)  

## ⚙️ Software Components
- **Onboard (Companion Computer):**  
  - `navigator.py` — autonomous GPS waypoint navigation  
  - `payload_control.py` — servo release logic for secure medical delivery  
  - `detector.py` — camera capture + delivery confirmation snapshots  
  - `telemetry_bridge.py` — forwards MAVLink data to dashboard  
  - Future: AI models for **victim detection** & **drop-point optimization**  

- **Dashboard (Ground Station):**  
  - Web UI for live mission tracking (location, ETA, payload status)  
  - Mission logbook for relief authorities  
  - Alert & confirmation system with **delivery photo proof**  
  - Future: cloud-based control panel with **multi-drone coordination**  

## 🚀 Quick Demo Steps
1. Load mission coordinates into drone (QGroundControl or script).  
2. Attach medical box & arm drone.  
3. Launch with `demo/demo_script.sh`.  
4. Dashboard shows live location.  
5. Drone reaches target → releases box → snaps photo → sends confirmation.  

## ✅ Safety & Constraints
- Box secured with servo until GPS target reached.  
- Failsafe: auto-return or land if signal lost.  
- Indoor hackathon demo with **mini payload** for safety.  
- Tested in controlled environment — real field tests only under DGCA/CAA approval.  

## 📊 Evaluation Metrics (Hackathon)
- Delivery success rate (box dropped at target zone).  
- Time taken from launch to delivery.  
- Dashboard tracking accuracy.  
- Safety mechanisms demonstrated.  

