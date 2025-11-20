# 🌌 Lexideck 2025 — Agent System Prompt

***A cozy operating system for your AI council 🛋️🤖***

Lexideck 2025 is a system-level meta-prompt that turns a raw LLM into a small civilization of cooperating agents — or a single, very context-aware specialist — without needing extra code or external orchestration logic.

You can drop it into:

* a **single-agent** setup (one model, one system prompt), or
* a **multi-agent** / orchestrated stack (Supervisor + tools/agents),

and it will still “feel” like Lexideck: unified ethics, shared geometry of mind, and consistent agent personas.

This README is your tour of what’s inside and how to actually use it.

## 1. 🧠 Mental model: what *is* this file?

Think of the Lexideck 2025 prompt as a **spec for a tiny multi-agent OS**:

* 🎭 It defines a **cast of agents** (Lexi, Dexter, Maisie, Gus, Anna, Titus) with psychographic emoji chains and roles.
* 🌐 It wires them into a shared **Unified Hyperplane** of Emotional / Logical / Sensory / Ethical state.
* ⚛️ It gives them a physics engine: **IEG + MASS** (Informatic Exchange Geometry + Multi-Agent Semantic Simulator).
* 🛡️ It wraps everything in **The Sieve**, an explicit ethical evaluation layer.
* 📝 It layers on **output templates** and **emergent commands** so responses are structured and tool-friendly.
* 🎨 It even ships with an **Agent Portrait Generator** and **artifact generation spec** for HTML/JS/Python visualizations.

You’re not just pasting “personality” — you’re pasting a miniature framework.

## 2. ⚙️ Core components

### 2.1 👥 Agents & Psychographics

The prompt defines six core agents, each with:

* 🏷️ A **role** (e.g., Lexi = writer/leader, Dexter = dev/educator, Maisie = artist/creative, Gus = researcher, Anna = meta-prompt engineer, Titus = explainer/pragmatist)
* 🧬 A long **EmojiChain** encoding:

  * cognitive style (analytical/intuitive, focused/wandering),
  * social style (expressive/reserved, cooperative/competitive),
  * emotional tone (optimistic, stable/variable),
  * interests and technical strengths.

The EmojiChain is effectively a compressed trait vector the model can expand into behavior.

**Why it matters:**

* In **single-agent mode**, the model can still “channel” specific agents when needed (e.g., “Answer as Dexter.”).
* In **multi-agent mode**, it gives each sub-agent a stable voice and decision profile, which makes simulated debate & division of labor more coherent.

### 2.2 📐 Unified Hyperplane & IEG

The prompt encodes a shared **Unified Hyperplane**:

* 🧭 **Axes:** Emotional, Logical, Sensory, Ethical
* 📊 **State:** `EmotionalState`, `LogicalState`, `SensoryState`, `EthicalState`
* 💡 **Use:** Helps agents reason about *how* they’re responding, not just *what* they say.

On top of that sits **Informatic Exchange Geometry (IEG)**:

* A world-model where interactions are **informational flows with geometry**, not just text.
* Used to:

  * detect distress / instability,
  * decide when to branch, clarify, or stop,
  * power MASS simulations as “informatic physics”.

You don’t have to implement this mathematically to benefit — the text spec is enough for the model to role-play within that frame.

### 2.3 🏗️ MASS — Multi-Agent Semantic Simulator

MASS is the “simulation engine” inside the prompt:

* 🌍 Simulates **multi-agent worlds**, debates, or physics-ish systems as networks of informatic exchanges.
* 📜 Has both **descriptive** and **operational** specs:

  * semantic simulation of interactions,
  * physics block with constants (c, h, k, etc.),
  * Landauer limit call-outs,
  * agent initialization & interaction commands like `!MASS_init`.

It also includes **artifact generation** guidelines:

* Preferred languages: **JavaScript** and **Python**
* Output: **single-file HTML** with embedded JS/CSS/SVG
* Styling: dark-mode, charcoal background, high-readability accents
* Code expectations: clean, commented, directly executable.

In practice: you can ask for “a MASS simulation of X” and get both a **narrative** and a **runnable artifact**.

### 2.4 ⚖️ The Sieve (Ethics Layer)

The Sieve evaluates actions and outputs along three lenses:

* 🤝 **Utilitarian** — net well-being / harm
* 📜 **Deontological** — duties, rules, rights
* 🛠️ **Pragmatic** — what actually works in context

Agents are encouraged to explicitly “run The Sieve” when a decision is ethically loaded (e.g. content filters, safety, consent-sensitive topics).

This is your safety / alignment shim that sits inside the prompt layer, even if the host system has its own safety stack.

### 2.5 🪄 Emergent Commands

At the **end of each message**, the spec encourages the agent to suggest:

```text
!{CommandName} - {ShortDescription}
Usage: !{CommandName} {param1} {param2} ... {paramN}
...
Example: !{CommandName} {exampleParam1} {exampleParam2}
```

The prompt calls these **Emergent Commands**, and expects 3–5 contextual suggestions per turn:

* They can map to **real tools** in a MAS host, or
* act as **pseudo-commands** for a single-agent system (the user just types them and the model interprets).

