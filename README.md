# Lean Playground courses

Course packs for the Lean Playground app on iPhone and iPad.

The app ships modules 1 and 2. Modules 3 to 13 are downloaded from the releases
of this repository once and then work offline.

| Pack | Module | Lessons |
| --- | --- | --- |
| equalities | 3 | 5 |
| compound | 4 | 5 |
| data | 5 | 5 |
| logic | 6 | 10 |
| induction | 7 | 5 |
| discrete | 8 | 10 |
| functional | 9 | 5 |
| verification | 10 | 5 |
| review | 11 | 5 |
| practice | 12 | 5 |
| ai | 13 | 10 |

## How the app checks a download

- `catalog.v2.json` lists every pack with its URL, size and SHA-256. The list
  is signed with Ed25519 (key `lp-course-2026-11`); the signed message is the
  domain string `LeanPlayground.CourseCatalog.v1\n` followed by the payload.
- The app keeps the public key and refuses a catalog with a bad signature, and
  a pack whose size or SHA-256 differs from the catalog.

Public key `lp-course-2026-11` (raw Ed25519, base64):

```
DF3GOsIf82ABN4KwePrcL79MwK+wUNgChhcMClRlsBc=
```

## Releases

Each release holds the catalog and the packs it lists. The app reads
`releases/latest/download/catalog.v2.json`, so the newest release is the one
in use. A pack keeps its file name for a given version, so an older catalog
still points to files that exist.

Since `packs-4` the course has a new module order (logic after data, discrete
mathematics and functional programming after induction). Builds before it read
`catalog.v1.json`; every later release carries the last v1 catalog unchanged,
so those builds keep the packs and module numbers they were made for.

### Mathlib basics

`mathlib-basics-1` is not a course release and is never marked latest. It holds
one AppleArchive with compiled `.olean` files of a part of Mathlib and the
libraries it is built on, made for the Lean inside Lean Playground 0.2 (8) and
later. The app pins the archive's size and SHA-256 in its own bundle, so it
downloads exactly this file. Every included library is under the Apache
License 2.0; their licences and a NOTICE are in the archive's `LICENSES`
folder. A new Lean in the app means a new release, `mathlib-basics-2`.

## Support and legal

- Support: [English](Legal/en/support.md) · [Русский](Legal/ru/support.md)
- Privacy Policy: [English](Legal/en/privacy.md) · [Русский](Legal/ru/privacy.md)
- Terms of Use: [English](Legal/en/terms.md) · [Русский](Legal/ru/terms.md)

The same pages are in the app, under About and licenses.

## Licence

The lessons are part of Lean Playground. Copyright 2026 Sergii Ziborov. All
rights reserved; see [LICENSE](LICENSE).
