# Checks, AI log and reflection

Status: Completed AI-assisted working draft. The official dictionary check and genuine earlier-attempt evidence remain unavailable. Student review is required under the handout's AI rules.

Source: teaching_prices_clean.csv, supplied in this conversation.
Analysis run: 2026-11-04 21:48:08 PKT (UTC+05:00).
Data label: ILLUSTRATIVE TEACHING DATA - NOT ACTUAL PBS OBSERVATIONS.

## Three numerical checks

| Check | Original prediction | Actual result | Comparison |
| --- | --- | --- | --- |
| Shape (rows, columns) | Not supplied | (96, 6) | No original prediction was supplied, so a difference cannot be calculated. |
| Distinct items | Not supplied | 4 | No original prediction was supplied, so a difference cannot be calculated. |
| Distinct dates | Not supplied | 12 | No original prediction was supplied, so a difference cannot be calculated. |

Original predictions were not supplied. The actual results above were obtained
from the CSV after AI use; they are not described as earlier predictions.

## Evidence from the CSV

- Columns: date, item, city, price, unit, data_label.
- Items: Staple A, Oil B, Pulse C and Sweetener D.
- Cities: City 1 and City 2. No real city names are supplied.
- Date range: 1 January to 19 March 2026, with 12 dates seven days apart.
- Eight records per date: four items in two cities.
- Twelve records per item-city pair. Total: 4 x 2 x 12 = 96.
- Missing/empty cells: 0. Full duplicate rows: 0.
- Duplicate (date, item, city) keys: 0.
- All dates parse as YYYY-MM-DD. All prices convert to numeric values.
- All unit entries are PKR per kg (illustrative).
- One row is an observed illustrative item-city-date price record.

These meanings are inferred from the header, labels and row structure.
They are not a substitute for the instructor's data dictionary.

## AI critique of the working questions

- Claim 1 uses "everything", but the file covers only four illustrative items.
  The specific Staple A question identifies the item, city, unit and two dates.
  Its answer cannot establish that every real good became more expensive.
- Claim 2 needs comparisons of the same item and date in the same unit. The
  matched-city question does this for all 48 item-date pairs. City labels are
  illustrative and cannot be replaced with real city names.
- Neither question should assume that a price change proves reduced
  affordability or a change in purchases. Those outcomes need additional data.

This is an AI review of the working questions in 1_attempt.md. It does not
claim that an earlier student-written draft or coaching exchange was supplied.

## Five AI-proposed questions: CSV review

The first three are answerable within this illustrative dataset. A4 and A5
are rejected for the specific reasons below. These are AI checks, not a claim
that the student has already performed the required independent verification.

| ID | AI question | Required variables | CSV decision | Specific evidence / reason |
| --- | --- | --- | --- | --- |
| A1 | How did the recorded price of Staple A in City 1 change from 1 January to 19 March 2026? | date, item, city, price, unit | Accept for this dataset | Matching rows show 101.0 and 114.5 PKR per kg (illustrative). Increase = 13.5, or 13.37%. Both dates and the same unit exist. |
| A2 | Which of the four items had the largest percentage increase in its recorded City 1 price between 1 January and 19 March 2026? | date, item, city, price, unit | Accept for this dataset | All four City 1 items have both endpoints. Sweetener D has the largest percentage increase: 149.0 to 178.5, or 19.80%. This is not the largest absolute increase. |
| A3 | For the same item and date, how much higher or lower was its recorded price in City 2 than in City 1 across the 12 dates? | date, item, city, price, unit | Accept for this dataset | All 48 item-date pairs have both cities and the same unit. City 2 minus City 1 equals 6.0 PKR per kg in every pair. |
| A4 | Did the share of household income needed to buy a fixed food basket rise over these dates? | Comparable prices, defined basket quantities, matching household income | Reject | The six CSV columns include no household income or basket quantities. Price records alone cannot calculate the requested share of income. |
| A5 | Did price increases cause households to buy smaller quantities? | Prices, purchased quantities, household information and a credible causal design | Reject | There is no purchase-quantity or household field. These illustrative price records cannot establish household buying responses or identify a causal effect. |

Rejected questions: 2 (A4 and A5).
Column checks for all five questions are documented in data/column_reference.md,
which was derived from the actual CSV. An independent check against the official
course dictionary remains unavailable because that dictionary was not supplied.

Independent student verification: not yet recorded.
Official dictionary filename and entries: not supplied.

