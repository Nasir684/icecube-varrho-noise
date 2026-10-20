# IceCube Var-Rho DOM Noise Discrimination

Concept note, locked pre-registration, and Phase-1 exploratory simulation for
a variance–correlation (Var-Rho) noise-rejection layer on IceCube-class
photon counting.

**Mechanism:** the two-stage Var-Rho gate (Var > 1000, ρ > 0.8,
hardware-verified baseline) discriminates pulse shape; one rate parameter
(the 50 ms bench hold-off) is re-derived for the DOM regime and locked at
10 μs with dead-time-corrected statistics.

**Three-layer architecture (exploratory finding, Phase 1):** the pulse gate
alone cannot reject a burst of clean pulses — bursts are rate phenomena.
The working system is three layers, reported separately: pulse (locked gate),
interval (short-Δt excess on the discriminator stream, the IceCube 2017 §3.8
method), and rate (sliding-window Poisson tests on the accepted stream).

**Status:** concept note v1.0.1 + pre-registration v1.0 (thresholds frozen
before any simulated event) + exploratory Phase-1 simulation (seed 684, all
rates with Wilson 95% intervals). Engineering analogue, control-only. Phase 2
(real hit-level data) is access-conditional and not claimed.

**Lineage:** QCID-Sigma v5.4 (10.5281/zenodo.23378709) → muon
pre-registration v1.1 (10.5281/zenodo.23405991) → swarm veto protocol
(10.5281/zenodo.23431140) → swarm computational validation
(10.5281/zenodo.23433610) → front-consistency veto
(10.5281/zenodo.23482628) → this record.

**License:** MIT / CC BY. Civilian application.
