# ORBIT Threat Model

## Scope

The current artifact is primarily a client-side analytical interface. The threat model covers user data, exports, browser execution, third-party resources, and future integrations.

## Assets

- User-entered questions and text
- Analytical inputs and derived values
- Exported JSON
- Provenance and configuration metadata
- Future model/API credentials, if integrations are added

## Trust boundaries

1. User input → browser application
2. Browser application → third-party CDN resources
3. Browser application → downloaded export
4. Future browser/application → remote model or API service

## Primary risks

### Data leakage

User-entered material must remain local unless a feature explicitly states that it sends data remotely and obtains appropriate user consent.

### Dependency compromise

Third-party JavaScript should be minimized. If a model runtime or other dependency is introduced, pin versions where practical and document its source, license, integrity strategy, and network behavior.

### Injection

User-controlled strings must not be inserted into HTML as trusted markup. Prefer `textContent`, DOM APIs, or a vetted sanitizer for dynamic content.

### Export oversharing

Exports should contain only the fields required for the selected export. Sensitive user content should not be included by default merely because it is available in application state.

### False authority

A technically correct algorithm can still produce misleading interpretations. Provenance, limitations, and confidence language are therefore security-adjacent trust controls, not merely documentation.

## Security requirements for future remote integrations

- Never ship provider secrets in client-side source.
- Use a server-side boundary for privileged credentials.
- Minimize transmitted data.
- Document retention and provider processing.
- Add explicit consent before transmission.
- Provide a local/offline path when feasible.

## Current boundary

The v4 artifact does not load a transformer model or require a privileged backend. The hash-vector fallbacks must remain clearly identified until a genuine embedding implementation is introduced.
