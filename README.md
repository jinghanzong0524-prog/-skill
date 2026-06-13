# nature-polishing Codex skill

This repository packages a single Nature Skills component, `nature-polishing`, for Codex.

It is intended for academic manuscript polishing, Chinese-to-English scientific translation, section restructuring, title/abstract improvement, overclaim control, terminology consistency, and LaTeX layout troubleshooting.

## Install in Codex

```bash
codex plugin marketplace add https://github.com/jinghanzong0524-prog/-skill --ref main
codex plugin add nature-polishing@nature-polishing
```

If the skill does not appear immediately, start a fresh Codex session.

## Local fallback

```bash
git clone https://github.com/jinghanzong0524-prog/-skill.git
cd -skill
mkdir -p ~/.codex/skills
cp -R skills/_shared ~/.codex/skills/
cp -R skills/nature-polishing ~/.codex/skills/
```

Then open a new Codex session and ask:

```text
Polish this abstract in Nature style.
```

## Codex trigger examples

- Polish this abstract in Nature style.
- Translate this Chinese academic paragraph into Nature-style English.
- Improve the logic of this Results paragraph without inventing data.
- Generate 5 defensible Nature-style titles for this manuscript.
- Fix the LaTeX float layout of this figure page.

## Source

This is a single-skill packaging of `nature-polishing` from:

https://github.com/Yuan1z0825/nature-skills

Original author: Yuan1z0825.
