# Evaluation — Desk / Day

Current status: **41/41 numerical checks pass in Node and the actual browser**. Coordinator production rechecks passed at executable checkpoint `f21d9f2b5eebd74ba33cfc34872629c73c1d9ad8`. Independent final reviewer verdict is pending in reviewer-owned REVIEW.md; no publication is claimed. Earlier pending statements below preserve the sequence and are superseded by the final witness section.

## Numerical evidence

Tests import the actual pure model. They cover baseline revenue200,000c/variable120,000c/contribution800c/profit30,000c/threshold63;62-unit−400c versus63-unit+400c;50-unit−10,000c;price1800c giving10,000c and84 units;one-cent contributions; zero/negative margin and zero/positive fixed costs; threshold outside supported range; maximum exact surplus990,000,000c and loss−1,010,000,000c; cent parsing and malformed/empty/negative/exponent/excess precision/out-of-range fields; adaptive quantities, exact formatting and current decision text.

The independent reviewer separately checked price19.99/cost12.34/fixed500.01: contribution765c, threshold66, quantity65 profit−276c and66 profit489c. Reviewer also exhaustively checked every supported current quantity0..10,000: sensitivity includes zero/current, unique bounded integer points and an above-current point whenever possible. This is reviewer source/model evidence, not a browser-render claim.

## Build evidence

Clean npm ci completed, canonical dependency checker passed, production build passed without warnings, and runtime license notices were generated. Source, expected prefix and notices links are present. These checks do not establish rendered behavior.

## Original UI acceptance checklist — superseded by final witness

Verify all six slides at desktop and320/390 frames, progress/nav, focused input arrows without slide changes, Enter submit, no hidden clipping, supported maximum/zero/negative cases, sensitivity hidden-to-visible reentry and table, fixed/current comparisons, pending/invalid/restore, actual clipboard contents/fallback, native history before interaction and disposal. The developer's current CUA inventory has zero browser surfaces after interruption of an earlier SQL download; coordinator has an independent browser. Attribution will distinguish its observations from developer checks.

## Preserved failures

Independent source review found a supported near-zero tick collision: price$10/cost$0/quantity10,000/fixed$99,999.99 produces a one-cent positive endpoint next to the zero label. Both tick positions differed by about0.00002px. The chart now always retains zero and omits another y-axis tick within22px. Exact values remain in the table. The left gutter increased to80px to accommodate the maximum-loss compact label; actual narrow rendering remains to be witnessed. No arithmetic changed. Current source reviewed; rendered output unverified.

Independent source review of pinned Reveal6.0.2 found that its 'focused' condition follows internal pointer focus, not DOM keyboard focus. This could leave keyboard-only deck arrows inactive and steal table-scrolling arrows after a click. The app now enables Reveal shortcuts only when the deck element itself is document.activeElement. Child inputs/buttons/tables keep native keys. Root must verify keyboard-only deck focus/arrows and table Right without a slide change. This is a source-identified defect, not an invented rendered failure.

## Independent production round: two required fixes

The coordinator observed stale Reveal live-region content after changing the applied scenario on slide3: its accessibility snapshot still contained the prior$0.01 result while the visible card correctly showed−$10,100,000.00. The app now calls the public slide(currentIndex) API at the end of its atomic render. Pinned source inspection confirms this refreshes the native current-slide announcement without a slidechanged event. Internal announceStatus/getStatusText are not on the returned public API and were deliberately not called. Root must recheck current result announcement, active slide, scroll and focus.

The coordinator also observed the maximum supported loss wrapping across three lines at320, splitting the number. The card now uses its own content width and the bounded amount length to choose a readable font size, preserves a16px minimum, and prevents money wrapping. The amount remains exact. Ordinary amounts can still use larger type. The failed screenshot narrow-maximum-card.png is preserved in campaign evidence; actual recheck remains pending.

## Final independent production witness — f21d9f2

The coordinator's actual CUA witness is recorded in the campaign file `presentation/UI-WITNESS.md`. It tested the production prefix with executable checkpoint `f21d9f2b5eebd74ba33cfc34872629c73c1d9ad8`, not a development-only build. The developer did not have an enabled browser surface for these observations and does not present them as its own render checks.

