# 🚗 Dynamic Pricing Engine for Urban Parking Lots

Capstone Project – Summer Analytics 2025  
Hosted by the Consulting & Analytics Club, IIT Guwahati

## 📌 Project Overview

This project implements a real-time dynamic pricing engine for 14 urban parking lots based on streaming data collected over 73 days. The goal is to maximize parking space utilization by adjusting prices dynamically in response to demand, congestion, queue length, and competition.

The system is built using only **Python, Pandas, NumPy, Pathway**, and **Bokeh** — with no external ML libraries — and follows a three-model framework of increasing complexity.

---

## 💡 Problem Statement

Urban parking spaces suffer from inefficiencies due to static pricing. This project simulates dynamic pricing to:
- Avoid overcrowding or underuse
- Adapt to real-time conditions like traffic or vehicle type
- Compete with nearby lots for better utilization

---

## 🧠 Models Implemented

### ✅ **Model 1: Baseline Linear Pricing**
- Price increases linearly with occupancy.
- Acts as a simple, reference pricing strategy.

### ✅ **Model 2: Demand-Based Pricing**
- Considers:
  - Occupancy rate
  - Queue length
  - Traffic congestion
  - Special events
  - Vehicle type
- Prices are scaled based on a normalized demand function.

### ✅ **Model 3: Competitive Pricing (Optional)**
- Adds location intelligence:
  - Computes proximity of nearby lots using latitude & longitude.
  - Adjusts price based on competition (e.g., if neighbors are cheaper or full).
- Simulates rerouting suggestions and market-driven behavior.

---

## 🔁 Real-Time Simulation with Pathway

- Data ingested as time-ordered streams.
- Pathway processes each event as it arrives to simulate real-time updates.
- Pricing logic is applied per time step.

---

## 📊 Visualization with Bokeh

Interactive visualizations for:
- Real-time pricing trends for each parking lot
- Comparison of pricing behavior across models
- Transparency in price fluctuation for decision-makers

---

## 📁 Project Structure

```plaintext
├── dataset.csv                  # Input dataset (73 days × 14 lots × 18 time points/day)
├── Dynamic_Pricing_Project.ipynb  # Colab-compatible notebook with all 3 models
├── README.md                    # Project documentation
