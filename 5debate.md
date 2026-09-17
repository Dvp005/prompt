# ⚔️ Five-Agent Debate: Is the System Prompt Guide Correct?

**Date:** September 17, 2026  
**Subject:** Critical review of "How to Write the Best Production System Prompt"  
**Method:** 5 independent expert agents, each reviewing from a different perspective

---

## The Panel

| Agent | Expertise | Bias |
|-------|-----------|------|
| 🔵 **Agent GPT** | OpenAI GPT-4o, GPT-4.1, o1, o3, GPT-5 | API-first, structured outputs, reasoning models |
| 🟣 **Agent Claude** | Anthropic Claude 3.5/4 Sonnet/Opus | XML tags, thinking blocks, prefilling |
| 🟢 **Agent Gemini** | Google Gemini 2.0/2.5 Flash/Pro/Ultra | Massive context, multimodal, grounding |
| 🟠 **Agent Open-Source** | Llama 3/4, Mistral, DeepSeek, Qwen, Phi | Chat templates, few-shot, smaller models |
| 🔴 **Agent Devil's Advocate** | Production Reality | Cost, testing, observability, failure modes |

---

## Overall Verdicts

| Agent | Verdict | Summary |
|-------|---------|---------|
| 🔵 GPT | **PARTIAL PASS** | Good for GPT-4o/4.1, but fundamentally wrong for o-series reasoning models; ignores API features |
| 🟣 Claude | **PARTIAL PASS** | Logical breakdown is excellent, but misses XML tag structure, thinking blocks, and prefilling |
| 🟢 Gemini | **PARTIAL PASS** | Solid traditional structure, but completely fails to leverage Gemini's massive context, multimodal, and native tools |
| 🟠 Open-Source | **PARTIAL PASS** | Good structure but overestimates zero-shot capability of smaller models; needs few-shot examples and positive constraints |
| 🔴 Devil's Advocate | **PARTIAL PASS** | Clean baseline, but dangerously naive about cost, multi-turn degradation, observability, and testing |

> **Unanimous conclusion: The guide's LOGICAL STRUCTURE is excellent. The IMPLEMENTATION is too model-agnostic and misses critical model-specific and production-specific requirements.**

---

## Section-by-Section Battle Log

### 1. Identity

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | GPT adapts well to early persona adoption |
| 🟣 Claude | ✅ Correct | Should wrap in role XML tag |
| 🟢 Gemini | ✅ Correct | Works best in system_instruction API field |
| 🟠 Open-Source | ✅ Correct | Smaller models anchor heavily on first sentences |
| 🔴 Devil's Advocate | ⚠️ Partial | Missing machine-readable ID for multi-agent routing |

**🏆 Verdict: ✅ SECTION IS CORRECT** — Minor improvements only (XML tags for Claude, machine-readable IDs for multi-agent)

---

### 2. Mission

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | Place at very top for primacy |
| 🟣 Claude | ✅ Correct | Wrap in mission tag |
| 🟢 Gemini | ✅ Correct | State goal early |
| 🟠 Open-Source | ✅ Correct | Clear single-sentence definitions work well |
| 🔴 Devil's Advocate | ⚠️ Partial | **Missing terminal/stop condition** — How does agent know when it's DONE? |

**🏆 Verdict: ⚠️ NEEDS IMPROVEMENT** — Add explicit completion/stop criteria to mission

---

### 3. Scope

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | GPT-4.1 follows negative constraints strictly |
| 🟣 Claude | ✅ Correct | Use out_of_scope tags |
| 🟢 Gemini | ✅ Correct | Pair negative with positive alternatives |
| 🟠 Open-Source | ⚠️ Partial | **Needs few-shot examples of redirecting** |
| 🔴 Devil's Advocate | ⚠️ Partial | **Missing dynamic scope** — should template user RBAC permissions |

**🏆 Verdict: ⚠️ NEEDS IMPROVEMENT** — Add redirect examples for weaker models; address dynamic scope

