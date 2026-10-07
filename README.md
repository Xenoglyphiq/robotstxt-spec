# robots.txt

Parse robots.txt files and decide whether a crawler may fetch a path. Implements [RFC 9309](https://www.rfc-editor.org/rfc/rfc9309.html), the Robots Exclusion Protocol, with Google's open-source parser as the tie-breaker where the RFC is loose.

The spec and conformance cases for robots.txt. Each language port lives in its own repo and is tested against the same cases.

## Ports

| Language | Repo | Package | Spec pinned | Conformance | Status |
|---|---|---|---|---|---|
| Julia | [`Xenoglyphiq/RobotsTxt.jl`](https://github.com/Xenoglyphiq/RobotsTxt.jl) | `RobotsTxt` | 0.1.2 | core ✓ io ✓ full ✓ (130/130) | version 0.1.0 committed; General registration pending |
| Swift | [`Xenoglyphiq/robotstxt-swift`](https://github.com/Xenoglyphiq/robotstxt-swift) | `RobotsTxt` | 0.1.2 | core ✓ io ✓ full ✓ (130/130) | **released 0.1.0**: git tag; Swift Package Index submission pending |
| Zig | [`Xenoglyphiq/robotstxt-zig`](https://github.com/Xenoglyphiq/robotstxt-zig) | `robotstxt` | 0.1.2 | core ✓ io ✓ full ✓ (130/130) | **released v0.1.0**: git tag; tagged `zig-package` for zigistry to index |

Install instructions and examples are in each port's repo.

## What's here

| Path | What |
|---|---|
| `spec/SPEC.md` | Behavior spec |
| `spec/capability.yaml` | Machine-readable contract: types, operations, errors, limits |
| `conformance/` | Test cases every port must pass; regenerate with `uv run conformance/generate/generate.py` |
| `bench/` | Shared benchmark input, method and the Rust reference |
| `.kit/` | Shared conventions, schemas and validator (vendored) |
| `CONTRIBUTING.md` | How changes to the spec are made |
| `DECISIONS.md` | Why the spec is the way it is, including where it differs from Google's parser and from the oracle |
| `CHANGELOG.md` | What each spec release changed |
| `NOTICE` | Attribution for test cases translated from `google/robotstxt` |

## Contributing

See `CONTRIBUTING.md`.

## License

MIT OR Apache-2.0. Some conformance cases are translated from `google/robotstxt` (Apache-2.0); see `NOTICE`.
