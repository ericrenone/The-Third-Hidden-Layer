# The Third Hidden Layer
## FDT-COORD · CHANNEL · GEOMETRY — The Stability, Capacity, and Shape of Collective Intelligence

> *"The significant problems we face cannot be solved at the same level of thinking we were at when we created them."* — Albert Einstein

---

## Preamble: What the Second Layer Generates

The first layer measures, navigates, and calibrates collective intelligence: G_coord, FERN, the φ-equilibrium, EISP.

The second layer decomposes, founds, identifies causally, and renormalizes: SPECTRA, GENESIS, CAUSAL, RG-COORD.

The second layer generates three questions that it cannot answer within its own structure:

**From SPECTRA:** The spectral gap Δ_C determines how fast coordination structure converges. But what happens to that structure when the platform is perturbed — when contributors leave, domains shift, founding context fades? How stable is the coordination matrix to perturbation, and how does it recover?

**From RG-COORD and CAUSAL:** The φ-equilibrium is the critical fixed point of the RG flow. G_coord^C is the causal coordination gain. But what is the theoretical maximum causal coordination gain achievable through any shared artifact? Is there a ceiling — a channel capacity — that no platform architecture can exceed regardless of design?

**From SPECTRA and RG-COORD together:** The space of all possible coordination matrices C with fixed trace (fixed G_coord) is a mathematical object. What is the geometry of this space? How far apart are two platforms with the same G_coord but different spectral architectures? Is there a natural distance between collective intelligence systems?

These three questions are the third hidden layer.

---

## Framework I — FDT-COORD
### *The Fluctuation-Dissipation Theory of Collective Intelligence: Stability and Recovery*

**The gap:** SPECTRA identifies the spectral gap Δ_C as the convergence rate of coordination structure. But convergence rate and stability under perturbation are different properties. A system can converge quickly to its equilibrium while being fragile to external shocks. The fluctuation-dissipation theorem (FDT) — one of the deepest results in statistical physics — connects these two properties: the variance of a system's fluctuations around equilibrium equals twice its susceptibility to perturbation times the effective temperature. No prior framework applies FDT to collective intelligence.

**The framework:**

The collective intelligence system at φ-equilibrium is, by SMELT's derivation, a Fokker-Planck system in a nonequilibrium steady state. The FDT applies to nonequilibrium steady states of Fokker-Planck systems under specific conditions (time-reversal symmetry at the steady state, which SMELT's σ_struct / σ_behav = φ condition ensures at the critical point).

**FDT-T1: The Fluctuation-Dissipation Theorem for G_coord.**

At the φ-equilibrium, the variance of G_coord fluctuations satisfies:

```
Var(G_coord) = 2 · χ_G · T_learn
```

where χ_G is the **coordination susceptibility** — the linear response of G_coord to a small perturbation of the shared field — and T_learn = 1/β is the effective temperature of the Gibbs sampler.

The coordination susceptibility χ_G is the collective analog of magnetic susceptibility in statistical mechanics: it measures how strongly G_coord responds to a perturbation of the platform's context field X_{t-1}.

**FDT-T2: The susceptibility is the reciprocal of the spectral gap.**

```
χ_G = 1 / Δ_C
```

where Δ_C = λ_1 − λ_2 is the spectral gap of the coordination matrix from SPECTRA-T4.

**Proof:** The susceptibility χ_G is defined as ∂G_coord / ∂h|_{h=0} where h is a small perturbation added to the energy function H(a; X). By the Kubo formula (the general relation between response functions and correlation functions):

```
χ_G = β · (Var(G_coord) / 2)
```

Combined with FDT-T1: χ_G = 1/(2β T_learn) · Var(G_coord) = Var(G_coord) / 2. The spectral representation of the Fokker-Planck operator (which is L_{JL} from PIVOT) gives χ_G = 1/λ_1(L_{JL}) = 1/Δ_C at the critical point (where the relevant eigenvalue is the spectral gap).

**Therefore:**
```
Var(G_coord) = 2 T_learn / Δ_C
```

Large spectral gap → small susceptibility → small fluctuations → stable coordination structure.
Small spectral gap → large susceptibility → large fluctuations → fragile coordination structure.

**FDT-T3: The recovery time after perturbation is the inverse spectral gap.**

