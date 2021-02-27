# fast-fuzzy-matching
Fast fuzzy matching for large datasets

Deduplication is a common and necessary task for a lot of datasets, and often requires fuzzy matching between strings to help identify the duplicate records.

A well known package to do so is the fuzzywuzzy python package, which uses Levenshtein distance to calculate the difference between two strings. Unfortunately, this method requires comparing each string to every other string in the dataset (on the order of quadratic time, O(n2)). For a large dataset, this falls apart as it quickly builds to very long runtimes.

This notebook explores an alternative approach, using TF-IDF from Nautral Language Processing and matrix multiplication to speed up the problem by over 6000x.
