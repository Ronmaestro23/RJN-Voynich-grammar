# Quick Start: How to Parse Voynichese in the RJN Model

This file gives a practical first-pass guide for parsing Voynichese according to the RJN Voynich Grammar model.

The goal is not to translate tokens as ordinary words.  
The goal is to parse them as compressed structural operator-chains.

Core principle:

> Voynich tokens are not ordinary lexical words.  
> They are compact procedural chains built from glyph roles, operator families, and closure markers.

---

## 1. Basic parsing rule

Always parse from larger defined families to smaller components.

Use this order:

1. Recognize defined compound families first:
   - `cth`
   - `ckh`
   - `cph`
   - `cfh`
   - `ch`
   - `sh`

2. Then parse remaining parts as smaller glyphs or modules:
   - `q`
   - `p`
   - `f`
   - `o`
   - `a`
   - `d`
   - `y`
   - `e`
   - `i / ii / iii`
   - `n`
   - `l`
   - `r`
   - `m`
   - `k`
   - `t`
   - `s`
   - `h`
   - `c`
   - `x`

3. Treat rare standalone or uncertain forms conservatively:
   - `c`
   - `g`
   - `z`
   - `v`

These rare forms are retained as fallback or transcription-sensitive flags.  
They are not used to create new grammar rules.

---

## 2. Main glyph roles

| Glyph / family | Structural role |
|---|---|
| `q` | Strong external initiation / process start / flow start |
| `p` | Operational initiation / procedure start / subprocedure start |
| `f` | Material, preparatory, or variant initiation |
| `o` | Process field / node / base field |
| `a` | Transition / toward / into next state or phase |
| `d` | Transformation / processing |
| `y` | Boundary / closure / finalization |
| `e` | Grade / intensity / internal differentiation |
| `i / ii / iii` | Phase count / sequence number |
| `n` | Phase boundary / stage endpoint |
| `l` | Local carrier / locality |
| `r` | Relation / output direction |
| `m` | Terminal mass / base / residue |
| `k` | Stabilization / fixation / left-binding connector |
| `t` | Transfer / routing |
| `s` | Regulation / status |
| `h` | Activation / execution / internal activation binder |
| `c` | Structural coupling stem / compositional binder |
| `ch` | Active coupled frame |
| `sh` | Activated regulation/status |
| `cth` | Active coupled transfer |
| `ckh` | Active coupled stabilization |
| `cph` | Active coupled procedure/separation |
| `cfh` | Active coupled variant/preparation |
| `x` | Separator / divider / boundary / framing marker |

---

## 3. Fallback and transcription-sensitive forms

| Form | Treatment |
|---|---|
| `c` | Standalone or reduced coupling stem; treated conservatively as transcription-sensitive when an expected coupled continuation `h`, `t`, `k`, `p`, or `f` is absent |
| `g` | Rare terminal residue / closure variant; likely transcription-sensitive or terminal scribal variant |
| `z` | Rare exceptional boundary marker; likely transcription-sensitive |
| `v` | Rare variant marker; likely transcription-sensitive |

These forms do not break the structural grammar.  
They are retained as flags for manuscript review, witness comparison, and possible transcription uncertainty.

---

## 4. Difference between family parse and internal composition

Some forms can be read at two levels.

Example:

