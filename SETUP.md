# Setup

Existing runtime Node22.19.0 and npm10.9.3. Exact dependencies: reveal.js6.0.2 and Vite8.3.4. Managed starter, reveal theme and local design tokens copied from the installed Browser App Builder package; the app and numerical model are original. `.npmrc` disables lifecycle scripts and exact-pins installations.

`npm install` and clean `npm ci --ignore-scripts --cache /private/tmp/bab-npm-cache` completed; npm reported18 audited packages and0 vulnerabilities at this run. Canonical dependency checker passed. `npm test` passed41/41 actual pure-model cases. Production build succeeded without a bundle warning:130.01KB JS/35.47KB gzip estimate,65.80KB CSS/14.63KB gzip estimate. Gzip sizes are build estimates, not guaranteed host transfer sizes. Notice generation retains reveal.js's MIT license; no second runtime library is installed.

Servers retained for review: test9517/session96508, production9518/session12161. Production prefix `/bab-example-presentation/`. Developer browser CUA currently exposes no enabled browser, so developer source/Node results are not labeled browser or rendered passes. The coordinator's independent active browser performs UI witnessing; reviewer assesses those observations separately.
