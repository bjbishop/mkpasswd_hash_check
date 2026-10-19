# Detect out-of-date password hashes

This pre-commit check detects password hashes that use older algorithms, prefer to use yescrypt's `$y$` hashes instead.

It flags hashes containing any of these markers:

- `$1$` (MD5)
- `$5$` (SHA-256)
- `$6$` (SHA-512)
- `$2a$` and `$2b$` (bcrypt)
- `$7$` (scrypt)
