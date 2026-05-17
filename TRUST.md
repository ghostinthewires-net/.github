# Trust Statement — ghostinthewires

Published: 2026-05-17  
Signed by: Signing subkey DA2C77E82F383B67  
Fingerprint: 991752BB 1870377D D82AD22D EC5A18D2 914A478D  

## Statement of Key Ownership

I, the primary maintainer of the ghostinthewires organization, assert that
the following cryptographic keys are under my sole control.

## Key Hierarchy

Master key [C]:  
  Fingerprint: 991752BB 1870377D D82AD22D EC5A18D2 914A478D  
  Algorithm:   Ed25519  
  Created:     2026-05-11  
  Expires:     Never  
  Storage:     LUKS2-encrypted offline media  

Signing subkey [S]:  
  Fingerprint: 5AAB E9E3 234D 6B7D 3E75 B509 DA2C 77E8 2F38 3B67  
  Algorithm:   Ed25519  
  Created:     2026-05-11  
  Expires:     2028-05-10  
  Storage:     YubiKey 5 series hardware, non-exportable from device  

Encryption subkey [E]:  
  Fingerprint: A517 AFA3 091E FC52 609A FEA1 13F4 2D52 7549 16FE  
  Algorithm:   Cv25519  
  Created:     2026-05-11  
  Expires:     2028-05-10  
  Storage:     YubiKey 5 series hardware, non-exportable from device  

Authentication subkey [A]:  
  Fingerprint: ED83 2F1D 7DB4 3470 DC4A 08E1 7A40 2E1D 377D DB61  
  Algorithm:   Ed25519  
  Created:     2026-05-11  
  Expires:     2028-05-10  
  Storage:     YubiKey 5 series hardware, non-exportable from device  

## Trust Architecture

This setup follows standard OpenPGP best practice for offline root keys.
The master certify key establishes the trust hierarchy by certifying the
subkeys. All operational signing is performed by the signing subkey.

All keys were generated airgapped on an ephemeral live OS with no network
or persistent storage. Subkeys were loaded onto YubiKey 5 series hardware
via keytocard and are non-exportable from the device. Both a primary and
backup YubiKey are provisioned with identical subkeys.

## Key Distribution

This key is published at the following locations. Verify the fingerprint
matches across all sources before trusting any signed artifact:

  https://ghostinthewires.net/.well-known/signing-key.asc
  https://keys.openpgp.org/search?q=gitw%40ghostinthewires.net
  https://github.com/ghostinthewires-net/.github/blob/main/KEYS.md

WKD automatic discovery:  
  gpg --auto-key-locate wkd --locate-keys gitw@ghostinthewires.net  

## Verification

This document is signed by the signing subkey DA2C77E82F383B67.

To verify:

  gpg --fetch-keys https://ghostinthewires.net/.well-known/signing-key.asc  
  gpg --verify TRUST.md.asc TRUST.md  

The master key fingerprint must match:  
  991752BB 1870377D D82AD22D EC5A18D2 914A478D  

The signing subkey fingerprint must match:  
  5AAB E9E3 234D 6B7D 3E75 B509 DA2C 77E8 2F38 3B67  

## Succession

A designated successor has been appointed as org owner. In the event the
primary maintainer becomes permanently unavailable, the successor will
assume ownership and publish a new signed trust statement using their own
GPG key.
