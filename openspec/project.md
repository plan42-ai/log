# Project Context

## Purpose
Provide a lightweight logging helper library for Plan42 Go services with structured logging defaults.

## Tech Stack
- Go 1.25
- Standard library logging utilities

## Project Conventions

### Code Style
Use gofmt for formatting and golangci-lint via `make lint`. Maintain simple, structured logging interfaces and avoid API bloat.

### Architecture Patterns
Single Go package exposing logging primitives and helpers. Designed for reuse across services with minimal dependencies.

### Testing Strategy
`go test ./...` for unit coverage. Keep tests deterministic around time/output formatting where possible.

### Git Workflow
Feature branches merged via PR; tag releases with `make tag` when publishing new versions.

## Domain Context
Used by numerous Plan42 services to standardize log structure. Changes should remain backward compatible to avoid breaking log parsing.

## Important Constraints
- Keep dependencies minimal and avoid pulling heavy logging frameworks.
- Preserve existing log formats to maintain observability pipelines.

## External Dependencies
None; library-only functionality.
