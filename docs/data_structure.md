# Data Structure

This document describes the directory layout of the Taste-Face dataset under the `data/` folder.

In the current release, **each participant receives exactly one stimulus for each taste type**.  
Therefore, there is a one-to-one correspondence between:

- a participant (`subject_id`)
- a taste category (`taste_type`)
- one video sequence and one frame sequence

No repeated trials exist for the same `(subject_id, taste_type)` pair.

The dataset is organized into three top-level components:

- `data/ratings/` : subjective rating tables (annotations)  
- `data/videos/`  : raw facial videos  
- `data/frames/`  : frame-level images extracted from raw videos  

---

## 1. `data/ratings/`

Contains the anonymized subjective rating table:

- `subjective_ratings_raw.csv`

Each row corresponds to **one participant’s rating for one taste stimulus** and can be aligned with the corresponding video and frame sequence using:

- `subject_id`
- `taste_type`

Because each taste is presented only once per participant, no trial index is required.

---

## 2. `data/videos/`

Raw facial videos are organized by participant:

```
data/videos/
└── S001/
├── sweetness.mp4
├── saltiness.mp4
├── sourness.mp4
├── bitterness.mp4
├── umami.mp4
└── astringency.mp4
```

### File naming convention

Each video file follows the pattern:

- `<taste_type>.mp4`

Where `taste_type` is one of:

- `sweetness`
- `saltiness`
- `sourness`
- `bitterness`
- `umami`
- `astringency`

Each file represents the unique recording of that taste stimulus for the given participant.

---

## 3. `data/frames/`

Frame-level images are extracted from the raw videos and stored in a directory structure mirroring `data/videos/`:

```
data/frames/
└── S001/
├── sweetness/
│ ├── frame_0001.jpg
│ ├── frame_0002.jpg
│ └── ...
├── saltiness/
│ ├── frame_0001.jpg
│ └── ...
└── ...
```


### Frame naming convention

Each frame image follows the pattern:

- `frame_<frame_index>.jpg`

Where `frame_index` is a zero-padded integer starting from `0001`.

---

## 4. Alignment between ratings, videos, and frames

A single trial is uniquely identified by the pair:

- `subject_id` + `taste_type`

This pair is consistently used across:

- the rating table  
  (`data/ratings/subjective_ratings_raw.csv`)
- the video file path  
  (`data/videos/<subject_id>/<taste_type>.mp4`)
- the frame directory path  
  (`data/frames/<subject_id>/<taste_type>/`)

Example alignment:

- rating row: `subject_id=S001`, `taste_type=sweetness`
- video path: `data/videos/S001/sweetness.mp4`
- frames directory: `data/frames/S001/sweetness/`

This design directly reflects the experimental protocol in which each taste
is presented exactly once to each participant.