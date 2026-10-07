# Certified analytical bounds for hypersonic reachable sets

This repository hosts the manuscripts and web assets for a preliminary PhD research proposal on computing guaranteed safety boundaries (reachable sets) for hypersonic atmospheric entry vehicles. 

Currently, computing the exact reachable set for a six-degree-of-freedom hypersonic vehicle is practically impossible for grid-based dynamic programming, and numerical solvers only provide educated approximations. This research proposes an analytical framework to produce certified outer bounds without relying on numerical simulations.

**Project Website:** [research.ekdynamics.science](https://research.ekdynamics.science)

## Repository Contents

* **`proposal.pdf`**: The 20-page preliminary PhD research proposal. Details the mathematical framework, the singular limit decomposition, and a reduced theorem proved in full.
* **`precis.pdf`**: A 2-page executive summary (précis) of the proposal, outlining the problem, the approach, the reduced theorem, and remaining open problems.
* **`index.html`**: The source code for the project's landing page.

## Methodology Highlights

Instead of tracking every chaotic detail of a vehicle tumbling through the atmosphere, this framework uses fundamental physics to draw an absolute outer boundary. The flight is partitioned into three regimes:
1. **The Skeleton:** Smooth, predictable motions (coasting in a vacuum, equilibrium glides).
2. **The Bubbles:** Violent, split-second atmospheric dips where the vehicle sheds massive amounts of speed.
3. **The Residual:** An analytic safety buffer accounting for leftover dynamics and tracking errors.

By dilating the timeline to isolate the "bubbles" (atmospheric dips) in a rescaled "slow time," the framework tracks the energy dissipated during these incredibly fast events. Because the spacecraft has a finite energy budget, tracking this dissipation mathematically bounds how far the ship can travel. The proposal proves this on a reduced model, where the argument can be carried through in full.

Formally, this is achieved by casting the flight dynamics as a linear problem on **occupation measures**, and by handling the thin-atmosphere limit so that the boundary-layer events are not lost along the way.

## Current Status & Contact

**Status:** I am actively seeking a PhD advisor to supervise the completion of this research.

**Author:** Ethan Knox  
**Email:** ethank5149@gmail.com