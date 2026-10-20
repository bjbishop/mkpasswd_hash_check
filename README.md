# Detect out-of-date password hashes

This pre-commit check detects password hashes that use older algorithms, prefer to use yescrypt's `$y$` hashes instead.

It flags hashes containing any of these markers:

- `$1$` (MD5)
- `$5$` (SHA-256)
- `$6$` (SHA-512)
- `$2a$` and `$2b$` (bcrypt)
- `$7$` (scrypt)

# Pre-commit.com

Use this hook within a [pre-commit](https://pre-commit.com) `.pre-commit-config.yaml` file like this:

```
  - repo: https://github.com/bjbishop/mkpasswd_hash_check.git
    rev: v1.0.0
    hooks:
      - id: reject_legacy_mkpasswd_hashes
```
