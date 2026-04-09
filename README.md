# bonfyre-cms

Lightweight CMS entry repo for Bonfyre.

This repo is a public entry vector for the CMS surface:

- dynamic content schemas
- REST API and embedded HTTP server
- token auth
- relation and namespace management
- compact bindings backed by `liblambda-tensors`

## Why This Exists

The live `BonfyreCMS` runtime currently lives in:

- `/Users/nickgonzales/Projects/bonfyre-oss/cmd/BonfyreCMS`

This repo gives that surface its own clear entry point so the Bonfyre page can link to it directly.

## Current Layout

- `cmd/bonfyre-cms/`
  - extracted CMS binary source
- `vendor/bonfyre-core/lib/libbonfyre/`
  - temporary local core dependency slice
- `vendor/liblambda-tensors/`
  - temporary local compression/library dependency slice
- `docs/`
  - extraction notes

## Dependency Note

This repo currently vendors the minimum local dependencies needed to validate the extraction:

- `lib/libbonfyre`
- `liblambda-tensors`

That is a migration convenience, not the long-term dependency model.
