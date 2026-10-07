# Changelog

Spec releases. Ports vendor a tagged release into `.spec/`; the version here is `spec_version` in `spec/capability.yaml`.

## 0.1.1 — 2026-10-06

No behavior change for implementations that follow the 0.1.0 text. Four new cases (129 total: 116 core, 13 io) pin what 0.1.0 said but didn't test, found by the Julia port:

- Matching uses a pattern's **original bytes**, never the U+FFFD text it's reported with. The 0.1.0 generator got this wrong; no 0.1.0 case depended on it. New cases `encoding.invalid_utf8_rule` and `encoding.invalid_utf8_rule_not_fffd`.
- Invalid UTF-8 is reported as **one U+FFFD per maximal invalid subpart**; new case `parse.invalid_utf8_subparts`.
- A crawl-delay too large for `f64` is skipped; new case `parse.crawl_delay_not_finite`.
- `bench/`: benchmark input (`robots.txt`, `paths.txt`, checksum 24281055), the shared method, and the Rust reference (`texting_robots` crate `=0.2.2`).

## 0.1.0 — 2026-10-06

First release: `parse`, `is_allowed`, `matching_rule`, `status_policy` and `crawl_delay` (an extension) in core, `fetch` in io; 3 error codes; 2 limits; 125 conformance cases (112 core, 13 io), cross-checked against `protego` 0.7.0 and including Google's RFC tests; decisions D-001 to D-010.
