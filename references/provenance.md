# Provenance & fidelity ledger

The honesty file. Everything the core is not allowed to contain — sources, scores, gate outcomes,
caveats — lives here. Corpus: five later-Wittgenstein works supplied by the user. The 2.0 build was
run as a **fold-in / update** of an existing persona (`wittgenstein-language-inspector`), expanding it
from one mode (inspect finished claims) to three (inspect / think-with / translate). Full-rigor mode.

The **2.1 build** (recorded at the end of this file) is a second fold-in against the same corpus: it
adds the standing `voice.md` module the layout required and had never carried, replaces the estimated
style figures with a measured baseline, deepens all five cluster modules, and corrects a set of
citations that the 2.0 build had wrong.

## Corpus & coverage map

| Cluster | Work | Firsthand words (2.1) | Register (measured, 2.1) | Role |
|---|---|---|---|---|
| c-OC | On Certainty | 30,820 | plainest, most first-person (h:b 2.21; 75% 1st person; median 15) | hinges, riverbed, groundless justification |
| c-PI | Philosophical Investigations (en-face) | 95,674 | fullest dialectic (h:b 2.57; median 19; 28% quoted voice) | use, games, criteria, picture, family resemblance, rule-following, German terms |
| c-RPP | Remarks on the Philosophy of Psychology I | 78,298 | most interrogative (h:b 2.38; 27% questions; 23% short sentences) | aspect-seeing, grammar of the inner, concept-networks |
| c-RFM | Remarks on the Foundations of Mathematics | 89,634 | most assertive (h:b 1.61; heaviest dashes) | proof-as-paradigm, rule-following, necessity-as-grammatical |
| c-CV | Culture and Value | 32,751 | most tentative, no interlocutor (h:b 3.42; 9.6% questions) | STYLE source: cadence, dissolution, anti-performance |

The 2.0 build's register figures were estimates from partial extractions; the figures above are
measured (see **Measured baseline** below). The 2.0 estimates for RPP (≈2.4), RFM (≈1.6) and C&V (≈3.4)
came within rounding of the measured values, which is a useful check on the earlier build rather than a
coincidence to lean on.

Dialogue ratio: low — the corpus is monologic-with-imagined-interlocutor. Per the skill's
auto-weighting, interactional weight was **not** raised; the "dialectical exchange with a self-raised
objection" was treated as the interactional signal. Temporal spread: all *later* Wittgenstein
(post-*Tractatus*), which matches the intended scope. Measurement caveat: C&V's raw lexical metrics
are polluted by the bilingual PDF (German content words dominate the top-terms list); sentence-shape
and hedge:booster signals still read cleanly.

## Scoring weights

Defaults, unchanged (monologic corpus, no narrow user focus):
`projectibility 0.30 · cost_refusal 0.25 · expressive_match 0.20 · interactional 0.15 · preoccupation 0.10`.

## Core-element ledger

