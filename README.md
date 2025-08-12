# MECE Framework Builder (Custom GPT + Prompt + Schema)

Turn messy topics into Mutually Exclusive, Collectively Exhaustive maps—fast.

## What’s here
- **Markdown-first instruction set** for a Custom GPT
- **Strict JSON schema** for machine-readable output
- **Tiny examples** (Markdown + JSON) and a validation step

> MECE = Mutually Exclusive, Collectively Exhaustive: no overlaps, no gaps.

---

## Why this exists
Many “frameworks” fail in two ways: overlapping buckets and missing areas.  
This builder enforces scope, applies a pairwise overlap check, and outputs a coverage checklist so each aspect maps to exactly one category.

---

## Quick start (ChatGPT / Custom GPT)
1) Paste the prompt from `prompts/mece_markdown.md` into a Custom GPT (or a chat).  
2) Provide:
   - **Topic** (required)
   - **Audience** (execs, operators, students, etc.)
   - **Scope** (what’s in/out; if absent, the GPT proposes a sensible scope and marks it **(Assumed)**)
   - **Depth** 1–3 (default **2**)
   - **Max_Categories** (3–8, default **5**)
   - **Subcats_Per_Category** (2–5, default **3**)
   - Optional: **Must_Include**\[...\], **Exclusions**\[...\]
3) Receive a MECE framework with:
   - **Categories** → **Subcategories** → **Distinctness notes** → **Coverage checklist** → **Overlap repair** → **Edge cases** → **MECE confirmation**

### JSON mode
Add `mode: json` anywhere in your message.  
The GPT returns **only** a JSON object conforming to `prompts/mece_json_schema.json`.

---

## Validating JSON output locally

### Using `ajv` (Node.js)
```bash
npm i -g ajv-cli
ajv validate -s prompts/mece_json_schema.json -d examples/example.json
