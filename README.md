# Voynich-Process-Operator-Grammar
Full decipherment with grammar on all sections
# Recursive Structural Decipherment of Voynichese

## Core reading principle

**Voynich tokens are not words.  
They are compressed operator-chains functioning as procedural instructions.**

Voynichese is therefore not decoded word-by-word.  
It is parsed sequence-by-sequence through a structural-functional operator grammar.

## Reproducibility note: transcription baseline and witness control

A reproduction attempt should use the same controlled transcription and witness protocol.

The parser was not developed on an uncontrolled mixed transcription. A crucial intermediate step was the Herbal H rule-set and correction protocol, which stabilizes the input layer before grammar is tested.

This matters because transcription artefacts can otherwise be mistaken for grammatical exceptions.

In short:

**Before the grammar can be tested, the transcription layer must be controlled.**

### Reproducible Herbal H derivation baseline

The reproducible derivation baseline used for the Herbal H rule-set is:

- Herbal section only
- H-lines only
- up to and including f57r
- f1r and f49v excluded as special/key pages
- repeated `e` and `i` collapsed to single `e` / `i`
- rule induction performed on baseline-H
- whole corpus used only for error checking
- `.py` and `.txt` used as the reproducible working file types

This baseline was used to derive the operational module rules, positional behavior, stop logic, and generator evaluation.

The Herbal H generator statistics belong to this defined baseline. They should not be blindly assumed to apply identically to every other manuscript section.

### Correction rule

A token may not be corrected freely or semantically.

If an H-token breaks the operative H-line rules, it is checked against the whole corpus. If the token occurs only rarely, it may be treated as a possible transcription problem.

It may only be replaced by a legal token from another witness on the same line and the same position.

If no legal witness replacement exists, the form is retained as a problem token and may not be used to expand the grammar.

The correction protocol is therefore conservative:

- H is the primary working witness.
- Other witnesses may confirm, question, or refine an H-reading.
- Whole-corpus frequency may identify likely transcription instability.
- No reading is corrected merely because the model would prefer it.
- No rare anomaly may be promoted into a new grammar rule without independent support.

A transcription problem must not be mistaken for a grammar problem.

A grammar problem must not be solved by arbitrary transcription correction.

### Corpus-wide use of the witness protocol

The witness-control protocol is intended to be used across the whole corpus.

The same principles apply beyond Herbal H:

- do not correct freely or semantically
- check anomalous H-forms against other witnesses
- use whole-corpus frequency only as an error filter
- accept replacement only from the same line and same position
- retain unresolved forms as problem tokens rather than expanding the grammar

However, the Herbal H generator statistics should not be treated as a universal frequency model for the whole manuscript.

Other regimes such as BALNEO, PHARMA, ASTRO, and STAR/TEXT may preserve the same underlying operator grammar while using different frequency profiles, stop behavior, dominant token families, visual constraints, and section-specific bias.

Therefore:

**The witness protocol is corpus-wide.**  
**The Herbal H baseline is the reproducible derivation base.**  
**Regime transfer must be tested section by section.**

### Operational level vs. deeper split level

The Herbal H report distinguishes between two split levels:

1. **Operational split level**  
   The validated level used in the reproducible generator and rule evaluation.

2. **Deeper hypothetical split level**  
   A finer operator layer where forms such as `chol` may be analyzed as `ch + ol`, and `chey` as `ch + e + y`.

The deeper split level is important for the final structural-functional parser, but it must not be confused with the earlier reproducible Herbal H baseline.

The correct development path is:

- first stabilize the transcription layer
- then derive operational modules
- then test positional and stop behavior
- then evaluate generator reproduction
- then move to deeper operator splitting
- then test regime transfer across the manuscript

### Why this matters

Many early scripts failed or produced unstable results because transcription noise affected token forms, suffixes, apparent exceptions, and module boundaries.

Without witness control, a reproduction attempt may accidentally test transcription noise rather than Voynich grammar.

The purpose of the H-/witness protocol is not to make the model easier to fit. Its purpose is the opposite: to prevent arbitrary correction, preserve problematic forms, and stop transcription artefacts from becoming false grammar.

This is why the parser should be tested only after the transcription layer has been controlled.

## A Hierarchical Functional Process-Operator Grammar

This repository presents a mathematically and statistically derived structural decipherment of Voynichese as a recursive hierarchical process-operator grammar.

The model was not derived from a prior language theory, cipher hypothesis, botanical identification, or alchemical doctrine. It emerged through a staged computational investigation of glyph behavior, token segmentation, positional constraints, macro-sequence structure, recursive module formation, closure behavior, regime variation, and key-page alignment.

