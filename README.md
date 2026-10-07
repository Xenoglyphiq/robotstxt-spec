# robots.txt

Parse robots.txt files and decide whether a crawler may fetch a path. Implements [RFC 9309](https://www.rfc-editor.org/rfc/rfc9309.html), the Robots Exclusion Protocol, with Google's open-source parser as the tie-breaker where the RFC is loose.

The spec and conformance cases for robots.txt. Each language port lives in its own repo and is tested against the same cases.

## Ports

| Language | Repo | Package | Spec pinned | Conformance | Status |
|---|---|---|---|---|---|
| Julia | `Xenoglyphiq/RobotsTxt.jl` | `RobotsTxt` | – | – | planned |
| Swift | `Xenoglyphiq/robotstxt-swift` | `RobotsTxt` | – | – | planned |
| Zig | `Xenoglyphiq/robotstxt-zig` | `robotstxt` | – | – | planned |

Install instructions and examples will be in each port's repo.

## What's here

| Path | What |
|---|---|
| `spec/SPEC.md` | Behavior spec |
| `spec/capability.yaml` | Machine-readable contract: types, operations, errors, limits |
| `conformance/` | Test cases every port must pass; regenerate with `uv run conformance/generate/generate.py` |
| `.kit/` | Shared conventions, schemas and validator (vendored) |
| `CONTRIBUTING.md` | How changes to the spec are made |
| `DECISIONS.md` | Why the spec is the way it is, including where it differs from Google's parser and from the oracle |
| `CHANGELOG.md` | What each spec release changed |
| `NOTICE` | Attribution for test cases translated from `google/robotstxt` |

## Contributing

See `CONTRIBUTING.md`.

## License

MIT OR Apache-2.0. Some conformance cases are translated from `google/robotstxt` (Apache-2.0); see `NOTICE`.
