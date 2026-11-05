# divij karanam

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

### [bounded-mpmc-queue](https://github.com/currencycaver29/bounded-mpmc-queue) · *Rust, lock-free concurrency*
A bounded multi-producer, multi-consumer queue that lets many threads pass data to each other without a lock.
- Ring buffer in the style of the LMAX Disruptor: each slot carries an atomic sequence number, so threads claim slots with compare-and-swap instead of a mutex.
- Acquire/Release memory ordering on the slot sequences, `unsafe` limited to `UnsafeCell` and `MaybeUninit`, and a `Drop` that cleans up items still in the queue.
- No dependencies. A stress test checks the count and checksum of every item under heavy contention, and a benchmark measures throughput with 1 to 16 threads on each side at three capacities.

### [Reliable recording pipeline](https://github.com/currencycaver29/Swades-AI-Hackathon) · *TypeScript, Next.js, Hono, PostgreSQL*
A browser recorder that doesn't lose audio, even if the tab closes or the network drops mid-upload. Built at a hackathon.
- Each chunk is saved to the browser's private file system (OPFS) before any upload, and deleted only after both the storage bucket and the database confirm it.
- Every chunk carries a SHA-256 checksum. Failed uploads retry with exponential backoff and jitter, and each failure is logged for auditing.
- A reconciliation step finds chunks the database acknowledged but the bucket lost, and re-sends them from OPFS. Recordings are then transcribed with Whisper or Google Cloud Speech, with automatic language detection.

### [mini-agent-orchestrator](https://github.com/currencycaver29/mini-agent-orchestrator) · *Python, FastAPI, OpenAI*
An AI agent that turns a plain-English request like "cancel order #9921 and email me the confirmation" into a plan and carries it out. Written from scratch, without LangChain.
- A planner turns the request into a small task graph (which step depends on which) using OpenAI, and falls back to a rule-based parser when there's no API key or the call fails.
- An orchestrator runs the steps in order, skips any step whose dependency failed (no confirmation email for an order that wasn't cancelled) and rejects unknown tools.
- Typed Pydantic models end to end, timing for every step, a REST API and a small web UI.