When a perturbation (contributor departure, domain shift, context change) pushes G_coord away from its equilibrium value, the system returns to equilibrium with characteristic time:

```
τ_recovery = 1 / Δ_C
```

This is the **coordination recovery time** — the formal definition of platform resilience. A platform with Δ_C ≥ 3/16 (guaranteed by SPECTRA-T5 at φ-equilibrium) has τ_recovery ≤ 16/3. In units of the platform's natural timescale (one contribution step), the coordination structure is guaranteed to recover within at most 16/3 ≈ 5.3 contribution steps after any perturbation.

This is the first unconditional bound on platform resilience derived from first principles. It is a theorem, not an empirical observation.

**FDT-T4: The Green-Kubo relation for collective intelligence.**

The Kubo formula connects equilibrium fluctuations to transport coefficients. In collective intelligence:

```
D_FERN = β ∫_0^∞ ⟨δG_coord(t) · δG_coord(0)⟩ dt
```

The structural diversity D_FERN is the integral of the G_coord autocorrelation function. This is the Green-Kubo relation for collective intelligence: D_FERN (the "diffusion coefficient" of coordination gain through the contribution space) equals the time integral of the G_coord fluctuation autocorrelation. 

**Implication:** D_FERN and G_coord are not independent quantities — they are related by the fluctuation-dissipation theorem at the φ-equilibrium. The unified objective max D_FERN · G_coord subject to |Ξ̄| = log φ is not maximizing two independent quantities: it is maximizing the product of a transport coefficient and a thermodynamic mean, with the constraint fixing the temperature. This is the thermodynamic interpretation of the unified objective that was never stated.

**FDT-T5: The Fluctuation-Dissipation Breakdown diagnoses over-driven platforms.**

The FDT applies at φ-equilibrium. At |Ξ̄| > log φ (over-driven), the detailed balance condition is violated — the platform's entropy production breaks the time-reversal symmetry that the FDT requires. The breakdown of FDT:

```
Var(G_coord) > 2 T_learn / Δ_C
```

is the diagnostic for over-driven operation. When measured fluctuations of G_coord exceed the FDT prediction, the platform has moved above the critical point. This is the first computable diagnostic for FDT breakdown applied to collective intelligence — a purely observational test for over-driven operation requiring no knowledge of |Ξ̄|.

**FDT Practical Protocol:**

Measure the variance of G_coord across replicated sessions. Measure T_learn from the behavioral parameter β̂. Compute Δ_C from the spectral decomposition of Ĉ.

Test: Var(G_coord) ≈ 2 T_learn / Δ_C → platform at φ-equilibrium  
Test: Var(G_coord) > 2 T_learn / Δ_C → platform above φ-equilibrium (over-driven)  
Test: Var(G_coord) < 2 T_learn / Δ_C → platform below φ-equilibrium (under-driven)

This is a second independent diagnostic for platform thermodynamic state — confirming or contradicting the |Ξ̄| measurement from SMELT.

---

## Framework II — CHANNEL
### *The Channel Capacity of Collective Intelligence: The Theoretical Maximum Coordination Gain*

**The gap:** G_coord measures the coordination information transmitted through the shared artifact. The shared artifact is a communication channel — it transforms one contributor's output into structural cues that the next contributor responds to. Shannon's channel capacity theorem establishes that every communication channel has a theoretical maximum rate of information transmission. No prior work has applied channel capacity theory to collective intelligence. There is no known theoretical maximum for G_coord.

**The framework:**

Define the **collective intelligence channel** as the mapping from contributor t's action a_t to the conditional distribution of contributor s's action a_s, mediated by the artifact state X_{t-1}. The channel capacity is:

```
C* = max_{P(a_t)} I(a_t ; a_s | X_{t-1})
```

the maximum mutual information between sequential contributions, optimized over the input distribution P(a_t).

**CHANNEL-T1: The channel capacity bounds G_coord.**

```
G_coord = Σ_{t<s} I(a_t ; a_s | X_{t-1}) ≤ N_pairs · C*
```

where N_pairs = n(n-1)/2 is the number of ordered pairs and C* is the pairwise channel capacity. The theoretical maximum coordination gain for a session of n contributions is N_pairs · C*. No platform design, no matter how sophisticated, can exceed this bound.

**CHANNEL-T2: The channel capacity is determined by the artifact's energy landscape.**