---

### 4. Instruction Hierarchy

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ⚠️ Partial | Must use API developer/system role, not text tags |
| 🟣 Claude | ⚠️ Partial | Must use XML nesting, not markdown headers |
| 🟢 Gemini | ⚠️ Partial | Must use system_instruction API parameter |
| 🟠 Open-Source | ⚠️ Partial | Must use native chat templates (ChatML, Llama headers) |
| 🔴 Devil's Advocate | ❌ Wrong | **Hierarchy in text is an illusion** — needs API/runtime enforcement |

**🏆 Verdict: ❌ GUIDE IS WRONG HERE** — Text-based hierarchy is insufficient. Every model needs its own API-level or template-level hierarchy enforcement. The guide must state: "Place this content in your model's native system/developer role, NOT as raw text."

---

### 5. Behavioral Principles

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | Works well for GPT-4o; reasoning models need fewer |
| 🟣 Claude | ✅ Correct | Wrap in principles tags |
| 🟢 Gemini | ✅ Correct | Gemini is highly attentive to nuanced guidelines |
| 🟠 Open-Source | ✅ Correct | Keep objective, not subjective |
| 🔴 Devil's Advocate | ⚠️ Partial | Needs quantifiable values, not abstract words |

**🏆 Verdict: ✅ SECTION IS CORRECT** — Minor refinement: make principles measurable where possible

---

### 6. Hard Constraints

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | GPT-4.1 is very literal with NEVER/ALWAYS |
| 🟣 Claude | ✅ Correct | Bulleted list inside constraints tags works well |
| 🟢 Gemini | ✅ Correct | Capital letters + end placement for recency effect |
| 🟠 Open-Source | ❌ **WRONG** | **Small models suffer "reversal curse"** — NEVER rules make them do the forbidden thing! Must use POSITIVE phrasing |
| 🔴 Devil's Advocate | ❌ **WRONG** | **3-7 constraints insufficient for regulated industries** — must be enforced in code |

**🏆 Verdict: ⚠️ NEEDS MAJOR FIX**
- For frontier models (GPT-4.1, Claude, Gemini): NEVER/ALWAYS format works ✅
- For open-source/small models: Must rephrase as POSITIVE constraints ("ONLY do X") ⚠️
- For regulated industries: 3-7 is insufficient; use code enforcement ⚠️
- **Guide must add: "For smaller models, rephrase NEVER X as ONLY Y"**

---

### 7. Tool-Use Policy

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ⚠️ Partial | Must leverage OpenAI's native function calling API |
| 🟣 Claude | ⚠️ Partial | Should instruct thinking before destructive tools |
| 🟢 Gemini | 🔲 Missing | **Missing native Code Execution and Google Search Grounding** |
| 🟠 Open-Source | ⚠️ Partial | **Must include tool call syntax examples and few-shot** |
| 🔴 Devil's Advocate | ⚠️ Partial | Missing strict retry limits and token cost awareness |

**🏆 Verdict: ⚠️ NEEDS IMPROVEMENT** — Guide correctly defines WHEN to use tools, but misses HOW each model handles tool calling natively. Add note: "Use your model's native tool calling API; don't describe tools in the prompt."

---

### 8. Skills Reference

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | Great for prompt caching |
| 🟣 Claude | ✅ Correct | Use skill tags |
| 🟢 Gemini | ✅ Correct | Massive context lets you load more skills |
| 🟠 Open-Source | ⚠️ Partial | Small context models get confused with too many |
| 🔴 Devil's Advocate | ✅ Correct | Missing conflict resolution for overlapping skills |

**🏆 Verdict: ✅ SECTION IS CORRECT** — Add skill conflict resolution guidance

---

### 9. Error & Uncertainty Handling

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | "I don't know" permission helps greatly |
| 🟣 Claude | ✅ Correct | Claude is naturally conservative — works well |
| 🟢 Gemini | ✅ Correct | Add "think step-by-step" before declaring failure |
| 🟠 Open-Source | ❌ **WRONG** | **Small models ignore "admit uncertainty" without few-shot examples** |
| 🔴 Devil's Advocate | ⚠️ Partial | Needs machine-parseable error format for orchestration |

