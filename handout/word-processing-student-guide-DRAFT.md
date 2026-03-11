# Student guide

## Workshop title
What predicts lexical decision speed? Analysing lexical variables with regression

## Purpose
This workshop uses a cleaned teaching file derived from the **English Lexicon Project** lexical decision dataset, with public **age-of-acquisition norms** merged in. The main aim is to use one real dataset to ask what lexical variables predict word-recognition speed. It also develops the kind of analytical reasoning used later in the module assessment.

## Learning goals
By the end, you should be able to:
- explain what the core lexical predictors index
- inspect RT data sensibly
- use simple descriptives and a simple correlation as a starting point for regression
- run a multiple regression predicting RT
- interpret the output in plain language
- write a short results response

## Quick recap: lexical decision
- In a lexical decision task, participants decide as quickly and accurately as possible whether a letter string is a real word.
- Lower RT means **faster** recognition.
- More frequent words are usually recognised faster.
- Lexical competition means that similar words can influence recognition.

## Step 1. Meet the dataset
Today’s file is:

`elp_lexical_decision_teaching.csv`

This prepared teaching file is built from **English Lexicon Project** lexical decision data, with **AoA** merged in from a public norms dataset.

Important:
- each row is **one English word**
- `mean_RT_ms` is the **average lexical decision RT** for that word
- today’s analysis is therefore an **item analysis of word-level means**
- the core live columns are `word`, `mean_RT_ms`, `length`, `log_frequency`, `AoA`, and `OLD20`

Optional extra variables may be present in the file for later discussion. If available, `mean_accuracy` can be used as a secondary descriptive check, but it is not required for the core live model.

## Step 2. Understand the core variables
Use this glossary before you make any predictions.

| Variable | What it means | Helpful reminder |
|---|---|---|
| `length` | number of letters | higher = longer word |
| `log_frequency` | log-transformed word frequency | higher = more frequent word |
| `AoA` | age of acquisition estimate | higher = learned later |
| `OLD20` | orthographic neighbourhood measure | lower = more similar neighbours |
| `mean_RT_ms` | average lexical decision RT | lower = faster recognition |

Important:
- you do **not** need the exact OLD20 formula for today’s workshop
- what matters is that it captures how similar a word is in spelling to other words

## Step 3. First look at the data
Check:
- summary statistics for **mean_RT_ms**, **length**, **log_frequency**, **AoA**, and **OLD20**
- the RT distribution
- a quick scatterplot of **mean_RT_ms** against **log_frequency**
- missing values
- anything implausible

If `mean_accuracy` is available in your file, you can also use it as a quick check on item difficulty.

At this stage, the goal is to understand the variables and the shape of the dataset before modelling.

## Step 4. Look at one simple relation between predictors
Before multiple regression, look at one simple predictor–predictor relation.

A good first check is:
- the correlation between **`log_frequency`** and **`AoA`**

Ask:
- are earlier-acquired words also often more frequent?
- if so, why might that matter once both predictors are entered into the same model?

If time permits, inspect one more simple predictor pair.

## Step 5. Make your predictions
Now that the study, dataset, and variables have been introduced, predict what you expect **before** running the regression.

| Predictor | What does it index? | Predicted relation with RT | Why? |
|---|---|---|---|
| `log_frequency` |  |  |  |
| `AoA` |  |  |  |
| `length` |  |  |  |
| `OLD20` |  |  |  |

## Step 6. Run the core regression
Core model:

`mean_RT_ms ~ length + log_frequency + AoA + OLD20`

For this workshop, assume the main regression assumptions have been checked for the prepared teaching file.

In Jamovi:
1. Open the dataset
2. Check descriptives for **mean_RT_ms**, **length**, **log_frequency**, **AoA**, and **OLD20**
3. Create a scatterplot of **mean_RT_ms** against **log_frequency** with clear axis labels
4. Run a simple correlation for **log_frequency** and **AoA**
5. Run a linear regression
6. Set **mean_RT_ms** as the dependent variable
7. Add **length**, **log_frequency**, **AoA**, and **OLD20** as predictors
8. Request coefficient estimates and model fit
9. If available, request confidence intervals and standardised estimates

If `mean_accuracy` is available, inspect it briefly as an optional descriptive check rather than part of the core model.

## Step 7. Record your results

| Predictor | Coefficient sign | Supported in this model? | Plain-language interpretation |
|---|---|---|---|
| `length` |  |  |  |
| `log_frequency` |  |  |  |
| `AoA` |  |  |  |
| `OLD20` |  |  |  |

Also note:
- the key summary statistics
- the figure showing **RT vs log frequency**
- model fit
- which of your original predictions were supported
- one overall conclusion

Here, **supported in this model** means a **unique association once the other predictors are included**. It does **not** by itself prove a separate causal mechanism.

## Step 8. Common limitations of an item analysis
Choose **one** clear limitation and explain it briefly.

Useful options:
- This is an **item analysis of word-level means**, so it does not model participant and item variability simultaneously.
- Predictors such as **frequency** and **AoA** can overlap, so coefficients may shift when correlated predictors are entered together.
- This is a **correlational** analysis of lexical properties, so it supports prediction but not a direct causal claim.
- Word-level means can hide heterogeneity and possible **speed–accuracy trade-offs**.

## Step 9. Short written response
Write a short response that includes:
- the key regression results
- which hypotheses were supported
- a plain-language interpretation of what the pattern suggests about lexical access and lexical organisation
- one limitation of the item analysis

Do **not** spend time writing a separate aim or method paragraph in class.

## Final link to the lectures
This workshop mainly supports the lexical decision material from the word-recognition lecture.

It also links more lightly to lexical integration: the predictors analysed here describe the structure of the kind of organised lexicon that newly learned words must eventually enter.