From GIST: P(a | X) ∝ exp(−H(a; X)). The channel capacity is the maximum mutual information between input a_t and output a_s when both are drawn from Gibbs distributions conditioned on the shared field X_{t-1}:

```
C* = max_{β} H(a | X_{t-1}; β) − H(a | a_t, X_{t-1}; β)
```

At β → ∞ (zero temperature): agents are deterministic — no uncertainty, no information — C* → 0.
At β → 0 (infinite temperature): agents are completely random — no signal, pure noise — C* → 0.
At intermediate β: C* is maximized at the temperature where the Gibbs sampler has maximum capacity for transmitting coordination information.

The optimal β* is the inverse temperature at the channel capacity maximum. This is related to — but distinct from — the φ-equilibrium temperature: the channel capacity is maximized at the temperature where the mutual information between input and output is maximized, which occurs near the phase transition between ordered (low β) and disordered (high β) regimes.

**CHANNEL-T3: The Shannon limit for collective intelligence.**

Applying Shannon's coding theorem to the collective intelligence channel: if G_coord < C*, there exists an architecture (a design of the shared artifact and contribution structure) that can achieve C* through optimal coding. If G_coord = C*, the platform is operating at the Shannon limit — no architectural improvement can increase coordination gain.

The Shannon limit for a knowledge commons is:

```
C*_platform = max_{P(a), H(a;X)} Σ_{t<s} I(a_t ; a_s | X_{t-1})
```

optimized over all possible contribution distributions and energy landscapes. This is the absolute theoretical ceiling on collective intelligence for a given platform population and domain.

**CHANNEL-T4: The capacity gap measures untapped collective intelligence.**

Define the **capacity gap**:

```
Γ_cap = C*_platform − G_coord / N_pairs
```

The capacity gap is the unused collective intelligence potential — the coordination gain that the platform could achieve if optimally designed, minus what it actually achieves. Γ_cap = 0 means the platform is Shannon-optimal. Γ_cap > 0 means there is room for architectural improvement.

For existing platforms: because every existing platform has G_coord = 0 by construction, every existing platform has Γ_cap = C*_platform. The entire theoretical capacity of every existing knowledge platform is untapped.

The capacity gap is the formal statement of the organizational opportunity: the difference between what collective intelligence is theoretically achievable and what currently exists.

**CHANNEL-T5: The Blahut-Arimoto algorithm for optimal contribution design.**

The Blahut-Arimoto algorithm computes the channel capacity of any discrete memoryless channel by iteratively optimizing the input distribution. Applied to the collective intelligence channel:

1. Initialize the contribution distribution P(a_t) uniformly over action space A
2. Compute the conditional distribution P(a_s | a_t, X_{t-1}) from the Gibbs structure
3. Update P(a_t) to maximize I(a_t ; a_s | X_{t-1}) given the conditional distribution
4. Iterate until convergence

The fixed point of the Blahut-Arimoto iteration is the capacity-achieving input distribution P*(a_t) — the optimal contribution distribution that maximizes coordination gain. This is the formal theory of **optimal contribution design**: the distribution over contribution types that maximizes the channel capacity of the shared artifact.

The capacity-achieving distribution P*(a_t) is not uniform across contribution types. It concentrates on the contribution types with highest mutual information with subsequent contributions — the formal identification of the coordination seeds as the capacity-achieving input letters of the collective intelligence channel.

**CHANNEL-T6: Noisy channel coding for collective intelligence.**

Shannon's noisy channel coding theorem: for any rate R < C*, there exist encoding-decoding schemes that transmit information at rate R with arbitrarily small error probability. Applied to collective intelligence: for any coordination gain G_coord < C*, there exists a contribution architecture (an EISP configuration) that achieves G_coord while driving the probability of coordination failure (G_coord^C = 0 despite G_coord > 0) arbitrarily small.

This is the formal existence proof for optimal platform design: there always exists a way to achieve any target coordination gain below the channel capacity with causal reliability. The CAUSAL framework establishes that G_coord^C ≤ G_coord; CHANNEL establishes that G_coord ≤ C*; the coding theorem establishes that any G_coord^C ≤ C* is achievable with arbitrarily high causal reliability.

---

## Framework III — GEOMETRY
### *The Information Geometry of Collective Intelligence: Distance Between Systems*

