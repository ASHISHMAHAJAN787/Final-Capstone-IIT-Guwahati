# Final-Capstone-IIT-Guwahati

# Dynamic Parking Pricing System

A real-time dynamic pricing engine for parking lots using occupancy, demand signals, and competitive analysis.

## 🔑 Key Features

### � Pricing Models
- **Model 1**: Baseline Linear Model (Simple occupancy-based pricing)
- **Model 2**: Demand-Based Function (Occupancy + queue length + traffic + special events + vehicle type)
- **Model 3**: Competitive Pricing (Geographic proximity + competitor analysis)

### ⚡ Real-time Processing
- Powered by Pathway for stream processing
- Continuous data ingestion from `dataset.csv`
- Dynamic time-windowing and price updates

### 📊 Visualization Dashboard
- Real-time price trend graphs
- Occupancy rate heatmaps
- Interactive Bokeh plots with hover tooltips
- Demand indicators visualization

### 🧠 Smart Pricing Logic
- Base price of $10 with 0.5x-2x dynamic range
- Multi-factor consideration:
  - Occupancy rates
  - Queue lengths 
  - Traffic conditions
  - Special events
  - Vehicle type weights
- Competitive geographic analysis

## 📈 Mathematical Models

### Model 2: Demand Function
Demand = α×(Occupancy/Capacity) + β×QueueLength - γ×Traffic + δ×IsSpecialDay + ε×VehicleTypeWeight
Price = BasePrice × (1 + λ × NormalizedDemand)


### Model 3: Competitive Logic
- Haversine distance calculations
- Competitor price adjustments
- Smart rerouting suggestions

## 🚀 Usage

```bash
1. Place your dataset.csv in the project directory
2. Run in Google Colab (automatic dependency installation)
3. Access the real-time Panel dashboard
4. Monitor dynamic price adjustments

✨ Key Improvements
Robust Data Pipeline: Automatic missing column handling

Multi-Strategy Approach: 3 progressive pricing models

Interactive Visuals: Real-time Bokeh dashboards

Location Intelligence: Competitor distance calculations

Production-Ready: Error handling + data validation
