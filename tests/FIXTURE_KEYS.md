# Test fixture keys

The `*.key` and `*.key.pub` files in this directory (for example
`test_rsa_openssh.key`, `test_ecdsa_384.key`, `test_ed25519_password.key`,
`badhash_key1.ed25519.key`) are **intentional, non-secret test fixtures**.
They exist only to exercise paramiko's key parsing, signing and password
handling tests, and they protect nothing.

Data-classification scans (for example BigID classifiers for "PKCS 1 Private
Key" and "OpenSSH Private Key") will flag them. Treat those hits as accepted.

Rules for this directory:

- Never reuse a key from here for a real host, account or service.
- Never add a key here that has ever been used outside tests.
- Real credentials, tokens and personal data must never be committed.

Email addresses that appear in source headers are public author contact
details and are likewise accepted.

Provenance: BigID smart-sample scan, run `ee00dcb2-b337-44dd-b4b6-3cefc4e267a2`,
12 objects scanned, 0 objects with personal information.
