# Vayu–Surya Charging Plaza · Digital Twin v1.0

An interactive, real-time microgrid simulation dashboard for a hybrid wind-solar EV charging plaza along the NH-48 highway.

## Overview

The **Vayu–Surya Charging Plaza Digital Twin** models the operational dynamics, physics, and financial performance of a modern renewable-powered EV charging station. It provides real-time visualization of energy generation, battery storage management, EV demand queuing, and grid interaction under variable environmental and economic conditions.

## Features

- **Interactive Plant View & Single-Line Diagram**: Dynamic SVG visualization featuring animated wind turbine rotation, celestial movement (sun/moon), weather overlays, live busbar flows, and parking bay status.
- **Microgrid Asset Simulation**:
  - **Wind Generation**: Switchable Suzlon turbine models (S52, S66, S97) with cubic power-curve approximations and 1/7-power-law shear corrections.
  - **Solar PV Arrays**: Canopy and rooftop arrays using clear-sky sine irradiance modeling with temperature coefficient adjustments.
  - **Battery Storage (BESS)**: 600 kWh / 300 kW battery system supporting off-peak grid charging, peak shaving, and islanded operations.
  - **Grid Connection**: 11 kV MSEDCL grid tie with configurable import/export limits, time-of-use (ToU) tariffs, and automatic AC bay throttling during peak tariff hours.
- **EV Queue & Charger Management**: Models 4× 60 kW DC Fast Chargers and 6× 22 kW AC Chargers across a variety of realistic EV models with dynamic battery state-of-charge (SoC) curves, arrival rates, and wait-time patience thresholds.
- **Real-Time Analytics & Financials**:
  - Live 24-hour power balance canvas chart tracking generation, load, and battery SoC.
  - Dynamic KPI panels measuring renewable share, energy delivered, gross revenue, grid energy costs, export credits, and estimated CO₂ avoided.
  - Interactive controls for weather presets (Clear & Breezy, Monsoon, Still Night, Gale/Cut-out), time acceleration (10× to 900×), manual wind/cloud overrides, and custom DC/AC tariffs.
  - Integrated real-time event log.

## Tech Stack

- **HTML5 & CSS3**: Custom dark-mode interface styled with custom CSS properties, responsive grids, and Google Fonts (`Barlow Condensed`, `IBM Plex Mono`, `Inter`).
- **SVG & Canvas API**: Animated vector visuals for plant components and low-latency dynamic charting for power balance metrics.
- **Vanilla JavaScript (ES6+)**: Fully self-contained physics, math engine, queue simulation, and UI state management without external framework dependencies.

## Usage

1. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
2. Use the top control bar to pause, reset, or adjust simulation speed (up to 900× real-time).
3. Tweak environmental factors (wind speed, cloud cover, EV arrival rate) or choose a scenario preset from the right panel.
4. Toggle operational rules like grid import/export, off-peak BESS charging, or peak-tariff AC throttling to observe financial and operational impacts on the microgrid.

---
*Disclaimer: Simulation only. Physics, tariffs, vehicle data, and turbine specifications are representative models meant for demonstration purposes.*
