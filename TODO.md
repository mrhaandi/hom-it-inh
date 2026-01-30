0\. Use LMCS style



1\. Expanded Proof Details in Section 3 (~1.5 pages)

The proofs in Section 3 are currently sketched. For a journal version, these can be expanded:



a) Full proof of Lemma 4 (lem:ring2) - Lines 553-569



Currently: "Induction on the size of M and case analysis of the normal form"

Expansion: Provide the full case analysis showing how the β-equivalence constraints force M to have the specific structure from Definition 9. This would include:

Base case: showing when M must equal z₁

Inductive case: showing when M must have form (rᵢ pⱼ M') or (rᵢ (λw.pⱼ w) M')

Explain why typing constraints eliminate other possibilities

b) Full proof of Lemma 5 (lem:ring1) - Lines 577-593



Similar expansion showing the inductive structure for terms in ℛₘ

Show explicitly how z₀ and z★ cases are distinguished

c) Detailed proof sketch for Theorem 6 (thm:shape) - Lines 597-614



Currently very brief; expand to show the connection between the substitutions S\_F, S\_H and the structural constraints

2\. Additional Examples (~0.75 pages)

a) Negative instance example:

Add an example of a simple semi-Thue system where the 0⁺ ⇒\* 1⁺ problem has no solution. For instance:



ℜ = {00 ⇒ 22, 01 ⇒ 10, 21 ⇒ 12}



Show why no 0ⁿ can reach 1ⁿ and how this manifests as the matching instance having no solution.



b) Full trace through Example 15 (xmp:H):



Currently the example shows β-equivalences but doesn't trace through the computation

Add step-by-step β-reduction showing how the constraints are satisfied

This would help readers understand the semantic intuition

c) Worked example of type computation:



Show explicitly how σ\_ℜ and τ\_ℜ are computed for a concrete ℜ

Include the full term F\_ℜ expanded for a 3-rule system

3\. Expanded Section 4 (Mechanization) (~0.75 pages)

a) Statistics and metrics:



Breakdown of ~4000 lines: how many for each component?

Number of lemmas/theorems

Proof automation usage (auto, lia tactics mentioned in conclusion)

b) De Bruijn representation discussion:



More detail on how the unscoped de Bruijn approach (line 867) affects the development

How substitution lemmas are handled

Any challenges with variable binding in the mechanization

c) Comparison with other library mechanizations:



Compare proof complexity with the intersection type inhabitation reduction

Reference to related undecidability mechanizations in the library

d) Code excerpts:



Add a code listing showing the definition of ring1 and ring2 predicates (currently only described textually)

Show the main reduction statement in Coq

4\. Expanded Section 5 (Uniform Approach) (~0.75 pages)

This section is currently quite brief and could be significantly expanded:



a) Intersection type definitions:



Add formal definition of intersection types (currently assumed known)

Define the inhabitation problem precisely

b) Elaborate on Remark 14 (rem:G):



Explain the finite model interpretation more carefully

Show how the partial function tables correspond to intersection type structure

Add the explicit intersection type T\_ℜ for a small example system

c) Sketch the direction (1) ⇔ (4) for λ-definability:



Currently stated as following from Remark 14

Give more details on how ℱ\_ℜ is constructed

Reference the Salvati et al. correspondence more explicitly

5\. Extended Related Work and Comparison (~0.5 pages)

a) Detailed comparison with Loader's proof:



What specific "intricate machinery" (line 168) does Loader use?

How does the type order compare?

What aspects are harder to verify mechanically?

b) Comparison with Joly's refinement:



Explain "shifting technical burden to λ-definability" (lines 398-400)

Why is the present approach more direct?

c) Discussion of decidable fragments:



More detail on Padovani's order-4 decidability result

What changes at order 5?

6\. Technical Supplements (~0.25 pages)

a) Strong normalization and confluence:



Add explicit theorem statements for simply typed terms

Reference the mechanization in the library

b) Order definition and calculation:



Provide a formal definition of type order (currently only informal at line 979)

Calculate the order for the types in the construction

