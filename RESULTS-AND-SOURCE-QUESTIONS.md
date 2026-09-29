# What the checked solidarity model establishes

The model separates three ingredients that are often conflated: how far a network reaches, which groups a person belongs to, and whether cooperating pays. Its useful result is an explicit demonstration that these can vary independently, together with an exact incentive threshold in a specified two-player game.

## Result-to-question map

These questions were posed in this project. No named historical open problem has been established as solved by this package. The source of each exact claim is the linked Lean definition and theorem, rather than an empirical paper that states the conclusion as an open conjecture.

| Project question | Checked answer and exact source | Meaning and assumptions |
|---|---|---|
| Can a bound on direct contacts force a bound on total connected population? | No: `path_connected`, `at_most_two_neighbors`, `unbounded_reachable`. | The natural-number path has at most two neighbors at each vertex and arbitrarily distant reachable vertices. This is an elementary graph construction. Reachability does not assert human coordination capacity. |
| Can local and larger memberships coexist, including overlapping identities? | `membership_nesting`, `overlapping_memberships`. | Inclusion is transitive; explicit sets have shared and distinct members within one population. These are elementary set facts supporting a representation choice. |
| Does connectedness entail trust? | `connected_without_trust`. | A connected graph can be paired with an empty independent trust relation. A coupling assumption would be needed to infer trust from edges. |
| Exactly when is mutual contribution stable in the declared donation game? | `cooperation_stable_iff`: cost is at most sanction. | Payoff is the benefit received from the other player minus one's own contribution cost or defection sanction. Stability means no unilateral deviation improves payoff against a contributing other player. Enforcement is reliable and exogenous. |
| Is demographic uniformity logically necessary or sufficient in this model? | `heterogeneous_cooperation_exists`, `homogeneous_cooperation_can_fail`. | Explicit different-label stable and same-label unstable examples. Labels do not enter the payoff function; this is a consequence of that declared model, not an empirical finding about demographic diversity. |
| Can shared symbols alone guarantee cooperation here? | `symbols_alone_insufficient`. | A common marker coexists with an unstable contribution profile when sanctions are absent. Markers are independent of payoffs. |
| When does mutual contribution improve on mutual defection? | `mutual_gain`. | The exact supplied sufficient inequality is cost < benefit + sanction. This welfare comparison is distinct from unilateral stability. |

The other declarations (`adj_symm`, `reach_trans`, `reach_symm`, `zero_reaches`, and `no_sanction_failure`) support these results. There are **16 theorem declarations**, including supporting lemmas, and **11 printed axiom reports**. Neither count is a count of new discoveries or solved external open problems.

## Evidence

The exact source was checked with Lean 4.19.0 and its bundled standard library, with no Mathlib dependency. [Hosted verification run 36365007772](https://github.com/Sodelin/Mathematics-of-Psychology-Formalized/actions/runs/36365007772) passed at source commit `841419eea726383da96e105b3b995910b80f2ed0`. Its log reports a successful build and the eleven requested axiom reports. The reports use either no axioms or the standard `propext` and `Quot.sound`. The workflow rejects proof placeholders and custom axiom declarations.

This publication update preserves the Lean source unchanged. The accompanying JSON records its byte hash. The formal statements establish consequences of the definitions; empirical interpretation and political recommendations require separate evidence.

## Reconciled publication coverage

The remembered 67-item package has now been located in the canonical broader repository, [Formalizing Soft Sciences](https://github.com/Sodelin/Formalizing-Soft-Sciences). It consists of these same 16 solidarity declarations plus 51 foundations declarations. Its main now also contains 18 checked declarations for a published CBT-model fragment, giving 85 in total. The [complete source-question map](https://github.com/Sodelin/Formalizing-Soft-Sciences/blob/7835157/PUBLICATION-COVERAGE-2026-09-29.md) explains each family and points to individual theorem inventories.

This repository preserves the earlier psychology checkpoint. Its 16 declarations are not additional to the 85 in the broader repository. The historical reference to a distinct earlier psychology corpus remains separate from the now-recovered 67-item package.
