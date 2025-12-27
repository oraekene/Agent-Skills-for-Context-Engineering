# Book SFT Pipeline

A complete example for training small language models to write in any author's style using supervised fine-tuning. Part of the [Agent Skills for Context Engineering](../../README.md) collection.

## Overview

This example demonstrates an end-to-end agent system for:
- Extracting and segmenting text from books (ePub format)
- Generating diverse synthetic instructions for SFT
- Training LoRA adapters on Tinker
- Validating style transfer with modern scenarios

## Skills Applied

This example integrates multiple context engineering skills:

| Skill | Application |
|-------|-------------|
| [project-development](../../skills/project-development/) | Staged pipeline architecture (acquire, prepare, process, parse, render) |
| [context-compression](../../skills/context-compression/) | Two-tier segmentation strategy for optimal chunk density |
| [multi-agent-patterns](../../skills/multi-agent-patterns/) | Orchestrator + specialized agents pattern |
| [evaluation](../../skills/evaluation/) | Modern scenario testing, originality verification |
| [context-fundamentals](../../skills/context-fundamentals/) | Prompt diversity prevents attention collapse |

## Structure

```
book-sft-pipeline/
├── README.md                 # This file
├── SKILL.md                  # Main skill documentation
├── examples/
│   └── gertrude-stein/       # Real training example with outputs
├── scripts/
│   └── pipeline_example.py   # Conceptual implementation
└── references/
    ├── segmentation-strategies.md
    ├── tinker-format.md
    └── tinker.txt
```

## Quick Start

1. Read `SKILL.md` for the complete methodology
2. Review `examples/gertrude-stein/` for a real implementation
3. Adapt `scripts/pipeline_example.py` for your use case

## Key Results

Trained Qwen3-8B-Base on Gertrude Stein's "Three Lives" (1909):

| Metric | Value |
|--------|-------|
| Training examples | 592 |
| Loss reduction | 97% |
| Pangram AI detector | 70% Human |
| Training time | 15 minutes |
| Total cost | $2 |

## Why This Matters for Context Engineering

While this example focuses on fine-tuning rather than inference-time context, the principles transfer:

1. **Segmentation is compression**: Breaking long content into coherent chunks is the same problem as managing long context windows
2. **Information density**: Smaller, high-signal chunks outperform larger, diluted ones
3. **Prompt diversity**: Prevents attention from collapsing onto surface patterns
4. **Staged pipelines**: Idempotent phases enable debugging and optimization

## License

MIT

