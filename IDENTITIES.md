# Identities — ghostinthewires

Published: 2026-05-17  
Signed by: Signing subkey DA2C77E82F383B67  
Fingerprint: 991752BB 1870377D D82AD22D EC5A18D2 914A478D  

## Official Presences

The following are the only official accounts and infrastructure operated
by the ghostinthewires organization. Any presence not listed here should
not be assumed to be affiliated with this organization.  

Domain:    https://ghostinthewires.net  
Email:     gitw@ghostinthewires.net  
GitHub:    https://github.com/ghostinthewires-net  
Codeberg:  https://codeberg.org/ghostinthewires  
Mastodon:  https://infosec.exchange/@ghostinthewires  

## Signing Key

All project artifacts, releases, commits, and documents are signed with:  

  https://ghostinthewires.net/.well-known/signing-key.asc  
  Fingerprint: 991752BB 1870377D D82AD22D EC5A18D2 914A478D  

## Verification

This document is signed by the signing subkey DA2C77E82F383B67.  

To verify the signature:  

  gpg --fetch-keys https://ghostinthewires.net/.well-known/signing-key.asc  
  gpg --verify IDENTITIES.md.asc IDENTITIES.md  

The signing subkey fingerprint must match:  
  5AAB E9E3 234D 6B7D 3E75 B509 DA2C 77E8 2F38 3B67  

To verify integrity against the repository checksums:  

  gpg --verify SHA512SUMS.asc SHA512SUMS  
  sha512sum -c SHA512SUMS  

  gpg --verify BLAKE3SUMS.asc BLAKE3SUMS  
  b3sum --check BLAKE3SUMS  

## Key Distribution

The signing key is available through multiple independent channels. Verify
the fingerprint matches across all sources before trusting any signed artifact.

  Direct:    https://ghostinthewires.net/.well-known/signing-key.asc  
  WKD:       gpg --auto-key-locate wkd --locate-keys gitw@ghostinthewires.net  
  Keyserver: https://keys.openpgp.org/search?q=gitw%40ghostinthewires.net  

## Trust Documentation

  KEYS.md:        https://ghostinthewires.net/keys  
  TRUST.md:       https://ghostinthewires.net/trust  
  Warrant Canary: https://ghostinthewires.net/canary.txt