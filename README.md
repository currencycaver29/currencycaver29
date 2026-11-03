# Divij Karanam

I build and measure systems where AI meets real-world limits: slow networks, small devices and languages that tokenizers were not built for. My work covers mobile ML, distributed training, IoT networking and NLP for Indian languages.

> Building the model is the easy part.
> The interesting part is measuring what happens when it meets real networks, real devices and real users.

[Research papers](#research) · [Current experiments](#current-experiments)

## Current experiments

**NaturaLens** · *wildlife recognition*
Point your phone at an animal, and NaturaLens names the species and keeps a log of what you've found. React Native app, Next.js web and a species data pipeline built on GBIF and IUCN, moving from cloud identification toward on-device inference.

[Low-communication training](https://doi.org/10.5281/zenodo.23889666) · *distributed ML over bad networks*
Training a language model across emulated regions linked by slow, lossy internet. Hierarchical aggregation with INT8 compression cut network time by 109–379× compared with standard data-parallel training.

## Research

[The Token Tax on Indian Languages](https://doi.org/10.5281/zenodo.23885241) · *NLP*
How many more tokens the 22 scheduled Indian languages need than English, across 14 tokenizers including GPT-4o, Llama 4, Gemma 3 and Sarvam-1.

[MQTT, CoAP and HTTP Under Constrained Networks](https://doi.org/10.5281/zenodo.23885253) · *IoT networking*
A reproducible benchmark of the three main IoT protocols under emulated 4G, 3G, 2G and lossy links, with JSON and CBOR payloads.

[Does Low-Communication Training Survive Bad Networks?](https://doi.org/10.5281/zenodo.23889666) · *distributed ML*
DDP vs DiLoCo vs hierarchical aggregation, measured over real TCP through a packet-level WAN emulator.

## Systems projects

[bounded-mpmc-queue](https://github.com/currencycaver29/bounded-mpmc-queue) · *Rust, lock-free*
A bounded multi-producer multi-consumer queue on a lock-free ring buffer with atomic sequence numbers.

[mini-agent-orchestrator](https://github.com/currencycaver29/mini-agent-orchestrator) · *Python, FastAPI*
An event-driven order-processing agent with hand-rolled core logic and no LangChain.

[polygon-id-auth](https://github.com/currencycaver29/polygon-id-auth) · *zero-knowledge identity*
A working identity authentication flow built on the Polygon ID JS SDK.
