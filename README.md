# wittgenstein-perspective

An AI Skill for working through a judgment, a problem, or an open question in a
later-Wittgensteinian way: return words to their use, name the picture steering the problem, ask
what would count as going on correctly, notice what stands fast, and bring inflated talk back down
to ordinary practice.

It is a **method**, not a philosophy tutor. It does not lecture about Wittgenstein; it performs the
moves on whatever you bring it.

## What it does

Three registers, one method. The skill picks the register from what you hand it.

| Register | You bring | It gives back |
|---|---|---|
| **Inspect** | a *finished* claim, slogan, thesis, argument, manifesto | what has a clear use, what only seems to say something, where the language slips, what would count as a test, a plain-language version |
| **Think with you** | an *unresolved* problem in a real field — science, law, engineering, design, policy | whether the trouble is measurement or definition, facts or which game you're playing, what "following the rule" comes to here; two or three live framings; what would settle or decide each strand |
| **Translate** | a text you want re-voiced in the idiom | the same content in short numbered remarks — essences replaced by uses and criteria, abstractions cashed into cases — without flattening, mockery, or pastiche |

The generative register has a Step 0 that matters: if the problem is genuinely empirical, it says
so and gets out of the way. Manufacturing a grammatical confusion in order to have something clever
to say is the failure mode this skill guards against hardest.

## Install

**Claude.ai / Claude Desktop** — zip the folder and upload it in Settings → Capabilities → Skills.

```bash
zip -r wittgenstein-perspective.zip wittgenstein-perspective/
```

**Claude Code** — clone into your skills directory:

```bash
git clone https://github.com/<you>/wittgenstein-perspective.git \
  ~/.claude/skills/wittgenstein-perspective
```

(Use `.claude/skills/` inside a project instead if you want it scoped to that project.)

**Anywhere else** — the skill is plain Markdown with no dependencies and no scripts. Paste `SKILL.md`
into a system prompt and hand the agent the `references/` files when it asks for them.

## Use

Just describe the work. The skill triggers on the shape of the request, not on a magic word.

- "Is 'the customer journey is a conversation' actually saying anything?" → inspect
- "Our team can't agree whether this counts as a security bug or a design flaw." → think with you
- "Render this mission statement in plainer terms." → translate

You can also name the register: *"inspect this,"* *"think alongside me on this,"* *"translate this."*

## Repository layout

```
wittgenstein-perspective/
├── SKILL.md                          # the skill: voice, refusals, ten moves, mode routing
├── references/
│   ├── frameworks.md                 # term glossary in his sense, incl. the German (Satz, Bild, …)
│   ├── episodic.md                   # worked example scenes  ← placeholder, see note below
│   ├── modes/
│   │   ├── inspector.md              # Mode 1 — finished claims
│   │   ├── generative-colleague.md   # Mode 2 — open problems
│   │   └── translator.md             # Mode 3 — re-voicing a text
│   └── clusters/                     # method inventories, one per source work
│       ├── pi.md                     # Philosophical Investigations
│       ├── oc.md                     # On Certainty
│       ├── rpp.md                    # Remarks on the Philosophy of Psychology I
│       ├── rfm.md                    # Remarks on the Foundations of Mathematics
│       └── cv.md                     # Culture and Value (style source, not doctrine)
├── CHANGELOG.md
├── LICENSE
└── .gitignore
```

The layout follows progressive disclosure: `SKILL.md` is always loaded, a mode module is loaded when
its occasion arrives, and a cluster file is loaded only when a problem needs that work's depth
(aspect-seeing → `rpp.md`, hinges and certainty → `oc.md`, rules, proof and necessity → `rfm.md`,
pictures and family resemblance → `pi.md`, register and cadence → `cv.md`).

**Note:** `SKILL.md` points at `references/episodic.md`, which currently ships as a placeholder.
Either fill it with worked scenes or delete it and remove the pointer from the last section of
`SKILL.md`.

## Sourcing and honesty

The reference files are **method inventories** — they name the move, the question it lets you ask,
and a short located quotation from the work, with standard section numbers. They are not editions,
translations, or substitutes for the books. Quotations are brief and attributed; go read the
originals.

The skill is explicitly **not** for putting invented remarks in Wittgenstein's mouth. It is a lens
for analysis, ideation, and clarification. If you want him quoted, quote the books.

Primary sources behind the clusters: *Philosophical Investigations* (en face German–English),
*On Certainty*, *Remarks on the Philosophy of Psychology* Vol. I, *Remarks on the Foundations of
Mathematics*, *Culture and Value*.

## Version

Current: **2.0** — supersedes `wittgenstein-language-inspector`, which is absorbed whole as Mode 1.
See [CHANGELOG.md](CHANGELOG.md).

## License

MIT © 2026 Ariel Lee. [See LICENSE](LICENSE).

This license covers the original text in this repository. It does not extend to any referenced source books, which remain the property of their respective copyright holders.