The central result is that Voynichese is not best explained as meaningless pseudo-text, ordinary prose, or a simple substitution cipher. Its structure resolves as a technical process notation in which glyphs, tokens, operator chains, macro-sequences, and diagrammatic regimes interact through stable grammatical roles.

---

## Core Claim

Voynichese is a recursive hierarchical process script.

Glyphs form tokens.
Tokens form operator chains.
Operator chains form macro-sequences.
Macro-sequences are interpreted through page-specific diagrammatic regimes.

The primary syntactic unit is not the word, line, folio, or paragraph. The primary unit is the sequence.

```text
LINE  != syntactic unit
FOLIO != syntactic unit
SEQUENCE = primary syntactic unit
```

---

## Claim Hierarchy

| Level | Claim | Status |
|---|---|---|
| A | Voynichese is a recursive hierarchical process-operator grammar. | Central demonstrated structural claim |
| B | Glyphs, tokens, macroforms, and sequence zones carry stable functional roles. | Strongly supported functional model |
| C | The visual system is grammatical and acts as a parallel classifier system. | Strongly supported diagrammatic claim |
| D | The functional roles correspond to technical medical, apothecary, and alchemical procedures. | Historical interpretation layer |
| E | The same grammar is diagrammed across herbal, balneo, pharma, astro, rosettes, zodiac, and star regimes. | Cross-regime extension |

## Methodological Origin

The investigation began without a proposed source language, cipher system, plant taxonomy, or alchemical reading.

The initial assumptions were minimal and material:

* the manuscript appears visually planned;
* the text is coordinated with drawings;
* the parchment was costly;
* the scribe was trained and confident;
* the work likely encoded a serious learned technical system.

The parser emerged after extensive computational testing. More than one thousand scripts tested glyph positions, token starts and endings, token decomposition, mini-token reuse, boundary roles, line roles, module discovery, recursive segmentation, grammar extraction, surface parsing, generation models, closure behavior, operation phases, entry transitions, and key-page signatures.

The apothecary/alchemical interpretation became plausible only after the structural parser and process roles had already emerged.

---

## Development Pipeline

The derivation passed through a staged computational pipeline, including tests for:

* boundary roles;
* line roles;
* sequence role classification;
* boundary prediction;
* module discovery;
* module validation;
* recursive segmentation;
* token decomposition;
* grammar extraction;
* corpus-validated surface parsing;
* symbol-role constraints;
* hierarchical module roles;
* closure-terminal behavior;
* operation sequence modeling;
* operation phase modeling;
* entry-transition matrices;
* entry-chain trigram behavior;
* line-phase coherence;
* f49v margin alignment;
* f49v margin signatures;
* manual margin glyph group tests.

The result is a model with both bottom-up mathematical/statistical grounding and top-down grammatical coherence.

---

## Formal Grammar Overview

The strongest form of the model is sequence-compositional and regime-dispatched.

```text
SYSTEM = REGIME_DISPATCHER(MACRO_SEQUENCE+)

MACRO_SEQUENCE =
    P_START?
  + SETUP_BLOCK+
  + TRANSITION_BLOCK*
  + Q_CORE_BLOCK+
  + CLOSURE_BLOCK+

TOKEN = PREFIX* + CORE + SUFFIX*

Q_BLOCK =
    q
  + OPERATION_CLUSTER
  + LOCAL_CLOSURE*
```

A full macro-sequence typically contains setup, transition, active q-core, and closure.

```text
P_START        = macro-start / procedure-start
SETUP_BLOCK    = preparation, ordering, distribution
TRANSITION     = activation passage toward the core
Q_CORE_BLOCK   = active process motor
CLOSURE_BLOCK  = stabilization, output, terminal base, or local closure
```

---

## Macro-Sequence Grammar

A recurring macro-sequence normally follows this form:

```text
P_START
  -> SETUP
  -> TRANSITION
  -> Q_CORE
  -> CLOSURE
```

`p` frequently marks macro-starts, while `q` marks internal active operations.

The closure zone is usually not a single endpoint. It is often zonal and hierarchical.

```text
CLOSURE_BLOCK = D_BLOCK+
D_BLOCK = d + (y | aiin | ar | ol | am | other_closure_module)
```

Representative closure hierarchy:

```text
dy    = transformation + end / closure
daiin = transformation to second phase or stable block ending
dar   = transformation to output
dol   = transformation into local carrier or vessel passage
dam   = transformation to terminal base
```

The sign `d` is not redefined in each compound. It remains a transformation or processing trigger. The following module determines the closure target.

---

## Recursion

The grammar is recursive.

`q`-blocks may contain smaller `q`-blocks. Closure can occur locally and globally. Macro-sequences may also contain embedded subsequences.

```text
Q_CORE = Q_BLOCK+

Q_BLOCK =
    q
  + OPERATION
  + Q_BLOCK?
  + CLOSURE?
```

