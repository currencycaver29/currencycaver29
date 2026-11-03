# Divij Karanam

I build and measure systems where AI meets real-world limits: slow networks, small devices and languages that tokenizers were not built for. My work covers distributed training, mobile ML, IoT networking and NLP for Indian languages.

> Building the model is the easy part.
> The interesting part is measuring what happens when it meets real networks, real devices and real users.

[Portfolio](https://currencycaver29.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/divjkarnm) · [Zenodo](https://zenodo.org/search?q=metadata.creators.person_or_org.name%3A%22Karanam%2C%20Divij%22) · [Research papers](#research)

## Experience

**Research Engineer** · VIRTKOM · *Sep 2026 – present · part-time, remote*
Research on large-scale LLM pre-training infrastructure for heterogeneous, distributed compute.

**App Developer** · NaturaLens · *Jul 2026 – present · remote*
Building a mobile app that identifies wildlife from a photo and keeps a log of what you've found. React Native app, Next.js web and a species database built from GBIF and IUCN data.

**Research Intern** · IIT Guwahati · *Jun – Jul 2025*
Worked under Dr. Anirban Dasgupta, Department of Electronics and Electrical Engineering, building research tools in Python and Tkinter.

**Open-source contributor** · [TensorFold](https://github.com/ashhart/TensorFold/pull/1988) · *Nov 2026*
Added Indian-script fixtures covering all 22 scheduled languages to TensorFold's tokenizer parity suite. Under review.

**B.Tech, Electronics & Communication Engineering** · IIT Guwahati · *2022 – 2026*

## Research

[The Token Tax on Indian Languages](https://doi.org/10.5281/zenodo.23885241) · *NLP* · [code](https://github.com/currencycaver29/indic-token-tax)
How many more tokens the 22 scheduled Indian languages need than English, across 14 tokenizers including GPT-4o, Llama 4, Gemma 3 and Sarvam-1.

[Does Low-Communication Training Survive Bad Networks?](https://doi.org/10.5281/zenodo.23889666) · *distributed ML* · [code](https://github.com/currencycaver29/lowcomm-training)
DDP vs DiLoCo vs hierarchical aggregation, measured over real TCP through a packet-level WAN emulator. Hierarchical aggregation with INT8 compression cut network time by 109–379×.

[MQTT, CoAP and HTTP Under Constrained Networks](https://doi.org/10.5281/zenodo.23885253) · *IoT networking* · [code](https://github.com/currencycaver29/iot-protocol-benchmark)
A reproducible benchmark of the three main IoT protocols under emulated 4G, 3G, 2G and lossy links, with JSON and CBOR payloads.

## Systems projects

[bounded-mpmc-queue](https://github.com/currencycaver29/bounded-mpmc-queue) · *Rust, lock-free*
A bounded multi-producer multi-consumer queue on a lock-free ring buffer with atomic sequence numbers.

[mini-agent-orchestrator](https://github.com/currencycaver29/mini-agent-orchestrator) · *Python, FastAPI*
An event-driven order-processing agent with hand-rolled core logic and no LangChain.

[polygon-id-auth](https://github.com/currencycaver29/polygon-id-auth) · *zero-knowledge identity*
A working identity authentication flow built on the Polygon ID JS SDK.
