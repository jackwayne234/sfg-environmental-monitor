# SFG Environmental Monitor — Water and Air Quality Detection

Solid-state environmental monitoring platform using SFG (sum-frequency generation) in PPLN waveguides. Detects petroleum contamination in water, volatile organic compounds in air, and other pollutants — all from a single device with no moving parts.

Part of the **SFG Detection Platform** — same core hardware (PPLN chamber + pump laser + Si detectors), different tuning per application.

| Application | Repo |
|---|---|
| Telecom (fiber monitoring) | [sfg-fiber-monitor](https://github.com/jackwayne234/sfg-fiber-monitor) |
| Energy (gas leak detection) | [sfg-energy-monitor](https://github.com/jackwayne234/sfg-energy-monitor) |
| Environmental (this repo) | [sfg-environmental-monitor](https://github.com/jackwayne234/sfg-environmental-monitor) |
| Healthcare (breath analysis) | [sfg-health-diagnostics](https://github.com/jackwayne234/sfg-health-diagnostics) |
| Market Research | [sfg-market-research](https://github.com/jackwayne234/sfg-market-research) |
| Directional Detection | [directional-gas-detector](https://github.com/jackwayne234/directional-gas-detector) |

## Target Contaminants

### Water
| Contaminant | IR Absorption | Notes |
|-------------|--------------|-------|
| Petroleum/oil | 3.0-3.5 um (C-H stretch) | Spills, runoff, strongest signal |
| Nitrate (NO3-) | 7.3 um | Agricultural runoff |
| Phosphate | 8.2-9.5 um (P-O stretch) | Fertilizer runoff |

### Air
| Pollutant | IR Absorption | Notes |
|-----------|--------------|-------|
| SO2 | 7.4 um | Industrial emissions |
| NH3 | ~8 um | Agricultural, industrial |
| VOCs | 3.0-3.6 um (C-H stretch) | Industrial emissions, same band as petroleum |
| O3 | 9.5 um | Smog, air quality |

## Key Challenge: Water Absorbs Mid-IR

Water itself absorbs strongly at 2.7, 3.0, and 6.1 um. You can't just shine IR through a water sample.

**Solution: ATR (Attenuated Total Reflection).** The IR beam bounces inside a crystal (ZnSe or diamond) in contact with the water. The evanescent field penetrates only 0.5-2 um into the sample — short enough to avoid total absorption by water, long enough to detect dissolved contaminants. This is standard in FTIR water analysis. For the SFG device, the ATR crystal couples evanescent IR into the PPLN waveguide for upconversion.

## Documentation

- [Target Contaminants](docs/target-contaminants.md) — Detailed contaminant properties
- [ATR Design](docs/atr-design.md) — Attenuated Total Reflection approach for water samples
- [Testing Plan](docs/testing-plan.md) — Experimental validation path
- [Competition](docs/competition.md) — Comparison with existing water/air monitoring

## Market

- Water quality monitoring: $5.67B (2024), growing to $8.55B by 2030
- EPA monitors ~150 pollutants under Clean Water Act
- PFAS monitoring required by 2027, compliance by 2029

## Status

- [x] Target contaminant wavelengths mapped
- [x] ATR approach identified for water monitoring
- [x] Overlap with energy application identified (same PPLN crystals)
- [ ] Oil-in-water detection experiment
- [ ] VOC air quality experiment
- [ ] Nitrate detection feasibility study

## Author

Christopher Riner | Active Duty U.S. Navy
ORCID: [0009-0008-9448-9033](https://orcid.org/0009-0008-9448-9033) | GitHub: [jackwayne234](https://github.com/jackwayne234)
