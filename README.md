# style

Writing style as characterized through PCA over linguistic features.

You can find this project in action on [amilleah.com](https://amilleah.com/projects/style).

## methods

Sentence-level style features are extracted with spaCy (`en_core_web_sm`), filtered, z-scored, and projected with PCA. 

Stability is estimated from 250 bootstrap resamples using p95 max principal angle for nested top-k subspaces. 

VAF is computed pairwise across newsletters: each newsletter's style subspace is tested on every other newsletter, then compared with SBERT semantic and random subspace baselines.

## setup + use

1. clone this repository or download it as a .zip and unzip it.
2. install `requirements.txt` using uv or pip.
    ```bash
    uv init && uv add -r requirements.txt
    ```
3. install a spacy model:
    ```bash
    uv run python -m spacy download en_core_web_sm
    ```
4. add your writing to `./corpus/`.
5. run the notebook.

## to-dos

- add plots

## attribution

`style.ipynb` is licensed under the Apache License 2.0.
- if modified, indicate it by adding it to the header comment, e.g. "modified by [name]: add .eml support"

For published websites, a link to the source code is sufficient. I'd also appreciate a link to my website: https://amilleah.com in the attribution! Thanks!
