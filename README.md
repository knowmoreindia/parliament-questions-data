# Lok Sabha questions

Every question MPs asked ministers in the Lok Sabha from 1999 to 2026: who asked, which ministry answered, the subject, the date, and links to the full question and answer.

3,93,513 questions.

## At a glance

| Table | Rows | Period | Where |
| --- | ---: | --- | --- |
| questions | 3,93,520 | 1999-11-29 to 2026-08-12 | `data/questions/` (6 files) |
| members-ls18 | 545 |  | `data/members_ls18.csv` |
| questions-text | 2,77,293 |  | release |

## Files

| Path | |
|---|---|
| `data/questions/ls<NN>.csv` | One row per question, one file per Lok Sabha |
| `data/members_ls18.csv` | The 545 members of the 18th Lok Sabha: party, State, constituency, terms, education, profession |

| Lok Sabha | Years | Questions |
|---|---|---|
| 13 | 1999 to 2004 | 73,324 |
| 14 | 2004 to 2009 | 66,371 |
| 15 | 2009 to 2014 | 79,400 |
| 16 | 2014 to 2019 | 79,149 |
| 17 | 2019 to 2024 | 60,549 |
| 18 | 2024 to 2026 | 34,720 |

The [release](https://github.com/knowmoreindia/parliament-questions-data/releases/latest) has `questions-ls<NN>.csv.gz`: the same rows with the full question and answer text, up to the 17th Lok Sabha. For the 18th, the text is only in the linked PDF and Word files.

Columns are described in `codebook.csv` and `datapackage.json`.

## Quick start

```python
import pandas as pd

base = "https://raw.githubusercontent.com/knowmoreindia/parliament-questions-data/main/data"
questions = pd.read_csv(f"{base}/questions/ls18.csv")
questions.groupby("ministry").size().sort_values(ascending=False).head(10)
```

## Worth knowing

- A question asked jointly lists every member in `members`. Names are as Digital Sansad prints them, so the same MP can be spelt differently across years.
- Starred and unstarred questions are numbered separately, so a question is identified by Lok Sabha, session, type and number. A handful of questions appear twice, as published.

## How to cite

Know More India, *Lok Sabha questions*, version 2026-11-26, https://github.com/knowmoreindia/parliament-questions-data. Licensed CC BY 4.0.

```bibtex
@misc{knowmoreindia_parliament_questions,
  author = {{Know More India}},
  title = {Lok Sabha questions},
  year = {2026},
  version = {2026-11-26},
  howpublished = {\url{https://github.com/knowmoreindia/parliament-questions-data}}
}
```

## Licence

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Credit: Know More India, from the Lok Sabha Secretariat (Digital Sansad).
