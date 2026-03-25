# Experimental Validation — Environmental Application

All environmental experiments build on the energy application equipment. If energy experiments are done first, incremental costs are significantly reduced.

## Experiment 1: Oil-in-Water Detection
**Cost: $12-20K standalone, $5-10K if energy equipment exists | Time: 2-3 weeks**

Best starting point — petroleum has the strongest, most distinctive mid-IR signature (3.0-3.5 um C-H stretch), and the wavelength overlaps with the methane detection crystal from the energy application.

**Setup:**
- ATR crystal: ZnSe, ~$200-500
- Water samples contaminated with known concentrations of diesel/oil
- Same PPLN crystal used for CH4 detection (3.27 um region)
- Same pump laser, detector, and optical bench from energy experiments

**Procedure:**
1. Baseline: ATR crystal in contact with clean water, record SFG output
2. Add known concentration of diesel to water (start at 100 ppm)
3. Measure SFG signal change
4. Progressive dilution to find minimum detectable concentration
5. Test with different hydrocarbons (diesel, motor oil, gasoline) to verify C-H stretch detection is general

**Go/No-Go:** If oil contamination is detectable at ppm levels in water, the platform works for water quality monitoring.

## Experiment 2: Air Quality VOC Detection
**Incremental cost: $5-8K | Time: 1-2 weeks**

VOCs absorb at 3.0-3.6 um (same C-H stretch region as petroleum and methane).

**Setup:**
- Gas cell with known VOC concentration
- Easy VOC source: acetone vapor (liquid acetone in a heated flask with carrier gas)
- Same PPLN crystal as CH4/oil detection — zero new optical hardware

**Procedure:**
1. Baseline with clean air in gas cell
2. Introduce acetone vapor at known concentration
3. Measure SFG signal attenuation
4. Test with other VOCs (toluene, xylene) if available

This demonstrates air quality monitoring capability with the same hardware used for gas leak and water quality detection.

## Experiment 3: Nitrate in Water
**Incremental cost: $8-15K | Time: 3-4 weeks**

**Challenge:** Nitrate absorbs at 7.3 um — outside the PPLN transparency window (5.2 um cutoff). This requires:
- Alternative nonlinear crystal: AgGaS2 (~$2-5K) or orientation-patterned GaAs (~$3-8K)
- Different pump wavelength may be needed
- More research required before attempting

**Recommendation:** Do after petroleum and VOC detection are validated. If 7.3 um proves impractical, focus the environmental application on contaminants with absorption in the 3-5 um window (petroleum, VOCs, dissolved organics).

## Total Cost

| Path | Cost | What You Validate |
|------|------|-------------------|
| Exp 1 (oil in water) | $5-10K incremental | Water quality detection works |
| + Exp 2 (VOCs in air) | +$5-8K | Air quality monitoring, same hardware |
| + Exp 3 (nitrate) | +$8-15K | Longer-wavelength detection feasibility |
| **Total** | **$18-33K** | **Environmental monitoring validated** |
