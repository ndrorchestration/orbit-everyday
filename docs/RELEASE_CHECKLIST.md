# ORBIT Release Checklist

## Product

- [ ] Today / Patterns / Questions views are implemented.
- [ ] Plain-language summaries are understandable without technical background.
- [ ] Technical detail is progressively disclosed.
- [ ] Empty/loading/error/success states are complete.

## Accessibility

- [ ] Keyboard-only pass completed.
- [ ] Focus visibility pass completed.
- [ ] Screen-reader semantics reviewed.
- [ ] Color-independent meaning verified.
- [ ] 44px minimum target audit completed.
- [ ] WCAG 2.2 AA contrast audit completed.
- [ ] Reduced-motion behavior tested.
- [ ] Canvas/text-equivalent audit completed.
- [ ] Narrow-mobile layout tested.

## Correctness

- [ ] All mathematical functions have deterministic test fixtures.
- [ ] Independent cross-checks exist for critical calculations.
- [ ] Boundary cases are tested.
- [ ] Provenance labels match actual implementation.
- [ ] No unsupported semantic claims remain.

## Security/privacy

- [ ] No secrets are present in source.
- [ ] User input is safely rendered.
- [ ] Network requests are documented and intentional.
- [ ] Export contents are reviewed for unnecessary sensitive data.
- [ ] Third-party dependencies and licenses are documented.

## Performance

- [ ] No runaway rerender/listener behavior.
- [ ] Expensive calculations are bounded/debounced.
- [ ] Canvas DPR handling is tested on mobile and desktop.
- [ ] Large-input behavior has a defined limit or graceful degradation.

## Evidence

- [ ] README matches shipped behavior.
- [ ] Verification notes are current.
- [ ] Quality gates are satisfied.
- [ ] A production build has been manually smoke-tested.
- [ ] Export/import behavior is reproducible where applicable.

**Release decision:** PASS only when all P0 gates are satisfied.
