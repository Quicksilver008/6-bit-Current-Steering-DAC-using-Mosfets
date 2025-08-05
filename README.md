# 6-bit Fully Differential Current-Steering DAC

This repository contains the design and simulation of a **6-bit fully differential current-steering Digital-to-Analog Converter (DAC)** using **LTSpice**. The design targets low static and dynamic non-linearities for use in mixed-signal applications.

---

## 🔧 Objective

Design and simulate a 6-bit fully differential current-steering DAC suitable for integration in mixed-signal systems using 180nm CMOS technology models.

---

## ⚙️ Key Components

- **PMOS Current Sources**  
- **Row and Column Decoder Logic**
- **Differential Output Stage**
- **180nm CMOS Technology Transistor Models**

---

## 📐 Methodology

- Designed schematic in **LTSpice** with attention to layout-aware practices (matching, symmetry, etc.)
- Performed **DC and transient simulations** to evaluate:
  - Integral Non-Linearity (INL)
  - Differential Non-Linearity (DNL)
  - Glitch Energy
  - Settling Time
  - Output skew
- **Optimized transistor sizing** to enhance current matching and reduce systematic offsets

---

## 🛠️ Tools Used

- **LTSpice** (for circuit design and simulation)
- **180nm CMOS Models** (compatible model cards used for transistor-level accuracy)

---

## 📊 Results Summary

| Metric                     | Result             |
|---------------------------|--------------------|
| INL (Integral Nonlinearity) | < 0.5 LSB         |
| DNL (Differential Nonlinearity) | < 0.5 LSB     |
| Power Consumption         | < 1 mW (nominal)   |
| Glitch Energy             | Analyzed via transient response |
| Output Skew               | Minimized via symmetric layout and matching |

---

## 📁 Repository Structure

```bash
├── schematics/
│   └── dac_6bit_diff.asc          # LTSpice schematic
├── models/
│   └── cmos180nm.lib              # Technology model
├── simulations/
│   ├── transient_results.raw
│   ├── dc_analysis.raw
├── plots/
│   ├── inl_dnl_plot.png
│   └── transient_response.png
└── README.md
