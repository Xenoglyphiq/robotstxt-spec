# Changelog

Spec releases. Ports vendor a tagged release into `.spec/`; the version here is `spec_version` in `spec/capability.yaml`.

## 0.1.1 — 2026-10-06

No behavior change; conformance cases are identical (only their `spec_version` stamp changed).

- `bench/`: benchmark input (`robots.txt`, `paths.txt`, checksum 24281055), the shared method, and the Rust reference (`texting_robots` crate `=0.2.2`).

## 0.1.0 — 2026-10-06

First release: `parse`, `is_allowed`, `matching_rule`, `status_policy` and `crawl_delay` (an extension) in core, `fetch` in io; 3 error codes; 2 limits; 125 conformance cases (112 core, 13 io), cross-checked against `protego` 0.7.0 and including Google's RFC tests; decisions D-001 to D-010.
