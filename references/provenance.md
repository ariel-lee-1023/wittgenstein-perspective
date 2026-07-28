# Provenance & fidelity ledger

The honesty file. Everything the core is not allowed to contain — sources, scores, gate outcomes,
caveats — lives here. Corpus: five later-Wittgenstein works supplied by the user. This build was run
as a **fold-in / update** of an existing persona (`wittgenstein-language-inspector`), expanding it
from one mode (inspect finished claims) to three (inspect / think-with / translate). Full-rigor mode.

## Corpus & coverage map

| Cluster | Work | In-context? | Register (measured) | Role |
|---|---|---|---|---|
| c-OC | On Certainty | full text in context | investigative | hinges, riverbed, groundless justification |
| c-PI | Philosophical Investigations (en-face) | text layer extracted | investigative | use, games, criteria, picture, family resemblance, rule-following, German terms |
| c-RPP | Remarks on the Philosophy of Psychology I | text layer extracted | investigative (hedge:booster ≈ 2.4) | aspect-seeing, grammar of the inner, concept-networks |
| c-RFM | Remarks on the Foundations of Mathematics | text layer extracted | assertive (≈ 1.6) | proof-as-paradigm, rule-following, necessity-as-grammatical |
| c-CV | Culture and Value | text layer extracted (bilingual) | tentative/confessional (≈ 3.4) | STYLE source: cadence, dissolution, anti-performance |

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
5. **Naming:** this build ships as `wittgenstein-perspective` and absorbs the old
   `wittgenstein-language-inspector` as Mode 1. If the host pipeline keys on the old slug, either
   rename the directory back or add an alias — folder/file-name consistency affects download-link and
   load stability across runtimes.
