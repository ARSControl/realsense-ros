# 🎥 RealSense ROS for Jetson Nano (Ubuntu 20.04)

This repository is a **working fork** of the official [Intel RealSense ROS](https://github.com/IntelRealSense/realsense-ros) repo, pinned to the **correct branch (tag `2.2.18`)** for compatibility with our setup.

It goes beyond a plain fork by including everything you need to get **Intel RealSense cameras running smoothly on a Jetson Nano with Ubuntu 20.04**:

✅ Correct ROS wrapper (`2.2.18`)  
✅ Matching `librealsense` version (`2.39.0`) **with CUDA support**  
✅ Prepackaged firmware — the right one to flash onto your camera  
✅ Handy bash script to **download, build, and install** the right stack in one go  

---

## 🚀 Features

- 🧩 **Out-of-the-box compatibility** for Jetson Nano + Ubuntu 20.04  
- ⚡ **CUDA acceleration** enabled in `librealsense` for better performance  
- 🛠️ **One-step installation script** to save you from dependency headaches  
- 📦 Includes the **camera firmware** that matches this setup  

---

## 📂 Contents

- `realsense-ros/` → ROS wrapper (tag `2.2.18`)  
- `scripts/install_librealsense.sh` → Bash script to build and install `librealsense 2.39.0` with CUDA  
- `firmware/` → Correct camera firmware for flashing  

---

## 🛠️ Installation

Clone this repo:
```bash
git clone https://github.com/ARSControl/realsense-ros.git
cd realsense-ros
```

Run the install script for `librealsense`:
```bash
bash scripts/install_librealsense.sh
```

Flash the firmware (if needed) from the `firmware/` folder, then build the ROS package:
```bash
catkin_make
source devel/setup.bash
```

---

## 📌 Notes

- Tested on **Jetson Nano (4GB) + Ubuntu 20.04**  
- NVIDIA JetPack **4.6** (L4T **32.6.1**)  
- ROS Noetic recommended  
- Make sure your Jetson has CUDA properly installed before running the script  

---

## 🤝 Acknowledgments

- Original work from [Intel RealSense ROS](https://github.com/IntelRealSense/realsense-ros)  
- Thanks to the open-source community for Jetson + RealSense integration tips  

---

## 🐧 TL;DR

👉 If you’re on a **Jetson Nano + Ubuntu 20.04** and just want RealSense to work — **this is the repo you need.**