Final question drafts are recorded in 1_attempt.md: Staple A's City 1 price change and the matched City 2 versus City 1 price differences. These drafts were written with AI assistance. An earlier student-written draft and coaching exchange were not supplied.

The five alternatives above were prepared from the CSV. They are not a
record of a coaching exchange about claims the student has not supplied.

## Supporting price checks

Comparison: 1 January 2026 to 19 March 2026, like item, city and unit.
Price unit: PKR per kg (illustrative). Percentage change is
(last price - first price) / first price x 100.

| Item | City | First price | Last price | Change | Percentage change |
| --- | --- | ---: | ---: | ---: | ---: |
| Staple A | City 1 | 101.0 | 114.5 | 13.5 | 13.37% |
| Staple A | City 2 | 107.0 | 120.5 | 13.5 | 12.62% |
| Oil B | City 1 | 298.0 | 344.0 | 46.0 | 15.44% |
| Oil B | City 2 | 304.0 | 350.0 | 46.0 | 15.13% |
| Pulse C | City 1 | 200.0 | 207.5 | 7.5 | 3.75% |
| Pulse C | City 2 | 206.0 | 213.5 | 7.5 | 3.64% |
| Sweetener D | City 1 | 149.0 | 178.5 | 29.5 | 19.80% |
| Sweetener D | City 2 | 155.0 | 184.5 | 29.5 | 19.03% |

All eight item-city endpoint prices increased over this interval. This does
not show that every price rose every week, or that all real goods became
more expensive. City 2 is exactly 6.0 PKR per kg higher than City 1 in all
48 matched item-date comparisons. These statements apply only to this file.

## AI-use record

The initial guide and templates were AI-assisted before this CSV analysis.
Keep that first interaction in AI_USE_LOG.md with its actual time from the chat.
The following row records this new analysis; it does not replace the first entry.

| Date/time + timezone | Tool / role | Input / request | Assistance | Status | Verification and evidence | Change |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-11-04 21:48:08 PKT (UTC+05:00) | ChatGPT / analysis and checking | Supplied teaching_prices_clean.csv | Counts, matched price comparisons and five question checks | CSV calculations verified by AI; student review pending | pandas counts plus an independent csv.DictReader count; all 96 rows checked for missing values and duplicate item-city-date keys; dictionary not supplied | Real outputs added to 2_work.ipynb and checks recorded below |

AI review accepted A1-A3 within the illustrative dataset and rejected A4-A5. The specific checks and reasons are recorded above. Independent student verification has not been claimed.

## Sources and verification record

The CSV calculations were verified by AI. The table distinguishes that work
from any independent student review; it does not claim that the student opened
links or checked sources.

| Source | What it supports | Verification record |
| --- | --- | --- |
| teaching_prices_clean.csv | Counts, labels and illustrative price comparisons above | Checked by AI against the actual file and independent counts. Student review not recorded. |
| data/column_reference.md | Field meanings, units, coverage and unavailable variables | Derived from the actual CSV; not an instructor-issued dictionary. |
| Course data dictionary - not supplied yet | Official column definitions and coverage | Student review not recorded |
| https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.shape.html | Shape is the row-column pair | Student review not recorded |
| https://pandas.pydata.org/docs/reference/api/pandas.Series.nunique.html | Distinct counts and missing-value handling | Student review not recorded |
| https://pandas.pydata.org/docs/reference/api/pandas.to_datetime.html | Date parsing | Student review not recorded |
| https://code.visualstudio.com/docs/datascience/jupyter-notebooks | Running and saving the notebook | Student review not recorded |
| https://git-scm.com/docs/git-commit | Saving a real Git snapshot | Student review not recorded |

## Reflection - 100 words

AI-assisted draft for the student to review and rewrite in their own words.

This dataset contains 96 price records for four items in two labelled cities across twelve weekly dates. It allows comparisons of recorded prices between dates and between the cities, using the same units. All four items have higher prices at the final date than at the first date in both cities. However, these are illustrative teaching observations, so they cannot establish actual Pakistani prices or national inflation. The file has no household incomes, budgets or quantities purchased. It therefore cannot show affordability, explain buying decisions or establish causes. Checking the columns narrowed the questions from affordability to supported price comparisons.

Word count: 100.

## Three additional sentences

The most tempting unsupported suggestion was whether price increases caused households to buy less, because it linked prices to daily life.

The CSV has no purchase quantities or household information, and its illustrative observations cannot identify a causal effect.

The questions were therefore narrowed to recorded price changes and differences between the two labelled cities.
