# Detect out of date SHA512 hassword hashes

This pre-commit check just detects the presense of the string '$6$' which might indicate a mkmasswd result using an older password hashing algorithm.  Prefer yescript's '$y$ instead.

TODO: add more old hash types
