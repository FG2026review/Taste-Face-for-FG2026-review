# Subjective Rating Table Schema

This document describes the structure of `data/ratings/subjective_ratings_raw.csv`.

| Column Name             | Description |
|-------------------------|-------------|
| `subject_id`            | Anonymous participant ID (e.g., S001, S002, ...). |
| `taste_type`            | One of: sweetness, saltiness, sourness, bitterness, umami, astringency. |
| `identified_correctly`  | Whether the participant correctly identified the taste category (1 = yes, 0 = no). |
| `perceived_intensity`   | Subjective perceived intensity (0–10). |
| `aftertaste_intensity`  | Subjective aftertaste intensity (0–10). |
| `overall_score`         | Overall evaluation score (average of perceived and aftertaste intensity). |

Each row corresponds to one participant's rating for one taste stimulus.

Samples with `identified_correctly = 0` are valid and remain part of the dataset. This field reflects human perceptual difficulty and does not change the ground-truth taste label.