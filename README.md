# Spatial-Audit Audio Editing Demo

This page provides qualitative audio examples for **Spatial-Audit**, a training-free spatial-semantic audio editing framework built on a spatially adapted TangoFlux backbone and FlowEdit.

All examples are 10-second binaural clips. Captions describe locations with phrases such as “from the left”, “from the front”, and “from the right”. Use headphones for the spatial comparisons.

## Why these examples are included

The revised evaluation addresses the reviewers' concerns in three complementary settings:

1. **In-domain HRTF data**: examples from the synthetic HRTF-based evaluation pipeline used for the main benchmark.
2. **Real-world binaural recordings**: independent MRSAudio recordings, outside the AudioCaps/HRTF construction pipeline. These recordings contain a single source, so the examples use spatial addition.
3. **Diverse temporal overlap**: examples with randomized event onset times and overlap durations, including replacement and removal cases that differ from the fixed training configuration.

For the real-recorded examples there is no synthetic ground-truth target. The audio is therefore intended for subjective comparison between Spatial-Audit and SmartDJ, as described in the revised manuscript.

## 1. In-domain HRTF-semantic-spatial examples

These examples compare the source mixture, the target/reference mixture, Spatial-Audit, AudioEditor, MMEdit, and SmartDJ. The target/reference waveform is the intended edited result for this synthetic setting.

### Addition

<details>
<summary><strong>Clock + woman speaking</strong> — add a left event</summary>

**Source:** `A clock ticking from the right.`  
**Target:** `A clock ticking from the right and a woman speaking from the left.`  
**Instruction:** `Add a woman speaking from the left.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_45204/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_45204/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_45204/spatial_audit.wav"></audio> |
| AudioEditor | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_45204/audioeditor.wav"></audio> |
| MMEdit | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_45204/mmedit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_45204/smartdj.wav"></audio> |

</details>

<details>
<summary><strong>River + goats</strong> — add a left event</summary>

**Source:** `A fast-flowing river from the right.`  
**Target:** `A fast-flowing river from the right and several goats bleating from the left.`  
**Instruction:** `Add several goats bleating from the left.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_80581/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_80581/ground_truth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_80581/Spatial_Audit.wav"></audio> |
| AudioEditor | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_80581/AudioEditor.wav"></audio> |
| MMEdit | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_80581/mmedit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="HRTF_semantic_spatial/add/add_s_80581/smartdj.wav"></audio> |

</details>

### Removal

<details>
<summary><strong>Baby laughter + keyboard</strong> — remove the right event</summary>

**Source:** `A baby laughing happily from the left and typing on a computer keyboard from the right.`  
**Target:** `A baby laughing happily from the left.`  
**Instruction:** `Remove typing on a computer keyboard from the right.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_1155/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_1155/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_1155/spatial_audit.wav"></audio> |
| AudioEditor | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_1155/audioeditor.wav"></audio> |
| MMEdit | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_1155/mmedit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_1155/smartdj.wav"></audio> |

</details>

<details>
<summary><strong>Keyboard + whistling</strong> — remove the left event</summary>

**Source:** `A person typing on a keyboard from the left and rhythmic whistling playing a tune from the left.`  
**Target:** `A person typing on a keyboard from the left.`  
**Instruction:** `Remove rhythmic whistling playing a tune from the left.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_117252/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_117252/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_117252/spatial_audit.wav"></audio> |
| AudioEditor | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_117252/audioeditor.wav"></audio> |
| MMEdit | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_117252/mmedit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="HRTF_semantic_spatial/remove/REM_M_117252/smartdj.wav"></audio> |

</details>

### Replacement

<details>
<summary><strong>Food sizzling + engine → ducks</strong> — replace left with right</summary>

