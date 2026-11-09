# Sample Data

This folder contains a small, self-contained subset of the Wall Street Journal (WSJ) section of OntoNotes 5.0, together with the matching PropBank annotations. It lets reviewers run [`demo_with_sample_data.ipynb`](../demo_with_sample_data.ipynb) end to end without downloading the full corpus.

## Files

Eight matching `.prop`/`.onf` pairs are included:

```text
wsj_0005  wsj_0016  wsj_0033  wsj_0052
wsj_0053  wsj_0054  wsj_0072  wsj_0084
```

- `wsj_XXXX.prop` — PropBank proposition file. Each line is one predicate-argument annotation. The second field is the sentence index; role pointers such as `12:0-ARG0` and `13:0-rel` refer to nodes in the parse tree.
- `wsj_XXXX.onf` — OntoNotes annotation file. Each sentence block contains a plain sentence, a treebanked sentence, a parse tree, and a leaf/role listing.
- `expected_output.csv` — the expected result of `demo_with_sample_data.ipynb` on these eight pairs: 107 rows and five columns (`SENTENCE`, `PREDICATES`, `ARG0`, `ARG1`, `Merged_Arguments`).

Only files with both a `.prop` and `.onf` counterpart are included, because the demo needs both sides of the alignment.

## Source and license

The `.onf` files come from OntoNotes 5.0 (LDC2013T19); the `.prop` files come from the [PropBank release](https://github.com/propbank/propbank-release). They are included only as a small testing sample and remain subject to their original licenses. The repository's GPL-3.0 license covers the extraction code, not the corpus data. Obtain the complete corpus from the [Linguistic Data Consortium](https://catalog.ldc.upenn.edu/LDC2013T19) for research use.

## Reproducing the output

Run `demo_with_sample_data.ipynb` from the repository root. It writes `outputs/sample_output.csv` and compares it with `expected_output.csv`.
