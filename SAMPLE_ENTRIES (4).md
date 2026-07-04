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

## Projection architectures — the graph reaching across the brain

Each structure carries a projection-architecture node: how it reaches out, or takes input, across the brain. These are among the most edge-dense entries in the corpus — and they **interlock**. `THAL0005` is the shared hub: the ACC projects *to* it, it projects *onward* to the cingulate, and the MCC receives *from* it. Three structures wired through one nucleus.

### Thalamus · `THAL0005` anterior-thalamic-nuclear-group — 8 edges
- `SUBDIVIDES_INTO →` `THAL0011` · `THAL0012` · `THAL0013` (AV / AD / AM nuclei)
- `RECEIVES_FROM →` `MAMM0001` mammillary-body
- `EXTENDS_TO →` `CING0001` cingulate-cortex
- `EXTENDS_TO →` `RSC0001` retrosplenial-cortex

### ACC · `ACC0013` subgenual-ACC-efferent-projection-architecture — 9 edges
*The area-25 output system: multi-channel deep-layer output to limbic, thalamic, striatal, and brainstem domains.*
- `PART_OF →` `ACC0002` subgenual-ACC-area-25
- `INCLUDES →` `ACC0015` · `ACC0016` · `ACC0017` (VEN / L5a-IT / L5b-ET projection populations)
- `EXTENDS_TO →` **`THAL0191`** mediodorsal-thalamic-nucleus · **`THAL0005`** anterior-thalamic-nuclear-group
- `EXTENDS_TO →` `AMYG00XX` amygdala · `HYPO00XX` hypothalamus · `PAG00XX` periaqueductal-gray *(placeholders)*

> The ACC's output loops straight back into the thalamus (`THAL0005` / `THAL0191`) — the reciprocal of the thalamic entry above.

### MCC · `MCC0170` MCC-afferent-projection-architecture — 16 edges
*Convergent, source-segregated, laminar-differentiated afferent input.*
- `RECEIVES_FROM ←` six **resolved** thalamic nuclei: **`THAL0005`** anterior · `THAL0191` mediodorsal · `THAL0180` midline · `THAL0009` intralaminar · `THAL0026` VA · `THAL0027` VL
- `RECEIVES_FROM ←` ten cortical/limbic sources staged as placeholders (amygdala, orbitofrontal, insula, entorhinal, dlPFC, premotor, SMA, M1, parietal) — edge-complete, awaiting their own builds.

---

## Cross-region connectivity — why this is a *graph*

The structures are not islands. The anterior thalamic nuclei reach into the cingulate — the classic Papez-circuit connection — which lets a query travel from one region into another:

> `THAL0005` anterior-thalamic-nuclear-group  `→ EXTENDS_TO →`  `CING0001` cingulate-cortex

The cingulate cortex is where the ACC corpus lives, so this edge is the bridge that lets reasoning cross from the thalamus into the cingulate region and back. That single traversable path is the difference between a pile of documents and a map you can reason across.

---

## Depth and edges — five ACC lenses + two thalamic hubs

Every structure is encoded across five lenses: **structure (STR)**, **regulation (REG)**, **activity (ACT)**, **cognitive/experiential states (COG)**, and higher-order **abstract models (ABST)**. Each entry carries typed edges to real target nodes and a *Shadow Narrative*. Best-of-the-best from the ACC, one per lens, followed by two edge-dense thalamic hubs.

### STR · `ACC0100` ACC-receptor-laminar-and-gradient-architecture — 20 edges
*MAKE / form · OC: organized receptor landscape across 15 quantified types with laminar density and gradient variation*
- `PART_OF →` `ACC0000` anterior-cingulate-cortex
- `INCLUDES →` `ACC0101` AMPA-receptor-laminar-distribution
- `INCLUDES →` `ACC0102` kainate-receptor-laminar-distribution
- `INCLUDES →` `ACC0103` NMDA-receptor-laminar-distribution
- `INCLUDES →` `ACC0104` GABAA-receptor-distribution
- `INCLUDES →` `ACC0105` sgACC-GABA-receptor-enrichment
- `INCLUDES →` `ACC0106` 5HT1A-receptor-gradient-architecture
- `INCLUDES →` `ACC0108` 5HT2A-receptor-laminar-architecture
- `INCLUDES →` `ACC0110` D1-receptor-gradient-architecture
- `INCLUDES →` `ACC0112` alpha2A-receptor-laminar-distribution
- `INCLUDES →` `ACC0114` alpha1-receptor-gradient-architecture
- `INCLUDES →` `ACC0115` mu-opioid-receptor-laminar-distribution
- `INCLUDES →` `ACC0116` delta-opioid-receptor-laminar-distribution
- `INCLUDES →` `ACC0117` kappa-opioid-receptor-laminar-distribution
- `INCLUDES →` `ACC0118` M1-muscarinic-receptor-laminar-distribution
- `INCLUDES →` `ACC0119` M2-muscarinic-receptor-distribution
- `INCLUDES →` `ACC0121` nicotinic-receptor-laminar-distribution
- `INCLUDES →` `ACC0123` 5HT3-receptor-distribution
- `INCLUDES →` `ACC0132` 5HT1B-receptor-distribution
- `INCLUDES →` `ACC0133` 5HT2C-receptor-distribution

