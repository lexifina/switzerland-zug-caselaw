# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py zg <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 4,276 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
afc4128bbc174758a25be5c0a875dd6e524d34775407715f6f4a1f9cfa4e9642 *zg_anwaltsaufsicht.parquet
eaa107337c56c013a51c6b227d76f63136d0848efac0a333fbfe2cbc28bde391 *zg_datenschutzstelle.parquet
4bbc5d769aad99574e8a934171cabfd5d7134360fea6239c8e8ab80190e1a825 *zg_kantonsgericht.parquet
8f97adc78eca8a48bc0ee29dddf9d3f99275622e148a15492ee0ac3f2da384c6 *zg_obergericht.parquet
3be1386d714720e1a5f06863c7ac599c259aeef455fffd0aacc994d452a14b00 *zg_regierungsrat.parquet
083b946e0307406f77cffc6c4dce6d27b89e1b62685828aba3dd837079af48ba *zg_strafgericht.parquet
aa967b61b0cdf617f1d7c930d2847e2f1390db57faf2f66170afbe37f1efc883 *zg_verwaltungsgericht.parquet
```
