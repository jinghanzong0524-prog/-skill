# LaTeX layout and float typesetting for Nature-style manuscripts

Load this for layout, spacing, float placement, sparse pages, stranded headings, and figure placement.

Golden rule: change -> compile -> render to image -> inspect -> iterate.

Diagnosis:
- Read log for Float too large, Overfull vbox, undefined refs.
- Render pages to PNG and build a contact sheet.
- Measure figure aspect ratios and page height budget.

Float-page looseness:
Use top-aligned float glue so floats pack from the top and slack collects at the bottom.

Wide-short figures:
A 3:1 or 4:1 figure cannot fill a portrait page at text width. Regenerate the figure with a taller aspect ratio, about 1.9:1 to 2.2:1, rather than stretching it.

Avoid landscape by default for Nature-style manuscripts.

Stranded headings:
Bind section heading, intro text, and figure into one unit with `\clearpage` plus `[H]` only when the figure is sized to fit.

Do not blanket-clearpage every section. Optimize for even page fullness, not minimum page count.
