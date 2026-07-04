# Sample Entries

A curated slice of the graph: real, operator-signed nodes with their typed edges, drawn from three brain structures that already interconnect — the **thalamus**, the **anterior cingulate cortex (ACC)**, and the **midcingulate cortex (MCC)**.

Each node carries a unique ID, an entity name, a one-line definition, and **typed edges** to other nodes. The edges are the point: they are what let the graph be *traversed and reasoned across*, not merely read.

> This is a small showcase, not the full corpus (~500 nodes). Full entries, provenance, and graph excerpts are available on request.

---

## Thalamus

**`THAL0000` · bilateral-thalamic-complex** — the paired diencephalic nuclear mass; the highest-level structural container of the thalamus.
- `SUBDIVIDES_INTO →` `THAL0001` dorsal-thalamus-nuclear-system
- `SUBDIVIDES_INTO →` `THAL0002` ventral-thalamus-reticular-shell
- `SUBDIVIDES_INTO →` `THAL0003` metathalamic-geniculate-complex
- `SUBDIVIDES_INTO →` `THAL0004` medullary-laminar-system
- `SUBDIVIDES_INTO →` `THAL0186` habenular-nuclear-complex
- `INCLUDES →` `THAL0204` thalamic-vascular-supply-system

**`THAL0001` · dorsal-thalamus-nuclear-system** — the principal excitatory thalamic nuclear aggregation.
- `PART_OF →` `THAL0000` bilateral-thalamic-complex
- `SUBDIVIDES_INTO →` `THAL0005` anterior-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0006` medial-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0007` lateral-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0008` ventral-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0022` pulvinar-nuclear-complex
- `SUBDIVIDES_INTO →` `THAL0180` midline-thalamic-nuclear-group
- `INCLUDES →` `THAL0187` thalamocortical-projection-architecture

**`THAL0005` · anterior-thalamic-nuclear-group** — limbic memory relay nuclei of the Papez circuit. *A cross-region hub (see the closing section).*
- `PART_OF →` `THAL0001` dorsal-thalamus-nuclear-system
- `SUBDIVIDES_INTO →` `THAL0011` anterior-ventral-thalamic-nucleus
- `SUBDIVIDES_INTO →` `THAL0012` anterior-dorsal-thalamic-nucleus
- `SUBDIVIDES_INTO →` `THAL0013` anterior-medial-thalamic-nucleus
- `RECEIVES_FROM →` `MAMM0001` mammillary-body
- `EXTENDS_TO →` `CING0001` cingulate-cortex
- `EXTENDS_TO →` `RSC0001` retrosplenial-cortex

**`THAL0008` · ventral-thalamic-nuclear-group** — ventral-tier, relay-dominant nuclei.
- `PART_OF →` `THAL0001` dorsal-thalamus-nuclear-system
- `SUBDIVIDES_INTO →` `THAL0026` ventral-anterior-nucleus
- `SUBDIVIDES_INTO →` `THAL0027` ventral-lateral-nucleus
- `SUBDIVIDES_INTO →` `THAL0029` ventral-posterior-nuclear-complex
- `CONTAINS →` `THAL0109` cerebellothalamic-integration-gate

**`THAL0009` · intralaminar-thalamic-nuclear-group** — nuclei embedded within the internal medullary lamina; a driver of cortical arousal.
- `PART_OF →` `THAL0010` internal-medullary-lamina
- `SUBDIVIDES_INTO →` `THAL0173` intralaminar-rostral-cluster
- `SUBDIVIDES_INTO →` `THAL0174` intralaminar-caudal-cluster
- `CONTAINS →` `THAL0193` thalamostriatal-salience-broadcast
- `CONTAINS →` `THAL0103` intralaminar-arousal-amplification

---

## Anterior cingulate cortex (ACC)

**`ACC0002` · subgenual-ACC-area-25** — subgenual anterior cingulate (area 25); a central node in mood regulation and a deep-brain-stimulation target in treatment-resistant depression.
- `PART_OF →` `ACC0000` anterior-cingulate-cortex
- `INCLUDES →` `ACC0015` subgenual-ACC-VEN-projection-population
- `INCLUDES →` `ACC0013` subgenual-ACC-efferent-projection-architecture
- `INCLUDES →` `ACC0014` subgenual-ACC-afferent-input-architecture

**`ACC0004` · pregenual-ACC-area-24** — pregenual anterior cingulate area 24, resolved to its cytoarchitectural subfields.
- `PART_OF →` `ACC0000` anterior-cingulate-cortex
- `SUBDIVIDES_INTO →` `ACC0030` pregenual-ACC-area-24a
- `SUBDIVIDES_INTO →` `ACC0031` pregenual-ACC-area-24b
- `SUBDIVIDES_INTO →` `ACC0033` pregenual-ACC-area-24c

**`ACC0003` · pregenual-ACC-area-32** — pregenual anterior cingulate area 32.
- `PART_OF →` `ACC0000` anterior-cingulate-cortex
- `INCLUDES →` `ACC0021` pregenual-ACC-amygdala-termination-field
- `INCLUDES →` `ACC0022` pregenual-ACC-efferent-projection-architecture

---

