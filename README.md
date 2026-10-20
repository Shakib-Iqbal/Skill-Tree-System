# Skill Tree

A skill recommendation system built on survey data. It uses an FP-tree to suggest which programming languages and databases to learn next, based on what developers in a given role already use and want.

## How it works

1. **Data prep**: Survey data cleaned for the language and database columns (about 3-13% missing for languages, about 30% for databases). Null fields are handled and items within each row are de-duplicated.
2. **Recommendation columns**: Two sets of lists, each covering languages and databases:
   - **Have**: skills people currently use.
   - **Have + Want**: skills people currently use plus skills they want to learn.
3. **FP-tree inputs**: For each row, skills are pruned by minimum support and sorted in descending order of item support. `DevType` is placed first (never pruned), so the tree's first level is dev type, followed by skills.
4. **Recommendations**: Start at the user's dev type, follow their skills down that branch, and suggest what commonly appears next.

## Design notes

- Order of learning is not modeled. "Have" reflects what developers in a role use together; "Have + Want" reflects what people with those skills also want.
- `YearsCode` / `YearsCodePro` are excluded as irrelevant to recommendations.
- Minimum support threshold is tuned once the tree is built.

## Project structure

```
skill-tree/
├── data/        # raw and cleaned survey data
├── notebooks/   # cleaning, FP-tree building, analysis
└── README.md
```

## Tech

Python, pandas, FP-tree / FP-growth.

## Status

In progress: dataset prepped and FP-tree inputs built; tree construction and recommendation logic next.