Keyboard-only deck focus and Right advanced slides1→2→3. Quantity Up changed100→101 without navigating, marked edits pending and disabled decision copy. Native Enter applied19.99/12.34/66/500.01: revenue$1,319.34, variable$814.44, contribution$7.65, result$4.89, threshold66. Invalid19.999 focused the price field with aria-invalid, retained$4.89 and disabled copy; Restore recovered the applied input values. The actual copied record included current inputs, arithmetic, assumptions and validation steps. Speaker/context notes were accessible. Clipboard-denial fallback was not independently exercised.

Sensitivity repeatedly entered from a hidden slide retained one SVG and its exact table. Fixed reference rows stayed$300/−$100/$100 while current$4.89 was separate. At320, native keyboard horizontal table scrolling moved121.212px without leaving slide5. All six320px slides measured319px document client/scroll widths and292px section widths; screenshots were visually inspected for readable controls/text, per-slide vertical scrolling and local table scrolling. A1440px production sensitivity view was also visually inspected and captured in `desktop-chart.png`. No390px-specific observation or cross-browser guarantee is inferred.

The near-zero boundary price$10/cost$0/quantity10,000/fixed$99,999.99 showed separate zero/−$100K ticks and exact$0.01 in its table. The maximum-loss chart's−$10.1M label fit. Negative contribution/zero fixed correctly said only zero quantity avoids loss; zero contribution/zero fixed said every volume; positive fixed/zero contribution said no finite quantity.

Both required rendered findings were independently closed. Applying the maximum-loss case on slide3 refreshed the native announcement to−$10,100,000.00 with matching cost and threshold content. At320 the exact amount was on one readable line, documented in `narrow-maximum-card-corrected.png`; the earlier failed capture remains preserved. On the main desktop app, applying price$18 preserved active slide3, focus in the fixed-cost input and section scroll0 while the visible result and native announcement both changed to$100/84units.

The actual browser test page reported41/41. Back from that page after a nondefault applied scenario, pending edit and slide5 restored slide1,20/12/100/500 inputs and baseline$300/63 before interaction. This verifies the observed native history path, not bfcache persistence. Console errors/warnings were empty. Host navigation to the local notice text was blocked; file presence and paths were checked separately, so no claim depends on that failed navigation. No model or source change was required after the corrected checkpoint. Independent reviewer decides final acceptance.

## 2026-10-09 revision — first rounds retained

The first new model run passed43/44: preset.name overwrote an alternative's name in the pure model. Alternative names now follow input spread;44/44 passed. npm ci succeeded/audit0. An initial dependency-check command used an incorrect skill-relative path and failed MODULE_NOT_FOUND; the canonical plugin/scripts/check-dependencies.mjs subsequently passed. Production built successfully.

Source1b25358d7bff65f1873beec1ddfdce8b1c585336 passed44/44 in the actual browser. Fresh production logs were empty and default policy/funding/profit figures appeared correctly. First desktop/narrow screenshots exposed overlapping narrow waterfall labels; shorter labels and reduced compact precision address it, while exact values remain in descriptions/appendix. Initial diagnostic capture preceded heading-font usage; fonts are now explicitly loaded before Reveal geometry. Initial narrow Reveal live announcement omitted dynamically populated fields; render now refreshes the current slide's announcement. Link target minimum grew from24 to26px to avoid subpixel measurements below24. These are new-source fixes; final evaluation follows a fresh checkpoint. Screenshots retain this first round in course evidence.

Final rapid reload→slide-select at72575d40e8ded5246dfe03d4701ca8cd39fef8e5 exposed a real Reveal error: navigation listener ran before asynchronous font/deck initialization completed (dispatchEvent on undefined). Source moves listener activation after initialization and keeps main inert until ready. This is distinct from the source-less MutationObserver message seen after CUA navigation. A fresh checkpoint and affected reload/navigation checks follow.

## 2026-10-09 final revised-source evaluation

Evaluated application source e51279243aa003d06db0aa80fc4f718a4f92758d. Relevant paths: PLAN.md, app/, tests/, scripts/, licenses/, .github/workflows/, package.json, package-lock.json, .npmrc, .node-version, vite.config.js. Locked npm ci (temporary cache), canonical dependency checker and production build passed under Node22.19.0/npm10.9.3; audit0. Fresh committed/staged/working comparisons and untracked relevant-source listing were clean. Report-only changes follow separately.

Independent arithmetic is encoded in44 numerical/boundary checks; all44 passed in Node and the actual browser at http://127.0.0.1:9705/tests/. Default full revenue$7.2m−variable$4.32m−fixed$2.4m=$480k; threshold33,334 (33,333 loses$24;33,334 gains$48). Full stress24,000 gives−$672k. Pilot12,000/$600k fixed gives$264k; stress7,200 gives−$81,600. Funding full$6.72m/pilot$1.896m. Exactly−$200k stress passes, one cent worse fails, and zero base result fails. Tests cover floor/cent rounding, low/high demand, zero/nonpositive contribution, all bounds, exact parsers and record semantics. No UI-heading tests were added.

