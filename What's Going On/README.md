## 📱 What's Going On - Omnichannel News Synthesis & Media Generation Automation Pipeline

An advanced, multi-tiered AI automation workflow built on Make.com that intercepts real-time incoming report streams via Telegram, verifies context against live data sources using a custom dynamic Cloudflare Worker, and orchestrates simultaneous multimedia publication across multiple major social platforms.

![What's Going On Workflow](/What's%20Going%20On/What's-Going-On-Make.png)

---

### 🚀 Workflow Architecture & Pipeline Breakdown

The architecture split-routes into two primary engine blocks based on the incoming operational stream payload types:

#### 1. Real-Time Broadcaster & Verification Engine (Upper Fork)
* **Ingress Point:** Monitored Telegram Channel Webhook intercept.
* **Context Verification Data Store:** Matches information trends against historical operational states.
* **Live Verification Worker API:** Queries a dynamic, stop-word filtering Cloudflare Worker that dynamically cross-references global news layers (via `NewsAPI.org` and `Currents API`) to contextually build high-credibility source frames without hardcoded data flags.
* **Multi-Platform Router:** Once synthesized, an asymmetric distribution layer concurrently fires out optimized text, links, and updates to **Blogger**, **Facebook Pages**, **Instagram Feed**, **Instagram Reels**, **LinkedIn Professional Network**, and fallback monitoring **Telegram Groups**.

#### 2. Advanced Vision & Video Orchestration Pipeline (Lower Fork)
* **Gemma Synthesis Matrix:** Triggers a structured Cloudflare Workers inference step utilizing `@cf/google/gemma-4-26b-a4b-it` to parse, filter, and output strict, syntax-escaped JSON content objects to eliminate breaking quote properties.
* **High-Fidelity Imagery Generation:** Passes the sanitised text blocks into a specialized Cloudflare Worker executing **FLUX.2 [klein] 9B** via a memory-isolated multipart `FormData` serialization stream to natively yield crisp 1024x1024 vertical imagery arrays.
* **FFmpeg Video Generation Microservice:** Passes the unique public URL of the freshly generated FLUX.2 image along with custom text properties to a local **FastAPI + FFmpeg Linux cluster**. The service:
  * Generates high-accuracy text-to-speech audio with dynamic word boundaries.
  * Compiles a customized SRT subtitle overlay positioned dynamically in the lower-third safe zone (`MarginV=280`, `Fontsize=42`).
  * Applies automated acoustic volume ducking parameters against looping background tracks.
* **Storage & Terminal Feedback:** Saves production files temporarily to an `ImgBB` cloud asset array, tracks indexing IDs inside a central Data Store, and updates control channels via a localized **Telegram Notification Bot**.

---

### 🛠️ Core Technology Matrix
* **Orchestration Platform:** Make.com (Advanced Router & Conditional Filter Modules)
* **Serverless Compute Layers:** Cloudflare Workers (V8 Runtime) & Workers KV Store
* **Generative AI Engines:** `@cf/google/gemma-4-26b-a4b-it` (Text Synthesis) & `@cf/black-forest-labs/flux-2-klein-9b` (Image Infrastructure)
* **Media Render Stack:** FastAPI (Python 3) + Edge TTS Engine + FFmpeg Filters Complex