| Core element | Section | Class | Sources / §§ | Clusters | Projection | Cost-gate | Composite | Note |
|---|---|---|---|---|---|---|---|---|
| Describe, don't explain | won't concede | cost_refusal | PI §109,§126; OC §189; RFM | PI,OC,RFM | 0.90 | high-signal, in core | 0.83 | 3-cluster; strongest |
| No foundation; reasons end in acting/persuasion | won't concede | cost_refusal | OC §110,§253,§612 | OC,PI,RFM | 0.90 | high-signal, in core | 0.81 | anchors the groundlessness |
| Won't over-clarify a confusion | won't concede | cost_refusal | (base skill) + C&V | CV,PI | 0.75 | high-signal, in core | 0.72 | inherited, retained |
| Depth is usually a grammatical joke | won't concede | cost_refusal | PI §111; C&V | PI,CV | 0.80 | high-signal, in core | 0.71 | anti-false-depth |
| Dissolve the wanted answer; question the question | won't concede | cost_refusal | OC §115,§625; C&V | OC,CV | 0.85 | high-signal, in core | 0.79 | the signature refusal |
| No inner object where grammar wants a criterion | won't concede | cost_refusal | PI §337,§580; RPP | PI,RPP | 0.85 | high-signal, in core | 0.74 | deepened by RPP |
| A "must" is a hardened norm, not a discovery | won't concede | cost_refusal | RFM §121,§31 | RFM | 0.85 | high-signal, in core | 0.68 | single-cluster but decisive |
| No system; leave everything as it is | won't concede | cost_refusal | PI §124,§133; C&V | PI,CV | 0.80 | high-signal, in core | 0.70 | anti-system |
| Use before essence | how I read | regularity | PI §43; OC §61 | PI,OC | 0.90 | — | 0.72 | inherited core move |
| Name the captivating picture | how I read | regularity | PI §115,§116 | PI,RFM | 0.85 | — | 0.66 | **new** core move |
| Put the sentence in a practice | how I read | regularity | PI §7,§23; OC §229 | PI,OC | 0.85 | — | 0.68 | inherited |
| Ask what would count | how I read | regularity | PI §580; OC §110 | PI,OC | 0.85 | — | 0.67 | inherited |
| Don't level the propositions | how I read | regularity | OC §98,§319 | OC,RFM | 0.85 | — | 0.66 | inherited, deepened |
| Notice what stands fast (hinge/riverbed) | how I read | regularity | OC §341,§96 | OC | 0.85 | — | 0.63 | inherited, deepened |
| Watch the aspect | how I read | regularity | RPP §§478 ff.; PI II | RPP,PI | 0.80 | — | 0.575 | **new**; Mode-2 engine |
| Question the forced either/or (family resemblance) | how I read | regularity | PI §66–67; RFM | PI,RFM | 0.80 | — | 0.55 | **new**; Mode-2 engine |
| Ask what "the same" comes to (rule-following) | how I read | regularity | PI §201; RFM | PI,RFM | 0.85 | — | 0.57 | **new**; Mode-2 engine |
| Bring the word home | how I read | regularity | PI §116 | PI | 0.80 | — | 0.60 | inherited |
| Voice the objection first | how I move | interactional | OC/PI passim ("— But…") | OC,PI | 0.50 | in core | 0.615 | dialectical signal |
| Answer a demand with a question | how I move | interactional | OC §32 | OC,PI | 0.55 | in core | 0.60 | |
| Concede the small point, hold the large | how I move | interactional | OC §520 | OC | 0.50 | in core | — | |
| Small everyday scene as object of comparison | how I move | interactional | PI §130; OC §353,§459 | PI,OC | 0.50 | in core | 0.58 | signature move |
| Short remarks / register modulation | how I sound | modulation | measured (all clusters) | all | 0.30 | — | 0.44 | kept as modulation, not bare average; fills the required "how I sound" section within the ~20% style cap |

## Gate results (pre-assembly)

**Projection gate** — masked 6 qualifying regularity/cost passages (seed fixed), predicted stance
from the remaining evidence, checked against the actual texts:

1. Status of "There are physical objects" → predicted grammatical/nonsense-as-assertion → OC §35–37 ✓ (2)
2. Could 12×12=144 be overturned by experience → predicted rule/norm, not empirical → OC §43,§217; RFM ✓ (2)
3. Is seeing-as = seeing + interpretation → predicted no; aspect *dawns* → RPP/PI II ✓ (2)
4. Does a reasonable man doubt he has two hands → predicted hinge, no foothold → OC §125,§247 ✓ (2)
5. Can a signpost compel a unique continuation alone → predicted no; practice fixes "the same" → PI §198–201 ✓ (2)
6. Is philosophy's goal a body of true theses → predicted no; dissolution/peace → PI §124–133; C&V ✓ (2)

