# Agentic coding doesn't kill your QA tools — it needs them more than ever

AI coding agents are changing how we write software. But if you're bootstrapping a greenfield web project with agents, there's something important to get right early: your existing QA tooling still matters — arguably more than before.

## 🧪 Unit testing

Agents make mistakes. That's just the reality today. But what's remarkable is how well they can course correct — _when given the right feedback._

When an agent writes code and then runs the test suite, it sees the CLI output. It can identify what broke and fix it, often without any human intervention. This makes executable tests one of the most powerful tools in an agentic workflow — not just as a safety net for you, but as an active feedback loop for the agent itself.

Practical tip: When starting a greenfield project, one of the first things you should do is make sure your agent can effortlessly run tests in the project environment. Set that up early.

## 🔍 Linting

Why spend tokens on a large language model to catch something like an unused variable or a function that was accidentally called without being awaited, when a deterministic algorithm can do it instantly and for free?

Linters are a far more efficient way to handle these low-level issues. Let the LLM focus on what it's actually good at — and let the linter handle the rest.

Practical tip: Set up your linter early and make sure the agent can run it and review the results. Better yet — include your linter config file as default context for the agent. That way, it's generating code that already targets compliance from the start, rather than fixing violations after the fact.

## ✨ Formatting

Formatters make all files look the same. That might sound trivial, but in a professional codebase, consistency removes the surprise element — and surprise when reading code is rarely a good thing.

Modern LLMs can output code in a reasonably consistent style. But running a formatter on top seals the deal. A deterministic algorithm guarantees conformance in a way that probabilistic output simply can't.

## The bigger picture

The pattern across all three is the same: set your agent up with the right feedback loops from day one. Tests, linters, and formatters aren't relics of a pre-AI era — they're the scaffolding that makes agentic coding reliable, efficient, and professional.

The best agents don't replace good engineering practices. They depend on them.
