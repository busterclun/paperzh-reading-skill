# Deep mode reference

## Three-layer reading record

### Layer 1 — orientation

Create a one-page argument map with:

| Element | Reading question | Evidence |
|---|---|---|
| Problem | What real problem is being addressed? | Introduction/page |
| Gap | What is missing from prior work? | Introduction/references |
| Question/hypothesis | What could be falsified? | Aim/hypothesis |
| Object/system | What exactly is represented? | Methods |
| Variables | What changes and what is controlled? | Methods/figures |
| Method | How are outputs generated? | Methods/equations |
| Evidence | Which result supports which claim? | Figure/table/equation |
| Conclusion | What does the evidence actually warrant? | Discussion/conclusion |

### Layer 2 — method and evidence

For each major claim, create an evidence row:

| Claim | Required evidence | Supplied evidence | Missing/weak evidence | Alternative explanation | Confidence | Boundary |
|---|---|---|---|---|---|---|

Read the following as appropriate to the field:

- experimental controls, repeats, calibration, uncertainty, detection limit, and data processing;
- numerical equations, closure/model choice, mesh and time-step independence, convergence, domain size, and validation;
- statistics, sample size, effect size, confidence interval, sensitivity, and train/test or cross-validation design;
- geometry, material/fluid properties, scale, interface/surface condition, operating and boundary conditions;
- whether the reported resolution can support the claimed mechanism.

### Layer 3 — critique and transfer

Every serious criticism should state:

`observation → why it matters → affected claim → severity → what would resolve it`.

Every proposed research transfer should state:

`gap → hypothesis → variables → controls → method → validation criterion → decision rule → priority`.

## Figure and table protocol

For every key figure/table:

1. Identify its role: setup, validation, trend, mechanism, comparison, or summary.
2. Read axes, units, scales, legend, normalization, color map, error bars, and sample size.
3. State what changes and what stays fixed.
4. Extract the actual trend and magnitude; avoid substituting visual impression for numbers.
5. Map the figure/table to the claim it supports.
6. Note resolution, missing uncertainty, overplotting, selection window, or other caveat.
7. State whether the evidence supports causality, association, or only consistency.

## Formula protocol

For each key equation:

- record its number and purpose;
- define symbols, units, and nondimensionalization;
- identify assumptions, neglected terms, closure, and boundary/initial conditions;
- state limiting cases or expected behavior where useful;
- explain how parameters enter the reported result;
- note whether the equation is derived, cited, fitted, or merely used;
- mark any symbol or derivation that cannot be determined from the supplied copy.

## Scenario-boundary matrix

Use this matrix whenever the paper concerns experiments, simulations, physical systems, or applied models:

| Dimension | Paper range | Tested? | Expected transfer risk | Review judgment |
|---|---|---|---|---|
| Material/working fluid |  |  |  |  |
| Temperature/pressure |  |  |  |  |
| Flow/state/regime |  |  |  |  |
| Geometry/scale/roughness |  |  |  |  |
| Inlet/outlet/boundary |  |  |  |  |
| Gravity/orientation/transient |  |  |  |  |
| Numerical/measurement resolution |  |  |  |  |

## Priority rubric

- **P0:** threatens validity, reproducibility, or the main conclusion.
- **P1:** high-value mechanism or generalization test with a realistic path to resolution.
- **P2:** useful refinement that does not change the main decision.

Priority is not importance alone. Include expected information gain, effort, risk, and the decision that the result would change.

