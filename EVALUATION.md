# Evaluation — Desk / Day

Current status: implementation built; **41/41 actual Node numerical checks pass**. Browser/render checks and independent final review are pending. No application PASS or publication is claimed.

## Numerical evidence

Tests import the actual pure model. They cover baseline revenue200,000c/variable120,000c/contribution800c/profit30,000c/threshold63;62-unit−400c versus63-unit+400c;50-unit−10,000c;price1800c giving10,000c and84 units;one-cent contributions; zero/negative margin and zero/positive fixed costs; threshold outside supported range; maximum exact surplus990,000,000c and loss−1,010,000,000c; cent parsing and malformed/empty/negative/exponent/excess precision/out-of-range fields; adaptive quantities, exact formatting and current decision text.

The independent reviewer separately checked price19.99/cost12.34/fixed500.01: contribution765c, threshold66, quantity65 profit−276c and66 profit489c. Reviewer also exhaustively checked every supported current quantity0..10,000: sensitivity includes zero/current, unique bounded integer points and an above-current point whenever possible. This is reviewer source/model evidence, not a browser-render claim.

## Build evidence

Clean npm ci completed, canonical dependency checker passed, production build passed without warnings, and runtime license notices were generated. Source, expected prefix and notices links are present. These checks do not establish rendered behavior.

## Pending actual UI evidence

Verify all six slides at desktop and320/390 frames, progress/nav, focused input arrows without slide changes, Enter submit, no hidden clipping, supported maximum/zero/negative cases, sensitivity hidden-to-visible reentry and table, fixed/current comparisons, pending/invalid/restore, actual clipboard contents/fallback, native history before interaction and disposal. The developer's current CUA inventory has zero browser surfaces after interruption of an earlier SQL download; coordinator has an independent browser. Attribution will distinguish its observations from developer checks.

## Preserved failures

Independent source review found a supported near-zero tick collision: price$10/cost$0/quantity10,000/fixed$99,999.99 produces a one-cent positive endpoint next to the zero label. Both tick positions differed by about0.00002px. The chart now always retains zero and omits another y-axis tick within22px. Exact values remain in the table. The left gutter increased to80px to accommodate the maximum-loss compact label; actual narrow rendering remains to be witnessed. No arithmetic changed. Current source reviewed; rendered output unverified.
