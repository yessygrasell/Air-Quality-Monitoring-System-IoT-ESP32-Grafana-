# 🌱 Air Quality Monitoring System (IoT | ESP32 | Grafana)

Proyek ini adalah implementasi Internet of Things (IoT) untuk memantau kualitas udara dalam rumah secara real-time.  
Sistem menggunakan **ESP32**, sensor **ZH03B (PM2.5 & PM10)**, dan **DHT11 (suhu & kelembaban)**, dengan integrasi **MQTT – Node-RED – InfluxDB – Grafana** untuk penyimpanan dan visualisasi data.

---

## 🚀 Fitur Utama
- 🔹 Monitoring real-time suhu, kelembaban, PM2.5, dan PM10  
- 🔹 Dashboard interaktif dengan Grafana  
- 🔹 Penyimpanan data historis di InfluxDB  
- 🔹 Integrasi IoT penuh dengan ESP32 & MQTT  
- 🔹 Flow Node-RED yang mengatur alur data sensor → database → visualisasi  
- 🔹 Visualisasi status kualitas udara berdasarkan standar AQI  

---

## ⚡ Teknologi yang Digunakan
- **Hardware**: ESP32, ZH03B (PM2.5 & PM10), DHT11  
- **Software**: Arduino IDE, Node-RED, MQTT Broker, InfluxDB, Grafana  

---

## ⚙️ Quick Start

### 1️⃣ Setup ESP32
1. Clone repo ini  
2. Buka `src/air_quality.ino` di Arduino IDE  
3. Install library:  
   - `DHT.h`  
   - `PubSubClient`  
   - `ArduinoJson`  
4. Edit SSID, password WiFi, dan alamat MQTT broker sesuai kebutuhan  
5. Upload ke board ESP32  

### 2️⃣ Setup MQTT Broker
- Install **Mosquitto MQTT** atau gunakan broker publik (contoh: `broker.hivemq.com`)  

### 3️⃣ Setup Node-RED
- Import flow dari `flows/flow.json`  
- Pastikan Node-RED sudah bisa publish ke InfluxDB  

### 4️⃣ Setup InfluxDB + Grafana
- Jalankan **InfluxDB** & buat bucket `ESP32DATA`  
- Tambahkan data source InfluxDB di Grafana  
- Buat dashboard dengan panel: suhu, kelembaban, PM2.5, PM10, & AQI  


---

## 📸 Dokumentasi Proyek

### 🔌 Diagram Wiring  
<img MONITORING KUALITAS UDARA="docs/wiring.png" alt="Wiring Diagram" width="500"/>  

### 🖥️ Flow Node-RED  
<img src="docs/nodered_flow.png" alt="Node-RED Flow" width="500"/>  

### 📊 Visualisasi InfluxDB  
<img src="docs/visualisasi_influxdb.png" alt="InfluxDB Visualization" width="500"/>  

### 📈 Dashboard Grafana  
<img src="docs/dashboard.png" alt="Grafana Dashboard" width="500"/>  

### 📦 Prototipe Alat  
<img src="docs/prototipe.png" alt="Prototype Device" width="500"/>  

---

## 📈 Hasil & Analisis
✅ Sistem berhasil memantau parameter udara secara akurat & stabil  
✅ Data historis membantu analisis tren polusi udara dalam rumah  
✅ Visualisasi Grafana memudahkan pemahaman kondisi udara  
✅ Kualitas udara dikategorikan berdasarkan nilai PM2.5 & AQI Index  


✅ Sistem berhasil memantau parameter udara secara akurat & stabil

✅ Data historis membantu analisis tren polusi udara dalam rumah

✅ Visualisasi Grafana memudahkan pemahaman kondisi udara

✅ Kualitas udara dikategorikan berdasarkan nilai PM2.5 & AQI Index
