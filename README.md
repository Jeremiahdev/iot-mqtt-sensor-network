# iot-mqtt-sensor-network

An end-to-end IoT telemetry system where ESP32 devices publish sensor data to a Mosquitto MQTT broker running on a Raspberry Pi. Incoming data is ingested into a SQLite database and visualized through a web-based dashboard. The system is deployed on a segmented IoT network for improved security and isolation.

---

## Overview

This project demonstrates a complete IoT data pipeline, combining embedded systems, networking, and backend development. ESP32 sensor nodes publish environmental data using MQTT. A Raspberry Pi hosts the MQTT broker, a subscriber service for data ingestion, and local storage. A frontend dashboard is used to visualize real-time and historical sensor data.

The system is designed to be scalable, secure, and representative of real-world IoT deployments.

---

## System Architecture

## Key Features

- ESP32-based sensor nodes publishing telemetry via MQTT  
- Mosquitto MQTT broker hosted on Raspberry Pi  
- Backend subscriber service to process and store data  
- SQLite database for local time-series data storage  
- Web-based dashboard for data visualization  
- Segmented IoT network using a dedicated router for device isolation  

---

## MQTT Topic Structure

Example topic hierarchy:

temp-project/
├── sensor1/
│ ├── temperature
│ └── humidity

## Repository Structure

iot-mqtt-sensor-network
├─ esp32/ # ESP32 firmware (ESP-IDF / Arduino)
├─ broker/ # Mosquitto configuration
├─ ingest/ # MQTT subscriber → SQLite
├─ database/ # Database schema and queries
├─ dashboard/ # Frontend dashboard (Next.js)
├─ docs/ # Diagrams and screenshots
└─ README.md


---

## Technologies Used

- **Embedded:** ESP32, Arduino / ESP-IDF  
- **Networking:** MQTT, Mosquitto, Wi-Fi, LoRa (for drone communication)  
- **Backend:** Python / Node.js (MQTT subscriber)  
- **Database:** SQLite  
- **Frontend:** Next.js  
- **Infrastructure:** Raspberry Pi, segmented IoT network  

---

## Security & Networking

- IoT devices are isolated behind a dedicated downstream router  
- MQTT broker and database are not exposed to the public internet  
- Controlled access is allowed only for required services (MQTT, SSH, HTTP)  
- Architecture reflects real-world IoT network segmentation practices  

---

## Setup (High-Level)

1. Flash ESP32 firmware and configure MQTT topic publishing  
2. Run Mosquitto broker on Raspberry Pi  
3. Start MQTT subscriber service to ingest data into SQLite  
4. Launch dashboard locally or deploy frontend for public viewing  

> Detailed setup steps are provided in each subdirectory README.

---

## Future Improvements

- Add additional sensor nodes (security, motion, door sensors)  
- Cloud database sync for public dashboard access  
- Authentication and role-based access for dashboard  
- Alerting and analytics based on sensor thresholds  

---

## Why This Project Matters

This project demonstrates:
- Embedded firmware development  
- IoT communication patterns  
- Secure network design  
- Backend data ingestion  
- Full-stack system integration  

It mirrors how production IoT systems are designed and deployed.

---

## Author

Jeremiah Austin Hughes  
Computer Engineering | Embedded Systems | IoT | Networking

