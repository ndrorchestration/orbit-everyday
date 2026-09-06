# Orbit Everyday

**Orbit Everyday** is the plain-language, privacy-oriented UX track for Orbit: an interface for turning analytical state into understandable **Today / Patterns / Questions** views without requiring users to interpret the underlying mathematics.

> **Current status: EXECUTABLE STATIC PROTOTYPE / UX RESEARCH TRACK.** This repository contains a substantial single-file `index.html` implementation with deterministic analytical functions and interactive visualizations. It is no longer accurate to describe the application source as missing. The prototype is not yet a released or fully verified consumer product.

## Role in the Orbit ecosystem

Orbit Everyday and Orbit-Driftwatch now have distinct purposes:

- **Orbit Everyday** — accessible UX, interpretation, local/static analytical experiments, privacy-oriented interaction design.
- **Orbit-Driftwatch** — executable public systems showcase for observable multi-agent orchestration, provider boundaries, provenance, source binding, and Driftwatch-derived telemetry.

Neither repository automatically validates the other. Shared ideas such as Today / Patterns / Open Questions describe design lineage, not transferred evidence.

## Current implementation

The checked-in `index.html` currently includes deterministic implementations and demonstrations for several analytical techniques, including:

- Gram-matrix/eigenvalue-derived effective-rank experiments;
- k-nearest-neighbor density calculations;
- autocorrelation and delay-selection helpers;
- Takens-style embedding experiments;
- Rosenstein-style Lyapunov-exponent estimation;
- deterministic seeded synthetic data generation;
- interactive visual and explanatory panels.

These are **implemented computational experiments**, not proof that the derived quantities have validated psychological, behavioral, or real-world semantic meaning.

## Everyday Accessible design

The intended primary experience remains:

- **Today** — what is most relevant now.
- **Patterns** — recurring structures explained in ordinary language.
- **Questions** — unresolved or repeatedly returning questions.

Technical calculations should support the explanation rather than substitute for it. A value such as an effective-rank estimate should not be presented as a conclusion about a person without an independently justified semantic interpretation.

## Privacy and offline boundary

The design target is:

- local-first;
- no application backend by default;
- no uploaded personal data required for the static analytical prototype;
- offline-capable where all required assets are local.

**Current limitation:** the present HTML imports web fonts from Google Fonts. Therefore a strict “zero network requests / fully offline” claim is **not yet verified** for the current file. The analytical logic itself is client-side, but the external-font dependency must be removed or vendored before the strict offline privacy gate can close.

No future backend integration should silently weaken the local-first model. Networked capabilities, if introduced, should be opt-in and separately disclosed.

## Evidence boundary

| Statement | Current status |
|---|---|
| Executable browser prototype exists | IMPLEMENTED |
| Deterministic analytical functions exist | IMPLEMENTED |
| Static/client-side analytical execution exists | IMPLEMENTED |
| Mathematical routines have complete independent verification | **NOT YET ESTABLISHED** |
| Today / Patterns / Questions product experience is release-complete | **NOT YET ESTABLISHED** |
| Strict zero-network offline operation | **NOT YET VERIFIED — external font dependency remains** |
| Analytical metrics have validated psychological/semantic meaning | **NOT ESTABLISHED** |
| Consumer-product privacy/security review is complete | **NOT ESTABLISHED** |

## Verification priorities

The release checklist in [`docs/RELEASE_CHECKLIST.md`](docs/RELEASE_CHECKLIST.md) remains the quality gate. Highest-value next checks are:

1. remove the external font/network dependency and verify zero-network static operation;
2. add deterministic fixtures and independent cross-checks for critical mathematical functions;
3. verify keyboard, screen-reader, contrast, reduced-motion, canvas alternatives, and narrow-mobile behavior;
4. reconcile every in-app `verified`/provenance label against retained evidence;
5. bound large-input behavior and expensive calculations;
6. smoke-test the exact release artifact in a clean browser context.

## Repository structure

```text
orbit-everyday/
├── index.html                  # current executable static prototype
├── README.md
├── LICENSE
├── docs/
│   └── RELEASE_CHECKLIST.md
└── .gitignore
```

A future modularization into `src/`, `tests/`, and `public/` may improve maintainability, but the current single-file prototype is real source and should be evaluated as such rather than described as missing.

## Quality rule

Orbit Everyday should be judged first from the user's perspective:

> Can a non-technical person understand what Orbit computed, what is directly observed versus inferred, why it may matter, and what remains uncertain?

Mathematical rigor supports that experience; it does not turn an exploratory metric into a validated human conclusion.
