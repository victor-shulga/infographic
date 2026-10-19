# infographic

A **Claude Code skill** that turns raw text into a LinkedIn infographic (1080×1350) in the
Victor Shulga brand: a real chart or diagram, not text in boxes.

You paste the content. Claude picks a shape from a catalogue of 24 (comparison table, step
grid, donut, funnel, growth curve, timeline, ladder, tier list, hub, Venn and more), refuses to
repeat the shape it used last time, and builds the creative either in Figma or as HTML that
headless Chrome screenshots to PNG.

## What you get

→ one finished 1080×1350 creative: rubric chip on top, centered caps headline, the visual, author footer

→ ten shapes with ready builders, fourteen more described in `references/infographic-templates.md`
(what each one is for, how it gets ruined, how to build it)

→ 31 line icons in `assets/icons/` and two reference scripts in `assets/html-render/` that run as-is

## Install

```bash
npx skills add victor-shulga/infographic
```

Then in Claude: "зроби інфографіку з цього тексту", "пончик з цими цифрами",
"інфографіка скриптом", "make an infographic from this".

## Requirements & integrations

| Integration | Used for | Required? | Auth/setup |
|---|---|---|---|
| Figma MCP (`use_figma`) | default backend: builds the creative in a new Figma file | One of the two backends | connect the official Figma connector in Claude |
| Google Chrome + Python 3 | HTML backend: `build.py` renders HTML, headless Chrome screenshots it | One of the two backends | Chrome installed locally, no keys |
| Claude Code or claude.ai | running the skill | Yes | `npx skills add` or «Upload a skill» |

The brand (colors, fonts, photo, wordmark) is baked into the skill. To use it for another
brand, swap the files in `skills/infographic/assets/` and the Brand block in `SKILL.md`.

## License

MIT

---

Built by [Victor Shulga](https://victorshulga.com), Fractional CRO for B2B service companies. Full skill stack: [victorshulga.com/stack](https://victorshulga.com/stack/).
