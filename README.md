# Keysmith

Hierarchical Deterministic Key Derivation for the Internet Computer

[![Build Status](https://github.com/dfinity/keysmith/workflows/build/badge.svg)](https://github.com/dfinity/keysmith/actions?query=workflow%3Abuild)

## Download

Download the latest tarball [here](https://github.com/dfinity/keysmith/releases).

## Verify

If you want to verify the authenticity of the tarball, then please also download the supplementary `SHA256.SIG` and `SHA256.SUM` files, as well as my public key, which you can find [here](https://sovereign.io/public.key).

Verify the SHA256 checksum of the tarball.

```text
grep "$(openssl dgst -sha256 keysmith-*.tar.gz)" SHA256.SUM
```

Verify the signature on the tarball.

```text
openssl dgst -verify public.key -signature SHA256.SIG SHA256.SUM
```

The command above should display the following output.

```text
Verified OK
```

## Install

Extract the executable from the tarball.

```text
tar -f keysmith-*.tar.gz -x 
```

Move the executable to a suitable location.

```text
sudo mv keysmith /usr/local/bin
```

## Usage

Below is list of commands and their behavior.

- `account` prints your account identifier.
- `generate` generates your mnemonic seed.
- `legacy-address` prints your legacy address.
- `principal` prints your principal identifier.
- `private-key` writes your private key to a file.
- `public-key` prints your public key.
- `version` prints the version number.
- `x-public-key` prints your extended public key.