```text
cth

Primary family parse:

cth = Active coupled transfer

Internal composition:

c + t + h
= coupling stem + transfer/routing + activation

Both are valid, but they operate at different levels.

For first-pass parsing, use the family reading first.

5. Token examples
Example 1: cth
cth
= active coupled transfer

Internal composition:

c + t + h
= coupling + transfer + activation

Functional reading:

an activated coupled transfer operation
Example 2: ch
ch
= active coupled frame

Internal composition:

c + h
= coupling + activation

Functional reading:

an activated coupled process frame
Example 3: sh
sh
= activated regulation/status

Internal composition:

s + h
= regulation/status + activation

Functional reading:

activated regulation or status control
Example 4: daiin
d + a + ii + n

Components:

d    = transformation / processing
a    = transition / toward next state
ii  = Phase count / sequence number
n   = Phase boundary / stage endpoint

Functional reading:

processed into a marked phase or stabilized process state

Short structural reading:

transformation into phase-state
Example 5: qokaiin

Possible parse:

q + o + k + a + ii + n

Components:

q    = process start / flow start
o    = process field / base field
k    = stabilization / fixation
a    = transition into next state
ii  = Phase count / sequence number
n   = Phase boundary / stage endpoint

Functional reading:

start a process field, stabilize it, and move it into a marked phase-state
Example 6: qotaiin

Possible parse:

q + o + t + a + ii + n

Components:

q    = process start / flow start
o    = process field / base field
t    = transfer / routing
a    = transition into next state
ii  = Phase count / sequence number
n   = Phase boundary / stage endpoint

Functional reading:

start a process field, route or transfer it, and move it into a marked phase-state
Example 7: ckh
ckh
= active coupled stabilization

Internal composition:

c + k + h
= coupling + stabilization + activation

Functional reading:

activated coupled stabilization
Example 8: cph
cph
= active coupled procedure/separation

Internal composition:

c + p + h
= coupling + procedure/subprocedure + activation

Functional reading:

activated coupled procedure or separation operation
Example 9: cfh
cfh
= active coupled variant/preparation

Internal composition:

c + f + h
= coupling + material/preparatory/variant initiation + activation

Functional reading:

activated coupled preparatory or variant operation
Example 10: dy
d + y

Components:

d = transformation / processing
y = boundary / closure / finalization

Functional reading:

local closure of a processing step

Short structural reading:

hard local closure
6. How to parse a line

A line should not be treated as a sentence in an ordinary language.

Instead, treat the line as a visible segment of a larger procedural sequence.

Example line:

qokaiin cth daiin dy

Step-by-step parse:

qokaiin = q + o + k + a + ii + n
cth     = active coupled transfer
daiin   = d + a + ii + n
dy      = d + y

Structural reading:

Start and stabilize a process field into a marked phase;
perform an active coupled transfer;
process into a phase-state;
close the local step.

Important:

LINE != syntactic unit
FOLIO != syntactic unit
SEQUENCE = primary unit

Lines and folios are visual units.
Sequences are the logical units.

7. How to parse a sequence

A full sequence is usually organized as a procedural chain.

General model:

MACRO_SEQUENCE =
    P_START?
    + SETUP_BLOCK+
    + TRANSITION_BLOCK*
    + Q_CORE_BLOCK+
    + CLOSURE_BLOCK+

Meaning:

P_START?          = optional macro/procedure opening
SETUP_BLOCK+      = setup or preparation phase
TRANSITION_BLOCK* = optional transition or activation phase
Q_CORE_BLOCK+     = active process core
CLOSURE_BLOCK+    = closure, stabilization, or finalization

The sequence is usually more important than the line.

8. Macro-level roles
p as macro/procedure start

p often marks a new main procedure, subprocedure, or macro-block.

p = operational initiation / procedure start / subprocedure start
q as active process start

q often starts an internal operation or process step.

q = strong external initiation / process start / flow start
d as transformation and closure trigger

d is the main transformation/processing marker and often participates in closure forms.

d = transformation / processing
dy = hard local closure
daiin = processed/stabilized phase-state
dar = local output direction
dol = local carrier or vessel-like closure
dam = terminal mass/base/residue closure
y as boundary and closure marker

y often marks a boundary, closure, edge, or finalization point.

y = boundary / closure / finalization
9. Do not create free translations

This model does not read Voynichese as ordinary word-by-word language.

Avoid this:

token = ordinary word
line = ordinary sentence
page = ordinary paragraph

Use this instead:

token = compressed operator-chain
line = visual segment
sequence = procedural unit
folio = physical layout unit
10. Conservative correction rule

The grammar does not require free correction of the corpus.

Rare forms may be flagged as:

fallback
transcription-sensitive
witness-sensitive
reduced
terminal
variant

But they must not be used to invent new grammar rules.

Core rule:

Fallback forms are accepted only as conservative flags, not as evidence for new grammar rules.
11. Minimal parser workflow

Use this workflow for any token:

Identify known compound families first:
cth, ckh, cph, cfh, ch, sh
Split the remaining token into known glyph roles.
Mark rare or unresolved forms as fallback/transcription-sensitive.
Do not force ordinary lexical translation.
Convert the token into a structural operator-chain.
Read the token within the larger sequence, not in isolation.
12. Minimal worked example

Token:

qokaiin

Parse:

q + o + k + a + ii + n

Roles:

q    process start / flow start
o    process field / base field
k    stabilization / fixation
a    transition into next state
ii  = Phase count / sequence number
n   = Phase boundary / stage endpoint

Structural reading:

Start a process field, stabilize it, and move it into a marked phase-state.

Not a normal word.

It is a procedural operator-chain.

13. What counts as a successful parse?

A successful parse does not need to produce a modern-language sentence.

A successful parse should show:

the internal operator structure of the token;
the role of the token inside the line or sequence;
whether the token belongs to setup, transition, active core, or closure;
whether any part is fallback or transcription-sensitive.

A strong parse is therefore structural before it is semantic.

## 14. What the parser should output

For every token, the parser should output:

1. the original token;
2. the structural split;
3. the glyph/family roles;
4. whether any component is fallback/transcription-sensitive;
5. the short structural reading.

Example:  

Token:  

qokaiin  

Output:  

qokaiin  
= q + o + k + a + ii + n  

q    = process start / flow start  
o    = process field / base field  
k    = stabilization / fixation  
a    = transition into next state  
ii  = Phase count / sequence number
n   = Phase boundary / stage endpoint 

Structural reading:  
start a process field, stabilize it, and move it into a marked phase-state  

Fallback flags:  
none  

For a full line, the parser should output each token separately first.  

Only after token parsing should the line be read as part of a larger sequence.  

Important:  

Do not force the line into an ordinary sentence.  
Do not invent new rules from rare forms.  
Do not treat fallback forms as semantic discoveries.  

## 15. Summary

The RJN model parses Voynichese as a recursive process-operator system.

The basic reading method is:

glyph roles
→ operator families
→ token chains
→ line segments
→ macro-sequences
→ procedural structure

The central claim is not that each token is an ordinary word.

The central claim is that Voynichese is a structured procedural notation system built from recurring operator roles.  
