\# Recurrence Test Summary — 2026-05-18


## 2026-05-18 Hardening Update

These recurrence results are preserved as exploratory tests.

A later hardened benchmark, **MODE Recurrence Engine v2 Hardened**, found that some earlier PASS results were too generous because raw replay matching can be inflated by best-window search, local cyclic structure, and max-search effects.

Important later findings:

- Ordered data still showed strong signed recurrence.
- Full shuffle and distribution surrogate controls were beaten.
- Block-shuffle control was **not** cleanly beaten.
- Random max-search baseline was **not** beaten.
- Forecasting remains unresolved despite one favorable confidence-filtered result.

Therefore, these files should be read as exploratory evidence of recurrence structure, not proof of reliable forecasting, hidden physics, causal prediction, or unique chronology detection.

Current safest interpretation:

> MODE recurrence tests show that ordered temporal data can contain detectable recurrence structure, but stronger controls are required before claiming predictive usefulness or unique time-order structure.


\## Project Context



These tests were performed as part of exploratory recurrence and replay analysis research connected to the MODE framework and related oscillatory signal experiments.



The work investigates whether deterministic replay/correlation methods can detect recurring structure in:

\- synthetic oscillatory systems

\- noisy oscillatory systems

\- real-world astrophysical datasets



The tests DO NOT claim:

\- hidden physics

\- universal determinism

\- future certainty

\- causal prediction

\- planetary prediction

\- earthquake forecasting



The tests ARE exploratory computational experiments focused on:

\- recurrence detection

\- replay similarity

\- temporal structure

\- oscillatory organization

\- forecasting limits



\---



\# Dataset Sources



\## Real Sunspot Dataset



Source:

https://www.sidc.be/SILSO/DATA/SN\_m\_tot\_V2.0.txt



Provider:

SILSO — Sunspot Index and Long-term Solar Observations

Royal Observatory of Belgium



Dataset:

Monthly historical sunspot numbers.



Reason used:

\- long historical record

\- real oscillatory behavior

\- known cyclical structure

\- scientifically maintained dataset



\---



\# TEST RESULTS



\---



\# TEST 01 — Dimensionless Scale Ratio Test



Purpose:

Compare atomic-scale and solar-scale proportional ratios.



Result:

FAIL\_DIMENSIONLESS\_RATIO\_SIMILARITY



Key Result:

\- Atomic ratio ≈ 35,975

\- Solar ratio ≈ 63,071

\- Relative difference ≈ 54.7%



Meaning:

The ratios are of similar order of magnitude but are not close enough to support strong scale equivalence claims.



Scientific Value:

Useful negative result.

Prevents overclaiming proportional similarity.



\---



\# TEST 02 — Shuffled Sunspot Baseline



Purpose:

Determine whether chronological structure matters.



Result:

PASS\_ORDERED\_STRUCTURE\_BEATS\_SHUFFLE



Key Result:

\- Ordered average ≈ 0.848988

\- Shuffled average ≈ 0.411879

\- Advantage ≈ +0.437108



Meaning:

Replay similarity strongly depends on preserved temporal ordering.



Scientific Value:

One of the strongest results.

Shows recurrence method detects real temporal structure rather than arbitrary value similarity.



\---



\# TEST 03 — Random Noise Control



Purpose:

Test whether replay falsely passes random noise.



Result:

PASS\_RANDOM\_NOISE\_REJECTED



Key Result:

\- Average ≈ 0.411043

\- Scores over 0.72 = 0/20



Meaning:

Random noise does not produce strong replay recurrence.



Scientific Value:

Important negative control.

Shows the framework is not trivially matching everything.



\---



\# TEST 04 — Titius-Bode Residual Test



Purpose:

Evaluate planetary spacing approximation quality.



Result:

PASS\_TITIUS\_BODE\_APPROXIMATE\_PATTERN



Key Result:

\- Inner-system average error ≈ 2.46%

\- Neptune error ≈ 29%



Meaning:

The pattern approximates planetary spacing through Uranus but fails strongly at Neptune.



Scientific Value:

Supports approximate empirical spacing pattern only.

Does not establish physical quantization law.



\---



\# TEST 05 — Planetary Period-Distance Test



Purpose:

Verify Kepler-like scaling relationship.



Result:

PASS\_STRONG\_KEPLER\_SCALING



Key Result:

\- Average ratio ≈ 0.999880

\- Average deviation ≈ 0.000965



Meaning:

Planetary periods and distances follow expected Kepler scaling extremely closely.



Scientific Value:

Calibration/control validation.

Not novel physics.



```

T² ∝ a³

```



\---



\# TEST 06 — Autocorrelation Baseline



Purpose:

Compare replay recurrence against simple autocorrelation.



Result:

PASS\_REPLAY\_BEATS\_AUTOCORRELATION



Key Result:

\- Replay average ≈ 0.848988

\- Autocorrelation average ≈ 0.402127

\- Advantage ≈ +0.446861



Meaning:

Replay recurrence performed much better than a fixed-lag cycle baseline.



Scientific Value:

Suggests replay matching captures more than simple cyclical periodicity.



\---



\# TEST 07 — Cross-Scale Normalized Recurrence



Purpose:

Test recurrence behavior across normalized synthetic systems.



Datasets:

\- atomic-like oscillation

\- planetary-like oscillation

\- MODE-like oscillation



Result:

