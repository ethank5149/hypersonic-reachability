# Certified analytical bounds for hypersonic reachable sets

This repository hosts the manuscripts and web assets for a preliminary PhD research proposal on computing guaranteed safety boundaries (reachable sets) for hypersonic atmospheric entry vehicles. 

Currently, computing the exact reachable set for a six-degree-of-freedom hypersonic vehicle is practically impossible for grid-based dynamic programming, and numerical solvers only provide educated approximations. This research proposes an analytical framework to produce certified outer bounds without relying on numerical simulations.

**Project Website:** [research.ekdynamics.science](https://research.ekdynamics.science)

## Repository Contents

* **`proposal.pdf`**: The 7-page preliminary PhD research proposal. Poses the problem, gives a reduced model in which the phenomenon is present, names the tools the analysis should need, and states the four problems that would have to be established. Nothing in it is claimed as proved.
* **`precis.pdf`**: A 2-page summary of the proposal: the question, the model, the structure expected, and what remains open.
* **`index.html`**: The source code for the project's landing page.

## Methodology Highlights

Instead of tracking every chaotic detail of a vehicle tumbling through the atmosphere, this framework uses fundamental physics to draw an absolute outer boundary. The flight is partitioned into three regimes:
1. **The Skeleton:** Smooth, predictable motions (coasting in a vacuum, equilibrium glides).
2. **The Bubbles:** Violent, split-second atmospheric dips where the vehicle sheds massive amounts of speed.
3. **The Residual:** An analytic safety buffer accounting for leftover dynamics and tracking errors.

By dilating the timeline to isolate the "bubbles" (atmospheric dips) in a rescaled "slow time," the approach tracks the energy dissipated during these very fast events. Because the spacecraft has a finite energy budget, that dissipation should bound how far it can travel. The proposal sets this out on a reduced model and states what would have to be established to make it a theorem.

Formally, this is achieved by casting the flight dynamics as a linear problem on **occupation measures**, and by handling the thin-atmosphere limit so that the boundary-layer events are not lost along the way.

## Current Status & Contact

**Status:** I am actively seeking a PhD advisor to supervise the completion of this research.

**Author:** Ethan Knox  
**Email:** ethank5149@gmail.com