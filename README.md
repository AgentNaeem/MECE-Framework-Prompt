# MECE-Framework-Builder Prompt
The MECE (Mutually Exclusive, Collectively Exhaustive) framework forces clarity: one place for each thing... and every important thing has a place. I’ve packaged my proprietary MECE Framework Builder as a Custom GPT + prompt. 

A practical prompt + schema to create **Mutually Exclusive, Collectively Exhaustive** frameworks for any topic.

Custom GPT Available Here: https://chatgpt.com/g/g-689b34fefa3481919acd1bf821f92b6a-m-e-c-e-gpt

## Why
Most frameworks fail due to **overlap** (duplicated buckets) or **gaps** (missing areas). This builder enforces scope, distinctness, and coverage.

## Use It In Two Ways
1. **Markdown mode (default):** human-readable output for docs, wikis, posts.  
2. **JSON mode:** structured output for validation, dashboards, or automation.

## Quick Start (ChatGPT / Custom GPT)
- Paste the prompt from `prompts/mece_markdown.txt`.
- Provide: Topic, Audience, Scope, Depth (1–3).  
- To switch to JSON: include `mode: json` in your message.

## Output Structure
- Categories with one-line definitions  
- Subcategories with one-sentence purpose  
- Distinctness notes (A vs B)  
- Coverage checklist (Aspect → Category)  
- Pairwise overlap test + fix  
- Edge cases & trade-offs  
- MECE confirmation

## JSON Schema
See `prompts/mece_json_schema.json`. Fields:
- `topic`, `audience`, `scope`
- `categories[] { name, definition, subcategories[] { name, purpose } }`
- `distinctness_notes[] { vs[2], reason }`
- `coverage_checklist[] { aspect, category }`
- `edge_cases[]`
- `mece_confirmation { mutually_exclusive_because, collectively_exhaustive_because }`

## Examples
- `examples/ai_marketing.markdown.md` – readable output  
- `examples/ai_marketing.json` – machine-readable output

## License
MIT
