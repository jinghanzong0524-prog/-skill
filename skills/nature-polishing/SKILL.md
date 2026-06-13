---
name: nature-polishing
description: Polish, restructure, or translate academic prose into Nature-leaning English using writing-strategy principles, curated Nature/Nature Communications article patterns, and phrase-level support from Academic Phrasebank. Use whenever the user asks to polish a manuscript paragraph, abstract, introduction, results, discussion, conclusion, title, methods section, or Chinese academic draft for publication-quality English. Also covers LaTeX layout/typesetting fixes: loose or sparse pages, stranded section headings, figures that do not fill the page or split across pages, "Float too large", multi-panel figure arrangement, and Supplementary Information that looks empty. Also trigger on academic writing, scientific writing, SCI/paper writing, English manuscript polishing, language editing, proofreading, 学术写作、科研写作、论文润色、写paper、SCI写作、英文论文润色、语言润色、润色、改写、学术英语、英文写作.
version: 6.1.0
author: Yuan1z skill, packaged for Codex by jinghanzong0524-prog
---

# Nature-Style Academic Polishing — Router

This skill is split into two layers:

- A static layer under `static/` that holds reusable content fragments.
- A dynamic layer, this file plus `manifest.yaml`, that detects the request axes and loads only the fragments needed.

Do not apply polishing logic from memory alone. Load the relevant local fragments first.

## Routing protocol

### 1. Load the manifest and core layer

Read `manifest.yaml`.

Also read every file listed under `always_load`.

### 2. Detect axis values

For each request, detect:

- `paper_type`: research / methods / hypothesis / algorithmic / review. Default: research.
- `section`: abstract / intro / results / discussion / conclusion / title / methods. May be multiple.
- `language`: en / zh-to-en.
- `journal`: nature / nat-comms / generic.

State the detected axis values in one short line before editing.

### 3. Load matching fragments

Read only the fragments selected by the detected axes. Skip the section axis only if the user supplied free-floating prose with no section context.

### 4. Polish using loaded material

Apply fragments in this order:

1. Paper-type playbook.
2. Section-specific job and failure modes.
3. Journal-specific framing and constraints.
4. Language-specific sentence and paragraph rules.
5. Core stance and ethics throughout.

If a structural problem cannot be fixed without inventing content, flag it instead of hiding it under polished language.

### 5. Use references only when needed

Use `references/` on demand for article patterns, phrasebank alternatives, style audits, or LaTeX layout work.

For LaTeX placement/layout tasks, load `references/latex-layout.md` directly and compile/render/inspect instead of judging from `.tex` alone.
