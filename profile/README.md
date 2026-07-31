# Zhivex

Build provider-agnostic AI applications and durable agents in TypeScript and
Python.

[![TypeScript SDK](https://img.shields.io/npm/v/%40zhivex-ai%2Fsdk?label=TypeScript%20SDK)](https://www.npmjs.com/package/@zhivex-ai/sdk)
[![Python SDK](https://img.shields.io/pypi/v/zhivex-ai-sdk?label=Python%20SDK)](https://pypi.org/project/zhivex-ai-sdk/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/Zhivex/zhivex-ai-sdk/blob/main/LICENSE)

Zhivex provides a common contract for text generation, streaming, structured
output, tools, multimodal input, routing, observability, and long-running agent
workflows. Applications can keep one orchestration layer while selecting the
provider that best fits each workload.

## Start here

| Runtime | Recommended entry point | Install | Documentation |
| --- | --- | --- | --- |
| TypeScript | [`@zhivex-ai/sdk`](https://www.npmjs.com/package/@zhivex-ai/sdk) | `bun add @zhivex-ai/sdk @zhivex-ai/openai` | [Quickstart](https://github.com/Zhivex/zhivex-ai-sdk/blob/main/docs/QUICKSTART.md) |
| Python | [`zhivex-ai-sdk`](https://pypi.org/project/zhivex-ai-sdk/) | `pip install zhivex-ai-sdk` | [Quickstart](https://github.com/Zhivex/zhivex-ai-sdk-py/blob/main/docs/QUICKSTART.md) |

### TypeScript

```ts
import { generateText } from "@zhivex-ai/sdk";
import { createOpenAI } from "@zhivex-ai/openai";

const openai = createOpenAI({ apiKey: process.env.OPENAI_API_KEY });
const result = await generateText({
  model: openai("gpt-4o-mini"),
  prompt: "Explain provider-agnostic AI in one sentence."
});

console.log(result.text);
```

### Python

```python
import asyncio
from zhivex_ai import create_openai, generate_text


async def main() -> None:
    openai = create_openai()
    result = await generate_text(
        model=openai("gpt-4o-mini"),
        prompt="Explain provider-agnostic AI in one sentence.",
    )
    print(result.text)


asyncio.run(main())
```

## What you can build

- Multi-provider AI services with a normalized application contract
- Tool-using and durable agents with sessions, approvals, replay, and traces
- Structured-output and multimodal workflows
- Provider routing, retries, budgets, and fallback policies
- Streaming APIs and chat experiences for TypeScript, React, and Python
- Local or hosted deployments with OpenAI, Anthropic, Gemini, Vertex, Qwen,
  Kimi, DeepSeek, Bedrock, OpenRouter, Ollama, vLLM, and other adapters

## Projects

- [Zhivex AI SDK for TypeScript](https://github.com/Zhivex/zhivex-ai-sdk)
- [Zhivex AI SDK for Python](https://github.com/Zhivex/zhivex-ai-sdk-py)
- [TypeScript packages on npm](https://www.npmjs.com/org/zhivex-ai)
- [Python package on PyPI](https://pypi.org/project/zhivex-ai-sdk/)

## Project health

- [TypeScript stability and support](https://github.com/Zhivex/zhivex-ai-sdk/blob/main/STABILITY.md)
- [Python stability and support](https://github.com/Zhivex/zhivex-ai-sdk-py/blob/main/STABILITY.md)
- [TypeScript security policy](https://github.com/Zhivex/zhivex-ai-sdk/security/policy)
- [Python security policy](https://github.com/Zhivex/zhivex-ai-sdk-py/security/policy)
- [TypeScript issues](https://github.com/Zhivex/zhivex-ai-sdk/issues)
- [Python issues](https://github.com/Zhivex/zhivex-ai-sdk-py/issues)
