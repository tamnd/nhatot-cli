---
title: "Installation"
description: "Install nhatot from a release, with go install, or from source."
weight: 20
---

## Prebuilt binaries

Every [release](https://github.com/tamnd/nhatot-cli/releases) carries archives for Linux, macOS,
and Windows on amd64 and arm64, plus deb, rpm, and apk packages for Linux.
Download, unpack, put `nhatot` on your `PATH`, done. The `checksums.txt`
on each release is signed with keyless [cosign](https://docs.sigstore.dev/) if
you want to verify before running.

## With Go

```bash
go install github.com/tamnd/nhatot-cli/cmd/nhatot@latest
```

That puts `nhatot` in `$(go env GOPATH)/bin`, which is `~/go/bin` unless
you moved it. Make sure that directory is on your `PATH`.

## From source

```bash
git clone https://github.com/tamnd/nhatot-cli
cd nhatot-cli
make build        # produces ./bin/nhatot
./bin/nhatot version
```

## Container image

```bash
docker run --rm ghcr.io/tamnd/nhatot:latest --help
```

## Checking the install

```bash
nhatot version
```

prints the version and exits.
