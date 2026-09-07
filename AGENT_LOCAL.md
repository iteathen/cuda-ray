# Repository context: cuda-ray

Universal engineering and design guidance comes from the account-global `AGENTS.md`.

## Mission and ownership

CUDA-RAY owns reusable ray/geometry/traversal semantics when accepted: ray/query and geometry/instance meaning, logical acceleration-structure ownership/build/update, traversal/intersection/hit/miss roles, finite ray-pipeline composition, semantic resource planning, and ray-specific conformance.

CUDA-JS owns CUDA/provider/compiler/resource mechanisms. Renderer/window/material/product semantics, generic Tensor math, media semantics, and NN policy remain with their natural owners.

## Local routing

Accepted `docs/decisions/`, `docs/specs/`, repository status/roadmap, and current issues own local implementation/activation truth.

## Local constraints

Maintained code uses JavaScript/ESM plus accepted Device-JS through public lower contracts; no Python, direct native/OptiX/FFI escape path, hand PTX, or private lower imports.