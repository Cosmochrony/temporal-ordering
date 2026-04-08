This repository contains the source of the  
[paper on projective temporal ordering and cumulative projected capacity](out/projective_temporal_ordering.pdf)  
(paper OXX de Cosmochrony / spectral admissibility programme).

This work introduces a **structural notion of temporal ordering**
based on the cumulative projected capacity observable

$I(n) = \sigma_{\mathrm{pair}}(0) - \sigma_{\mathrm{pair}}(n)$.

Starting from the spectral admissibility cascade, we identify a **monotone
accumulation variable** that measures the amount of spectral structure
stably projected up to depth $n$.

We then show that:

- $I(n)$ is **strictly non-decreasing** along all tested admissible trajectories,
- temporal ordering emerges as a **projective relation**, not a dynamics,
- monotonicity reflects a **one-way activation mechanism** in spectral space,
- the construction is fully compatible with **observable rank stability (O24)**.

The derivation requires **no background time parameter, no thermodynamic
assumption, and no dynamical evolution of the substrate**.
Temporal ordering appears as a **structural consequence of non-injectivity**.

## Conceptual Overview

The paper proceeds in three logical steps:

1. **Identification of the correct observable**  
   The natural spectral observable $\sigma_{\mathrm{pair}}(n)$ measures
   residual projective capacity and is strictly decreasing. Its complement
   $I(n)$ instead measures cumulative projected structure and is the only
   candidate compatible with a monotone ordering.

2. **Projective temporal ordering**  
   Time is defined as an ordering relation on admissible projections:

   $U_t \prec U_{t+1} \iff I(U_t) \le I(U_{t+1})$.

   This ordering does not correspond to motion in the substrate $\chi$,
   but to changes in admissible selections $\sigma(U_t) \in \Pi^{-1}(U_t)$
   under a fixed non-injective projection $\Pi$.

3. **Structural irreversibility (one-way activation)**  
   Numerical results show that once spectral modes are stably projected,
   they do not deactivate. This induces a strictly monotone accumulation
   of structure and provides a non-thermodynamic form of irreversibility.

## Core Claims

The paper establishes the following statements:

1. **Temporal ordering arises from cumulative spectral projection**  
   The observable $I(n)$ provides a monotone ordering parameter intrinsic
   to the admissibility cascade.

2. **Time is not a fundamental parameter of the substrate**  
   The ordering is induced by the structure of admissible projections,
   not by an evolution of $\chi$.

3. **Non-injectivity is the origin of temporal ordering**  
   The multiplicity of fibres $\Pi^{-1}(o)$ implies that successive
   admissible selections generate an intrinsic ordering.

4. **Irreversibility is structural, not thermodynamic**  
   The one-way activation property reflects accumulation of admissible
   spectral structure without invoking entropy or probability.

5. **Observable rank remains invariant**  
   Temporal progression reorders admissible configurations but does not
   increase the observable rank, in agreement with O23–O24.

## What This Paper Does Not Assume

To avoid conflating structural and dynamical notions of time, the paper does not assume:

- a fundamental time parameter,
- a dynamical evolution of the substrate $\chi$,
- thermodynamic entropy or coarse-graining,
- probabilistic interpretation of the cascade,
- any background spacetime structure.

The analysis is entirely **projective and spectral**.

## Keywords

Temporal ordering, non-injectivity, spectral admissibility, cumulative capacity,
irreversibility, projective dynamics, emergence of time

## Repository Contents
```
paper/
├── pdf/ # Compiled paper PDF
├── tex/ # LaTeX sources
└── README.md
```

## Links

- 📄 [Paper PDF](https://github.com/Cosmochrony/.../projective_temporal_ordering.pdf)
- 🌐 Website: https://cosmochrony.org

## Citation

If you reference this work, please cite:

> J. Beau, *Projective Temporal Ordering and Cumulative Projected Capacity*, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models.  
These tools were used as analytical assistants for exploring alternative
formulations, checking internal consistency, and improving clarity.  
All claims, interpretations, and final formulations remain the sole
responsibility of the author.

## Contributions

This repository is intended as a research reference.

Critical feedback, independent analyses, and formal scrutiny are welcome.  
Please open an issue to discuss conceptual points, monotonicity mechanisms,
possible counterexamples, or extensions to larger primes.
