# MECE Framework Builder (Custom GPT + Prompt + Schema)

Turn messy topics into **Mutually Exclusive, Collectively Exhaustive** maps — fast.  
This repo contains:
- A **Custom GPT** instruction set (Markdown-first, JSON on command)
- A **JSON Schema** for strict, machine-readable output
- **Examples** in both Markdown and JSON

> MECE = *Mutually Exclusive, Collectively Exhaustive*: no overlaps, no gaps.

---

## Why this exists
Most “frameworks” fail on two fronts: **overlap** (duplicated buckets) and **gaps** (missing areas).  
This builder enforces **scope**, runs a **pairwise overlap test**, and outputs a **coverage checklist** so every important thing has a single home.

---

## Quick start (ChatGPT / Custom GPT)
1. Open the GPT (link below) or paste the prompt from `prompts/mece_markdown.md`.
2. Provide:
   - **Topic** (required)
   - **Audience** (e.g., execs, operators, students)
   - **Scope** (what’s in/out)
   - **Depth** **1–3** or **light/standard/deep** (default **2 / standard**)
   - Optional: `Max_Categories`, `Subcats_Per_Category`, `Must_Include`, `Exclusions`
3. Get a MECE framework with:  
   **categories → subcategories → distinctness notes → coverage checklist → overlap fix → edge cases → confirmation**

**JSON mode:** add `mode: json` anywhere in your message. The GPT will return only a JSON object that validates against `prompts/mece_json_schema.json`.

---

## Files
