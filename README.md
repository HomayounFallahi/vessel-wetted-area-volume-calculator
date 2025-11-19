

***

# 📐 Vessel Wetted Area & Volume Calculator

A lightweight, browser-based tool for process engineers to calculate partial volumes and wetted surface areas of horizontal and vertical process vessels with various head configurations.

## 📋 Overview

This application provides accurate geometric calculations for process vessels, allowing engineers to determine liquid volume and wetted surface area based on liquid level. It supports multiple head types, vessel orientations, and unit systems.

**Developed by:** [Homayoun Fallahi](https://ir.linkedin.com/in/homayoun-fallahi)  

## ⚙️ Installation & Usage

### Single-File Application

1. Download `VesselCalculator.html` from the repository.
2. Open the file in any modern web browser (Chrome, Edge, Firefox, Safari).
3. No installation, internet connection, or server setup is required.

## 🖥️ App Interface

<div align="center">
  <img src="/interface/horizontal-view.png" alt="Horizontal Vessel Calculation" width="45%"/>
  <img src="/interface/vertical-view.png" alt="Vertical Vessel Calculation" width="45%"/>
</div>
<div align="center">
  <img src="/interface/results-breakdown.png" alt="Results Breakdown" width="45%"/>
  <img src="/interface/visualization.png" alt="Dynamic SVG Visualization" width="45%"/>
</div>

*(Note: Replace the image paths above with actual screenshots of your application)*

## ✨ Features

### ⚙️ Core Functionality
- **Dual Orientation**: Support for both Horizontal and Vertical vessel arrangements.
- **Comprehensive Head Support**: Calculates geometry for:
  - Hemispherical
  - Semi-Ellipsoidal (2:1)
  - Torispherical (ASME F&D)
  - Bumped
  - Flat
- **Standards Compliance**: Option to toggle between ASME and DIN standards for specific head geometries.

### 📊 Interactive Visualization
- **Dynamic SVG Rendering**: Real-time visual representation of the vessel and liquid level.
- **Liquid Level Indication**: Visual feedback changes as you adjust the liquid height input.
- **Cross-Sectional View**: Accurate aspect ratio representation of the cylinder and heads.

### 💻 User Interface
- **Unit Flexibility**: Instant switching between Meters (m), Millimeters (mm), and Inches (in).
- **Smart Inputs**: Automatic calculation of dependent variables (e.g., Dish Depth `z` auto-fills based on Diameter for standard heads).
- **Detailed Breakdown**: View separate metrics for the Cylinder body vs. the Heads.
- **Reactive Design**: Built with Tailwind CSS for a responsive, dark-mode interface suitable for desktop and tablet.

## 📖 How to Use

### Getting Started

1. **Launch the Tool**: Open the HTML file in your browser.
2. **Select Orientation**: Choose between Horizontal or Vertical via the toggle buttons.
3. **Choose Head Type**: Select the geometry of the vessel heads (e.g., Semi-Ellipsoidal).
4. **Select Units**: Click your preferred unit system (m, mm, or in).
5. **Input Dimensions**: Enter the required dimensions (Diameter, Length, Liquid Level).
   - *Note: Additional fields (like Knuckle Radius) appear dynamically based on head type.*
6. **Review Results**: Results update instantly in the "Calculation Results" panel.

### 🔑 Key Workflows

#### Analyzing Partial Volumes
- Enter the liquid height (`h` or `H1`) to get the exact volume of liquid and the surface area in contact with the fluid.
- Use the "View Breakdown" dropdown to separate the volume held in the cylindrical section from the volume held in the heads.

#### Validating Geometry
- Use the visualizer to ensure the input dimensions result in a realistic vessel shape.
- Warnings will appear if inputs are invalid (e.g., Liquid level higher than vessel diameter).

### 🔢 Input Parameters

| Parameter | Symbol | Description |
|-----------|--------|-------------|
| Inside Diameter | $D_i$ | Inner diameter of the vessel shell |
| Liquid Level | $h$ | Height of liquid from the bottom of the vessel |
| Length | $L$ | Tan-to-Tan length of the cylindrical section |
| Dish Depth | $z$ or $b$ | Depth of the dished head (internal) |
| Knuckle Radius | $R_k$ | Radius of the knuckle (for Torispherical heads) |

## Supported Geometries

The application supports calculations for the following configurations:

1. **Horizontal Cylinders** with:
   - Flat Ends
   - Dished Ends (Hemispherical, Ellipsoidal, Torispherical)
2. **Vertical Cylinders** with:
   - Flat Bottoms
   - Dished Bottoms (Hemispherical, Ellipsoidal, Torispherical)
3. **Head Standards**:
   - ASME (American Society of Mechanical Engineers)
   - DIN (Deutsches Institut für Normung)

## Calculations & Validation

The application calculates:

- **Wetted Area**: The total internal surface area in contact with the liquid.
- **Liquid Volume**: The volume occupied by the liquid at height $h$.
- **Geometric Ratios**: Correctly handles $L/D$ ratios and head depth ratios.

**Validation Source:**
The outputs of this tool have been cross-referenced and validated against **Aspen HYSYS** rigorous vessel models to ensure high accuracy for process engineering applications.

## 🤝 Acknowledgments

- **Neutrium**: Mathematical formulas and geometric derivations were sourced from [Neutrium.net](https://neutrium.net/).
- **AspenTech**: Validation of results performed using Aspen HYSYS.

---

**Note**: This tool is designed to assist process engineers in rapid calculations. While validated against industry software, it does not replace professional engineering judgment or detailed mechanical design analysis.
