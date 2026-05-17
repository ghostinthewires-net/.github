# .github

Org-wide documentation for the ghostinthewires project.

## Contents

### Integrity Verification
- [`SHA512SUMS`](SHA512SUMS) — SHA512 hashes of all tracked files.
- [`SHA512SUMS.asc`](SHA512SUMS.asc) — Detached GPG signature of SHA512SUMS.
- [`BLAKE3SUMS`](BLAKE3SUMS) — BLAKE3 hashes of all tracked files.
- [`BLAKE3SUMS.asc`](BLAKE3SUMS.asc) — Detached GPG signature of BLAKE3SUMS.

### Keys and Trust
- [`KEYS.md`](KEYS.md) — Public keys and their purposes. Verify signatures on all project artifacts against the signing key listed here.
- [`KEYS.md.asc`](KEYS.md.asc) — Detached GPG signature of KEYS.md.
- [`SECURITY.md`](SECURITY.md) — Vulnerability disclosure policy.
- [`SECURITY.md.asc`](SECURITY.md.asc) — Detached GPG signature of SECURITY.md.
- [`TRUST.md`](TRUST.md) — Signed cryptographic assertion of key ownership and trust hierarchy.
- [`TRUST.md.asc`](TRUST.md.asc) — Detached GPG signature of TRUST.md.

### Warrant Canary
- [`canary/canary-current.txt`](canary/canary-current.txt) — Current warrant canary.
- [`canary/canary-current.txt.asc`](canary/canary-current.txt.asc) — Detached GPG signature of current canary.
- [`canary/`](canary/) — Archive of all historical canaries with signatures.

Served at:
- https://ghostinthewires.net/canary.txt
- https://ghostinthewires.net/canary.txt.asc

### Automation
- [`.githooks/pre-commit`](.githooks/pre-commit) — Pre-commit hook that generates and signs SHA512SUMS and BLAKE3SUMS on every commit.
- [`.githooks/pre-commit.asc`](.githooks/pre-commit.asc) — Detached GPG signature of the pre-commit hook.

### Organization Profile
- [`profile/README.md`](profile/README.md) — Organization profile page, displayed on the ghostinthewires-net GitHub org page.
- [`profile/README.md.asc`](profile/README.md.asc) — Detached GPG signature of the org profile.

### This File
- [`README.md`](README.md) — This document. Lists and describes all files in this repository.
- [`README.md.asc`](README.md.asc) — Detached GPG signature of this README.

## Verifying Files

```bash
# Import the signing key (once)
gpg --fetch-keys https://ghostinthewires.net/.well-known/signing-key.asc

# Verify any file
gpg --verify FILE.asc FILE

# Verify all tracked files
gpg --verify SHA512SUMS.asc SHA512SUMS && sha512sum -c SHA512SUMS
gpg --verify BLAKE3SUMS.asc BLAKE3SUMS && b3sum --check BLAKE3SUMS
```