> **Shadow.** Quantitative autoradiography across 15 receptor types establishes ACC as a receptor-defined cortical territory with internally differentiated laminar and regional architecture. Glutamatergic receptors separate across cortical depth; GABAergic receptors show a global-low/local-exception pattern; serotonergic receptors divide into gradient- and lamina-weighted systems; cholinergic and opioid receptors add subtype-specific depth structure. Together they define a coherent architectural fingerprint that organizes the downstream subtype entries this container houses. *(Palomero-Gallagher et al. 2008, 2009.)*

### REG · `ACC0300` ACC-VIP-disinhibitory-gate-regime — 4 edges
*SUPPRESS / attenuate · OC: SST control of pyramidal apical tufts via interneuron suppression*
- `MODULATES →` `ACC0301` ACC-SST-apical-gating-regime
- `IS_MODULATED_BY →` `ACC0304` ACC-nicotinic-VIP-access-regime
- `IS_INSTANTIATED_IN →` `ACC0053` ACC-VIP-interneuron-population
- `PART_OF →` `ACC0351` ACC-disinhibition-dominant-regulatory-principle

> **Shadow.** VIP interneurons inhibit SST interneurons, releasing pyramidal apical tufts from dendritic inhibition and increasing effective synaptic gain for convergent cortical and thalamic inputs. This disinhibitory gate is the primary mechanism through which cholinergic, serotonergic, and glutamatergic inputs regulate dendritic integration in ACC. VIP interneurons have been causally implicated in prediction-error computation (Nature 2024). The VIP→SST→pyramidal disinhibitory motif is the dominant routing architecture in ACC microcircuits.

### ACT · `ACC0520` ACC-sgACC-depressive-hyperactivation-event — 6 edges
*AMPLIFY / escalate · OC: sustained elevated excitatory activity*
- `EXECUTES_ON →` `ACC0002` subgenual-ACC-area-25
- `IS_MODULATED_BY →` `ACC0352` ACC-depression-SST-expression-erosion
- `IS_MODULATED_BY →` `ACC0365` ACC-stress-induced-CCK-perisomatic-inhibition
- `RESULTS_IN →` `ACC0707` ACC-depressive-experiential-state
- `PART_OF →` `ACC0000` anterior-cingulate-cortex
- `IS_CLASSIFIED_AS →` `ACC0921` ACC-endogenous-perturbation-domain

> **Shadow.** sgACC (Brodmann area 25) in major depression shows sustained elevated excitatory output on fMRI/PET, with elevated glutamate and reduced GABA on spectroscopy. The hyperactive state develops alongside somatostatin-interneuron erosion and reduced cortical GABA, disinhibiting pyramidal output. Unlike bounded pharmacological events, this is a trajectory-scale configuration persisting weeks-to-months — the most reproducible neuroimaging biomarker of treatment-resistant depression (Mayberg). Remediable from distinct angles: SSRI raphe-autoreceptor desensitization, subcallosal deep-brain stimulation, and ablative cingulotomy. The experiential consequence is held separately as ACC0707, preserving ACT/COG lens orthogonality.

### COG · `ACC0705` ACC-chronic-pain-experiential-state — 3 edges
*MAKE / evoke · OC: aversive affect with anticipatory dread*
- `IS_RESULT_OF →` `ACC0509` ACC-nerve-injury-LTP-amplification-event
- `IS_RESULT_OF →` `ACC0512` ACC-amputation-LTD-abolition-event
- `PART_OF →` `ACC0000` anterior-cingulate-cortex

> **Shadow.** The chronic-pain experiential state has a two-dimensional phenomenal structure: an affective component (unpleasantness) and an anticipatory component (dread). The two are dissociable and supported by distinct plasticity mechanisms — postsynaptic NMDAR-dependent LTP sustains the affective dimension (Koga et al. 2015); presynaptic kainate-dependent LTP sustains the anticipatory dimension. Concurrent LTP saturation and LTD abolition remove homeostatic correction, locking the state into persistence. It is the "emoji layer" above the plasticity machinery — what it is like to be in chronic pain, with both misery now and dread of misery to come (Bliss et al. 2016).

