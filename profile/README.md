# ghostinthewires

A security-focused open source organization building tools, infrastructure, and documentation for people who treat privacy as a right, not a feature.

---

## Projects

### [netrunner](https://github.com/ghostinthewires-net/netrunner)
A reproducible, hardened Linux workstation available in Arch and Gentoo editions. Full disk encryption, hardware-backed unlock via TPM2 and YubiKey, kernel hardening, private DNS, and Wayland/Hyprland — documented, auditable, and overridable.

### [hardline](https://github.com/ghostinthewires-net/hardline)
Hardened Raspberry Pi network infrastructure. DNS filtering, VPN-routed containers, firewall, and network monitoring — the infrastructure layer that netrunner and other systems depend on.

### [handbook](https://github.com/ghostinthewires-net/handbook)
An operational security handbook covering the full lifecycle of operating on the internet with integrity and privacy — threat modeling, cryptographic key infrastructure, system hardening, and publishing with verifiable integrity.

---

## Trust and Verification

All releases are signed. Verify signatures before running anything.

- **Signing key:** https://ghostinthewires.net/.well-known/signing-key.asc
- **Fingerprint:** `991752BB 1870377D D82AD22D EC5A18D2 914A478D`
- **Key documentation:** [KEYS.md](../KEYS.md)
- **Warrant canary:** https://ghostinthewires.net/canary

```bash
gpg --fetch-keys https://ghostinthewires.net/.well-known/signing-key.asc
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum -c SHA256SUMS
```

---

## Philosophy

Privacy is a human right, not a privilege. Every decision in these projects is documented, every hardening choice is explained, and everything can be turned off. Nothing is silently applied.