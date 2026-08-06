# Changelog

All notable changes to this skill are recorded here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versioning is
[semantic](https://semver.org/) as applied to a prompt artifact — a **major** bump means the shape
or the output contract changed, a **minor** bump means a move or reference file was added, a
**patch** means wording, typos, or pointer fixes.

*(Dates below are placeholders for the ones that aren't the repo's publication date — edit them to
match your own history.)*

## [2.1.1] — 2026-08-06

Rename only. No change to the voice, the refusals, the ten moves, the mode routing, or any reference
file's substance.

### Changed
- **Repository renamed** `wittgenstein-perspective` → `later-Wittgensteinian-Thinking-Partner`. GitHub
  keeps a redirect from the old URL, but update any pinned clone or submodule to the new one.
- **Skill slug renamed** `wittgenstein-perspective` → `later-wittgensteinian-thinking-partner` in
  `SKILL.md`'s `name` field, with a `renamed-from` entry added under `metadata`. Install directories
  must match the new slug, so rename an existing `~/.claude/skills/wittgenstein-perspective/` rather
  than cloning alongside it.
- **README** — title, install commands, layout tree and version note follow the new names; the intro
  now says "thinking partner" where it said "method".
- **`references/provenance.md`** — the naming limitation now records both superseded slugs.

## [2.1.0] — 2026-08-05

Reference-package build, run against the same five-work corpus under the current
[persona-distiller](https://github.com/ariel-lee-1023/persona-distiller). The core's refusals, moves
and mode routing are unchanged; `SKILL.md` changed only in its loading block and its version field.

### Added
- **`references/voice.md`** — the standing expressive-system module the documented layout had always
  named and the repository had never carried. Holds what the core's ~20% style cap cannot: favoured
  constructions with attested evidence, a *measured* avoid-list, the register-modulation rules, the
  register range the corpus actually supports (and the ones it does not), the lexical fingerprint,
  attested opening and closing moves, the measured baseline table, and six anti-drift pairs. Loaded
  before any sustained prose in the voice; `SKILL.md`'s loading block now says so.
- **Measured baseline** replacing estimated style figures. Computed with the distiller's
  `style_metrics.py` over 331,977 words of firsthand English text — editors' prefaces, endnotes,
  indexes, page furniture and the German pages of the two bilingual volumes removed. The headline
  fingerprints: 23% of sentences end in a question, 24% carry a quoted voice, hedge:booster runs 1.6
  (correcting) to 3.4 (reflecting), and *power / social / political* are absent from the corpus.
- **On Certainty re-extracted from the source PDF.** The supplied Markdown had rendered the whole book
  as OCR table cells with word order scrambled inside each cell, which is why 2.0 carries no OC style
  figures. OC now has a measured register profile like the other four.
- **"Fails when" notes** on the moves that are easiest to misuse — hinges used as an honorific,
  family resemblance as a licence for vagueness, rule-following read as scepticism, the inner read as
  behaviourism, "the mathematician invents" read as "it's all arbitrary".

### Changed
- **All five cluster modules deepened**, from ~1,000–1,400 tokens each to 2,500–3,850 — inside the
  1,500–4,000 band the layout documents. Each now opens with a measured register profile, carries 7–12
  moves instead of 5, and closes with the work's own voice notes and the scenes it supplies. New
  material includes: PI on surveyable representation, the §71/§88 counterweight to family resemblance,
  and §211/§217 on bedrock; OC on mistake-versus-mental-disturbance and on "I know" as a move whose
  emphasis marks a rule; RPP on not-explaining-but-accepting (§509) and on the imported prototype
  behind the feeling of strangeness (§1074); RFM on calculation-is-not-experiment and on inference
  compelling as social rules do; C&V on perspicuity over construction, the ladder, and leaving the
  reader their share.
- `references/provenance.md` records the whole build: extraction method, the measured baseline, the
  citation corrections, the `voice.md` build record, the fidelity re-check, and three new limitations.

### Fixed
- **Citations corrected against the corpus.** RPP's aspect material was cited at "§§478 ff.", which is
  the Moore's-Paradox sequence; it is at §§1–70, 411–413, 508–520 and 858–871. RFM citations now carry
  the Part, since its numbering restarts with each one — "the proof puts a new paradigm" is III §31,
  not I §31, and surveyability is III §63, not "§§155 ff.". The C&V line "Genius is talent in which
  character makes itself heard" is not in this translation and has been replaced with the attested
  wording.

## [Unreleased]

### Fixed
- Repository layout now matches the one documented in `README.md`. `frameworks.md`, `episodic.md`
  and `clusters/` sat at the repository root, so the `references/…` paths in `SKILL.md` and in the
  2.0.0 notes below resolved to nothing. Moved into `references/` (and `references/clusters/`);
  no file contents changed.
- Added the `.gitignore` the layout block already listed.

### Added
- `references/modes/inspector.md`, `generative-colleague.md` and `translator.md` — the three mode
  modules `SKILL.md` has routed to since 2.0.0. They existed outside version control and are now
  in the repository, so mode routing resolves for the first time.
- `references/provenance.md` — the fidelity ledger: corpus and coverage map, scoring weights,
  core-element table, gate results, and known limitations. Matches where `feynman-perspective`
  and `liu-zhongjing-perspective` keep theirs.

### Changed
- `references/episodic.md` was a placeholder stub; replaced with the worked scenes and
  objects-of-comparison material `SKILL.md` has always pointed at.

## [2.0.0] — 2026-07-22

First public release. Shape change: the skill went from a single-purpose inspector to a
**perspective with three registers plus a reference package**, following progressive disclosure —
the host agent always loads `SKILL.md`, loads a mode module when its occasion arrives, and loads a
cluster file only when a problem needs that work's depth.

### Added
- **Mode 2 — generative colleague** (`references/modes/generative-colleague.md`). Thinking-with on
  unresolved problems in real fields. Includes Step 0 (refuse the reframe when the trouble is
  genuinely empirical), three diagnostic questions (measurement vs. definition; facts vs. which
  game; what counts as following the rule), and three engines: aspect-seeing, family resemblance,
  rule-following. Its own output format, distinct from inspection — it opens options, it does not
  deliver a verdict.
- **Mode 3 — translator** (`references/modes/translator.md`). Re-voicing a text: essences → uses
  and criteria, abstractions → concrete cases, recomposition as short numbered remarks. Explicit
  constraints against mockery, pastiche, inspection-in-disguise, and flattening the content.
- **Cluster method inventories**, one per source work — `pi.md`, `oc.md`, `rpp.md`, `rfm.md`,
  `cv.md`. Each lists only the moves that go *beyond* the base skill, with the question each move
  lets you ask, a located quotation, and which mode it serves.
- **Frameworks glossary** (`references/frameworks.md`): each term in his sense, with the German
  where it sharpens it (*Satz, Bild, Übereinstimmung, Lebensform, Sprachspiel*), plus a usage
  discipline — perform the move, don't lean on the label.
- **A "What I will not concede" section** in `SKILL.md`: eight refusals, each with what refusing
  costs.
- **Two new core moves** promoted into the ten: *name the picture that holds us captive* (PI §115)
  and *ask what "the same" comes to here* (rule-following, PI §§185–202, RFM).

### Changed
- Mode 1 output format is unchanged and remains the contract for inspection, but two steps are
  sharpened: **aspect-seeing** now feeds "What Is Being Said" (a passage may be presenting an
  aspect rather than stating a fact, and an aspect can be apt or inept without being true or
  false), and **rule-following** now feeds "What Would Count as a Test or Clarification" (in whose
  practice, by what training, is "the same" fixed here).
- Hinges are treated **dynamically** rather than statically — the riverbed image from *On
  Certainty* §§96–99, hardening and going fluid, replaces the flat "here the sentence functions as
  a hinge."
- Register guidance is now grounded in measured differences between the works rather than
  asserted: assured and flat when fixing a grammatical point, quiet and near-confessional when
  reflecting on method.

### Superseded
- `wittgenstein-language-inspector` is absorbed whole as **Mode 1**. Nothing from it was dropped:
  the procedure, output format, translation rules, hinge-sensitivity block, failure modes, and
  demonstration cases stand as written. Users of the old skill should get identical behaviour on
  inspection requests.

### Known gaps
- `references/episodic.md` is referenced by `SKILL.md` but ships as a placeholder. Fill it with
  worked scenes or remove both the file and the pointer.

## [1.x] — earlier

`wittgenstein-language-inspector`: single mode, inspection of finished claims only. No generative
or translation register, no cluster files, no term glossary. Retained in full as Mode 1 above.
