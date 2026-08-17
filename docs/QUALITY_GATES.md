# ORBIT Quality Gates

These gates define the release bar for the Everyday Accessible surface.

## P0 — correctness and trust

- Every displayed claim maps to a documented computation or is explicitly labeled as interpretation.
- Fallbacks cannot be presented as semantic understanding.
- No security-sensitive data is sent anywhere without explicit user action and documentation.
- Exported values carry field-level provenance.
- Errors fail visibly and conservatively; no fabricated result is substituted silently.

## P0 — accessibility

- Keyboard-only operation is supported.
- Focus is always visible.
- Color is never the sole carrier of meaning.
- Interactive targets are at least 44×44 CSS pixels.
- Text and controls meet WCAG 2.2 AA contrast targets.
- Motion honors `prefers-reduced-motion`.
- Canvas content has an equivalent textual summary.
- Status updates are exposed to assistive technology.
- Mobile layouts work without horizontal scrolling at common narrow widths.

## P0 — usability

- The primary conclusion appears before technical detail.
- A first-time user can understand each screen without knowing the underlying mathematics.
- Technical evidence is available through progressive disclosure.
- Empty, loading, error, and success states are explicit.
- No unexplained score is presented without a label describing what it means and what it does not mean.

## P1 — engineering quality

- No console errors during normal navigation.
- No unbounded timers/listeners created by rerendering.
- Expensive calculations are debounced or memoized where appropriate.
- Canvas dimensions account for device pixel ratio without causing runaway memory use.
- Export and clipboard operations handle permission/API failure.
- HTML insertion escapes user-controlled text where interpolation is used.
- Third-party dependencies are minimized and pinned where practical.

## P1 — scientific communication

For every method document:

1. input data
2. parameters
3. algorithm
4. validation method
5. limitations
6. interpretation boundary

Implementation verification must not be described as proof that a scientific hypothesis is true.

## Release rule

A release is blocked by any P0 failure. P1 issues may ship only when documented with an owner and follow-up milestone.
