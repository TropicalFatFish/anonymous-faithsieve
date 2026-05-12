---
pretty_name: OlympiadBench 350 v2
language:
- en
license: apache-2.0
tags:
- math
- reasoning
- step-level supervision
- olympiad
task_categories:
- question-answering
- text-classification
size_categories:
- n<1K
---

# OlympiadBench 350 v2

This dataset contains 350 Olympiad-style math problem-proof pairs with step-level process labels.

## Fields

- `id`: formal benchmark ID, from `Olympiad001` to `Olympiad350`.
- `problem`: problem statement.
- `steps`: list of proof steps, one step per string.
- `first_error_step`: `correct` when all proof steps are correct; otherwise the one-based index of the first incorrect proof step.

## Label semantics

`first_error_step = "correct"` means all proof steps are judged correct.  
`first_error_step = n` means the first incorrect proof step is step `n`, using one-based indexing over the `steps` list.

## Split

The benchmark is intended as a held-out evaluation set. Use the `test` split.
