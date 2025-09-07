````markdown
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

## 🛠️ Installation

⚠️ Castalia 3.3 supports **OMNeT++ versions 4.3–4.6** only (not 5.x+).  
Recommended OS: **Ubuntu 16.04/18.04** or **macOS**.

### 1️⃣ Install Dependencies
```bash
# Ubuntu
sudo apt-get update
sudo apt-get install build-essential
````

On macOS, install **XCode command-line tools**.

### 2️⃣ Install OMNeT++ 4.6

```bash
# Download OMNeT++ 4.6
wget https://github.com/omnetpp/omnetpp/releases/download/omnetpp-4.6/omnetpp-4.6-src.tgz

# Extract
tar xvfz omnetpp-4.6-src.tgz
cd omnetpp-4.6/

# Set environment variables
export PATH=$PATH:~/omnetpp-4.6/bin
export LD_LIBRARY_PATH=~/omnetpp-4.6/lib
echo "export PATH=\$PATH:~/omnetpp-4.6/bin" >> ~/.bashrc
echo "export LD_LIBRARY_PATH=~/omnetpp-4.6/lib" >> ~/.bashrc
source ~/.bashrc

# Build OMNeT++ (without Tcl)
NO_TCL=1 ./configure
make
```

Verify:

```bash
which opp_makemake
# should print ~/omnetpp-4.6/bin/opp_makemake
```

### 3️⃣ Install Castalia

```bash
# Clone this repo
git clone https://github.com/your-username/wireless-network-simulator.git
cd wireless-network-simulator/Castalia

# Build Castalia
./makemake
make
```

A soft link named **CastaliaBin** will be created in the project directory.

### 4️⃣ Add Custom Code (Optional)

* Place new modules in `src/node/communication/mac/yourModuleName/`.
* Follow OMNeT++ naming conventions (lowercase dirs).
* For external libraries, update `makemake` with:

  * `-I` → include path
  * `-L` → library path
  * `-l` → library name

Rebuild:

```bash
make clean
./makemake
make
```

---

## ▶️ Running Simulations

Run sample simulations:

```bash
cd Castalia/Simulations
./run <simulation-file.ini>
```

---

## 📌 Note

This simulator is intended for **algorithm and protocol validation** in wireless networking research.
It is **not platform-specific** and does not emulate code compiled for sensor hardware.

---