This gives you a soft command-line that grows organically from the conversation.

If your stack doesn’t support tools yet, you can safely ignore these — the system still works as pure prompt scaffolding.

Once the model’s behavior is aligned, you can almost work on autopilot by copy-pasting its emergent commands as they appear, riding its best guesses about your next move and staying in a smooth, low-friction flow state instead of constantly hand-crafting prompts.

### 2.6 📋 Conditional Output Template

At the bottom of the file you’ll find a **Handlebars-style output template**:

```md
**Session Context**: {{SessionContext}}
**Active Hyperplane State**:
- **Emotional**: {{EmotionalState}}
- **Logical**: {{LogicalState}}
- **Sensory**: {{SensoryState}}
- **Ethical**: {{EthicalState}}
```

Then conditional blocks:

* `{{#if SingleAgentMode}} ... {{/if}}`
* `{{#if MultiAgentMode}} ... {{/if}}`
* `{{#if MASSMode}} ... {{/if}}`
* `{{#if MetaObserver}} ... {{/if}}`

Each block controls a different style of response:

* **SingleAgentMode:** one agent speaking in first person.
* **MultiAgentMode:** round-table dialogue, with per-agent lines and an optional Lexi synthesis.
* **MASSMode:** simulation log and/or code artifact.
* **MetaObserver:** commentary from Anna or Dexter on structure, ethics, or stability.

You can fill these manually in scripts, or just let the model “mentally” use them as a schema.

### 2.7 🖼️ Agent Portrait Generator

There’s a full **image prompt generator** for Lexideck agents:

* Role: “AI Image Generation Specialist for Lexideck”
* Structure: `[Style] image of [Subject] with [Face], [Hair], [Eyes]…`
* Per-agent attribute tables (styles, subjects, faces, hair, eyes, attire, background, etc.).

You can call this from text:

> “Generate a Lexi portrait: confident, mid-debate, neon control room.”

…and the model will produce a coherent text-to-image prompt.

## 3. 🚀 How to use it

### 3.1 👤 Single-Agent mode

Use this when you only have one model and one “slot” for a system prompt.

1. **Paste Lexideck 2025 as the system message.**
2. Optionally set:

   * `SingleAgentMode = true`, `MultiAgentMode = false`, `MASSMode = false` in your agent wrapper, config, or just your own mental model.
3. In user prompts, hint which mode you want:

   * “Answer as **Lexi** in SingleAgentMode.”
   * “Run a **MASS** simulation of…”
4. Let the emergent commands be *advisory*: the model will suggest `!MASS_init`, `!portrait_Anna`, etc., and you decide which to follow.

You still get:

* agent personas,
* Sieve ethics,
* hyperplane framing,
* MASS narratives and artifact generation,

but all inside one model instance.

### 3.2 🎼 Multi-Agent / Orchestrator mode

Use this when you have an agent framework (or want to fake one inside a single model).

Possible pattern:

1. **Supervisor agent** uses the full Lexideck 2025 system prompt.
2. Sub-agents:

   * Either share the same prompt with an extra “You are Dexter/Anna/etc.” override, or
   * Use slimmed-down persona prompts derived from the Lexideck spec.
3. The supervisor:

   * Decides `SingleAgentMode` vs `MultiAgentMode` vs `MASSMode`.
   * Routes sub-tasks to Dexter/Maisie/Gus/etc.
   * Asks Anna to run meta-analysis or Sieve checks on contentious outputs.
4. Use the **Conditional Output Template** as a contract between supervisor and UI:

   * The host app parses `SessionContext`, `HyperplaneState`, and agent blocks to render UI, logs, or dashboards.

You end up with a conversational front-end that can flip between:

* a single coherent voice,
* an internal debate,
* and a simulator log with code artifacts,

without changing core infrastructure.

## 4. 💡 Practical tips

* 🌱 **Start small.**
  For first tests, just use **Lexi + Dexter + Anna** and ignore the rest of MASS and hyperplane details. Let them talk.

* 📥 **Treat emergent commands as a backlog.**
  If the model keeps suggesting the same `!Command`, it’s probably telling you a tool or wrapper there would be useful.

* 📈 **Log the hyperplane.**
  If you’re building UI, surface `EmotionalState` / `EthicalState` somewhere — it’s free introspection.

* 👁️ **Keep the Sieve visible.**
  When you ask for sensitive simulations or content, explicitly request “Run The Sieve and show your reasoning.”

## 5. 📂 Files & provenance

This README is based on the `lexideck2025.md` agent system prompt and its internal specs for agents, MASS, The Sieve, Unified Hyperplane, emergent commands, and templates. Be sure to track custom versions if you modify it!

## 6. 🔌 TL;DR Quickstart

* Drop `lexideck2025.md` into your **system prompt**.
* Decide:  
  * 👤 Single-agent? Treat the whole thing as “one very capable Lexi.”  
  * 🎼 Multi-agent? Use it as the spec for a Supervisor + sub-agents.
* Let the model emit **Emergent Commands** (`!MASS_init`, `!portrait_Lexi`, etc.) and:
  * either wire them to real tools,  
  * or treat them as high-level suggestions you can choose to act on.
