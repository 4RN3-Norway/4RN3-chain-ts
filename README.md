# 4RN3-chain-ts

![Generated with AI assistance: Tailored for 4RN3-chain-ts](https://img.shields.io/badge/Generated_with_AI_assistance-Tailored_for_4RN3--chain--ts-red)
![language: TypeScript](https://img.shields.io/badge/language-TypeScript-blue)
![license: MIT](https://img.shields.io/badge/license-MIT-green)

**4RN3-chain-ts** is a modular, AI-powered full-stack development stack built on TypeScript. It leverages multiple state-of-the-art AI models, a flexible architecture, and lightweight developer ergonomics to provide a smart, OOP-friendly foundation for modern application and library development.

This repo defines the **stack itself** — including conventions, model roles, and technology pairings — not any specific app or plugin built on top of it.

---

## 🧠 Overview

**4RN3-chain-ts** combines the strengths of different AI models and modern dev tools to form a reasoning-first, shell-friendly TypeScript ecosystem:

| Purpose                     | Tooling |
|-----------------------------|---------|
| Prompt Routing / Orchestration | Lightweight Model (pref. [Llama 4 Maverick Instruct](https://fireworks.ai/models/fireworks/llama4-maverick-instruct-basic)) |
| Codegen (OOP/TS)            | Claude 3.7 Sonnet |
| Fast boilerplate            | GPT-4o |
| Reasoning/docs/plans        | o3 (or o4-mini) |
| Test generation             | GPT-4o |
| Bug fixing                  | Claude 3.7 Sonnet |
| UI (if applicable)          | Nuxt 3, Tauri (desktop) |
| DB (if applicable)          | Postgres |
| Runtime                     | TypeScript (pref. [Bun](https://bun.sh)) |

Each model in the stack is chosen for a specific role. This lets you build fast, well-structured applications using task decomposition, automated bugfixing, and domain-specific reasoning — all with minimal overhead.

---

## 🔄 Prompt Routing & Execution Chain

A lightweight instruction-following model (such as [LLaMA 4 Maverick Instruct](https://fireworks.ai/models/fireworks/llama4-maverick-instruct-basic)) is used to **analyze input prompts**, route tasks to appropriate models, and generate responses in a structured multi-stage chain.

Each stage receives the **original prompt** and **all prior stage outputs**, enabling iterative, context-aware development.

---

### 🧪 Example: Model-Orchestrated Prompt Flow

**Prompt:**
> Generate a maths library that saves previous actions to a database.
# 4RN3-chain-ts

![Generated with AI assistance: Tailored for 4RN3-chain-ts](https://img.shields.io/badge/Generated_with_AI_assistance-Tailored_for_4RN3--chain--ts-red)
![language: TypeScript](https://img.shields.io/badge/language-TypeScript-blue)
![license: MIT](https://img.shields.io/badge/license-MIT-green)

**4RN3-chain-ts** is a modular, AI-powered full-stack development stack built on TypeScript. It leverages multiple state-of-the-art AI models, a flexible architecture, and lightweight developer ergonomics to provide a smart, OOP-friendly foundation for modern application and library development.

This repo defines the **stack itself** — including conventions, model roles, and technology pairings — not any specific app or plugin built on top of it.

---

## 🧠 Overview

**4RN3-chain-ts** combines the strengths of different AI models and modern dev tools to form a reasoning-first, shell-friendly TypeScript ecosystem:

| Purpose                     | Tooling |
|-----------------------------|---------|
| Prompt Routing / Orchestration | Lightweight Model (pref. [Llama 4 Maverick Instruct](https://fireworks.ai/models/fireworks/llama4-maverick-instruct-basic)) |
| Codegen (OOP/TS)            | Claude 3.7 Sonnet |
| Fast boilerplate            | GPT-4o |
| Reasoning/docs/plans        | o3 (or o4-mini) |
| Test generation             | GPT-4o |
| Bug fixing                  | Claude 3.7 Sonnet |
| UI (if applicable)          | Nuxt 3, Tauri (desktop) |
| DB (if applicable)          | Postgres |
| Runtime                     | TypeScript (pref. [Bun](https://bun.sh)) |

Each model in the stack is chosen for a specific role. This lets you build fast, well-structured applications using task decomposition, automated bugfixing, and domain-specific reasoning — all with minimal overhead.

---

## 🔄 Prompt Routing & Execution Chain

A lightweight instruction-following model (such as [LLaMA 4 Maverick Instruct](https://fireworks.ai/models/fireworks/llama4-maverick-instruct-basic)) is used to **analyze input prompts**, route tasks to appropriate models, and generate responses in a structured multi-stage chain.

Each stage receives the **original prompt** and **all prior stage outputs**, enabling iterative, context-aware development.

---

### 🧪 Example: Model-Orchestrated Prompt Flow

**Prompt:**
> Generate a maths library that saves previous actions to a database.
```txt
[PROMPT]
Generate a maths library that saves previous actions to a database.

[PLAN]
Analyze the prompt and propose a multi-stage approach to fulfill it.
Response: I will create a TypeScript math utility module that logs operations to a PostgreSQL database using Bun. The stages will include type-safe operations, async logging, a query layer...

[PROTOTYPE]
Generate a rough prototype or high-level sketch of the system.
Response: We'll define a class-based interface, with methods like `add`, `subtract`, and a `Logger` service for persistence...

[CODEGEN]
Refine the prototype into structured, working TypeScript code.
Response: Code generation completed. The module includes `MathService`, `Logger`, and PostgreSQL integration...

[TESTGEN]
Test the code with multiple checks for exported functions.
Response: Created a test suite using Bun's test runner, including unit tests for all math methods and DB write checks...

[BUGFIX]
Fix this error:
TypeError: maths.add is not a function. (In 'maths.add(1, 1)', 'maths.add' is undefined)
Response: Issue was due to incorrect import/export. Updated the module to ensure named exports align with import syntax. Suggest rerunning tests...

[DOCGEN]
Produce documentation for the generated code (e.g., JSDoc, README).
Response: Generated API docs in markdown and inline JSDoc for all exported types and classes...
```
- Each stage receives the original prompt and previous results, allowing iterative refinement and contextual awareness.
- The prompt chain is stateless, designed to work with local files or shell orchestration.

This enables a declarative, AI-routed dev pipeline that mirrors conventional build chains — but entirely through prompt-driven stages.

---

## ✨ Features
- 🧩 AI-driven modular architecture with model-task mapping
- 🧠 Model-specialized logic: use the right AI for the right job (reasoning, codegen, boilerplate, etc.)
- 🔀 Prompt router layer using LLaMA or similar model to select the best AI for the job
- ⚙️ Shell-capable agent layer for testing, bugfixing, and orchestration
- 💻 Optional UI layer with Nuxt 3
- 🖥️ Optional Desktop UI support with Tauri 2
- 🗃️ Optional database support with PostgreSQL
- 🔋 TypeScript-native with focus on OOP and modularity
- 🪶 Lightweight by default, expandable via plugins, services, and tools

---

## 🛠️ Installation

To use or extend the stack, you’ll need:
- Bun (preferred): https://bun.sh
- Or Node.js + your TS toolchain of choice
- No memory or persistence layer required — everything is prompt-injected
- Note: this is the recommended stack — anything above can be replaced with your own use

---

## 🧪 Usage

This repo doesn’t define a single CLI or binary — instead, it outlines how to structure your stack or toolchain using:
- Claude for structured OOP code
- GPT-4o for fast generation (e.g., LICENSE, README, boilerplate)
- o3/o4 for deeper reasoning (e.g., planning, design docs, complex logic)

How you use the stack is up to you: it could power a CLI, be integrated into dev tools, run as a service, or support a full-stack app.

---

## 🧱 Philosophy
- Don’t generalize everything. Use models for what they’re best at.
- Stateless by default. You don’t need memory if you can prompt smartly.
- Modularity over framework. Compose small model tasks instead of monoliths.

---

## 📄 License

This project is licensed under the MIT License.

---

## 🚧 Status

Actively in development. This is the stack definition repo — actual plugins, apps, and helpers may live in separate repositories under the same namespace.
