# CUDA-RAY Project Charter

**Status:** Accepted architecture after bootstrap integration; production implementation not authorized.

## Purpose

Own reusable provider-neutral ray, geometry, acceleration-structure and traversal semantics without turning CUDA-JS into a ray framework or absorbing renderer/product meaning.

## Owns, when separately accepted

- ray/query and geometry primitive/instance semantics;
- logical acceleration-structure build/update/ownership meaning;
- traversal/intersection/hit/miss/callable-program roles;
- finite ray-pipeline composition and semantic resource planning;
- provider-neutral equivalence and ray-specific conformance.

## Does not own

CUDA device/context/memory/launch/provider lifecycle; raw OptiX handles/ABI/compiler resources; renderer/window/swapchain/material/product semantics; generic Tensor math; media/NN policy.

## Provider boundary

CUDA-JS owns bounded native/provider/compiler mechanisms selected for OptiX/CUDA realization. CUDA-RAY maps reusable ray semantics over those public mechanisms. The semantic model must not depend on arbitrary provider objects.

## Dependency direction

Base dependency is `cuda-ray -> public cuda-js`; optional semantic composition remains profile-selected.

## Activation gate

Issue #3 must select a bounded provider-neutral ray profile and lower-layer gap disposition before source/API implementation.

## Non-goals

Renderer/game engine, arbitrary OptiX passthrough, material framework, or RT-hardware-driven public API design.