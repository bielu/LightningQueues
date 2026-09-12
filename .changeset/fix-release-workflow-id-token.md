---
---

CI-only fix: grant `id-token: write` to the jobs that call the shared `release.yml`, so the
workflow passes GitHub's startup validation. Deliberately empty (no package bump) — this changes
only the release pipeline, not anything in the published packages, and must not perturb the
`0.0.0 -> 1.0.0` arithmetic that `first-stable-release.md` pins.
