 Anti-Collision-Radar-for-UAVs
Project done in collaboration with Micron Avionics on their new light weight and cheap radar design that will be mounted on UAVs.
 Anti-Collision Radar for UAVs: Capacitive Hat Monopole Antenna Array

 Project Overview
This project focuses on the design, simulation, and experimental validation of a quad monopole antenna array integrated into a PCB for UAV (Unmanned Aerial Vehicle) anti-collision radar applications. The design employs capacitive hat monopole antennas to reduce physical antenna height while maintaining electrical performance at 1060MHz. The array consists of one active feed antenna and three passive parasitic elements to enhance directivity and front-to-back ratio.

  Objectives
- Design a compact monopole antenna array operating at 1060MHz for UAV applications
- Reduce antenna height using capacitive hats while maintaining quarter-wavelength electrical performance
- Improve directivity and front-to-back ratio using parasitic elements
- Validate design through simulation (NECWinPro) and physical measurement (VNA)

  Technical Specifications
| Parameter | Value |
|-----------|-------|
| Operating Frequency | 1060 MHz (design), 889 MHz (achieved) |
| Wavelength (λ) | 0.282 m |
| Quarter Wavelength | 0.070 m |
| Antenna Height | λ/8 = 0.035 m |
| PCB Type | Double-sided with ground planes |
| Feed Impedance | 50 Ω |
| Antenna Configuration | 1 active + 3 parasitic monopoles |
| Capacitive Hat Type | Wire and rectangular patch variants |

  Antenna Design

 Key Formulas
- Wavelength: \( \lambda = \frac{c}{f} = 0.282\text{m} \)
- Quarter Wavelength: \( \frac{\lambda}{4} = 0.070\text{m} \)
- Monopole Height: \( M = \frac{\lambda}{8} = 0.035\text{m} \)
- Reflection Coefficient: \( \Gamma = \frac{Z_L - Z_0}{Z_L + Z_0} \)
- Return Loss: \( Gain = -20 \log|\Gamma| \)

 Design Features
1. Capacitive Hats: Extend electrical length without increasing physical height
2. Quad Array Configuration: One driven element + three parasitic elements
3. Symmetrical PCB Layout: All antennas equidistant from PCB edges
4. Ground Planes: Both top and bottom layers for improved radiation efficiency

  Experimental Setup

 Hardware Components
- PCB: Custom-designed square board with specific hole sizes
  - Feed antenna hole: 2.35mm diameter
  - Parasitic antenna holes: 2.45mm diameter
- Antenna Types:
  1. Wire capacitive hat monopoles
  2. Rectangular copper patch capacitive hat monopoles
- Measurement Equipment:
  - Voltage Network Analyzer (VNA)
  - Dream Catcher software
  - NECWinPro for simulation

 PCB Layout
```
┌─────────────────┐
│  ●       ●      │
│                 │
│                 │
│  ●       ●      │
└─────────────────┘
● = Antenna positions (equidistant spacing)
```

  Results

 Simulation Results (NECWinPro)
- VSWR: 2.68 dB at 1060MHz
- Front-to-Back Ratio: 8 dB (simulated)
- Directivity: Principal beam oriented toward feed antenna

 Experimental Results
| Measurement | Value |
|-------------|-------|
| Resonance Frequency | 889 MHz |
| S11 at Resonance | -3.89 dB |
| Front-to-Back Ratio | 6 dB (experimental) |
| Beamwidth | 180° |
| Gain | ~12 dB (with minor calibration ripples) |

 Radiation Patterns
- Directivity: Enhanced in feed antenna direction
- Beamwidth: 180° half-power beamwidth
- Pattern: Directional with reduced backward radiation

  Performance Comparison

 Achieved vs. Target
| Parameter | Target | Achieved |
|-----------|--------|----------|
| Frequency | 1060 MHz | 889 MHz |
| F/B Ratio | 12 dB | 6 dB |
| VSWR | <2.0 dB | 2.68 dB |
| Beamwidth | N/A | 180° |

 Key Findings
1. Height Reduction: Capacitive hats successfully reduced physical antenna height while maintaining performance
2. Frequency Shift: Experimental resonance at 889MHz vs. design target of 1060MHz
3. Directivity Improvement: Parasitic elements enhanced front-to-back ratio to 6dB
4. Consistency: Both wire and patch capacitive hats resonated at same frequency
5. Beam Steering: Principal beam successfully directed toward feed antenna

  Design Considerations

 Simplifications Made
- Dielectric effects omitted
- Infinite ground plane assumption
- Conduction losses ignored
- Environmental conditions not considered

 Optimization Opportunities
1. Capacitive Hat Dimensions: Tuning for exact frequency matching
2. Antenna Spacing: Optimizing for improved F/B ratio
3. PCB Material: Considering dielectric properties
4. Ground Plane Size: Impact on radiation pattern

  Project Structure
```
anti-collision-radar-uav/
├── README.md
├── docs/
│   ├── technical_report.pdf
│   ├── pcb_specifications.pdf
│   └── measurement_protocol.pdf
├── simulations/
│   ├── necwinpro_files/
│   ├── radiation_patterns/
│   └── impedance_analysis/
├── hardware/
│   ├── pcb_design/
│   ├── bom.md
│   └── assembly_instructions.md
├── measurements/
│   ├── vna_data/
│   ├── radiation_patterns/
│   └── calibration_data/
└── images/
    ├── pcb_layout.png
    ├── antenna_models.jpg
    └── measurement_setup.jpg
```
  Applications
- UAV Anti-Collision Systems: Compact directional antennas for radar
- Aerial Communication: Directional links for UAV swarms
- RF Sensing: Directional signal detection and monitoring
- Compact Radar Systems: Where antenna height is constrained

  References
1. Balanis, C. A. (2005). Antenna Theory: Analysis and Design
2. Pozar, D. M. (2011). Microwave Engineering
3. Thiel, D. V., & Smith, S. (2002). Switched Parasitic Antennas for Cellular Communication
4. Johnson, R. C., & Jasik, H. (1984). Antenna Engineering Handbook

 👥 Contributors
- Waleed Umer (5336317) - Design, simulation, and experimental validation
- Francis Mensah - Project partner
- David Thiel - Technical supervision
- Will Sutton - PCB design and fabrication

 📄 License
This project is part of academic research. Please cite appropriately if used for reference.

 🔮 Future Work
1. Frequency Tuning: Adjust capacitive hat dimensions for 1060MHz resonance
2. F/B Ratio Improvement: Optimize spacing and parasitic element tuning
3. Multi-band Design: Expand frequency range for broader applications
4. Integration Testing: Test with actual UAV radar systems
5. Environmental Testing: Evaluate performance under real-world conditions

---

This project demonstrates the successful application of capacitive hat monopole technology to create compact, directional antenna arrays suitable for UAV anti-collision radar systems. While some performance targets were not fully met, the design shows promising results and provides a foundation for further optimization.
