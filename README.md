# IceCube Var-Rho DOM Noise Discrimination

**Record DOI:** https://doi.org/10.5281/zenodo.23494707

IceCube's optical modules count single photons in the dark, and everything
that isn't a photon still gets counted. The low-energy science that lives
down in that noise — supernova monitoring above all — is a rate
measurement, so it lives or dies on whether a rate increase can be
trusted. This record documents a noise-rejection layer built for exactly
that problem.

The method is the two-stage variance-correlation gate from this program's
hardware-verified baseline (Var > 1000, ρ > 0.8), transferred to DOM
pulses. One parameter couldn't transfer: the 50 ms hold-off that worked on
the muon bench would mangle a kilohertz-rate photon stream, so the
pre-registration re-derived it for the DOM regime and locked it at 10 μs,
with all rate claims dead-time-corrected.

The first simulation taught us something the concept note didn't start out
knowing: a burst of clean pulses sails through any pulse-shape gate,
because a burst is a rate phenomenon, not a shape phenomenon. So the
working system is three layers, each reported separately — pulse (the
locked gate), interval (short time-gap excess on the raw discriminator
stream, the IceCube 2017 method), and rate (sliding-window Poisson tests
on the accepted stream).

What's in this repository:

- **Concept note v1.0.1** — the argument, the mapping, the addendum
  recording the three-layer finding; carries this DOI in its header.
- **Pre-registration v1.0** — every threshold frozen before any simulated
  event; falsifiers N1–N5 with numbers attached; Wilson 95% intervals
  mandatory. Fingerprint 6bde4e432a366938.
- **Phase-1 simulation** — notebook (seed 684, Run-All), results.json, and
  two figures: the retention and rate-honesty boundary plot, and the N1
  by-layer plot.

Headline exploratory numbers: the correlated noise component stands ~860×
above its Poisson expectation on the interval layer; signal retention stays
above the locked floor across the full rate scan; burst detection reaches
86.3% [74.3–93.2]%, limited by burst strength rather than the method; the
certified rate-honesty boundary for the locked hold-off is 1 kHz.

Status, plainly: this is an engineering analogue and a control study. The
real-data phase needs IceCube's hit-level streams, which aren't public, so
it waits on access — no claim is made here that it doesn't.

Lineage: QCID-Sigma v5.4 (10.5281/zenodo.23378709) → muon
pre-registration v1.1 (10.5281/zenodo.23405991) → swarm veto protocol
(10.5281/zenodo.23431140) → swarm computational validation
(10.5281/zenodo.23433610) → front-consistency veto
(10.5281/zenodo.23482628) → this record.

License: MIT / CC BY. Civilian application.
