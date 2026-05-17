# Keys

This document lists the public keys used by the ghostinthewires project and their purposes.

## Email Encryption

For sending encrypted email to gitw@ghostinthewires.net.
This key is managed by Proton Mail. The private key is held in Proton Mail's infrastructure.

- **Key URL:** https://ghostinthewires.net/.well-known/pgp-key.asc
- **Fingerprint:** F90D E5A4 2657 59CA 4CB3 3F2D 8CF1 8303 85E9 3B4F
```
-----BEGIN PGP PUBLIC KEY BLOCK-----

xjMEaf+NVxYJKwYBBAHaRw8BAQdA9Xf5OD0xrNn+e/UQ3mqeNNtQk4r2U1gY
CTvcC/ylp7bNM2dpdHdAZ2hvc3RpbnRoZXdpcmVzLm5ldCA8Z2l0d0BnaG9z
dGludGhld2lyZXMubmV0PsLAEQQTFgoAgwWCaf+NVwMLCQcJEIzxgwOF6TtP
RRQAAAAAABwAIHNhbHRAbm90YXRpb25zLm9wZW5wZ3Bqcy5vcmf299uMxv5U
0usFAkyEpit+BREbzyO8K1S6wOh3aY0c3gMVCggEFgACAQIZAQKbAwIeARYh
BPkN5aQmV1nKTLM/LYzxgwOF6TtPAAAsygEAvpSyezzEKefxTuqWOn9Jnk1G
FF/EZlXKtgdnLElqlGwA/jpWYwVkNhv2mRFGoV/sKhAuBu+hrb+Wyg8DVbTN
1M8JzjgEaf+NVxIKKwYBBAGXVQEFAQEHQO9nP76YaXgMjphUUWwVSuWGUerS
fkADFKvGjaetvjkVAwEIB8K+BBgWCgBwBYJp/41XCRCM8YMDhek7T0UUAAAA
AAAcACBzYWx0QG5vdGF0aW9ucy5vcGVucGdwanMub3JnN7Ge0YG22e19T7JO
6/DPBPWvs7xLYRxJZ2Dm7gcAkdgCmwwWIQT5DeWkJldZykyzPy2M8YMDhek7
TwAAs6AA/R5ncQdh04rYLn2wiR56Ai0Eej1JIJPDyXlPOqRIdVsPAQC/OH9Q
fnywibm3oKZpTWoIqA1/8XY8hxTPZdpuPmBfBw==
=Xi8C
-----END PGP PUBLIC KEY BLOCK-----
```
## Signing Key

For verifying signatures on release artifacts, commits, the warrant canary, and project documents.
Subkeys are loaded onto YubiKey 5 series hardware and non-exportable from the device.
Generated airgapped on an ephemeral live OS with no network or persistent storage.
Master certify key stored offline on LUKS2-encrypted media.

- **Key URL:** https://ghostinthewires.net/.well-known/signing-key.asc
- **Master Fingerprint:** 991752BB 1870377D D82AD22D EC5A18D2 914A478D

Subkeys:

| Purpose | Algorithm | Fingerprint | Expires |
|---|---|---|---|
| Sign [S] | Ed25519 | 5AAB E9E3 234D 6B7D 3E75 B509 DA2C 77E8 2F38 3B67 | 2028-05-10 |
| Encrypt [E] | Cv25519 | A517 AFA3 091E FC52 609A FEA1 13F4 2D52 7549 16FE | 2028-05-10 |
| Authenticate [A] | Ed25519 | ED83 2F1D 7DB4 3470 DC4A 08E1 7A40 2E1D 377D DB61 | 2028-05-10 |
```
-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEagFS4hYJKwYBBAHaRw8BAQdAlm9Yyw2JMtbMAr1z5GaDI6zQK7GKEIBPwxeN
upBTRWm0Kmdob3N0aW50aGV3aXJlcyA8Z2l0d0BnaG9zdGludGhld2lyZXMubmV0
PoiQBBMWCgA4FiEEmRdSuxhwN33YKtIt7FoY0pFKR40FAmoBUuICGwEFCwkIBwIG
FQoJCAsCBBYCAwECHgECF4AACgkQ7FoY0pFKR4204QEAwxn50tr9dXO85bazALNF
/PqWglotqRYZur1mLwTFwhUBALmwP5aarjBJdRVO6Qfi1S/aL7E2mYt76gzmu20a
vWYLuDMEagFTTBYJKwYBBAHaRw8BAQdAUuLrPwlzS6i4qNNJAri3sF6wGkPsDuOr
YPTDrs1nbYuI9QQYFgoAJhYhBJkXUrsYcDd92CrSLexaGNKRSkeNBQJqAVNMAhsC
BQkDwmcAAIEJEOxaGNKRSkeNdiAEGRYKAB0WIQRaq+njI01rfT51tQnaLHfoLzg7
ZwUCagFTTAAKCRDaLHfoLzg7Z0RcAQD7Wg5nw8TPwpp9rPDXyD7DzYUqkBvewlhp
vzSBaew+rAD+PU3C9WNwNCtdonX/2Eux167hF8KAvNcWlRtzf9QhkQKtGwD/UOSG
OZTeCqhXyR3yfHAWy0p53ghCGnQQMmgk7XtqrJ8BAMaPPI2S7nrJWy7eBWADEyti
Mv0fP4papGeYeNA2Eb8GuDgEagFTbxIKKwYBBAGXVQEFAQEHQHnaTeV2bycaB5/O
EWsWJq8l3llpoHWmlMsZ+e3CfBV1AwEIB4h+BBgWCgAmFiEEmRdSuxhwN33YKtIt
7FoY0pFKR40FAmoBU28CGwwFCQPCZwAACgkQ7FoY0pFKR40cjAEAzRVVQfqL59+4
SkAOYh6iC3kqSeKHNu9cfxm5ubFa8+kBAIV5bMErPTWkiycPpk1gr5SAdfJyMjec
fjQeYm35AZkDuDMEagFTjRYJKwYBBAHaRw8BAQdAQk6J8jmZiQZdLbmBrChEx/eT
Esdr36p7jOA/YrSLtUqIfgQYFgoAJhYhBJkXUrsYcDd92CrSLexaGNKRSkeNBQJq
AVONAhsgBQkDwmcAAAoJEOxaGNKRSkeNqZQBAOCmCUN+NmICnOpRCf/mUl5n2MAu
KkLUstGCHuMn1rinAQD9TAG+pkFBmthkUNqllVEfvUVOYHR2SqZbQrLgoljiAA==
=9egF
-----END PGP PUBLIC KEY BLOCK-----
```
## Verifying a Signature

```bash
# Import the signing key
gpg --fetch-keys https://ghostinthewires.net/.well-known/signing-key.asc

# Verify a detached signature
gpg --verify FILE.asc FILE

# Verify SHA256SUMS
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum -c SHA256SUMS
```

## Key Rotation

Subkeys expire 2028-05-10. When keys are rotated, this document will be updated and re-signed.
The master certify key fingerprint (`991752BB 1870377D D82AD22D EC5A18D2 914A478D`) will remain consistent across rotations.
