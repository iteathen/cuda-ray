# CUDA-RAY Agent Entry Point

Read before changing the repository. Authority: owner instruction -> this file -> accepted ADRs -> accepted specs -> charter -> status/roadmap/issues.

Use `assess -> research -> reassess -> plan -> execute -> qualify -> review -> cleanup/document` and `LEGO -> SOLID -> CUPID -> KISS`.

LEGO is the outer architecture rule: ownership, universality, replaceability, scope containment, damage-limiting encapsulation, and context containment. A LEGO is too large when one agent cannot hold its complete authoritative working set—contract, implementation, invariants, lifecycle/resource/failure rules, tests/conformance, and immediate dependency/consumer interfaces—in focused attention with substantial headroom for reasoning and review. Context fit is a first-class boundary criterion alongside semantic, lifecycle, resource/failure, substitution, and change cohesion. When exceeded, recursively split at the strongest real seam or narrow scope; do not create arbitrary modules that duplicate truth or require cross-boundary internal knowledge. Inside a valid LEGO, SOLID structures responsibilities and dependency direction, CUPID shapes the implementation, and KISS removes remaining unjustified complexity; lower levels may not defeat higher ones.

CUDA-RAY owns reusable ray/geometry/traversal semantics when separately accepted: ray/query and geometry/instance meaning, logical acceleration-structure ownership/build/update, traversal/intersection/hit/miss roles, finite ray pipeline composition, semantic resource planning and ray-specific conformance.

CUDA-RAY does not own CUDA device/context/memory/launch/provider lifecycle, raw OptiX handles/ABI, renderer/window/swapchain/material/product semantics, generic Tensor math, media semantics or NN policy.

CUDA-JS owns any bounded native OptiX/provider/compiler/resource mechanisms selected later. CUDA-RAY owns reusable provider-neutral ray semantics above them. Provider availability is not public semantic authority.

Direct native/FFI/CUDA C++/PTX/private imports or duplicated provider lifecycle are lower-layer gap signals. Maintained code, when authorized, is JavaScript/ESM plus accepted restricted Device-JS through public lower contracts; no Python/native escape path without a successor decision.

Repository creation authorizes no production source/API. #3 is the activation roadmap; #2 owns repository controls. Accepted bounded specs are required before implementation.

Completion requires exact-effect review, qualification, cleanup and honest support/performance claims.