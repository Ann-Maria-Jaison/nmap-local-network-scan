
# 📡 Local Network Port Scan

## 📌 Objective
Perform a basic network reconnaissance scan using Nmap to identify active devices and their open ports on the local network.

---

## 🧰 Tools Used

- **Nmap v7.95**
- **OS**: Kali Linux

### 🔧 Command Used:
```bash
sudo nmap -sS -Pn -T4 --top-ports 100 192.168.1.0/24 -oN fast_scan.txt
````

---

## 🌐 IP Range Scanned

* **Target Subnet**: `192.168.1.0/24`
* **Determined using `ifconfig`**
  → Active interface: `wlan0`, IP: `192.168.1.250`

---

## 🖥️ Active Hosts Detected

> More than 60 devices were detected as "up" in the scanned subnet.

**Some sample active IPs:**

* `192.168.1.1`
* `192.168.1.10`
* `192.168.1.21`
* `192.168.1.37`
* `192.168.1.59`
* ... (and many more)

---

## 🚫 Port Scan Results

For **all live hosts**, Nmap reported:

```
100 filtered tcp ports (no-response)
```

---

## 🔐 Interpretation

The hosts are alive but:

* Are using **firewalls** to block port scanning
* Do not offer TCP services on the **top 100 ports**
* May be using **UDP services**, which were not scanned in this run

---

## 📁 Repository Contents

* `fast_scan.txt` – Raw Nmap output
* `README.md` – This file explaining the task, method, and findings