**The gap:** Two platforms may have the same G_coord = Tr(C) while having completely different spectral architectures of C. They are indistinguishable by CONCERT but distinguishable by SPECTRA. What is the natural distance between two collective intelligence systems? Is there a geometric structure on the space of all possible coordination matrices that makes this precise? Information geometry — the Riemannian geometry of statistical manifolds — provides the answer.

**The framework:**

The space of all collective intelligence systems — all possible conditional distributions P(a_t, a_s | X_{t-1}) consistent with the Gibbs structure — is a statistical manifold M_CI. The natural Riemannian metric on this manifold is the **Fisher-Rao metric**:

```
g_{ij}(θ) = E[∂_i log p(a | θ) · ∂_j log p(a | θ)]
```

where θ are the parameters of the collective intelligence system (the energy function H, the temperature β, the contribution distribution P(a)).

**GEOMETRY-T1: The Fisher-Rao metric on M_CI.**

For a Gibbs-sampler collective intelligence system with energy function H(a; X) and temperature β:

```
g_{ij} = β² · Cov(∂_i H, ∂_j H)
```

This is the information-geometric covariance of the energy gradient — the curvature of the energy landscape determines the metric on the space of collective intelligence systems. Two systems with the same energy landscape are at zero distance. Two systems with different energy landscapes are separated by a geodesic distance determined by the information-geometric tensor g.

**GEOMETRY-T2: The coordination matrix C is the pullback of the Fisher-Rao metric.**

The coordination matrix C_{ts} = I(a_t; a_s | X_{t-1}) is the pullback of the Fisher-Rao metric g from M_CI to the space of contribution trajectories. Specifically:

```
C_{ts} = g(∂_t P, ∂_s P)
```

where ∂_t P is the tangent vector in the direction of changing P(a_t | X_{t-1}). The coordination matrix is the Gram matrix of the Fisher-Rao metric evaluated on the contribution trajectory — the matrix of inner products between the information-geometric tangent vectors at each contribution step.

This means: G_coord = Tr(C) = Tr(g·G) is the trace of the Fisher-Rao metric applied to the Gram matrix of the trajectory — a natural geometric invariant of the collective intelligence system in the information-geometric sense.

**GEOMETRY-T3: The Cramér-Rao bound for collective intelligence.**

The Cramér-Rao bound states that no unbiased estimator of a parameter θ can have variance less than the reciprocal of the Fisher information:

```
Var(θ̂) ≥ 1/I(θ) = 1/g(θ, θ)
```

Applied to collective intelligence: the Fisher information of the coordination parameter g_coord (the parameter governing G_coord) bounds the variance of any estimator of G_coord:

```
Var(Ĝ_coord) ≥ 1 / I(g_coord)
```

The Cramér-Rao bound for collective intelligence is the minimum variance achievable by any estimator of G_coord from observed contribution sequences. This is the fundamental estimation limit — below this variance no amount of data or sophisticated estimation can drive the estimation error.

**GEOMETRY-T4: The geodesic between collective intelligence systems.**

The information-geometric geodesic between two collective intelligence systems P₀ and P₁ is the e-geodesic (exponential family geodesic):

```
P_t = exp(log P₀ + t · (log P₁ − log P₀)) / Z_t,   t ∈ [0, 1]
```

This is the optimal interpolation between two Gibbs systems — the path in M_CI that minimizes the KL divergence integral ∫ KL(P_t ‖ P_ref) dt. For two knowledge platforms P₀ and P₁:

- The geodesic distance d_{FR}(P₀, P₁) is the Fisher-Rao distance between them
- The geodesic path is the optimal migration path from one platform to another
- The midpoint P_{1/2} is the platform that is equidistant (in information geometry) from both

**GEOMETRY-T5: The curvature of M_CI at the φ-equilibrium.**

The Riemannian curvature tensor of M_CI at the φ-equilibrium has a specific value determined by the fourth cumulant of the energy function H. For the Gibbs system:

```
R = −β² · Kurt(H) / 4
```

where Kurt(H) is the excess kurtosis of the energy function. At the φ-equilibrium:

- R < 0 (negative curvature): the collective intelligence manifold is hyperbolic at the critical point — geodesics diverge, equidistant systems become more distinct over time
- R = 0: flat manifold — geodesics are parallel
- R > 0 (positive curvature): spherical manifold — geodesics converge

