# ORBIT Everyday Accessible

## Product direction

ORBIT Everyday Accessible is the human-facing presentation layer for the ORBIT analytical engine. It should make useful findings understandable without requiring users to know linear algebra, eigendecomposition, kNN density estimation, Takens embedding, or Lyapunov analysis.

## Required experience

- **Light mode by default**
- **Inter, 16px minimum body text**
- **WCAG AA-oriented contrast and focus treatment**
- **44px minimum interactive targets**
- **Mobile-first responsive layout**
- Plain-language labels and explanations
- Progressive disclosure: show the conclusion first; expose technical detail through **Show the math** / evidence controls
- No backend required for the everyday experience
- Computation remains local/on-device where practical
- No claim should be presented as semantic, predictive, or verified unless the underlying computation supports that claim

## Three primary views

### Today

A concise current-state view. Show only the most useful findings, status, and next action. Avoid unexplained numerical metrics.

### Patterns

Translate the analytical outputs into understandable observations. Examples:

- clusters → "These items tend to appear together"
- density gaps → "There is an area with relatively little activity"
- entropy → "The signal is spread across several patterns"
- effective rank → "The information appears to use several distinct dimensions"
- temporal analysis → "This pattern appears to repeat over time"

The exact wording must remain proportional to what the computation actually establishes.

### Questions

A user-facing space for unresolved items, with explicit distinction between:

- observed evidence
- interpretation
- unresolved question
- user decision

The existing Debt Ledger mechanism can provide the underlying interaction, but its hash-vector fallback must never be described as semantic understanding.

## Progressive disclosure

Every technical finding should support this hierarchy:

1. **What happened?** — plain language
2. **Why does ORBIT say that?** — concise evidence
3. **Show the math** — formula, method, parameters, and provenance
4. **Inspect/export** — raw computed values where useful

## Provenance rules

Use three states consistently:

- **Verified** — the named computation actually runs against the displayed data and has an appropriate validation check.
- **Computed** — the mechanism is real, but no independent validation claim is being made.
- **Fallback** — an approximation or deterministic substitute is being used and must be named explicitly.

Never use a blanket "verified" label for an entire screen when individual fields have different provenance.

## Accessibility acceptance criteria

- Keyboard reachable controls
- Visible focus indicator
- No interaction dependent on color alone
- Canvas visualizations have text alternatives or adjacent numerical summaries
- Form controls have labels
- Status changes are announced through accessible status/alert semantics
- Touch targets are at least 44×44 CSS pixels
- Layout remains usable at narrow mobile widths
- Reduced-motion preference is respected for non-essential animation
- Content remains understandable when technical detail is collapsed

## Scope boundary

The v4 technical artifact remains useful as the verification/research surface. The Everyday Accessible surface is a separate presentation concern: it should simplify the language and navigation without weakening the underlying computation or provenance model.
