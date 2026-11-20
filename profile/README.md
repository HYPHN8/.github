# HYPHN8

**Applied AI systems & workflow engineering studio building open-source Apple Silicon infrastructure.**

We build practical local-first AI workflows and native Apple Silicon primitives designed to run cleanly on unified memory without heavy container or sidecar stacks.

---

### Open-Source Repositories

| Repository | Description | Stack |
|---|---|---|
| [**`metal-agent-bus`**](https://github.com/HYPHN8/metal-agent-bus) | Zero-copy unified-memory multi-agent semantic bus, hybrid retrieval engine (`fp32` / `fp16` / `int8`), and KV-prefix-affinity router. | Swift 6 · Metal (runtime MSL) |

### Engineering Principles

- **Unified-memory native:** Share `MTLBuffer` `.storageModeShared` memory directly between Swift actors and Metal compute shaders—no IPC copies or vector-database sidecars.
- **Model-agnostic infrastructure:** Sit cleanly above MLX, `llama.cpp`, Ollama, or hosted APIs without locking into a single inference engine.
- **Zero-friction builds:** Runtime-compiled Metal Shading Language (`MTLDevice.makeLibrary(source:)`) so packages build and test directly with SwiftPM and Command Line Tools.
- **Measured over claimed:** Every kernel ships with CPU-vs-Metal numerical parity tests and reproducible Apple Silicon benchmarks.

---

[hyphn8.ai](https://hyphn8.ai) · [rodrigo@hyphn8.ai](mailto:rodrigo@hyphn8.ai)