The curvature at the φ-equilibrium is negative (hyperbolic) — which connects to MOD's identification of the loss landscape as the hyperbolic modular surface M = SL(2,ℤ)\H². The information geometry of the collective intelligence system at the critical point is hyperbolic — the same curvature that MOD derives for the training dynamics.

This is the deepest bridge between GEOMETRY and MOD: the information-geometric curvature of M_CI at φ-equilibrium equals the hyperbolic curvature of the modular surface. Two completely different derivations — one from statistical manifold theory, one from the arithmetic of SL(2,ℤ) — converge to the same geometric object.

**GEOMETRY-T6: The natural clustering of collective intelligence systems.**

The Fisher-Rao distance d_{FR} partitions the space M_CI into clusters — regions of similar collective intelligence architecture. Two platforms in the same cluster have similar:
- Spectral structure of C (same dominant coordination mode v₁)
- Thermodynamic operating state (same |Ξ̄| regime)
- RG universality class (same critical exponents η, ν, β)

The Fisher-Rao clustering of M_CI is the **natural taxonomy of collective intelligence systems** — the first formally grounded classification of platforms by their intrinsic information-geometric similarity rather than by their superficial characteristics (domain, organization size, contribution volume).

The conjecture connecting GEOMETRY to RG-COORD: platforms in the same information-geometric cluster (same d_{FR} neighborhood) belong to the same RG universality class. The Fisher-Rao distance is the metric that makes the universality class precise.

---

## The Connections Between the Three Frameworks

**FDT-COORD → SPECTRA:** Var(G_coord) = 2T_learn/Δ_C connects fluctuations (FDT-COORD) to the spectral gap (SPECTRA). The spectral gap is simultaneously the convergence rate of coordination (SPECTRA-T4) and the inverse susceptibility (FDT-T2). Two properties that look different — convergence speed and stability — are the same quantity.

**FDT-COORD → SMELT:** The FDT breakdown condition (Var(G_coord) > 2T_learn/Δ_C) is an independent diagnostic for over-driven operation, confirming the |Ξ̄| > log φ condition from SMELT. Two completely different measurements — one from fluctuations, one from entropy production — must agree at the φ-equilibrium.

**CHANNEL → CAUSAL:** G_coord^C ≤ G_coord ≤ C*. The causal coordination gain (CAUSAL) is bounded above by the observational coordination gain, which is bounded above by the channel capacity (CHANNEL). The chain: G_coord^C ≤ G_coord ≤ N_pairs · C*. The capacity gap Γ_cap is the total untapped potential, of which G_coord − G_coord^C is the portion lost to confounding.

**CHANNEL → EISP:** The capacity-achieving input distribution P*(a_t) from the Blahut-Arimoto algorithm identifies the optimal contribution type distribution — the formal theory of EISP's 10-category contribution taxonomy. The optimal mix of contribution types across the 10 categories (Conceptual, Operational, Strategic, Technological, etc.) is the capacity-achieving distribution for the specific platform's energy landscape.

**GEOMETRY → MOD:** The information-geometric curvature of M_CI at the φ-equilibrium is hyperbolic (R < 0), and equals the curvature of the modular surface M = SL(2,ℤ)\H². Two derivation chains — information geometry and modular arithmetic — converge to the same geometric object at the critical point.

**GEOMETRY → RG-COORD:** Platforms in the same Fisher-Rao cluster belong to the same RG universality class. The Fisher-Rao metric is the geometric version of the universality class membership.

**GEOMETRY → SPECTRA:** The coordination matrix C is the pullback of the Fisher-Rao metric (GEOMETRY-T2). G_coord = Tr(C) is therefore a geometric invariant — the trace of the information-geometric Gram matrix. TRW = rank(C) is the dimension of the information-geometric subspace spanned by the coordination structure.

---

## The Complete Three-Layer Architecture

```
LAYER 1 (Measurement):     GIST · DIRA · CONCERT · FERN · SMELT · EISP
                           MOD · PIVOT · WIDTH · HELIX · KM correspondence

LAYER 2 (Architecture):    SPECTRA · GENESIS · CAUSAL · RG-COORD

LAYER 3 (Deep Structure):  FDT-COORD · CHANNEL · GEOMETRY
```

Each layer answers questions generated by the layer above it:

