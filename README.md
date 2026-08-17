# Orbit Everyday

**Orbit Everyday** is the plain-language interface for Orbit: a private, on-device way to understand where your thoughts return.

## Everyday Accessible

The product is designed for non-technical users. The interface should explain results in terms of what a person can **see, understand, and do next**, rather than exposing mathematical machinery as the primary experience.

### Core experience

Three tabs:

- **Today** — what is most relevant right now.
- **Patterns** — recurring themes and loops, explained in ordinary language.
- **Questions** — unresolved or repeatedly returning questions.

The system should help a person recognize patterns without requiring them to understand the underlying mathematics.

## Accessibility baseline

- Light mode by default.
- Inter, 16px body text.
- Minimum 44px interactive targets.
- Responsive desktop and mobile layout.
- Plain-language labels and explanations.
- Progressive disclosure for technical detail.
- No technical metric should be required to understand the primary result.

## Technical foundation

The accessible interface sits above real analytical methods. Current technical direction includes:

- Gram-matrix eigenvalue analysis.
- k-nearest-neighbor (kNN) density analysis.
- Lyapunov-style stability analysis.

These methods are implementation details unless a user explicitly chooses to inspect them. For example, an internal value such as `effRank 0.42 via Gram eigenvalues` should be translated into an understandable explanation before it is presented as a user-facing result.

## Privacy model

Orbit Everyday is intended to remain:

- **Private**
- **On-device**
- **Offline-capable**
- **No-backend by default**

The interface must not weaken this privacy model merely to make the product easier to demonstrate.

## Repository status

This repository is the canonical implementation workspace. The current repository contains the project baseline and documentation, but the previously supplied `orbit-everyday-github.zip` artifact was available only as an HTML archive-preview wrapper rather than recoverable application source.

Accordingly, this repository does **not** invent missing application code. The next implementation commit should add the verified source artifact when it is available.

## Structure target

```text
orbit-everyday/
├── .gitignore
├── LICENSE
├── README.md
├── src/
├── public/
├── tests/
└── docs/
```

## Quality rule

Orbit Everyday should be judged first from the user's perspective:

> Can a non-technical person understand what Orbit found, why it matters, and what they can do next?

Mathematical rigor remains important, but it supports the experience rather than becoming the experience.
