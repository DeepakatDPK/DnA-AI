# Model Recommendations (Single and Multi-Model + MCP)

Date: 2026-04-03

## Goal

Build an AI system with:
- High-end code generation
- Strong reasoning and calculation
- Vision understanding
- Better performance through MCP tools

## Best Single-Model Recommendation

- Primary: `qwen3-vl:30b` (via Ollama)

Why:
- Strong multimodal capability (text + image)
- Good coding and reasoning quality
- Long-context support
- Good fit for MCP tool-driven workflows

Fallback for lower hardware:
- `qwen3-vl:8b`

## Best Multi-Model Recommendation

- Vision + general intelligence: `qwen3-vl:30b`
- Code specialist: `qwen3-coder:30b`
- Deep reasoning/calculation: `deepseek-r1-distill-qwen-32b`
- Reviewer/second opinion: `nemotron-cascade-2-30b-a3b`
- Fast router: `lfm2.5-1.2b-thinking`

## MCP for Performance

MCP improves capability and reliability by giving models exact tools and context.

Recommended MCP servers/tools:
- Calculator / Sympy (exact math)
- Python execution (verification)
- File system/codebase search
- Browser/search for external references
- Vector retrieval (RAG memory)

## Important Note on Current Local Models

Your current local set is mostly text-focused. For robust vision tasks, add a strong VLM such as Qwen3-VL.

## Sources

- Ollama library (Qwen3-VL): https://ollama.com/library/qwen3-vl
- Ollama library (Qwen3-Coder): https://ollama.com/library/qwen3-coder
- Qwen3-Coder HF card: https://huggingface.co/Qwen/Qwen3-Coder-30B-A3B-Instruct
- Qwen3-VL-30B-A3B HF card: https://huggingface.co/Qwen/Qwen3-VL-30B-A3B-Instruct-FP8
- DeepSeek-R1-Distill-Qwen-32B HF card: https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-32B
- Nemotron-Cascade-2-30B-A3B HF card: https://huggingface.co/nvidia/Nemotron-Cascade-2-30B-A3B
- MCP docs: https://modelcontextprotocol.io/docs/getting-started/intro