This explains why Voynichese can appear repetitive while still behaving as structured process notation.

---

## Primitive Operator Inventory

The primitive inventory is kept maximally consistent. A glyph retains its functional role unless a higher macro-binding is active.

Core examples:

| Glyph / family | Structural role |
|---|---|
| q | Strong external initiation / process start / flow start |
| p | Operational initiation / procedure start / subprocedure start |
| f | Material, preparatory, or variant initiation |
| o | Process field / node / base field |
| a | Transition toward a state or phase |
| d | Transformation / processing / closure trigger |
| y | Boundary / closure / finalization |
| e | Grade, intensity, internal differentiation |
| i / ii | Phase or sequence marking |
| ch | Basal operator |
| cth | Strengthened or full operator |
| cph | Specialized parallel operator |
| k | Prefix binder / left connector |
| h | Internal binder |
Compound forms are treated compositionally rather than as isolated lexical words.

For example:

```text
d + y    -> dy
d + aiin -> daiin
d + ar   -> dar
d + ol   -> dol
d + am   -> dam
```

---

## Diagrammatic Grammar

The visual program is treated as a parallel grammar rather than decoration.

Roots, stems, leaves, flowers, stars, human figures, animal-like structures, teeth, claws, bones, scales, heads, containers, and chambers function as diagrammatic classifiers.

Different page regimes organize the same operator inventory differently:

* herbal pages compress vertical process diagrams;
* balneo pages unfold hydraulic and reservoir logic;
* pharma pages encode vessels, containers, and substance classes;
* astro and star pages use nodes, stars, labels, and radial structures as process categories;
* rosettes and special pages expose large-scale system architecture;
* key pages such as f49v and f66r function as operator demonstrations rather than ordinary prose.

---

## Repository Scope

This repository is intended to document:

1. the structural parser;
2. the macro-sequence grammar;
3. the primitive operator inventory;
4. the recursive token and sequence model;
5. the regime dispatcher;
6. the diagrammatic classifier system;
7. the computational derivation pipeline;
8. selected case studies and key-page alignments.

The repository does not claim that every historical substance name has been identified. The core claim is structural and grammatical.

---

## Recommended Reading Order

1. Start with the main paper draft.
2. Review the formal grammar overview.
3. Examine the parse-tree examples.
4. Review the script log and development pipeline.
5. Compare the corpus examples against the macro-sequence model.
6. Study the key-page tests, especially f49v and f66r.
7. Review the regime-specific interpretations.

---

## Minimal Model

The minimal generative model is:

```text
SYSTEM = MACRO_SEQUENCE+

MACRO_SEQUENCE =
    P_START?
  + SETUP_BLOCK+
  + TRANSITION_BLOCK*
  + Q_CORE_BLOCK+
  + CLOSURE_BLOCK+

Q_CORE_BLOCK = Q_BLOCK+

Q_BLOCK =
    q
  + OPERATION_CLUSTER
  + LOCAL_CLOSURE*

CLOSURE_BLOCK = D_BLOCK+

D_BLOCK = d + CLOSURE_TARGET
```

The essential reading principle is:

```text
Voynichese is not decoded word-by-word.
Voynichese is parsed sequence-by-sequence.
```

---

## Status

Working draft for public repository release and specialist review.

The current model presents a complete structural decipherment of Voynichese as a recursive hierarchical functional process-operator grammar. The structural layer is mathematically and statistically derived. The historical recipe layer is presented as the strongest current interpretation of the derived functional roles.
This repository documents the author’s original public disclosure of the structural-functional Voynich parser, operator inventory, grammar model, and working word list.

## How to cite

Ronny Juul Nielsen. A Recursive Structural Decipherment of Voynichese as a Hierarchical Functional Process-Operator Grammar. Working draft, May 2026. GitHub repository: Ronmaestro23/RJN-Voynich-grammar-and-word-list.

Use, testing, criticism, or derivative work based on this structural-functional Voynich parser, operator grammar, word list, or interpretive framework should cite the author and repository.


## Author

Ronny Juul Nielsen  
May 2026

## License

Code and analysis scripts are licensed under the MIT License.

Documentation, paper drafts, diagrams, interpretive framework, structural grammar model, and explanatory material are licensed under Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0), unless otherwise stated.

## Citation / priority

This repository presents the structural-functional process-operator grammar model of Voynichese developed by Ronny Juul Nielsen.

If you use the operator inventory, parser model, token-as-operator-chain principle, regime dispatcher, or folio demonstrations from this repository, please cite this repository and the accompanying parser paper.

Core model:
Voynich tokens are not words. They are compressed operator-chains functioning as procedural instructions.

Public working release: May 2026.
Author: Ronny Juul Nielsen.

© 2026 Ronny Juul Nielsen.