PASS\_CROSS\_SCALE\_RECURRENCE



Key Result:

\- Average recurrence ≈ 0.995039

\- Maximum difference ≈ 0.007706



Meaning:

Normalized oscillatory systems showed highly similar recurrence behavior.



Scientific Value:

Supports recurrence consistency across synthetic oscillatory scales.

Does NOT establish physical linkage between scales.



\---



\# TEST 08 — Integer Scaling Real Data Test



Purpose:

Test whether integer pre-digest scaling preserves recurrence structure.



Result:

PASS\_INTEGER\_SCALING\_PRESERVES\_REAL\_RECURRENCE



Key Result:

\- Raw score ≈ 0.848988

\- x27 difference ≈ 0.000003



Meaning:

Integer scaling preserved replay recurrence almost perfectly.



Scientific Value:

Supports integer pre-digest stability concept.



\---



\# TEST 09 — Cross-Dataset Recurrence



Purpose:

Test replay across multiple signal regimes.



Datasets:

\- solar-like periodic

\- chaotic drift

\- burst activity

\- mixed oscillation



Result:

PASS\_MULTI\_REGIME\_RECURRENCE



Key Result:

\- Structured systems passed strongly

\- Chaotic drift failed strongly



Meaning:

Replay recurrence works on structured signals but not chaotic drift.



Scientific Value:

Important discrimination result.

Suggests recurrence depends on organized structure.



\---



\# TEST 10 — Forecast Window Error Test



Purpose:

Test replay-based future forecasting.



Result:

FAIL\_REPLAY\_FORECAST\_SIGNAL



Key Result:

\- Average forecast correlation ≈ 0.416099



Meaning:

Replay similarity did not reliably predict future continuation.



Scientific Value:

Important boundary result.

Recurrence detection does not automatically imply predictive power.



\---



\# TEST 11 — Ensemble Replay Forecast



Purpose:

Improve forecasting using weighted ensemble replay matches.



Result:

FAIL\_ENSEMBLE\_REPLAY\_FORECAST



Key Result:

\- Average forecast ≈ 0.415589

\- No meaningful improvement over single replay forecast



Meaning:

Ensemble replay did not improve forecasting quality.



Scientific Value:

Forecast limitations persisted despite averaging multiple replay histories.



\---



\# TEST 12 — Confidence Filtered Forecast



Purpose:

Forecast only when replay similarity exceeds high-confidence threshold.



Result:

PASS\_CONFIDENCE\_FILTERED\_FORECAST



Key Result:

\- Accepted forecast average ≈ 0.671758

\- Strong accepted forecasts = 12/17



Meaning:

Higher replay similarity corresponded to better forecast performance.



Scientific Value:

Most promising forecasting-related result.

Suggests replay confidence may contain predictive information.



Important Caveat:

Forecast failures still occurred within accepted high-confidence cases.



\---



\# TEST 13 — Regime-Aware Forecast



Purpose:

Restrict replay matching to similar trend regimes.



Regimes:

\- rising

\- falling

\- stable



Result:

PARTIAL\_REGIME\_AWARE\_FORECAST



Key Result:

\- Accepted forecast average ≈ 0.655481



Meaning:

Regime matching modestly improved replay forecasting consistency.



Scientific Value:

Suggests regime structure matters for replay forecasting.



\---



\# TEST 14 — Walk-Forward Baseline Comparison



Purpose:

Compare replay forecasting against naive persistence forecasting.



Result:

FAIL\_REPLAY\_FORECAST\_NOT\_USEFUL\_YET



Key Result:

\- Replay average ≈ 0.492048

\- Naive baseline ≈ 0.449075

\- Replay wins = 10/25



Meaning:

Replay forecasting slightly exceeded naive baseline on average but not consistently enough to establish useful forecasting capability.



Scientific Value:

Current replay forecasting is not yet reliable or practically useful.



\---



\# OVERALL CONCLUSIONS



\## Strongest Supported Findings



The experiments support evidence for:

\- recurrence detection

\- ordered temporal structure detection

\- replay similarity behavior

\- integer scaling preservation

\- cross-regime recurrence discrimination

\- replay dependence on non-random structure



The framework consistently:

\- beat shuffled controls

\- rejected random noise

\- detected organized oscillatory structure



\---



\# CURRENT LIMITATIONS



The experiments do NOT currently establish:

\- reliable forecasting

\- future prediction

\- causal prediction

\- hidden physical laws

\- universal determinism

\- cross-scale physical equivalence



Forecasting results remain:

\- partial

\- unstable

\- inconsistent

\- weaker than recurrence detection



\---



\# MOST IMPORTANT SCIENTIFIC RESULT



The strongest result from this test suite is:



Replay recurrence strongly depends on preserved temporal structure and organized oscillatory behavior, while shuffled and random datasets fail substantially.



\---



\# CURRENT BEST CHARACTERIZATION



This work is best described as:



An exploratory recurrence and replay analysis framework investigating temporal structure detection in oscillatory systems and real-world astrophysical datasets.



Not:

\- a prediction engine

\- a proof of hidden physics

\- a deterministic universe model



\---



\# FUTURE DIRECTIONS



Potential future research directions:

\- improved regime classification

\- spectral similarity matching

\- phase-aware replay analysis

\- walk-forward forecasting refinement

\- cross-dataset astrophysical validation

\- statistical significance benchmarking

\- additional negative-control studies



\---

