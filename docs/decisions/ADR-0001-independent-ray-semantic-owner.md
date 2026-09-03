# ADR-0001: Independent Ray/Geometry Semantic Owner

**Status:** Accepted
**Date:** 2026-09-02

## Context

OptiX and RT hardware provide an accelerated ray-tracing realization, but ray/geometry/acceleration/traversal meaning is a reusable domain distinct from generic CUDA runtime mechanics and from renderer/material/product policy.

## Decision

`cuda-ray` owns reusable provider-neutral ray semantics. CUDA-JS retains native/provider/compiler/resource mechanisms. Renderer/media/NN/product meaning stays with natural owners.

## Deletion test

Deleting any renderer/product/provider leaves CUDA-RAY coherent; deleting CUDA-RAY leaves CUDA-JS coherent as a generic runtime.

## Implementation gate

Issue #3 selects a bounded semantic profile and classifies lower-layer provider/compiler gaps before any production source/API. OptiX is a realization candidate, not semantic authority.

## Consequences

Ray semantics gain one durable owner without making CUDA-JS a rendering framework or coupling the API to one vendor pipeline.