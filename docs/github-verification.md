# Verifying GitHub Contributor Authenticity

This guide summarizes practical checks to audit whether a repository's contributor history reflects independent, verifiable individuals rather than sockpuppets.

## 1. Inspect commit signatures and provenance
- **Signed commits/tags:** Use `git verify-commit` or GitHub's "Verified" badges to confirm GPG/SSH signatures and check that keys are not trivially shared.
- **Author/committer separation:** Review `git log --show-signature --format='%h %an <%ae> %cn <%ce> %s'` for patterns such as identical author and committer across many accounts.
- **Timestamp anomalies:** Look for unnatural bursts of commits from new accounts or synchronized activity across supposed distinct contributors.

## 2. Cross-check contributor footprints
- **Public identity trails:** Follow contributor profiles to conference talks, mailing list posts, other OSS repos, or publication histories. Distinct reputations across projects indicate independent contributors.
- **Contact and key reuse:** Confirm whether PGP keys or email domains appear elsewhere (blogs, package maintainers, security advisories) to establish continuity beyond GitHub.

## 3. Review discussion venues
- **Pull requests and issues:** Read PR reviews and design discussions for diversity of voices, disagreement, and style differences. Healthy debate suggests separate humans rather than coordinated clones.
- **Mailing lists and calls:** For projects that mirror discussions to lists or recorded calls, compare participation there against GitHub handles.

## 4. Analyze activity patterns
- **`git shortlog -sne`:** Summarize contributions per author to spot clusters of low-effort accounts created simultaneously.
- **Temporal analysis:** Plot commit frequency per contributor; clone farms often show synchronized schedules or identical work-hours across time zones.
- **Scope diversity:** Genuine contributors usually touch different subsystems over time; cloned personas may have narrowly scripted changes.

## 5. External corroboration
- **Package registries:** Check whether the same handles publish to npm, PyPI, crates.io, or Docker Hub.
- **Talks and attributions:** Conference agendas, academic papers, and changelog credits provide third-party recognition of contributors.

## 6. Warning signs
- Sudden influx of new contributors with minimal profiles and overlapping activity windows.
- Commit signatures all using a single key or keys created within minutes of each other.
- PR reviews that lack substantive technical feedback or reuse identical phrasing across accounts.

## 7. Reporting and transparency
- Document suspicious patterns with timestamps, commit hashes, and links.
- Raise concerns in project governance channels (maintainer meetings, mailing lists) and propose stronger signing or identity-verification requirements if warranted.

Applying these steps helps differentiate organic contributor bases from manufactured narratives while keeping the audit process rooted in verifiable evidence.