### ABST · `ACC0920` ACC-exogenous-perturbation-domain — 17 edges
*CODE / label · categorical container · OC: categorizes ACC-related intervention events altering system operating state*
- `CLASSIFIES →` `ACC0509` nerve-injury-LTP-amplification-event
- `CLASSIFIES →` `ACC0510` injury-LTP-occlusion-event
- `CLASSIFIES →` `ACC0512` amputation-LTD-abolition-event
- `CLASSIFIES →` `ACC0514` ZIP-LTP-erasure-event
- `CLASSIFIES →` `ACC0540` ischemic-ablation-event
- `CLASSIFIES →` `ACC0550` cingulotomy-ablation-event
- `CLASSIFIES →` `ACC0555` TBI-diffuse-axonal-injury-event
- `CLASSIFIES →` `ACC0556` subgenual-deep-brain-stimulation-event
- `CLASSIFIES →` `ACC0557` optogenetic-inhibition-event
- `CLASSIFIES →` `ACC0560` SSRI-raphe-autoreceptor-desensitization-event
- `CLASSIFIES →` `ACC0561` guanfacine-alpha2A-PE-enhancement-event
- `CLASSIFIES →` `ACC0567` subanesthetic-ketamine-exposure-event
- `CLASSIFIES →` `ACC0580` chronic-mild-stress-exposure
- `CLASSIFIES →` `ACC0513` metaplastic-LTD-rescue-event · `ACC0515` BDNF-silent-synapse-recruitment-event · `ACC0516` NB001-LTP-blockade-event · `ACC0511` injury-synaptic-tagging-blockade-event

> **Shadow.** Groups perturbations originating outside the ACC system — injury, pharmacology, stimulation, experimental paradigms — that impose state changes on ACC circuitry rather than emerging from intrinsic dynamics. Membership is set by external imposition. The categorical layer supports cross-entry traversal and domain-level analysis without duplicating the structural/causal edges each event already carries. Boundary case: placebo-analgesia is excluded despite its externally framed context, because the encoded event is endogenous μ-opioid release — the boundary is the source of imposition, not the framing of the paradigm.

### THAL · `THAL0001` dorsal-thalamus-nuclear-system — 11 edges *(the thalamic hub)*
*MAKE / form · OC: principal excitatory thalamic nuclear aggregation*
- `PART_OF →` `THAL0000` bilateral-thalamic-complex
- `SUBDIVIDES_INTO →` `THAL0005` anterior-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0006` medial-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0007` lateral-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0008` ventral-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0021` posterior-thalamic-nuclear-group
- `SUBDIVIDES_INTO →` `THAL0022` pulvinar-nuclear-complex
- `SUBDIVIDES_INTO →` `THAL0180` midline-thalamic-nuclear-group
- `INCLUDES →` `THAL0187` thalamocortical-projection-architecture
- `INCLUDES →` `THAL0179` thal-intrinsic-interneuron-microcircuit-network
- `INCLUDES →` `THAL0067` thalamocortical-relay-neuron-population

> **Shadow.** The dorsal thalamus is the principal excitatory nuclear aggregation — the obligatory relay tier between subcortical structures and cortex. Its seven nuclear groups partition the entire relay-and-association thalamus, and it houses the thalamocortical projection architecture and relay-neuron population that carry its output to cortex. The single highest-degree hub of the thalamic graph.

### THAL · `THAL0000` bilateral-thalamic-complex — 9 edges
*MAKE / form · OC: paired diencephalic nuclear mass*
- `SUBDIVIDES_INTO →` `THAL0001` dorsal-thalamus-nuclear-system
- `SUBDIVIDES_INTO →` `THAL0002` ventral-thalamus-reticular-shell
- `SUBDIVIDES_INTO →` `THAL0003` metathalamic-geniculate-complex
- `SUBDIVIDES_INTO →` `THAL0004` medullary-laminar-system
- `SUBDIVIDES_INTO →` `THAL0186` habenular-nuclear-complex
- `INCLUDES →` `THAL0204` thalamic-vascular-supply-system
- `INCLUDES →` `THAL0078` third-ventricle-medial-interface
- `INCLUDES →` `THAL0080` thalamic-hilum-entry-zone
- `INCLUDES →` `THAL0082` thalamic-polar-axis-orientation

> **Shadow.** The bilateral thalamic complex is the highest-level structural container — the paired diencephalic nuclear mass astride the third ventricle, the obligatory routing hub between subcortical structures and cortex. It subdivides into the dorsal thalamus, the reticular shell, the geniculate complex, the medullary laminar system, and the habenular complex.

---

*Every node here is operator-signed and provenance-tracked, built to a fixed doctrine so it behaves as a stable, queryable graph node. Representative sample only; the full corpus and detailed provenance are available on request.*
