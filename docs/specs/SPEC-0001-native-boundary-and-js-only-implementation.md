# SPEC-0001: Native Boundary and JavaScript/TypeScript Implementation

**Status:** Accepted architecture/ownership authority; production ray profiles remain separately gated.

**Version:** 1.0.0

**Owner:** CUDA-RAY

**Lower authority:** `iteathen/CUDA-JS` SPEC-0032

## Purpose

CUDA-RAY owns reusable provider-neutral ray/geometry/traversal semantics. CUDA-JS is the sole native CUDA/provider integration owner.

## Repository implementation rule

Maintained CUDA-RAY source is JavaScript/TypeScript. Restricted Device-JS generation is permitted only through public CUDA-JS contracts.

CUDA-RAY does not maintain C, C++, CUDA C++, PTX, direct native FFI, native addons, OptiX/provider bindings, native handles/pointers, ABI structs or platform discovery code. Native evidence may be produced externally and recorded, but native oracle/provider source is not maintained here.

A missing native mechanism routes to CUDA-JS before any local workaround.

## CUDA-RAY owns

- ray, geometry, primitive, acceleration-structure and traversal meaning where provider-neutral;
- intersection/hit/miss and ray-query semantics;
- ray-specific material/liveness/resource policy;
- provider eligibility/equivalence/fallback at the ray semantic boundary;
- JavaScript/TypeScript reference and conformance evidence.

## CUDA-JS owns

- native allocations/views/transfers/device/context resources;
- compiler/artifact/operation/synchronization mechanisms;
- OptiX or other native provider resources if selected;
- graphics/external-memory interop mechanisms;
- native provider handles, errors and teardown.

Rendering/window/display/product semantics do not enter CUDA-RAY merely because ray results are visualized.

## Memory-policy boundary

Ray-specific acceleration-structure or traversal lifetime meaning remains CUDA-RAY-owned. Generic cross-domain allocation pooling, physical placement, reuse, migration or spill strategy requires its own JavaScript/TypeScript owner if independently justified and must consume public CUDA-JS.

## Activation gate preservation

This specification does not select a ray representation, traversal algorithm, provider or production API.

## Non-goals

No native ray backend, no renderer, no arbitrary OptiX passthrough, no generic memory manager, no production capability or support claim.
