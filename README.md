# Reachable sets in a thin-layer limit

This repository hosts the manuscripts and web assets for a preliminary PhD research proposal on computing guaranteed safety boundaries (reachable sets) for hypersonic atmospheric entry vehicles.

Computing the exact reachable set for a six-degree-of-freedom hypersonic vehicle is out of reach for grid-based dynamic programming, and a bound produced by a numerical solver inherits that solver's accuracy. This research proposes an analytical framework for certified outer bounds, and proves the framework's central inclusion for a reduced model.

**Project Website:** [research.ekdynamics.science](https://research.ekdynamics.science)

## Repository Contents

* **`proposal.pdf`**: The 13-page mathematical core. States the singularly perturbed model and its hypotheses, defines the occupation measures and their topology, and gives one reduced theorem with a complete proof, followed by how hypersonic entry instantiates the model and what remains open.
* **`precis.pdf`**: A 2-page summary, leading with the theorem and closing with the three remaining problems.
* **`index.html`**: The source code for the project's landing page.

## Methodology Highlights

Instead of tracking every chaotic detail of a vehicle tumbling through the atmosphere, this framework uses fundamental physics to draw an absolute outer boundary. The flight is partitioned into three regimes:
1. **The Skeleton:** Smooth, predictable motions (coasting in a vacuum, equilibrium glides).
2. **The Bubbles:** Violent, split-second atmospheric dips where the vehicle sheds massive amounts of speed.
3. **The Residual:** An analytic safety buffer accounting for leftover dynamics and tracking errors.

By dilating the timeline to isolate the "bubbles" (atmospheric dips), the framework tracks the energy dissipated during these very fast events. Because the vehicle has a finite energy budget, that dissipation bounds how many dips there can be, how long each lasts, and therefore how far the vehicle can travel.

## What is proved

For a reduced model that keeps the concentration and discards everything else, the reachable set of the family is contained in that of the skeleton-and-bubble limit system, widened by a residual that is explicit in the data and vanishes with the thinness of the layer. The inclusion holds uniformly over every control, every initial state and every admissible model of the aerodynamics.

The proof is elementary throughout: a dissipation identity integrated once supplies a budget; the budget bounds the number of passes and the time spent in the layer; one change of variable, from time to delivered impulse, makes the inner problem independent of the small parameter; and Gronwall's inequality assembles the pieces. No compactness argument and no measure appears in it.

**Occupation measures** enter after the singular limit rather than before it: the limit system is a low-dimensional reachability problem with one guard and a set-valued reset, which is the hybrid form the occupation-measure relaxation handles, and that is where the certificate is produced. **Lions' concentration-compactness principle** is expected to be needed for the companion statement at the level of measures, for the structure rather than for the constants.

Carrying the result to a full entry vehicle requires three further results: admitting capture into the equilibrium glide, posing the bubble about a control-dependent section, and an averaging theorem with explicit constants valid through resonance. The third is the critical path.

## Current Status & Contact

**Status:** I am actively seeking a PhD advisor to supervise the completion of this research. The reduced theorem above is proved; the central theorem for the full entry problem is open, and the averaging result it rests on is the part an advisor is wanted for.

**Author:** Ethan Knox  
**Email:** ethank5149@gmail.com