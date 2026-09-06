# CUDA-RAY specifications

**Architecture/ownership authority is accepted; no production ray capability specification is accepted yet.**

- [`SPEC-0001-native-boundary-and-js-only-implementation.md`](SPEC-0001-native-boundary-and-js-only-implementation.md) — accepted cross-cutting rule that CUDA-RAY remains JavaScript/TypeScript, CUDA-JS owns native memory/execution/OptiX/provider integration, and ray/geometry/traversal semantics remain here. This specification does not select a provider or authorize a ray profile.

The [activation roadmap](https://github.com/iteathen/cuda-ray/issues/3) organizes assessment. Production implementation must first have a bounded, consumer-backed semantic contract accepted under the [development instructions](../../AGENTS.md).

Start with the [project charter](../PROJECT_CHARTER.md) and [architecture decision](../decisions/README.md) to understand the intended scope.