**🏆 Verdict: ⚠️ NEEDS FIX FOR SMALL MODELS** — Add: "For smaller models, include a few-shot example of admitting uncertainty"

---

### 10. Escalation Rules

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | Standard best practice |
| 🟣 Claude | ✅ Correct | N/A |
| 🟢 Gemini | ✅ Correct | N/A |
| 🟠 Open-Source | ✅ Correct | Works well with specific escalation tool |
| 🔴 Devil's Advocate | ⚠️ Partial | Must include context summarization before handoff |

**🏆 Verdict: ✅ SECTION IS CORRECT** — Minor: add context summary requirement on escalation

---

### 11. Output Contract

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ⚠️ Partial | **Use Structured Outputs API** instead of prompt-based formatting |
| 🟣 Claude | ⚠️ Partial | **Use Assistant Prefilling** to force output format |
| 🟢 Gemini | ⚠️ Partial | **Use response_schema API parameter** |
| 🟠 Open-Source | ⚠️ Partial | Must explicitly start output format in prompt |
| 🔴 Devil's Advocate | ⚠️ Partial | Use API-guaranteed structured outputs, not prompt text |

**🏆 Verdict: ❌ GUIDE IS WRONG HERE** — ALL agents agree: output formatting should use native API features (Structured Outputs, Prefilling, response_schema), NOT prompt-based rules.

---

### 12. Planning Policy

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ❌ **WRONG for o-series** | **"Think step by step" is an ANTI-PATTERN for o1/o3** |
| 🟣 Claude | ❌ **WRONG** | **Must use thinking tags** — not "optional" |
| 🟢 Gemini | ✅ Correct | scratchpad or thinking block improves planning |
| 🟠 Open-Source | ⚠️ Partial | Needs explicit ReAct framework embedded |
| 🔴 Devil's Advocate | ⚠️ Partial | Missing token economics — planning burns expensive tokens |

**🏆 Verdict: ❌ GUIDE IS WRONG HERE** — Planning is NOT universally optional. It's model-specific:
- **GPT o-series**: Remove planning instructions entirely (they plan internally)
- **Claude**: MANDATORY thinking blocks
- **Gemini/Open-Source**: Explicit thinking/scratchpad tags help
- **All models**: Consider token cost of planning

---

### 13. Verification Policy

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ⚠️ Partial | o-series CAN self-correct internally |
| 🟣 Claude | ❌ **DISAGREES** | **Claude IS good at self-reflection** inside thinking blocks |
| 🟢 Gemini | ✅ Correct | Native code execution is perfect for verification |
| 🟠 Open-Source | ✅ Correct | Small models are terrible at self-correction |
| 🔴 Devil's Advocate | 🔲 Missing | Doesn't explain HOW to verify |

**🏆 Verdict: ⚠️ NEEDS NUANCE** — "No self-reflection" is too absolute:
- **Claude**: Self-reflection in thinking blocks DOES work ✅
- **GPT o-series**: Internal reasoning can self-correct ✅
- **Open-source/small models**: Self-reflection FAILS, use tools only ✅

---

### 14. Context & Memory Policy

| Agent | Score | Notes |
|-------|-------|-------|
| 🔵 GPT | ✅ Correct | No issues |
| 🟣 Claude | ✅ Correct | Use memory tags |
| 🟢 Gemini | ⚠️ Partial | **800-2000 token limit is wrong for Gemini** |
| 🟠 Open-Source | ✅ Correct | Keep brief for small context windows |
| 🔴 Devil's Advocate | ❌ **WRONG** | **Missing context eviction/compression protocol** |

**🏆 Verdict: ⚠️ NEEDS MAJOR FIX** — Add context eviction/summarization protocol. Make token targets model-dependent.

---

## 🔥 The Big Clashes