## Midcingulate cortex (MCC) — framework entries

Higher-order nodes that capture whole networks and models, not just anatomy.

**`MCC0930` · midcingulo-insular-salience-network-framework** — maps the anterior-midcingulate–anterior-insula salience network across subcortical and limbic nodes.
- `ORGANIZES →` `MCC0102` anterior-midcingulate-cortex
- `ORGANIZES →` `INS-XXXX` anterior-insula *(placeholder — insula not yet built)*

**`MCC0934` · aMCC-affect-pain-control-integration-framework** — maps the convergence of negative affect, pain, and cognitive control on the anterior midcingulate as a shared functional hub.
- `ORGANIZES →` `MCC0102` anterior-midcingulate-cortex

---

## Cross-region connectivity — why this is a *graph*

The structures are not islands. The anterior thalamic nuclei reach into the cingulate — the classic Papez-circuit connection — which lets a query travel from one region into another:

> `THAL0005` anterior-thalamic-nuclear-group  `→ EXTENDS_TO →`  `CING0001` cingulate-cortex

The cingulate cortex is where the ACC corpus lives, so this edge is the bridge that lets reasoning cross from the thalamus into the cingulate region and back. That single traversable path is the difference between a pile of documents and a map you can reason across.

---

## Five-lens depth — REG · COG · ABST, with Shadow Narratives

The structural entries above are one of five analytic lenses. Every structure is also encoded for how it is **regulated (REG)**, what it **does (ACT)**, the **cognitive/experiential states (COG)** tied to it, and the higher-order **abstract models (ABST)** that organize it. Each entry carries a *Shadow Narrative* — the sourced prose reasoning behind the node. Three edge-rich examples, all from the ACC:

### REG · `ACC0300` ACC-VIP-disinhibitory-gate-regime
*SUPPRESS / attenuate · S2 · OC: SST control of pyramidal apical tufts via interneuron suppression*
- `MODULATES →` `ACC0301` ACC-SST-apical-gating-regime
- `IS_MODULATED_BY →` `ACC0304` ACC-nicotinic-VIP-access-regime
- `IS_INSTANTIATED_IN →` `ACC0053` ACC-VIP-interneuron-population
- `PART_OF →` `ACC0351` ACC-disinhibition-dominant-regulatory-principle

> **Shadow.** VIP interneurons inhibit SST interneurons, releasing pyramidal apical tufts from dendritic inhibition and increasing effective synaptic gain for convergent cortical and thalamic inputs. This disinhibitory gate is the primary mechanism through which cholinergic, serotonergic, and glutamatergic inputs regulate dendritic integration in ACC. VIP interneurons have been causally implicated in prediction-error computation (Nature 2024). The VIP→SST→pyramidal disinhibitory motif is the dominant routing architecture in ACC microcircuits.

### COG · `ACC0705` ACC-chronic-pain-experiential-state
*MAKE / evoke · S3 · OC: aversive affect with anticipatory dread*
- `IS_RESULT_OF →` `ACC0509` ACC-nerve-injury-LTP-amplification-event
- `IS_RESULT_OF →` `ACC0512` ACC-amputation-LTD-abolition-event
- `PART_OF →` `ACC0000` ACC

> **Shadow.** The chronic pain experiential state has a two-dimensional phenomenal structure: an affective component (unpleasantness) and an anticipatory component (dread). The two are dissociable and supported by distinct plasticity mechanisms — postsynaptic NMDAR-dependent LTP sustains the affective dimension (Koga et al. 2015); presynaptic kainate-dependent LTP sustains the anticipatory dimension. Concurrent LTP saturation and LTD abolition remove homeostatic correction, locking the state into persistence. It is the "emoji layer" above the plasticity machinery — what it is like to be in chronic pain, with both misery now and dread of misery to come (Bliss et al. 2016).

### ABST · `ACC0920` ACC-exogenous-perturbation-domain — **17 edges**
*CODE / label · S3 · categorical container · OC: categorizes ACC-related intervention events altering system operating state*
- `CLASSIFIES →` seventeen external-perturbation events, including `ACC0550` cingulotomy-ablation · `ACC0556` subgenual-deep-brain-stimulation · `ACC0567` subanesthetic-ketamine-exposure · `ACC0560` SSRI-raphe-desensitization · `ACC0555` TBI-diffuse-axonal-injury · `ACC0557` optogenetic-inhibition · `ACC0509` nerve-injury-LTP · `ACC0580` chronic-mild-stress …

> **Shadow.** Groups perturbations originating outside the ACC system — injury, pharmacology, stimulation, experimental paradigms — that impose state changes on ACC circuitry rather than emerging from intrinsic dynamics. Membership is set by external imposition. The categorical layer supports cross-entry traversal and domain-level analysis without duplicating the structural/causal edges each event already carries. Boundary case: placebo-analgesia is excluded despite its externally framed context, because the encoded event is endogenous μ-opioid release — the boundary is the source of imposition, not the framing of the paradigm.

---

*Every node here is operator-signed and provenance-tracked, built to a fixed doctrine so it behaves as a stable, queryable graph node. Representative sample only; the full corpus and detailed provenance are available on request.*
