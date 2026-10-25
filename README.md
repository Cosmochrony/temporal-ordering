This repository contains the source of the paper on projective temporal ordering and cumulative projected capacity  
(paper of the Cosmochrony / spectral admissibility programme).

This work proposes a **candidate monotone proxy for temporal ordering**
based on the cumulative projected capacity observable

$I(n) = \sigma_{\mathrm{pair}}(0) - \sigma_{\mathrm{pair}}(n)$,

which measures the amount of spectral structure projected up to BFS depth $n$
along the spectral admissibility cascade.

The paper reports and separates three statements:

- **Mode retention (proved, immediate):** the cumulative Gram–Schmidt span satisfies
  $V_n \subseteq V_{n+1}$; modes, once projected, do not leave it.
- **Monotonicity (observed numerically, conjectured):** for
  $q \in \lbrace 29, 61, 101, 151, 211 \rbrace$, across 274 pairs and 504 post-burn-in steps
  ($n_{\mathrm{burn}} = 2$), no decrease of $I(n)$ larger than $10^{-6}$ of its plateau value occurs, for
  any conjugate pair. The traces are exactly non-decreasing for $q \le 101$; for $q = 151$ and $211$,
  exact plateau decreases of order $10^{-10}$ occur, so the pair-averaged trace is non-decreasing only
  within tolerance. Exact monotonicity of $I(n)$ is equivalent to
  $\sigma_{\mathrm{pair}}(n)$ being non-increasing; it does not follow from mode retention, since the
  inclusion of spans does not control the shellwise ratio $\sigma_c(n) = \delta r_n / |S_n|$. The
  stepwise statement is the paper's conjecture (one-way activation); the numerical result is the
  tolerance bound $I(n+1) - I(n) \ge -10^{-6} I_{\max}$.
- **Order on states (conditional):** $I(n)$ is computed along a trajectory and is not shown to depend
  on the effective state alone, and the non-strict inequality allows plateaus. A strict partial order
  on states requires the acyclicity hypothesis [H-acyc] of the Foundation paper, which is not
  established.

The proposed ordering is not a dynamics of the substrate $\chi$, and it is compatible with
**observable rank stability (O24)**.

## Conceptual Overview

The paper proceeds in three logical steps:

1. **Identification of the observable**  
   The spectral observable $\sigma_{\mathrm{pair}}(n)$ measures residual projective capacity and
   decreases in every tested case up to plateau fluctuations below the tolerance; its stepwise decrease is not a consequence of the construction.
   Its complement $I(n)$ measures cumulative projected structure and is the natural candidate for a
   monotone ordering.

2. **Projective temporal ordering along a trajectory**  
   Successive effective states are linked by admissible transitions
   $U_n \to \mathcal{A}(U_n) \to U_{n+1}$. The fibre $\Pi^{-1}(U_n)$ records the configurations
   that realise $U_n$, and $U_{n+1}$ is the image of an admissible continuation of one of them
   (reprojecting a configuration of the fibre itself would return $U_n$). Along the tested BFS
   trajectories, $I(n+1) - I(n) \ge -10^{-6} I_{\max}$ at every post-burn-in step. This is a property of the depth
   index along a trajectory, not an order on states.

3. **Mode retention and one-way activation**  
   Mode retention is a cumulative retention of projected structure, not a thermodynamic statement. The
   observed one-way activation (non-increase of $\sigma_{\mathrm{pair}}$) is what makes $I(n)$ a
   monotone proxy; it remains conjectural.

## Core Claims

1. **A candidate monotone proxy along the admissibility cascade**  
   $I(n)$ is observed to be non-decreasing along all tested trajectories, after burn-in and up to the
   stated threshold; a proof is open.

2. **Time is not a fundamental parameter of the substrate**  
   The proposed ordering is read from admissible projections, not from an evolution of $\chi$.

3. **Non-injectivity raises the ordering question; it does not orient the states**  
   The multiplicity of fibres $\Pi^{-1}(o)$ makes successive admissible realisations distinct from
   the underlying configurations, but a chain of non-injective steps can revisit a state; orienting it
   requires [H-acyc].

4. **Cumulative retention is structural, not thermodynamic**  
   Mode retention reflects accumulation of projected spectral structure without invoking entropy or
   probability. The first transition $U_0 \to U_1$ is not guaranteed: projective incompleteness gives
   a non-trivial fibre, not an admissible successor.

5. **Observable rank remains invariant**  
   Temporal progression reorders admissible configurations but does not
   increase the observable rank, in agreement with the supplied selection rule of O23
   (conditional on its supplied spinor carrier) and its stabilisation in O24.

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
code/  # Figure, stability-diagnostic output and its provenance (stability_provenance.txt)
tex/   # LaTeX sources (compiled into out/ by compile.sh)
README.md
```

## Reproducibility

Table 1 is regenerated by `o_stability_diagnostic.py` from the
[spectral-o25](https://github.com/Cosmochrony/spectral-o25) repository on the archived o25 pipeline outputs
of the [simulation](https://github.com/Cosmochrony/simulation) repository. The script reports the exact test
and the $10^{-6}$ tolerance test side by side. `code/stability_provenance.txt` records the commits, the input
files with their SHA-256 digests and the command; `code/stability_diagnostic_output.txt` is the unedited
output.

## Links

- 📄 Paper (Zenodo): https://doi.org/10.5281/zenodo.19474639
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
