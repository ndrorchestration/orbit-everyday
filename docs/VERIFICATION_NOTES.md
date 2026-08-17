# ORBIT v4 Verification Notes

## Current implementation

`index.html` is the technical verification artifact. It intentionally exposes the analytical machinery and labels the substrate used by each feature.

## Verified surfaces

- k-means clustering: Lloyd's algorithm on the generated point set
- kNN graph: actual nearest-neighbor graph over the displayed points
- effective rank: Gram matrix eigenvalue computation with power iteration/deflation and a Jacobi cross-check
- void map: kNN density estimate with a data-derived percentile threshold
- lens entropy: Shannon entropy over normalized singular values
- temporal analysis: Takens embedding and Rosenstein-style divergence estimation
- export: includes field-level provenance and underlying sample data

## Honest fallback surfaces

- Debt similarity uses deterministic hash vectors rather than semantic embeddings.
- Capture uses a deterministic hash vector rather than a transformer model.

These fallbacks are intentionally retained so the artifact does not imply capabilities it does not ship.

## Important interpretation boundary

A numerical method being correctly implemented does not automatically establish that the resulting interpretation is scientifically valid for arbitrary real-world data. The user-facing layer should distinguish implementation verification from domain validity.

## Next implementation gate

The next product milestone is not adding more mathematics. It is converting the verified technical surface into the Everyday Accessible experience defined in `EVERYDAY_ACCESSIBLE.md`: three human-language views (Today, Patterns, Questions), light-mode default, mobile-first interaction, 44px targets, WCAG AA-oriented presentation, and progressive disclosure of technical evidence.
