# Fast Learner - Lightning-Fast Learning Skill

> Let AI conduct deep research for you, turning learning into a structured dialogue

[![GitHub stars](https://img.shields.io/github/stars/your-repo/fast-learner)](https://github.com/weiambt/fast-learner)
[![Version](https://img.shields.io/badge/version-1.0.0-blue)]()

[English](./README.md) | [中文](./README_zh.md)

## Philosophy

**Spend the least time, grasp the most essential knowledge.**

Fast Learner believes that efficient learning is not about cramming information, but rather a closed loop of "Research → Understand → Internalize → Verify". Through the AI medium, learning becomes a structured dialogue: first let AI complete deep research, then find your real points of confusion through interactive Q&A, and finally achieve true internalization through active recall.

## Core Principles

### Three Fundamental Principles

| Principle | Description |
|-----------|-------------|
| **Precise, Not Redundant** | Only present the most essential content, no textbook reading |
| **Understanding Drives Memory** | Build frameworks and connections first, memory second |
| **Teaching Promotes Learning** | Test input through output, solidify understanding through questioning |

### Four Learning Stages

```
    ╭─────────────────────────────────────────────────────────────╮
    │                    Fast Learner Learning Loop               │
    ╰─────────────────────────────────────────────────────────────╯

                          ┌──────────┐
                          │ AI Research│
                          └────┬─────┘
                               │
                               ▼
                          ┌──────────┐     ┌──────────┐
                          │ Interactive│ ──▶│ Assessment│
                          │   Q&A     │     │   Test   │
                          └────┬─────┘     └────┬─────┘
                               │               │
                               ▼               ▼
                          ┌──────────┐     ┌──────────┐
                          │ Generate │ ◀──│ Learning │
                          │  Notes   │     │  Results │
                          └──────────┘     └──────────┘

    ※ Loop explanation: After assessment, notes can be generated; notes can also trigger new follow-up questions
```

## Design Highlights

### 1. Progressive Understanding
Don't require users to figure out all their questions at once. Let AI complete the research first, then users ask questions progressively in the dialogue to find their real points of confusion.

### 2. Multi-Dimensional Answer Structure
Automatically adapt the answer framework based on the type of question:
- **Conceptual Understanding** → What/Why/ProsCons/Scenarios/Future
- **Tool Usage** → What/How/Examples/Caveats
- **Troubleshooting** → Symptoms/Causes/Diagnosis/Solutions
- **Comparison & Choice** → A vs B/Scenarios/Recommendation

### 3. Socratic Questioning
Provide concise answers first, then wait for user follow-ups. Guide deep understanding through layered questioning, truly understanding rather than superficially memorizing.

### 4. Learning Technique Integration
Integrate efficient learning methods into answers:

**Memory Techniques**
- Mnemonics, associations, flashcard reviews

**Understanding Techniques**
- Analogies to everyday life, drawing architecture diagrams

**Application Techniques**
- Run demos first, then investigate deeply; practice in small steps

**Engineering-Level Methods**
- First Principles — Return to the most essential definitions
- Feynman Technique — Explain complex concepts in simple language
- Structured Thinking — MECE principle for classification
- Deliberate Practice — Focus on weak areas
- Output-Driven — Learn by teaching

## Installation

### Method 1: For Claude Code / Copilot CLI

Copy the skill to the `~/.claude/skills/` directory:

```bash
# Clone or copy the skill to the skills directory
git clone https://github.com/weiambt/fast-learner
cp -r /path/to/fast-learner ~/.claude/skills/fast-learner

# Restart Claude Code / Copilot CLI, the skill will be automatically discovered
```

### Method 2: For Other Platforms

Copy the skill to the platform's skills directory (please refer to the corresponding platform's documentation).

### Verify Installation

After successful installation, you can verify it in the following ways:
- Say "Learn XXX" in conversation to trigger the skill
- Say "/fast-learner" to check if the skill loads properly

## Quick Start

### Trigger Methods

| Trigger | Action |
|---------|--------|
| "Learn XXX" | Start researching topic XXX |
| "Summarize" | Generate learning notes |
| "Create Questions" | Generate assessment questions |
| "Test" | Start assessment and verification |
| "Append" | Append content to notes |
| "Correct" | Correct note content |
| "Export" | Export and convert note format |

### Typical Usage Flow

```
User: I want to learn Go concurrency programming
AI: [Step 1] Researching...
    [Step 2] Complete, prepared the following:
    - Core concepts: Goroutine, Channel
    - Applicable scenarios: IO-bound, high concurrency
    - Best practices: Avoid leaks, use select

User: What's the difference between Goroutine and threads?
AI: Lightweight execution units vs OS native threads...
     (Concise answer, waiting for follow-up)

User: Why do we need Channel?
AI: [Socratic] What do you think is the problem with direct shared memory?
     (Guide deep understanding through questioning)

User: Summarize
AI: [Generate structured notes to ~/fast-learner/]

User: Create questions
AI: [Generate 3 multiple choice + 2 short answer questions]
User: [Answer]
AI: [Scoring + Analysis + Suggestions]
```

## Working Directory

Default working directory: `~/fast-learner/`

On first use, you will be asked to confirm, and you can specify a custom path.

```
~/fast-learner/
├── 2024-01-15-Go-Concurrency-Notes.md
├── 2024-01-16-Python-Coroutines-Notes.md
└── ...
```

## File Structure

```
fast-learner/
├── SKILL.md              # Main skill file
├── README.md             # English version
├── README_zh.md          # Chinese version
└── references/
    └── note-template.md  # Note generation template
```

## Design Philosophy Extension

### Why Do We Need a Learning Assistant?

We identified three major pain points in technical learning:

1. **Information Overload** — Too much material, don't know what's important
2. **Fragmented Understanding** — Understand the words but can't form a systematic understanding
3. **Unlasting Memory** — Learn and forget, can't retain long-term

Fast Learner addresses these three problems specifically through the closed loop of "AI Research + Structured Notes + Assessment Verification".

### Comparison with Traditional Learning Methods

| Dimension | Traditional Method | Fast Learner |
|-----------|-------------------|--------------|
| Research Phase | Self-search, time-consuming and incomplete | AI 4-step systematic research, core coverage in 5 minutes |
| Understanding Process | One-way input, passive reception | Interactive Q&A, active thinking |
| Note Organization | Manual organization, inconsistent structure | Template-driven, unified structure |
| Effect Verification | None or inefficient self-testing | Active recall-style assessment |

### Applicable Scenarios

- Technical interview preparation
- Quick start for new technologies
- Knowledge system organization
- Team internal training materials
- Personal knowledge management

## Changelog

### v1.0.0 (2024-01)
- Initial release
- Support for AI research, interactive Q&A, note generation, and assessment verification

## Contributing

Issues and Pull Requests are welcome!

## License

MIT License
