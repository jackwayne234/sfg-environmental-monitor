# Target Contaminants — Water and Air

## Water Contaminants

### Petroleum / Oil (C-H Stretch, 3.0-3.5 um)

The strongest and most distinctive mid-IR signature for water contamination. The C-H stretching vibration at 3.0-3.5 um is characteristic of all hydrocarbons — diesel, crude oil, gasoline, lubricants.

- Absorption peak: 3.3-3.4 um
- Same wavelength region as methane — **reuses the same PPLN crystal** from energy application
- Strong signal, easy to detect
- Best starting point for water quality validation

Applications: oil spill detection, refinery runoff monitoring, stormwater discharge monitoring, bilge water compliance

### Nitrate (NO3-, 7.3 um / 1370 cm-1)

Major water quality concern from agricultural runoff. Nitrate contamination causes algal blooms, dead zones, and is regulated under the Safe Drinking Water Act (MCL: 10 mg/L).

- Absorption: 7.3 um (1370 cm-1)
- This is **outside the easy PPLN range** (LiNbO3 transparent to 5.2 um)
- May require alternative nonlinear crystal: AgGaS2 or orientation-patterned GaAs (OP-GaAs)
- More challenging — pursue after petroleum detection is validated

### Phosphate (PO4, 8.2-9.5 um)

Fertilizer runoff indicator. Contributes to eutrophication.

- Absorption: 8.2-9.5 um (P-O stretch)
- Well outside PPLN range
- Requires alternative crystal material
- Lower priority than petroleum and nitrate

## Air Pollutants

### Volatile Organic Compounds (VOCs, 3.0-3.6 um)

Same C-H stretch region as petroleum and methane.

- Absorption: 3.0-3.6 um
- **Same PPLN crystal as CH4 and petroleum detection**
- Easy to test: acetone vapor (readily generated from liquid acetone)
- Applications: industrial fence-line monitoring, indoor air quality, workplace exposure

### Sulfur Dioxide (SO2, 7.4 um)

Industrial emissions marker.

- Absorption: 7.4 um (1355 cm-1)
- Outside easy PPLN range (same challenge as nitrate)
- Alternative crystal needed

### Ammonia (NH3, ~8 um)

Agricultural and industrial emissions.

- Absorption: ~8 um region
- Outside PPLN range
- Alternative crystal needed

### Ozone (O3, 9.5 um)

Smog and air quality indicator.

- Absorption: 9.5 um
- Well outside PPLN range
- Requires far-infrared capable nonlinear material

## Wavelength Accessibility Summary

| Wavelength Range | PPLN Compatible? | Contaminants |
|-----------------|-----------------|--------------|
| 3.0-5.0 um | Yes | Petroleum, VOCs, some dissolved organics |
| 5.0-5.2 um | Edge of range | Marginal |
| 5.2-10 um | No (need alt crystal) | Nitrate, phosphate, SO2, NH3, O3 |

**Practical implication:** Start with 3.0-5.0 um targets (petroleum, VOCs) which reuse existing PPLN hardware. Longer-wavelength targets require separate R&D for alternative nonlinear crystals.
