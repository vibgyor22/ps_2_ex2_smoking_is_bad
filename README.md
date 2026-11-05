# PS 2, ex 2 Smoking is bad

A cousin claims smoking increases life expectancy because smokers in this dataset survive more often
(76% vs 69%). The notebook `smoking_is_bad.ipynb` checks whether that holds up.

**Short answer:** it doesn't. Smokers in the sample are younger, and age drives survival. Comparing
people of the same age, smokers survive less often in almost every age group (Simpson's paradox).
Age-standardised survival is 70% for smokers vs 74% for non-smokers. Gender and salary are not the drivers.

# Setup

The environment (named `smoke`) is managed with [Pixi](https://pixi.sh). From the repo root:

```bash
pixi install
pixi shell
```

Then open the notebook:

```bash
pixi run lab
```

Or run it top to bottom from the terminal:

```bash
pixi run run-notebook
```

## Pre-commit

This repository uses pre-commit to run checks before each commit. The only hook is
[nbstripout](https://github.com/kynan/nbstripout), which clears notebook outputs so commits
only contain code changes. The config is in `.pre-commit-config.yaml`.

To install the hook (once per clone):

```bash
pre-commit install
```

To run the checks manually:

```bash
pre-commit run --all-files
```