Actual built app at http://127.0.0.1:9706/bab-example-presentation/ displayed the pilot by default. Editing quantity20,000 live selected defer;60,000 selected full launch with$1.92m base and$192k stress. Blank input retained explicitly labeled last-valid values and disabled copy; Restore recovered. Input ArrowUp changed60,000→60,001 without leaving slide4; focused-deck ArrowLeft navigated. Enter on Copy succeeded and actual clipboard text included$1,896,000 funding, policy, full/pilot stress and limitations. Presentation mode changed to Exit presentation and Escape recovered. Browser-native full-screen availability is not separately certified; the visible presentation mode was exercised. Back after60,000 reset quantity40,000, recommendationpilot and selector0 before interaction, an honest fresh reset. Persisted bfcache was not observed.

All seven desktop/narrow slides were captured and inspected. Three distinct charts render from current data; hidden-to-visible waterfall/volume after60,000 showed$10.8m−$6.48m−$2.4m=$1.92m and updated demand. Exact tables and model appendix are reachable.320-frame maximum price1000/cost0/quantity1m/fixed100m showed$100m proposed funding and$900m full profit; document did not overflow. Keyboard ArrowRight on the exact table moved local scrollLeft to100 after native scrolling settled. One scripted select was attempted before initialization completed and was reset by initialization; fresh ready-state observation then ordinary navigation succeeded without an application error. Main remains inert until ready.

Final authored1440/320/390 frames measured1439/319/389; scrollWidth matched each. Outer document heights1109/1234/1221 with individual slide scrolling for taller content. EB Garamond400/Open Sans400/600 all reported loaded. Observed requests were same-origin hashed JS/CSS and three font assets; no external request appeared in those document performance entries. All measured visible controls were at least24px. Default overview and all-slide desktop/320 evidence, plus390 overview, are saved in the assigned course folder. This is responsive CSS evidence, not a physical-device or full assistive-technology certification.

After the initialization fix, a fresh final tab, rapid reload→slide selection and live chart reentry produced no warnings/errors. A source-less MutationObserver message appeared in older CUA navigation sessions; attribution remains unestablished. The actual app-attributed Reveal initialization failure was fixed and separately rechecked. Public BUILD-STORY links resolve after authorized publication. No source change followed this checkpoint; earlier failures remain above.

## 2026-10-09 independent root review

Root independently issued PASS for e51279243aa003d06db0aa80fc4f718a4f92758d after full model/policy/UI source review, actual44/44 suite and defaultpilot→typed20kdefer→60kfull$1.92m/$192k. It observed invalid price retaining values, Restore recovery, matching risk/funding table, successful rapid reload/select after the initialization correction and empty logs. It inspected320 waterfall labels/readability and independently accepted the explicit policy/boundary checks. Publication of main is authorized; live verification follows separately. This entry is report-only.

## 2026-10-09 remaining-checklist correction rounds

The1450-unit/$100000fixed counterexample is now an independently hand-checked regression: full base4400/stress−37360/funding256600; pilot6320/−6208/71980. Both pass and full-first governance still selects full launch. The explanation now exposes this preference and asks what strategic benefit justifies it. Copy is labeled policy recommendation; one-period/no-learning-value boundaries are explicit.45/45 Node model cases pass; dependency check, fresh npm ci and production build pass.

Narrow slides now use page flow. All-slides reading reuses the current seven DOM sections/model/charts and reveals notes, clearing Reveal hidden/inert restrictions while active; slide mode restores them. Chart geometry and fonts scale together for200% text. The app supplies concise title/input statuses and disables Reveal's additional whole-slide live region; removing the old same-index slide refresh on every valid edit prevents those unnecessary refreshes. This is a source-level interaction correction, not evidence of actual screen-reader speech.

Actual production/320px/200% and keyboard/reading-mode checks are pending root review because this subagent's browser inventory is empty. ALL-11,ALL-16 andDECK-10 remain actual-human evidence gates. Previous failed/evaluated rounds remain retained.

Source follow-up after9bb8a19: removed a redundant setPending early return that could preserve the full-screen-unavailable status after another valid edit. Exiting presentation now restores the correct live/invalid state label. The global label is plain text, not a second live region; short input announcements remain unchanged. Targeted mode-exit inspection is required; model and reading-layout behavior are unchanged.

