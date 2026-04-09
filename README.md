# 🛡️ Fake Product Identification Using Blockchain

A blockchain-based web application to detect fake products by tracking product ownership using smart contracts.

---

## 🚀 Features

* Add product (Manufacturer)
* Add seller
* Transfer product ownership
* Verify product authenticity using blockchain

---

## 🧰 Tech Stack

* Solidity (Smart Contracts)
* Truffle (Deployment Framework)
* Ganache (Local Blockchain)
* Node.js
* Lite-server (Frontend)

---

## ⚙️ Prerequisites

Make sure you have:

* Node.js (v16 recommended)
* npm
* Git
* Truffle
* Ganache CLI

---

# 🖥️ Setup & Run (Ubuntu / AWS EC2)

Follow **exact steps carefully** 👇

---

## 1️⃣ Update System

```bash
sudo apt update
 sudo apt install -y git curl build-essential  
```

---

## 2️⃣ Install Node.js (v16)

```bash
 curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -  
 sudo apt install -y nodejs  
```

Verify:

```bash
 node -v  
npm -v
```

---

## 3️⃣ Install Truffle & Ganache

```bash
sudo npm install -g truffle
 sudo npm install -g ganache  
```

---

## 4️⃣ Clone Repository

```bash
git clone https://github.com/kalyan0996/Fake-Product-Identification.git
cd Fake-Product-Identification
```

👉 **IMPORTANT:** Always run next commands inside this folder

---

## 5️⃣ Install Dependencies

```bash
npm install --legacy-peer-deps
npm install lite-server --save-dev
```

---

## 6️⃣ Start Blockchain (Terminal 1)

```bash
ganache --host 0.0.0.0 --port 7545
```

👉 Keep this terminal running

---

## 7️⃣ Deploy Smart Contracts (Terminal 2)

```bash
cd ~/Fake-Product-Identification

truffle compile
 truffle migrate --reset  
```

---

## 8️⃣ Run Frontend (Terminal 3)

```bash
cd ~/Fake-Product-Identification

npm run dev -- --host 0.0.0.0
```

---

## 9️⃣ Access Application

Get public IP:

```bash
curl ifconfig.me
```

Open in browser:

```
http://<PUBLIC-IP>:3000
```

Example:

```
http://3.108.55.16:3000
```

---

# ☁️ AWS EC2 Configuration (IMPORTANT)

Go to **Security Group → Inbound Rules**

Add:

| Type       | Port | Source    |
| ---------- | ---- | --------- |
| SSH        | 22   | Your IP   |
| Custom TCP | 3000 | 0.0.0.0/0 |
| Custom TCP | 7545 | 0.0.0.0/0 |

---

# 🧠 How It Works

* Ganache → Local blockchain network
* Truffle → Deploy smart contracts
* Smart Contract → Stores product ownership
* Frontend → Interacts with blockchain

---

# 🧪 Testing Flow

1. Add product (Manufacturer)
2. Add seller
3. Transfer ownership
4. Verify product authenticity
5. Check Ganache logs



---

# 👨‍💻 Author

**Kalyan**

---

# ⭐ Future Improvements

* Deploy to Ethereum Testnet (Sepolia)
* MetaMask Integration
* QR Code Verification
* Improved UI/UX
* Database Integration (MongoDB / IPFS)

---
