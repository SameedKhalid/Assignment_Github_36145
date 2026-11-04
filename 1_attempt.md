# Assignment 1: Claims, questions and attempt record

Student: Muhammad Sameed Khalid | ERP: 36145

## Timing and original-attempt evidence

This file contains a post-AI working draft. It is not a record of an attempt
completed before AI use. A genuine earlier snapshot, commit hash and initial
predictions were not supplied. Existing earlier evidence should be preserved
if it exists; the values below are actual results, not reconstructed predictions.

## Working claim 1

**Claim:** Everything costs more now.

**Question:** How did the recorded price of Staple A in City 1 change between 1 January and 19 March 2026, measured in the dataset's illustrative PKR per kg?

**Variables needed:** date, item, city, price and unit.

The claim is too broad because it does not identify which goods, where or
compared with when. The question fixes one item, one city, two observed dates
and one unit. The file has the two required matching observations.

**Supporting check:** Staple A in City 1 is 101.0 on 1 January and 114.5 on
19 March. The increase is 13.5 illustrative PKR per kg, or about 13.37%.
This supports the narrow comparison, not a claim about every good or every week.

## Working claim 2

**Claim:** Prices are higher in City 2 than in City 1.

**Question:** For each item on each of the 12 dates, how much did its recorded price in City 2 differ from its price in City 1, using the same illustrative PKR per kg unit?

**Variables needed:** date, item, city, price and unit.

This question compares the same item and date in the two labelled cities.
It avoids comparing different products, dates or measurement units. All four
items have both cities recorded on all 12 dates.

**Supporting check:** There are 48 matched item-date comparisons. City 2 is
6.0 illustrative PKR per kg higher in each pair.

These are generic working claims and AI-assisted question drafts. This file
does not claim that the student personally heard these exact statements.

## Predictions and actual results

| Check | Original prediction | Actual result | Comparison |
| --- | --- | --- | --- |
| Shape (rows, columns) | Not supplied | (96, 6) | No genuine prediction was available for comparison. |
| Distinct items | Not supplied | 4 | No genuine prediction was available for comparison. |
| Distinct dates | Not supplied | 12 | No genuine prediction was available for comparison. |

There are four items in two cities on twelve dates, giving 4 x 2 x 12 = 96
data rows. The six columns are date, item, city, price, unit and data_label.

## Scope and definitions checked against the CSV

One row records an illustrative price for one item in one labelled city on
one date. The item labels are Staple A, Oil B, Pulse C and Sweetener D.
The dates run weekly from 1 January to 19 March 2026. All units are
PKR per kg (illustrative). The data_label field states that these are
illustrative teaching data, not actual PBS observations.

The header and all rows were checked. The official dictionary remains
unavailable, so these observed definitions are not represented as an
independent dictionary check.

## Column reference

The field definitions, units, observed coverage and unavailable variables are
documented in ../../data/column_reference.md. That file is derived from the
supplied CSV; it is not presented as the instructor's original dictionary.
