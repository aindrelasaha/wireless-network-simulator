# Wireless Network Simulator

This project demonstrates a **Wireless Network Simulation Framework** for **Wireless Sensor Networks (WSN)**, **Body Area Networks (BAN)**, and networks of low-power embedded devices.  
It is built on the **OMNeT++ platform** with **Castalia**, providing a realistic environment to test **distributed algorithms, wireless protocols, and radio models**.

---

## ✨ Features
- **Channel Modeling**
  - Realistic path loss maps and temporal variation of channel conditions  
  - Full support for **node mobility** and interference modeling  
- **Radio Modeling**
  - SINR-based packet reception with PSK/FSK and custom modulation support  
  - Multiple TX power levels and power-state switching with delay modeling  
- **Sensing & Energy**
  - Device noise, bias, and CPU power consumption  
  - Node clock drift modeling for realistic timing  
- **Protocols**
  - MAC and routing protocol support for performance evaluation  

---

## 🚀 What This Project Does
- Simulates **50+ wireless nodes** under varying interference, mobility, and power constraints.  
- Implements and evaluates **3+ MAC/routing protocols**, measuring throughput, latency, and packet delivery ratio.  
- Automates **100+ simulation runs** in Python for reproducibility and parameter tuning.  

---

## 🔧 Tech Stack
- **Languages:** C, C++, Python  
- **Frameworks/Tools:** OMNeT++, Castalia, Wireshark (for trace analysis)  

---

## 📌 Note
This simulator is intended for **algorithm and protocol validation** in wireless networking research.  
It is **not platform-specific** and does not emulate code compiled for sensor hardware.  

---
