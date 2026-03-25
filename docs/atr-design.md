# ATR (Attenuated Total Reflection) Design for Water Monitoring

## The Problem

Mid-infrared light is heavily absorbed by water itself. Strong water absorption bands at 2.7, 3.0, and 6.1 um make it impossible to shine IR directly through a water sample and measure dissolved contaminants — the water signal overwhelms everything.

## The Solution: ATR

In Attenuated Total Reflection, the IR beam travels inside a high-refractive-index crystal (ZnSe, diamond, or germanium) and reflects off the crystal surface that's in contact with the water sample.

At each reflection point, an evanescent wave penetrates 0.5-2 um into the water. This is short enough that water absorption doesn't dominate, but long enough that dissolved contaminants interact with the IR beam and leave their absorption fingerprint.

```
                    Water sample (in contact with crystal surface)
                    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    IR in -->  /    /    /    /    /    /    /  --> IR out (to PPLN)
              /____/____/____/____/____/____/
              ATR crystal (ZnSe, diamond, Ge)
```

Each internal reflection samples a thin layer of the water. Multiple reflections accumulate the signal. A typical ATR crystal has 5-12 reflection points.

## ATR Crystal Options

| Material | Transparency | Refractive Index | Pros | Cons | Cost |
|----------|-------------|-----------------|------|------|------|
| ZnSe | 0.6-22 um | 2.4 | Broad range, affordable | Soft, scratches | $200-500 |
| Diamond | 0.2-80 um | 2.4 | Extremely durable, broad range | Expensive | $2,000-5,000 |
| Germanium | 1.8-23 um | 4.0 | High refractive index (deep penetration) | Opaque in visible | $300-800 |

For field deployment and durability: diamond ATR is preferred (already standard in portable FTIR).

## Integration with SFG Detection

The ATR crystal output (attenuated IR carrying contaminant absorption signatures) feeds directly into the PPLN waveguide array for SFG upconversion. The SFG output wavelength identifies which contaminant is present; the SFG output intensity indicates concentration.

```
Water sample → ATR crystal → PPLN waveguide array + pump → Si detector array
                                                                    ↓
                                                          "Which contaminant is present?"
```

The short interaction path (0.5-2 um per reflection) is actually compatible with PPLN waveguide geometry. The evanescent coupling depth is similar to what's used in integrated photonic sensors.

## Existing ATR-FTIR for Water

ATR-FTIR is already the standard for laboratory water quality analysis:
- EPA Method 418.1 (oil and grease in water) uses IR absorption
- ATR-FTIR benchtop instruments: $30,000-100,000
- Portable ATR-FTIR: $40,000-50,000

The SFG device replaces the FTIR spectrometer with a solid-state PPLN array — no scanning mirror, no cooled detector, no Fourier transform computation. Simpler, more rugged, lower cost for targeted contaminants.

**Limitation:** FTIR sees the entire spectrum (catches unexpected contaminants). The SFG device only detects pre-tuned contaminants. For screening unknowns, FTIR is still better. For monitoring known targets in the field, SFG wins on durability.
