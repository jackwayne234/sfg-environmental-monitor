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
| Pollutant | IR Absorption | SFG Output | PPLN Compatible? | Notes |
|-----------|--------------|------------|-----------------|-------|
| VOCs | 3.0-3.6 um (C-H stretch) | ~805-810 nm | Yes | Same band as petroleum |
| **NH3** | **3.00 um (v3 N-H stretch)** | **785 nm** | **Yes** | QPM period ~21.1 um |
| SO2 | 7.35 um (v3 asymmetric stretch) | 930 nm | No (need alt crystal) | Industrial emissions |
| NO2 | 6.17 um (v3 asymmetric stretch) | 908 nm | No (need alt crystal) | Industrial emissions |
| O3 | 9.5 um | ~955 nm | No (need alt crystal) | Smog, air quality |

**Key correction:** NH3 has a usable absorption band at **3.00 um** (v3 N-H stretch), which is fully within the PPLN transparency window. The previously listed ~8 um band is the v2 bending mode. The 3.00 um band is what the NUTMEG project (Covesion + QLM, Innovate UK funded) targets for NH3 detection using PPLN waveguide upconversion.

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
- [x] NH3 reclassified as PPLN-compatible (3.00 um v3 band, not just 8 um v2 band)
- [x] Prior art validated — NUTMEG project confirms NH3 via PPLN upconversion
- [ ] Oil-in-water detection experiment
- [ ] VOC air quality experiment
- [ ] NH3 detection (within PPLN range — shares hardware with energy application)
- [ ] Nitrate detection feasibility study (requires alt crystal)

## Author

Christopher Riner | Active Duty U.S. Navy
ORCID: [0009-0008-9448-9033](https://orcid.org/0009-0008-9448-9033) | GitHub: [jackwayne234](https://github.com/jackwayne234)
