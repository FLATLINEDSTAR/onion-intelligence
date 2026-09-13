# onion-intelligence

## Project Purpose
The **onion-intelligence** repository hosts the core intelligence engine of the FLATLINEDSTAR ecosystem. It provides high‑level decision‑making, analytics, and policy logic that consumes observations from the data pipeline and produces actionable insights.

## Current Status
**Planning** – the repository currently contains only a placeholder README. No production code exists yet.

## Why It Exists
It separates *intelligence* (the reasoning layer) from the *platform* (deployment/runtime) allowing the engine to be versioned, tested, and used independently (e.g., by the `onion-cli`).

## Architecture Role
- Consumes normalized data from **query‑engine** (and indirectly from `tech-fingerprint`, `entity-extractor`, `change-detector`).
- Exposes a stable Go/Python/JS SDK via `onion-sdk` for downstream consumers.
- Provides a set of public interfaces such as `OnionTarget`, `OnionObservation`, `SearchQuery`, `SearchResult`.

## Planned Features (MVP)
- Define core data models and interfaces.
- Implement rule‑engine skeleton.
- Provide a JSON‑RPC API for query execution.

## Installation / Usage
*Not applicable until implementation.*

## Development
- Language: Go (primary) with optional bindings for Python.
- Follow the contribution guidelines in the organization `.github` directory.

## Testing
- Unit tests for each rule module.
- Integration tests using mocked observations from downstream services.

## Contributing
See the organization‑wide `CONTRIBUTING.md`.

## Roadmap
- **Phase 1**: Define data contracts (shared types in `onion-sdk`).
- **Phase 2**: Implement rule engine core.
- **Phase 3**: Expose public API and integrate with `onion-platform`.

## Relationship to FLATLINEDSTAR Ecosystem
It is the flagship intelligence component; the `onion-platform` application orchestrates it, while `onion-cli` can invoke its APIs directly.

## License
MIT – see LICENSE in the root repository.