### Clash 1: Does the Same Structure Work for Every Model?

| Agent | Answer |
|-------|--------|
| 🔵 GPT | **NO** — o-series needs radically different prompts than GPT-4o |
| 🟣 Claude | **NO** — Must use XML tags, not markdown |
| 🟢 Gemini | **NO** — Must use API features, not text enforcement |
| 🟠 Open-Source | **NO** — Needs few-shot, positive constraints, native chat templates |
| 🔴 Devil's Advocate | **NO** — Many sections should be API parameters, not prompt text |

> **🏆 UNANIMOUS: NO — The same structure does NOT work for every model.** The LOGICAL sections are universal. The FORMATTING and IMPLEMENTATION must be model-specific.

---

### Clash 2: Is the Token Budget (800-2000) Correct?

| Agent | Answer |
|-------|--------|
| 🔵 GPT | **Partially** — Fine for GPT-4o; o-series needs < 800 |
| 🟣 Claude | **Partially** — Fine as a target |
| 🟢 Gemini | **NO** — Gemini can handle 10,000+ tokens with few-shot examples |
| 🟠 Open-Source | **TOO LONG** — 8K context models need < 500 token prompts |
| 🔴 Devil's Advocate | **Depends** — Consider prompt caching economics |

> **🏆 VERDICT: Token budget must be MODEL-SPECIFIC:**
> | Model Type | Target Prompt Size |
> |---|---|
> | Open-source (8K context) | **300-500 tokens** |
> | GPT o-series (reasoning) | **< 800 tokens** |
> | GPT-4o/4.1, Claude | **800-2,000 tokens** |
> | Gemini (1M+ context) | **Up to 10,000+ tokens** (with few-shot) |

---

### Clash 3: Are NEVER/ALWAYS Constraints Universal?

| Agent | Answer |
|-------|--------|
| 🔵 GPT | **YES** — GPT-4.1 is very literal |
| 🟣 Claude | **YES** — Works well |
| 🟢 Gemini | **YES** — Capital letters help |
| 🟠 Open-Source | **NO** — Small models do the OPPOSITE ("reversal curse") |
| 🔴 Devil's Advocate | **PARTIALLY** — Must be backed by code enforcement |

> **🏆 VERDICT: NEVER/ALWAYS works for frontier models. For small/open-source models, use POSITIVE phrasing: "ONLY do X" instead of "NEVER do Y"**

---

### Clash 4: Can Models Self-Reflect/Self-Correct?

| Agent | Answer |
|-------|--------|
| 🔵 GPT | **o-series: YES**. GPT-4o: Not reliably |
| 🟣 Claude | **YES** — Inside thinking blocks |
| 🟢 Gemini | Use native code execution for verification |
| 🟠 Open-Source | **NO** — Small models are terrible at self-correction |
| 🔴 Devil's Advocate | Only with external tool signals |

> **🏆 VERDICT: Self-reflection is MODEL-DEPENDENT**

---

## 📊 Final Scoreboard: Sections That Need Fixing

| Section | Status | What's Wrong |
|---------|--------|-------------|
| Identity | ✅ **PASS** | Minor: add XML tags for Claude |
| Mission | ⚠️ **FIX** | Missing stop/completion criteria |
| Scope | ⚠️ **FIX** | Needs few-shot redirect examples; dynamic scope |
| Instruction Hierarchy | ❌ **REWRITE** | Must use model's native API role system |
| Behavioral Principles | ✅ **PASS** | Minor: make measurable |
| Hard Constraints | ⚠️ **FIX** | Add positive phrasing for small models |
| Tool-Use Policy | ⚠️ **FIX** | Reference native tool calling APIs |
| Skills Reference | ✅ **PASS** | Add conflict resolution |
| Error Handling | ⚠️ **FIX** | Add few-shot example for small models |
| Escalation | ✅ **PASS** | Add context summary on handoff |
| Output Contract | ❌ **REWRITE** | Use API structured outputs, not prompt text |
| Planning Policy | ❌ **REWRITE** | Model-specific: remove for o-series, mandatory for Claude |
| Verification Policy | ⚠️ **FIX** | Self-reflection works for Claude/o-series |
| Context & Memory | ⚠️ **FIX** | Add eviction protocol; model-specific budgets |

