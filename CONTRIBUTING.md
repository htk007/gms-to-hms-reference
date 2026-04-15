# Contributing

This repository is maintained to a high editorial standard. Contributions that add noise, speculation, or unverified claims will be rejected without negotiation.

---

## What We Accept

| Type | Criteria |
|------|----------|
| New service mapping | Must cover a GMS service not yet documented. Must include a technically precise gotcha, verified effort estimate, and valid Huawei docs link. |
| Correction to existing mapping | Must cite an official source (Huawei docs, Android docs, or a verifiable production incident). |
| New roadmap item | Must be a real GMS service with a plausible HMS counterpart. |
| Tooling / automation | Discussed in an issue before implementation. |

---

## PR Requirements

Every pull request must satisfy **all** of the following before review begins:

1. **One concern per PR.** Do not bundle unrelated service mappings or mix content edits with formatting fixes.
2. **Technically precise gotcha.** The "Gotcha / Key Difference" field must describe an architectural or behavioral difference at the API/SDK level — not a general observation. Vague statements ("works differently") will be rejected.
3. **Verified effort estimate.** Justify your `Easy / Medium / Hard` rating in the PR description with a brief rationale (e.g., surface-area of API change, backend involvement, credential/console requirements).
4. **Source link.** Include at least one link to official Huawei documentation or a credible primary source supporting your claim.
5. **No marketing language.** Descriptions must be neutral and precise. Phrases like "seamlessly," "powerful," or "easy to use" will be edited or the PR will be rejected.
6. **Consistent format.** Follow the exact template used in existing `docs/` files. Do not alter heading levels, bullet keys, or file naming conventions.

---

## Review Process

- All PRs require **at least one approval** from a maintainer.
- Maintainers may request changes up to **two rounds**. If unresolved after two rounds, the PR is closed.
- PRs that have been inactive for **14 days** after a change request are closed automatically.

---

## Scope Boundaries

This repository maps **API/SDK equivalence only**. The following are explicitly out of scope:

- AppGallery Connect console tutorials
- General Android development advice not specific to GMS/HMS migration
- Huawei-only features with no GMS analogue
- Device compatibility matrices

Open an issue to discuss anything that falls outside these boundaries before investing time in a PR.

---

## Code of Conduct

All contributors are expected to engage professionally. Technical disagreements are resolved by citing authoritative sources, not by debate volume.
