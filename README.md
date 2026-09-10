<div align="center">

  <a href="https://github.com/sindresorhus/awesome">
    <img width="260" src="https://raw.githubusercontent.com/sindresorhus/awesome/main/media/logo.png" alt="Awesome Logo">
  </a>

  <h1>Awesome Self-Hosted AI Gateways</h1>

  <p>
    A curated list of awesome self-hosted LLM gateways, API routers, load balancers, fallback systems, and proxy engines for production AI applications.
  </p>

  <p>
    <a href="https://github.com/sindresorhus/awesome">
      <img src="https://raw.githubusercontent.com/sindresorhus/awesome/refs/heads/main/media/badge.svg" alt="Awesome Badge">
    </a>
  </p>

</div>

---

Managing multiple AI models, handling rate limits, optimizing costs, and ensuring high availability requires robust self-hosted routing infrastructure. This list collects open-source and self-hostable solutions designed to sit between your application and AI providers (OpenAI, Anthropic, Google Gemini, DeepSeek, Groq, local models, etc.).

---

## Contents

- [Self-Hosted Gateways](#self-hosted-gateways)
- [Key Features Matrix](#key-features-matrix)
- [Contributing](#contributing)

---

## Self-Hosted Gateways

Core open-source and self-hostable projects providing proxying, token management, rate limiting, and model fallback.

| Project | Lang | Demo | Commercial / Billing | Smart Fallback | Load Balancing | Dynamic Mapping | Description |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **[better-new-api](https://github.com/Neighboth/better-new-api)** ![Recommended](https://img.shields.io/badge/-Recommended-brightgreen) ![Beta](https://img.shields.io/badge/-Beta-blue) | Go | [https://pixrouter.com](Demo) | ✅ | ✅ | ✅ | ✅ | Polished and enhanced fork of New-API with active bug fixes, performance improvements, and extended channel stability. |
| **[New API](https://github.com/QuantumNous/new-api)** | Go | - | ✅ | ✅ | ✅ | ✅ | Enhanced One-API fork built for commercial/sales operations and enterprise token management. |
| **[LiteLLM](https://github.com/BerriAI/litellm)** | Python | - | ❌ | ✅ | ✅ | ✅ | Call 100+ LLM APIs using the OpenAI format with virtual key management and budget tracking. |
| **[One-API](https://github.com/songquanpeng/one-api)** | Go | - | ✅ | ✅ | ✅ | ✅ | OpenAI API management & routing platform for aggregating multiple providers into a unified endpoint. |
| **[9router](https://github.com/decolua/9router)** | TypeScript | - | ❌ | ✅ | ✅ | ✅ | Open-source unified AI API gateway and model router with key distribution. |
| **[LMRouter](https://github.com/LMRouter/lmrouter)** | Go | - | ❌ | ✅ | ✅ | ✅ | High-performance, lightweight LLM routing proxy focused on low-overhead execution. |
| **[Bifrost](https://github.com/maximhq/bifrost)** | Go | - | ❌ | ✅ | ✅ | ✅ | High-performance, open-source AI gateway with a unified OpenAI-compatible API, multi-provider routing, automatic failover, load balancing, and governance controls. |
| **[Portkey Gateway](https://github.com/Portkey-AI/gateway)** | TypeScript | - | ❌ | ✅ | ✅ | ✅ | Fast AI Gateway for routing to 250+ LLMs with 1 API, retries, and semantic caching. |
| **[RouteLLM](https://github.com/lm-sys/RouteLLM)** | Python | - | ❌ | ✅ | ❌ | ✅ | Framework for serving and routing LLMs dynamically based on prompt complexity and cost optimization. |

---

## Key Features Matrix

When evaluating or selecting a self-hosted AI gateway for production environments, consider the following key capabilities:

* **Smart Fallback & Retry:** Automatically switch to backup models or providers when a request times out, hits rate limits (429), or encounters 5xx server errors.
* **System Prompt & Parameter Rewriting:** Modify requests on the fly (e.g., inject custom fallback headers or default system prompts).
* **Load Balancing:** Distribute traffic across multiple API keys or upstream endpoints using Round Robin, Weighted, or Latency-based strategies.
* **Token & Cost Management:** Track per-user, per-token, or per-channel expenditure in real time with billing/top-up integrations.
* **Dynamic Model Mapping:** Map custom model alias names (e.g. `gpt-4o-custom`) to specific upstream provider endpoints transparently.

---

## Contributing

Contributions are welcome! Please read the guidelines before submitting a pull request:

1. Search existing entries to avoid duplicates.
2. Ensure project links are active and directly relevant to self-hosted AI routing/gateways.
3. Follow the table formatting above and keep descriptions concise, factual, and neutral.

---

*Maintained with ❤️ by the open-source community.*