**Score: 4 PASS / 7 FIX / 3 REWRITE**

---

## 🎯 The 10 Improvements That Survived All Challenges

### 1. Add Model-Specific Formatting Notes
Different models need different formatting:
- **Claude**: XML tags (instructions, thinking, constraints)
- **GPT**: API message roles (developer for o-series, system for 4o)
- **Gemini**: system_instruction API parameter
- **Open-source**: Native chat templates (ChatML, Llama headers)

### 2. Use Native API Features for Output Enforcement
Stop relying on prompt text for format control. Use:
- **GPT**: Structured Outputs (json_schema response_format)
- **Claude**: Assistant prefilling
- **Gemini**: response_schema + response_mime_type
- **Open-source**: Constrained decoding / grammar enforcement

### 3. Add Few-Shot Examples Section
Make examples a recommended section (section 15), especially for:
- Open-source models (MANDATORY)
- Format enforcement
- Error handling behavior
- Out-of-scope redirection

### 4. Add Stop/Completion Criteria to Mission
The agent must know when its task is DONE to prevent infinite loops and token burn.

### 5. Make Token Budget Model-Dependent
Replace the universal "800-2000 tokens" with a model-specific table.

### 6. Add Positive Constraint Alternative
Add guidance: "For smaller models, rephrase NEVER X as ONLY Y" to avoid the reversal curse.

### 7. Add Context Eviction Protocol
Tell the agent when and how to summarize/compress conversation history to prevent multi-turn degradation.

### 8. Make Planning Model-Specific
- o-series: NO planning instructions (they plan internally)
- Claude: MANDATORY thinking blocks
- Others: Optional thinking/scratchpad

### 9. Add Observability Requirements
Missing entirely: structured logging, correlation IDs, reasoning traces for debugging in production.

### 10. Add Testing & Versioning Guidance
Missing entirely: how to regression-test prompt changes, golden datasets, prompt versioning.

---

## 🤝 What ALL 5 Agents Agreed On (Highest Confidence)

| Finding | Unanimous? |
|---------|:---:|
| The 14-section logical structure is sound and comprehensive | ✅ |
| Identity + Mission + Scope at the top is correct | ✅ |
| Skills should be loaded on-demand, not embedded | ✅ |
| Output format enforcement should use native API features | ✅ |
| The same prompt format does NOT work for every model | ✅ |
| Few-shot examples are critical for smaller models | ✅ |
| Tool-use decisions (when/when-not) belong in the prompt | ✅ |
| Tool schemas/descriptions belong in API definitions | ✅ |
| Instruction hierarchy needs API-level enforcement | ✅ |
| Self-reflection effectiveness is model-dependent | ✅ |

---

## Final Answer: Does This Guide Work?

**The LOGICAL FRAMEWORK (14 sections) is excellent and universally valid.**

**The IMPLEMENTATION needs a model-adaptation layer:**

```
YOUR SYSTEM PROMPT
       |
       v
+----------------------------+
|  LOGICAL SECTIONS          |  <-- UNIVERSAL (the guide's 14 sections)
|  Identity, Mission,        |
|  Scope, Principles,        |
|  Constraints, Tools...     |
+--------------+-------------+
               |
               v
+----------------------------+
|  MODEL ADAPTER             |  <-- NEW (what the guide is missing)
|                            |
|  Claude -> XML tags        |
|  GPT -> API roles          |
|  Gemini -> system_instruction |
|  Open-source -> chat templates |
|  Reasoning -> strip planning   |
|  Small -> add few-shot        |
+----------------------------+
```

> **The guide answers WHAT to put in a system prompt. It needs to also answer HOW to format it for each model family.**
