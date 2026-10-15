# Seat Availability and Allocation Tracker

MDP (2026), VIT Chennai. A smart library seat system that shows which seats are vacant, lets students reserve a seat, and confirms the booking with an RFID tap plus a weight sensor.

## Team
- Sanjay (26BCE1065)
- Subhanithi T (26BCE1067)
- Harsh Ramkrishna Bhadani (26BCE5273)
- Ayushi Sanjeev Prasad Jaiswal (26BEL1093)
- Nithilarin Prabakaran (26BME1248)

Guide: Dr. Raja M, SCOPE

## How it works
Load cell + HX711 -> ESP32 (+ RC522 RFID) -> MQTT -> Node.js server + database -> web dashboard

- Seat is **Occupied** when the load cell reads 15 kg or more
- A reserved seat is confirmed only when the RFID tap and the weight agree
- If not confirmed within 15 minutes, the booking is released automatically
- The first student to select a seat gets it

## This repository
`index.html` is the web frontend prototype (student portal and staff console). It runs with demo data and needs no installation: open it in a browser.

- Student login: any name and registration number
- Staff sign in: demo passcode `admin123`
- Seat states: green = vacant, yellow = reserved, red = occupied

## Planned
- ESP32 firmware (HX711 + RC522)
- Node.js + MQTT backend with Firebase Realtime Database
- Connect the website to live sensor data

## Status
Review 2 (20% milestone): frontend prototype complete.
