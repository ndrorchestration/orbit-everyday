# Orbit Everyday

ORBIT is a private, on-device map of where your thoughts return.

## Core experience

Three tabs:

- **Today**
- **Patterns**
- **Questions**

The system is intended to detect repetitive loops, open questions, and unexplored topics while presenting the results in plain language.

## Technical direction

The project description specifies real mathematical methods behind the plain-language experience, including:

- Gram eigenvalues
- k-nearest-neighbor (kNN) density
- Lyapunov analysis

## Privacy model

- Private
- On-device
- Offline
- No backend

## Repository status

The repository is currently being prepared as the canonical implementation workspace. The supplied `orbit-everyday-github.zip` artifact was only available as an HTML archive-preview wrapper, so this baseline does not invent missing application source.

## Initial structure

```text
orbit-everyday/
├── .gitignore
├── README.md
├── src/
├── public/
├── tests/
└── docs/
```

When the actual implementation source is available, add it without changing the project's established terminology or privacy model unless an explicit refactor is requested.