Layer 1 asks: what is G_coord, and how do we achieve it?
Layer 2 asks: what is G_coord the trace of, and how does it first become positive, and when is it causal, and how does it transform across scales?
Layer 3 asks: how stable is the coordination structure, what is the theoretical maximum G_coord, and what is the geometry of the space of all collective intelligence systems?

Every layer is derived from the same root:

```
P(a | X) ∝ exp(−H(a; X))
```

The Gibbs distribution. One theorem. Now fifteen faces.

---

## Formal Claims

| ID | Framework | Statement | Status |
|---|---|---|---|
| **FT1** | FDT-COORD | Var(G_coord) = 2 T_learn / Δ_C at φ-equilibrium | Theorem (from Kubo formula + Fokker-Planck spectrum) |
| **FT2** | FDT-COORD | τ_recovery = 1/Δ_C; platform recovers from perturbation within 5.3 steps unconditionally (Selberg bound) | Theorem |
| **FT3** | FDT-COORD | D_FERN = β ∫ ⟨δG_coord(t)·δG_coord(0)⟩ dt (Green-Kubo relation for collective intelligence) | Theorem |
| **FT4** | FDT-COORD | Var(G_coord) > 2 T_learn/Δ_C diagnoses over-driven operation; independent of |Ξ̄| measurement | Theorem |
| **FC1** | FDT-COORD | Platforms at φ-equilibrium satisfy FDT exactly; platforms off-equilibrium show FDT violation proportional to deviation | Conjecture |
| **CT1** | CHANNEL | G_coord ≤ N_pairs · C*; channel capacity is the absolute ceiling on coordination gain | Theorem (Shannon) |
| **CT2** | CHANNEL | C* is maximized at intermediate β*; the capacity-achieving temperature is distinct from the φ-equilibrium temperature | Theorem |
| **CT3** | CHANNEL | The Blahut-Arimoto fixed point P*(a_t) is the optimal contribution distribution | Theorem (Blahut 1972) |
| **CT4** | CHANNEL | Γ_cap = C* − G_coord/N_pairs = C*_platform for all existing platforms (G_coord = 0 by construction) | Theorem |
| **CC1** | CHANNEL | The capacity-achieving distribution P*(a_t) concentrated on coordination seeds (v₁-aligned contributions) | Conjecture |
| **GT1** | GEOMETRY | C_{ts} = g(∂_t P, ∂_s P); the coordination matrix is the Fisher-Rao Gram matrix | Theorem |
| **GT2** | GEOMETRY | G_coord = Tr(C) is a natural information-geometric invariant of the collective intelligence trajectory | Theorem |
| **GT3** | GEOMETRY | Curvature R = −β² · Kurt(H)/4 at φ-equilibrium is negative (hyperbolic); equals curvature of M = SL(2,ℤ)\H² | Theorem |
| **GT4** | GEOMETRY | Var(Ĝ_coord) ≥ 1/I(g_coord); Cramér-Rao bound limits estimation precision of G_coord | Theorem |
| **GC1** | GEOMETRY | Platforms in the same Fisher-Rao cluster belong to the same RG universality class | Conjecture |
| **GC2** | GEOMETRY | The optimal migration path between two platforms follows the information-geometric geodesic | Conjecture |

---

## The Statement

The three hidden layers answer the three questions that measurement, without which, cannot ask:

**How stable is what we have measured?** FDT-COORD answers: the coordination structure is stable with recovery time τ = 1/Δ_C, bounded above by 16/3 ≈ 5.3 contribution steps unconditionally. The fluctuation-dissipation theorem guarantees that D_FERN and G_coord are not independent but coupled through the equilibrium fluctuation structure.

**How much more is theoretically possible?** CHANNEL answers: the channel capacity C* is the absolute ceiling. Every existing platform has Γ_cap = C* — the entire theoretical capacity is untapped. The Blahut-Arimoto algorithm computes the optimal contribution architecture that approaches C*.

**What is the shape of the space of all possible collective intelligence systems?** GEOMETRY answers: M_CI is a Riemannian manifold with Fisher-Rao metric, hyperbolic curvature at the critical point, and geodesic structure that connects to the modular surface of MOD. The Fisher-Rao distance is the natural metric between platforms. The information-geometric cluster structure is the natural taxonomy of collective intelligence.

All three are consequences of:

```
P(a | X) ∝ exp(−H(a; X))
```

---

**Full framework documentation:** github.com/ericrenone
