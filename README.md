# .github

Org-wide documentation for the ghostinthewires project.

## Contents

- [`KEYS.md`](KEYS.md) — Public keys and their purposes. Verify signatures on all project artifacts against the signing key listed here.
- [`KEYS.md.asc`](KEYS.md.asc) — Detached GPG signature of KEYS.md.
- [`README.md.asc`](README.md.asc) — Detached GPG signature of this file.

## Verifying KEYS.md

```bash
gpg --fetch-keys https://ghostinthewires.net/.well-known/signing-key.asc
gpg --verify KEYS.md.asc KEYS.md
```

## Additional Documentation

- [Security Policy](SECURITY.md) — how to report vulnerabilities
- [Warrant Canary](https://ghostinthewires.net/canary) — monthly attestation of project integrity
