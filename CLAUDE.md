# Claude Guidelines

## Build/Test Commands
- Go: `go test ./...` (all tests), `go test -v ./path/to/test -run TestName` (single test)
- Rust: `cargo test` (all tests), `cargo test test_name` (single test)
- React/TS: `npm test` (all tests), `npm test -- -t "test name"` (single test)
- Lint: `golangci-lint run` (Go), `cargo clippy` (Rust), `eslint .` (TS/React)

## Code Style Guidelines
- **Backend**: Go or Rust only for API development (per project requirements)
- **Frontend**: React with TypeScript, functional components preferred
- **Imports**: Group by standard lib, external, internal; alphabetical order
- **Formatting**: Use standard formatters (gofmt, rustfmt, prettier)
- **Types**: Strong typing required, no implicit conversions, avoid `any` in TS
- **Naming**: Follow language conventions (camelCase for JS/TS, snake_case for Rust)
- **Error Handling**: Explicit error handling, no silent failures
- **Security**: Follow OWASP best practices, input validation, proper auth
- **Documentation**: Document public interfaces and complex functions

Refer to design docs for project-specific requirements. Collaboration with team members required.