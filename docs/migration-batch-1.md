# Migration Batch 1

This is the first extraction batch for `bonfyre-cms`.

## Goal

Move the live `BonfyreCMS` binary into its own public-facing repo while keeping its core and compression-library dependencies explicit.

## Batch Contents

### 1. `BonfyreCMS`

Current source:

- `/Users/nickgonzales/Projects/bonfyre-oss/cmd/BonfyreCMS`

Target:

- `cmd/bonfyre-cms/`

### 2. `libbonfyre` dependency slice

Current source:

- `/Users/nickgonzales/Projects/bonfyre-core/lib/libbonfyre`

Target:

- `vendor/bonfyre-core/lib/libbonfyre/`

### 3. `liblambda-tensors` dependency slice

Current source:

- `/Users/nickgonzales/Projects/liblambda-tensors`

Target:

- `vendor/liblambda-tensors/`

## Acceptance Criteria

1. vendored `libbonfyre` builds locally
2. vendored `liblambda-tensors` builds locally
3. `bonfyre-cms` builds from the extracted path
4. the repo can serve as a clean backlink target from the live Bonfyre page

## Progress

- imported:
  - `BonfyreCMS`
  - vendored `libbonfyre` dependency slice
  - vendored `liblambda-tensors` dependency slice
- verification:
  - vendored `libbonfyre` builds locally
  - vendored `liblambda-tensors` builds locally
  - `bonfyre-cms` builds from the extracted path
  - usage surface runs from the extracted binary
