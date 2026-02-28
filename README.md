# Real-Time Network Traffic Dashboard

An interactive Streamlit-based dashboard for monitoring and visualizing live network traffic using Scapy.

## 🚀 Features

* Real-time packet capture
* Protocol distribution visualization
* Packets-per-second timeline
* Top source IP analysis
* Thread-safe packet processing
* Memory management (rolling 10,000 packet buffer)

---

## 🛠️ Tech Stack

* Python
* Streamlit
* Pandas
* Plotly
* Scapy

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install dependencies

```bash
pip install streamlit pandas plotly scapy
```

### 3. Install Npcap (Windows only)

Scapy requires Npcap for packet sniffing:

https://nmap.org/npcap/

Install with default settings.

---

## ▶️ Running the Dashboard

Streamlit apps must be launched using the Streamlit CLI:

```bash
streamlit run dashboard.py
```

After running, Streamlit will display:

```
Local URL: http://localhost:8501
```

Open that URL in your browser.

---

## ⚠️ Important Notes

* On Windows, you may need to run the terminal as Administrator to allow packet capture.
* If no packets appear, verify that Npcap is installed.
* The dashboard auto-refreshes every 2 seconds.

---

## 📊 Dashboard Visualizations

* Protocol Distribution (Pie Chart)
* Packets Per Second (Time Series)
* Top Source IP Addresses (Bar Chart)
* Recent Packets Table

---

## 🧠 Architecture Overview

* Packet capture runs in a background daemon thread.
* A thread-safe `PacketProcessor` class stores structured packet metadata.
* Data is converted to a Pandas DataFrame for visualization.
* Streamlit handles reactive UI rendering.

---

## 📌 Future Improvements

* Geolocation IP mapping
* Filtering by protocol or IP
* Port-based filtering
* Persistent storage (SQLite or CSV export)
* Async capture optimization

---

## 📜 License

MIT License

---

## 👨‍💻 Author

Krzysztof Smykla

---

## ⭐ Contributing

Pull requests are welcome. For major changes, open an issue first to discuss improvements.
