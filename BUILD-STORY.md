# How Desk / Day was built

The original simulated student brief was: “I need to present a product-launch recommendation to the board. I want a polished slide story with a few local assumptions I can change during discussion, charts that update correctly, and an appendix explaining the model. Live means interactive in the room, not fetching new external data.”

The actual [simulated planning conversation](PLANNING-CONVERSATION.md) narrowed the initial example to a small pop-up. That record is retained. The user's later live-app revision restored the board-level stakes, multiple charts and model appendix; it did not fabricate another student approval. [The current plan](PLAN.md) and [decisions](DECISIONS.md) explain the revised scope.

Browser App Builder's managed-build, analytical-presentation and decision-model workflows shaped the implementation: exact cents, explicit assumptions, local calculations, browser-visible tests and a source checkpoint before evaluation. Reveal.js owns the seven-slide story. Three native SVG charts show economics, downside alternatives and demand sensitivity. Licensed local EB Garamond and Open Sans follow Campus Designer typography and published colors, without marks or affiliation claims.

The default synthetic board case recommends a$1.896m staged pilot. Its$264,000 base result and−$81,600 stress result clear the explicit policy; the full launch's−$672,000 stress does not. Lower demand defers the commitment; stronger demand can permit the full launch. Valid inputs update all slides, and invalid fields visibly preserve the last valid result. The appendix distinguishes funding from profit, discloses scaling policy and omitted cash-flow/tax/inventory effects, and avoids demand or probability claims.

[Model tests](tests/model.test.js) check independent known answers, policy boundaries, cent precision and numeric edges. [Evaluation](EVALUATION.md) preserves observed browser/production results and failed rounds. [Deployment](DEPLOYMENT.md) distinguishes reviewed source from live publication. Every figure is synthetic; this is an independent classroom example.

## Try the experiment

Predict before changing the controls. “Read all slides” presents the same current assumptions, charts, appendix and speaker notes as a document. On a narrow screen, the current slide expands in the page; “Go to the live result” and “Back to the inputs” keep the challenge slide navigable. Reload restores the board case; copy the **policy recommendation** before leaving. That record contains calculated policy, not your judgment or an approval.

1. **Predict when a profitable case should pause.** In the board case, compare full-launch base/stress results with the pilot. Before selecting “Lower ·20,000,” predict whether a smaller pilot still passes. Then select “Stronger ·60,000,” and explain which gate changes. Both demand presets restore the board-case price$180, unit cost$108 and fixed cost$2.4m; changing only quantity under other edited costs may give a different answer.

   **Answer:** The default full launch earns$480,000 at base demand but loses$672,000 at60% volume, beyond the$200,000 loss limit. The pilot earns$264,000 at base and loses$81,600 in stress; funding is$1,896,000. At20,000 full demand, both operating options fail, so defer. At60,000, full launch earns$1,920,000 at base and$192,000 in stress, passing both gates. Stress volumes are assumptions, not probabilities or worst-case guarantees.

2. **Challenge the governing preference.** Set price$180, unit cost$108, full annual sales1,450, and fixed cost$100,000. Before looking at the result, calculate both options' base result,60%-volume stress and funding. Predict which you would prefer, then compare that judgment with the model policy.

   **Answer:** Full launch sells1,450 base kits and870 stress kits: base1,450×$72−$100,000=$4,400; stress870×$72−$100,000=−$37,360; funding1,450×$108+$100,000=$256,600. Pilot sells floor(30%×1,450)=435 base kits,261 stress kits and carries$25,000 fixed cost: base$6,320, stress−$6,208, funding$71,980. Both pass. The **full-first governance preference** still selects full launch even though the pilot has a higher base result, smaller stress loss and lower funding. What strategic benefit justifies full scale? Write your own choice and one piece of evidence that could change it. The app has no modeled strategic benefit; passing gates is not proof of the best economic choice.

3. **Separate a smaller launch from learning.** Return to the board case. State exactly how pilot scale is modeled, then name one thing a pilot could reveal about demand, conversion, supplier cost or operations. Explain how that information could change a later full-launch decision.

   **Answer:** Pilot demand is30% of full demand, rounded down to whole kits; pilot fixed cost is25% of full fixed cost, rounded to cents. The arithmetic compares one-period operating choices. It assigns no value to information, contains no second-stage rollout and does not predict what the pilot will teach. A later scale decision needs updated evidence and a separately justified policy.

4. **Check live-state honesty.** Enter a blank price. Before restoring it, explain which assumptions the visible figures still use. Choose “Restore valid values,” then switch into all-slides reading and inspect the appendix and policy record.

   **Answer:** Blank price is invalid; all results retain the last valid scenario and copying is disabled. Restore returns those same valid values. Reading mode shares the model state rather than taking a stale screenshot. The model excludes inventory losses, financing, timing, taxes and price-driven demand response.

## Optional extension: a different argument and decision rule

Replace the business question, enumerate meaningful alternatives, state a defensible choice rule and explain what evidence could falsify it. Decide whether your rule maximizes a defined measure or applies a governance preference; do not silently treat these as equivalent. Hand-check the option arithmetic and at least one boundary where the choice changes. Keep only the numerical model needed for that argument. Renaming the company or editing prices alone does not complete this extension.
