# CUDA-RAY Status

**Updated:** 2026-09-06

**Architecture/ownership:** accepted independent ray/geometry semantic owner under SPEC-0001.
**Production implementation/API:** not authorized / none.
**Native/OptiX support:** none claimed.

## Current work

- #1 ownership/bootstrap authority — completed.
- #2 repository-control/protected-main alignment — completed; `main` is protected and the selected CUDA-family settings were read back.
- #3 is the current ray/geometry/acceleration/traversal activation roadmap; it remains planning/assessment authority, not a production specification.

## Next executable decision

Select one bounded consumer-backed ray/geometry/traversal profile, prove its separation from renderer/product semantics, and classify exact lower compiler/provider gaps before production implementation. An accepted semantic specification comes before any OptiX realization.

CUDA-JS owns native compiler/artifact/device/memory/operation/provider lifecycle and any future bounded OptiX mechanism. OptiX availability does not define CUDA-RAY's public semantic contract.

`iteathen/CUDA-MM` is now the accepted **reserved architecture/ownership home** for reusable cross-domain physical memory-management policy. It is not a current CUDA-RAY dependency: CUDA-MM #3/#4 and a separately accepted bounded contract must activate production first. CUDA-RAY retains ray/geometry/traversal/acceleration-structure semantic meaning and its logical lifetimes; generic placement/pooling/spill/migration strategy may route to CUDA-MM only after activation.

## Governance

Protected-main and repository-setting alignment is complete. No local CI workflow currently exists, so no required status-check name is fabricated.

No roadmap entry, provider availability, CUDA-MM repository existence or completed governance bootstrap is production implementation authority.