**Source:** `Food sizzling in a pan from the front, followed by an engine running from the left.`  
**Target:** `Food sizzling in a pan from the front, followed by ducks quacking from the right.`  
**Instruction:** `Replace an engine running from the left with ducks quacking from the right.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_s_97541/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_s_97541/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_s_97541/spatial_audit.wav"></audio> |
| AudioEditor | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_s_97541/audioeditor.wav"></audio> |
| MMEdit | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_s_97541/mmedit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_s_97541/smartdj.wav"></audio> |

</details>

<details>
<summary><strong>Thunder + bell → crumpled paper</strong> — replace a left event</summary>

**Source:** `Continuous low rumbling thunder from the left, followed by a cathedral bell ringing from the left.`  
**Target:** `Continuous low rumbling thunder from the left, followed by paper being crumpled from the left.`  
**Instruction:** `Replace a cathedral bell ringing from the left with paper being crumpled from the left.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_t_111436/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_t_111436/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_t_111436/spatial_audit.wav"></audio> |
| AudioEditor | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_t_111436/audioeditor.wav"></audio> |
| MMEdit | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_t_111436/mmedit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="HRTF_semantic_spatial/replace/REP_t_111436/smartdj.wav"></audio> |

</details>

## 2. Real-world MRSAudio recordings

These are independent 10-second binaural recordings from MRSAudio. Each source contains one recorded event, so the task is spatial addition. There is no synthetic ground-truth target; Spatial-Audit and SmartDJ are provided for direct listening comparison.

### Triangle → toy train

**Source:** `A triangle being struck from the right.`  
**Instruction:** `Add a toy train moving from the front.`

| Audio | File |
|---|---|
| Real source | <audio controls preload="none" src="MRSAudio/add/real_05978/source.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="MRSAudio/add/real_05978/Spatial_audit_edited.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="MRSAudio/add/real_05978/smartdj_edited.wav"></audio> |

### Hand clapping → stick bell

**Source:** `Hand clapping from the front.`  
**Instruction:** `Add the ringing sound of a stick bell from the right.`

| Audio | File |
|---|---|
| Real source | <audio controls preload="none" src="MRSAudio/add/real_13924/source.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="MRSAudio/add/real_13924/spatial_audit_edited.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="MRSAudio/add/real_13924/smartdj_edited.wav"></audio> |

### Clash cymbals → maracas

**Source:** `Clash cymbals sounding from the front.`  
**Instruction:** `Add maracas being shaken from the left.`

| Audio | File |
|---|---|
| Real source | <audio controls preload="none" src="MRSAudio/add/real_47153/source.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="MRSAudio/add/real_47153/spatial_audit_edited.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="MRSAudio/add/real_47153/smartdj_edited.wav"></audio> |

## 3. Diverse temporal overlap

These cases use randomized onset times and overlap durations at inference time. In the revised evaluation, the representative replacement case has approximately 3.2–7.7 seconds of source-event overlap, while the removal case has approximately 0.8–8.2 seconds. Addition is shown separately because its input contains only one event before editing.

### Removal — long overlap

**Source:** `A man chanting into a microphone from the right and continuous spray from the left.`  
**Target:** `A man chanting into a microphone from the right.`  
**Instruction:** `Remove continuous spray from the left.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="vary_overlap/remove/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="vary_overlap/remove/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="vary_overlap/remove/spatial_audit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="vary_overlap/remove/smartdj.wav"></audio> |

### Replacement — overlapping events

**Source:** `An audience gives applause from the left and an idle vehicle engine running from the right.`  
**Target:** `An audience gives applause from the left and a man is making a speech from the left.`  
**Instruction:** `Replace an idle vehicle engine running from the right with a man making a speech from the left.`

| Audio | File |
|---|---|
| Source | <audio controls preload="none" src="vary_overlap/replace/source.wav"></audio> |
| Target / reference | <audio controls preload="none" src="vary_overlap/replace/groundtruth.wav"></audio> |
| Spatial-Audit | <audio controls preload="none" src="vary_overlap/replace/spatial_audit.wav"></audio> |
| SmartDJ | <audio controls preload="none" src="vary_overlap/replace/smartdj.wav"></audio> |

## Reproducibility notes

- Spatial-Audit uses the spatially adapted TangoFlux backbone with inversion-free FlowEdit.
- The editing stage is training-free; source and target captions provide the semantic and spatial conditions.
- SmartDJ instructions follow its documented spatial command format, including `at the left`, `at the front`, or `at the right`.
- The HRTF examples include the existing baseline outputs for qualitative comparison. MRSAudio examples compare Spatial-Audit and SmartDJ because no synthetic target is available.
- All audio files in this page are provided for research demonstration only and remain subject to the licenses of the underlying datasets and models.
