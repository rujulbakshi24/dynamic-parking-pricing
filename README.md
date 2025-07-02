# dynamic-parking-pricing
This project implements a **Dynamic Parking Pricing System** using real-time occupancy and demand data. It includes two main components:

1. **Model 1: Demand-based Pricing with Bokeh Visualization**
2. **Model 2: Real-time Streaming Simulation using Pathway**

---

## 🔧 Tech Stack Used

| Tool / Library    | Purpose                                      |
|-------------------|----------------------------------------------|
| Python            | Core programming language                    |
| Pandas            | Data manipulation and processing             |
| Bokeh             | Interactive visualizations                   |
| Pathway           | Real-time data streaming and transformation |
| Google Colab      | Notebook environment                         |

---
## 🧠 Project Overview

### 🔹 Model 1: Bokeh-Based Visualization (Baseline Pricing)

- Computes `OccupancyRate = Occupancy / Capacity`
- Calculates `DemandScore` based on:
  - Queue Length
  - Traffic Condition Nearby
  - Vehicle Type
  - Special Day (binary)
- Normalizes demand to a range of `[0, 1]`
- Updates price using:
- Compares prices across locations using **Bokeh**

### 🔹 Model 2: Real-Time Streaming with Pathway

- Reads parking data from a CSV stream (`stream_input.csv`)
- Simulates live feed using **Pathway**
- Extracts:
- `SystemCodeNumber`
- `Timestamp`
- `Occupancy`, `Capacity`, `QueueLength`, etc.
- Outputs the stream results to `stream_output.json`

---

## 🏗️ Architecture Flow

```text
CSV (Input) --> Pathway Schema --> Stream Transformation --> JSON Output
                            ↓
                    Bokeh-Based Visualization
