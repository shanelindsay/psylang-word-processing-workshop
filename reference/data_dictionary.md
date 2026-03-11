# Data dictionary

## Core variables

- `word`: lexical item
- `mean_RT_ms`: average lexical decision response time in milliseconds
- `length`: number of letters
- `log_frequency`: word frequency on a log scale
- `AoA`: age of acquisition estimate
- `OLD20`: orthographic neighbourhood similarity measure

## Quick reminders

- Lower `mean_RT_ms` = faster recognition
- Higher `log_frequency` = more frequent word
- Higher `AoA` = learned later
- Lower `OLD20` = more similar spelling neighbours

## Trial-level extension file

The student pack also includes `word-processing-trial-level-data.csv`.

Key fields:

- `Sub_ID`: participant ID
- `Trial`: trial number
- `Type`: lexicality code
- `D_RT`: trial response time
- `D_Word`: word shown on that trial
- `Outlier`: outlier flag
- `D_Zscore`: z-scored response time

## Optional extra variables in the current dataset

- `mean_accuracy`: average accuracy for the item
- `concreteness`: concreteness rating
- `morph_family_size`: morphological family size