## Current root browser witness — correction source 9bb8a19, status follow-up c5e033a

Root observed 45/45 passing model cases in the actual browser, all seven sections and three charts in Read all slides, and the exact 1450-kit/$100,000-fixed counterexample at application source `9bb8a19846870a7f0c216ff55c32253d6534e82a`. Full base/stress/funding were $4,400 / −$37,360 / $256,600; pilot values were $6,320 / −$6,208 / $71,980. The prominent full-first policy explanation exposed the pilot's better displayed figures. Returning to slides and selecting assumptions preserved inputs.

Root also confirmed Reveal's aria-status remains aria-hidden=true and aria-live=off after mode cycling/navigation. Generic duplicate text in a DOM snapshot is not evidence of actual screen-reader duplication or successful speech behavior. The current source `c5e033a2e2df414a7d08afdc5dfd1cdac15ed9f1` only restores the live/invalid status after leaving presentation mode; targeted presenter-exit verification remains pending. No model/layout rerun is claimed for that follow-up.

This is a report-only update. Full production, copy, 320px and 200% text review and final independent acceptance remain pending. ALL-11, ALL-16 and DECK-10 human evidence gates stay open; no novice or assistive-technology session is inferred from these checks.

## Retained production failure — intraslide links at c5e033a

At actual319px production, root selected Challenge the assumptions and activated Go to the live result with Enter. Its target remained1332px below the frame top in an1100px-high frame; focus stayed on the anchor. A pointer click also left the target out of view and focused the deck. The current slide expanded in page flow correctly, so overflow layout was not the cause. Source inspection confirms Reveal intercepts hash anchors at the slides container and interprets an element ID as navigation to its containing slide.

The two local input/result links now prevent native hash navigation and stop that click from reaching Reveal, explicitly focus their existing tabindex=-1 target without an implicit scroll, then scroll its start into view. The same browser operation handles desktop slide scrolling, narrow outer-page flow and Read all slides. Ordinary input focus is untouched. Targeted real keyboard/pointer, both directions and reading/slide checks are pending root; no model rerun is required for this link-only correction.

## Root retest closes the intraslide-link failure — source debbe173

Root actually verified both input/result link directions in319px narrow and1280px desktop production, in slide mode and Read all slides. Focus was exactly `#live-result` or `#assumptions`, and each target was visible. The eight retained observations are in course `browser-anchor-retest.json`; narrow result top was33.81px in an1100px-high frame with319px document width/scroll width. The earlier c5e failure remains above.

Present/Exit restored Current valid assumptions, closing the status follow-up. Blank price produced the retained-values warning on release gates and disabled Copy; Restore recovered. Quantity ArrowUp changed40000 to40001 while focus stayed on quantity and the fourth slide remained selected. The actual clipboard contained40001, full base480072 and the policy/alternatives, rather than merely showing a copy-success message.

The separate200%-text production frame measured root/deck32px and1280px document/scroll width. Root inspected the live output and retained `enlarged-live-result.png`. This closes that specific result-view observation, not all chart, table or maximum-value layout checks. No screen-reader speech or novice observation is claimed. App source remains debbe173666df2b5ec41b4a12f1a14918ca4a920; this report changes no application behavior and reruns no unchanged model suite.

## Root maximum-value and chart-layout witness — source debbe173

Root inspected the actual 319px production presentation with price1000, cost0, quantity1000000 and fixed cost100000000. The live result remained readable at $900 million base contribution, $500 million stress contribution and $100 million funding; course `narrow-maximum.png` preserves that view. The economics, risk and sensitivity chart slides were visually inspected with their zero references, labels, legends and exact alternatives. Two ArrowRight presses scrolled the narrow alternatives table to scrollLeft245 of272 while retaining the fourth slide. An earlier reading of0 was taken before native scrolling finished, not a remaining failure.

In the separate1280px frame with root text32px, the risk SVG measured1124px wide with24px chart text and was readable; `enlarged-maximum-risk.png` preserves the result. Root also inspected the enlarged economics ($1 billion sales less $100 million fixed = $900 million contribution) and all five sensitivity rows, including quantity0→−$100 million and1000000→$900 million. These observations close the specified maximum-value/chart/table views. They do not assert that every view on all seven slides or any screen-reader task passed. No application source changed and the unchanged45-case model suite was not repeated.