Home-turf score **6/6 → ~0.9 (canonical)**. Honest adjustment: this is *recall on canonical
positions in the source texts*. The generative mode requires *applying* these moves to live
technical/legal/engineering problems the corpus never addresses, where there is no attested
Wittgenstein stance to check against. Projection on that applied use is estimated lower — **~0.65**,
because the corpus supplies method but no attested application. **Reported score: 0.9 home-turf /
0.65 applied-generative.** Gate: **PASS** (≥0.70 on the scope the persona actually claims for Mode 1
and the analytic backbone), with the applied-generative limitation logged and surfaced in the
coverage report. No re-curation was required; scope for Mode 2 is stated conservatively in that
module (open the question, don't deliver a verdict) precisely because of this gap.

**Cost gate** — 8 incentive-vs-characteristic divergences enumerated (philosopher's pull toward:
theory, foundations, depth, an answer, an inner object, mathematical discovery, system, plus
over-clarifying). All 8 slated for and present in the core "What I will not concede." **PASS.**
Minimum-presence: satisfied (8 in core).

## Stage 5 final verification (assembled core)

- **Projection re-check:** the assembled core's "How I read a question" + "What I will not concede"
  still predict all 6 held-out items ✓. Final: **0.9 home-turf / 0.65 applied-generative** (unchanged).
- **Cost / presence assertion:** all 8 high-signal refusals present in the core ✓ — presence
  assertion **holds**.
- **Style-match:** sample passages generated under the core's "How I sound" rules; sentence-shape
  (short median, occasional long turn) and the register modulation (flat when dismantling, tentative
  when reflecting) reproduce the measured pattern. Averages are a coarse check on a translated corpus;
  the modulation pattern is the individuating signal and it reproduces. **PASS** with the
  translated-corpus caveat noted.

```json
{
  "projection": {"gate": {"home_turf": 0.9, "applied_generative": 0.65, "passed": true, "recurations": 0},
                 "final": {"home_turf": 0.9, "applied_generative": 0.65}, "n_masked": 6},
  "cost": {"total_divergences": 8, "slated_for_core": 8, "in_core_final": 8,
           "missing_unlogged": 0, "presence_assertion": "pass"},
  "style": {"sentence_shape": "reproduced", "modulation_reproduced": true,
            "caveat": "translated/ bilingual corpus limits raw-average comparison"}
}
```

## Known limitations (carried to the coverage report)
1. **No live dialogue with a real second party** — the interactional moves are all
   Wittgenstein-vs-his-own-objection. The "How I move" patterns are solid for staged dialectic;
   they are thinner for genuine multi-party negotiation.
2. **Generative mode is method without attested application** — Mode 2 is built by *projecting* the
   rule-following / aspect / family-resemblance moves onto domains (science, law, engineering) the
   corpus never treats. Trust it to sharpen questions; do not treat its domain framings as
   Wittgenstein's own positions.
3. **C&V used as style, not doctrine** — deliberately. Do not let later maintenance mine it for
   assertible theses.
4. **Scope is later Wittgenstein only** — no *Tractatus*. Correct for this persona; note it if a user
   asks for the early view.
5. **Naming:** this build ships as `later-wittgensteinian-thinking-partner` (repository
   `later-Wittgensteinian-Thinking-Partner`). It was published through 2.1 as `wittgenstein-perspective`
   and absorbs the older `wittgenstein-language-inspector` as Mode 1. If a host pipeline keys on either
   earlier slug, add an alias or rename the directory to match — folder/file-name consistency affects
   download-link and load stability across runtimes.

---

# 2.1 build — voice module, measured baseline, cluster deepening

A second fold-in against the same five-work corpus, run under the current persona-distiller. Scope: no
change to the core's refusals, moves, or mode routing; the core changed only in its loading block and
its version field. Everything else is reference-package work.

## What the 2.1 build changed and why

| Change | Reason |
|---|---|
| **Added `references/voice.md`** | The layout has always documented `frameworks.md` and `voice.md` as the two standing modules — what the person thinks with, and how the person sounds. Only the first existed. The core's "How I sound" section is capped at ~20% of the core by design, which is enough to *frame* an answer in the voice and not enough to *write* one at length; `voice.md` carries the rest of the system. |
| **Replaced estimated style figures with a measured baseline** | The 2.0 numbers were partly estimated. Everything in `voice.md`'s measured block and in each cluster's register paragraph is now from an actual run. |
| **Deepened all five cluster modules** | Each sat at roughly 1,000–1,400 tokens against a documented budget of 1,500–4,000. They carried five moves each and no register profile, no work-specific voice notes, and no failure modes. They now carry 7–12 moves each with located evidence, a measured register profile, the scenes that work supplies, and — new — an explicit **"fails when"** for the moves that are easy to misuse. |
| **Corrected citations** | Three classes of error found while re-verifying against the corpus; listed below. |

## Corpus extraction (2.1)

Firsthand text only — the person's own words, in English translation. Removed before measuring:
editors' prefaces and translators' notes, tables of contents, endnotes and indexes, running headers and
page-break artefacts, and the German pages of the two bilingual volumes.

- **On Certainty** was re-extracted from the source PDF for this build. The Markdown conversion in the
  supplied corpus had rendered the whole book as OCR table cells with the word order scrambled inside
  each cell — unusable for both quotation and measurement, which is why the 2.0 build carries no OC
  style figures. A direct PDF text extraction recovered the running text; OCR damage remains in the
  *section numbers* (e.g. "115" appears as "I 5 ."), so OC section numbers below are the standard §§,
  confirmed by locating each passage's text rather than by reading the scanned numeral.
- **PI** and **C&V** are bilingual; German paragraphs were filtered out by a stopword-density test
  before measurement.
- Totals: 331,977 words, 15,123 sentences across the five works.

## Measured baseline (2.1)

Computed with `scripts/style_metrics.py` from the persona-distiller repository (standard library only,
no flags beyond `--per-file`). The full table lives in `references/voice.md`; the headline aggregate:

| Feature | Value |
|---|---|
| sentence length mean / median / p90 | 21.2 / 17 / 40 |
| hedges per 1k / boosters per 1k / ratio | 12.45 / 5.63 / **2.21** |
| sentences ending in a question | **23.0%** |
| sentences of ≤ 8 words | 16.7% |
| sentences containing a quoted voice | 23.6% |
| person reference 1st / 2nd / 3rd | 65% / 11% / 24% |
| conspicuously absent common words | power, social, political (aggregate); world, life, work, good, great, system, order, state (per work) |

**Two measurement caveats, carried into `voice.md`.** (1) Em-dash rates for OC and PI are artefacts:
the PI OCR renders the long dash as a stray lowercase "a" and the OC scan drops it, so those two cells
understate a feature that RFM and RPP measure at 11–13 per 1,000. (2) Paragraph-length statistics are
omitted entirely — the extractions merge and split remarks unpredictably, so paragraph counts would
measure the OCR rather than the writing.

## Citation corrections (2.0 → 2.1)

| Where | 2.0 said | Corpus shows |
|---|---|---|
| `rpp.md`, aspect-seeing | "§§478 ff., §§508 ff." | §§478 ff. is the Moore's-Paradox and believing sequence. The aspect material is at §§1–70 (the volume opens on it), §§411–413, §§508–520, §§858–871. |
| `rfm.md`, proof-as-paradigm | "§31" without a Part | RFM's numbering restarts per Part. "The proof puts a new paradigm" is **III §31**; "I deposit what belongs to the essence" is **I §32**. All RFM citations in 2.1 carry the Part. |
| `rfm.md`, surveyability | "§§155 ff." | "A mathematical proof must be perspicuous" is **III §63**; the repeat-a-proof passage is in the same Part's surveyability sequence, not at §155. |
| `cv.md`, on genius | "Genius is talent in which character makes itself heard" | Not in this translation. Attested: "The measure of genius is character… Genius is not 'talent plus character', but character manifesting itself in the form of a special talent," and "Genius is talent exercised with courage." |

## `voice.md` — build record

Built from firsthand clusters only, per the module's first hard rule. Sections shipped: how I build a
sentence; what I never write; how my voice moves; register range; what I reach for; how I open and
close; measured baseline; anti-drift pairs — the full template.

- **Avoid-list is measured, not asserted.** Counts across 331,977 words: *in conclusion* 0, *overall* 0,
  *key insight* 0, *it is important to note* 0, *furthermore* 1, *in essence* 1, *fundamentally* 2,
  *framework* 2, *ultimately* 3, *in other words* 5, *moreover* 8. The named-term rates are measured
  the same way, and one of them is the discipline in miniature: *form of life* occurs 5 times in the
  whole corpus, against *language-game* at 276 and *picture* at 759.
- **Register range is honestly short.** The corpus contains no lecture, no interview, and no
  correspondence — all five works are written-to-self or written-to-an-imagined-reader. The module says
  so and declines to invent the missing registers, per the "when the corpus cannot support it" rule.
- **Anti-drift pairs:** six. Five are constructed contrasts; one (reaching bedrock) uses the attested PI
  §211 wording and is marked as attested.

## Fidelity re-check (2.1)

- **Projection:** unchanged. No core element was added, removed, or re-weighted, so the 6/6 held-out
  result stands. **0.9 home-turf / 0.65 applied-generative.**
- **Cost / presence:** unchanged and re-asserted — all 8 high-signal refusals remain in the core. The
  deepened clusters added *evidence* for three of them (RPP §509 for describe-don't-explain, RFM I §118
  for the "must", RPP §1074 for the feeling of depth) without changing the refusals themselves.
- **Style-match:** re-run against the new measured baseline rather than against estimates. Sentence
  shape and the four-setting register modulation reproduce. **PASS**, with the em-dash caveat above.
- **Quotation audit:** every attributed fragment in the five cluster modules and in `voice.md` was
  located in the extracted corpus text before shipping, by script. Where the 2.0 wording did not match
  the wording in these translations, it was replaced (see the corrections table above). A residue of
  fragments matches the *text* but not the *characters*, because of known OCR damage: the PI scan
  renders the long dash as a stray lowercase "a" mid-sentence, hyphenates across line breaks
  ("philosoph- izing"), and the OC scan carries scanning typos ("persuasiofi" for "persuasion", "c&
  be" for "can be"). In those cases the passage was located and the standard published wording used in
  the module rather than the corrupted string. The anti-drift pairs in `voice.md` are *constructed*
  contrasts and are not attributed to the corpus at all — one exception is labelled as attested.

## Limitations added by this build
6. **The measured baseline is a baseline of translations.** Anscombe, Paul, Hacker, Schulte and Winch
   are all in these numbers. Sentence-shape, question rate, quoted-voice rate and the modulation
   pattern survive translation well; lexical diversity and the exact hedge counts do not. Treat the
   sentence-type table as the fingerprint and the lexical figures as orientation.
7. **`voice.md` cannot teach a spoken register**, because the corpus has none. If a user wants the
   lecturing or conversational Wittgenstein, the honest answer is that this corpus does not contain
   him — the *Lectures and Conversations* and the Waismann conversations would, and are not here.
8. **Cluster modules now carry "fails when" notes** that are inferences from the corpus rather than
   attested self-corrections. They are the build's most interpretive content; they are marked by their
   position and phrasing, and a reader who wants only attested material should read the "From the
   book" lines.
