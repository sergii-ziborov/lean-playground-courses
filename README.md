# Lean Playground courses

Course packs for the Lean Playground app on iPhone and iPad.

The app ships modules 1 and 2. Modules 3 to 9 are downloaded from the releases
of this repository once and then work offline.

| Pack | Modules | Lessons |
| --- | --- | --- |
| equalities | 3 | 5 |
| compound | 4 | 5 |
| data | 5 | 5 |
| induction | 6 | 5 |
| verification | 7 | 5 |
| review | 8 | 5 |
| practice | 9 | 5 |

## How the app checks a download

- `catalog.v1.json` lists every pack with its URL, size and SHA-256. The list
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
`releases/latest/download/catalog.v1.json`, so the newest release is the one
in use. A pack keeps its file name for a given version, so an older catalog
still points to files that exist.

## Support and legal

- Support: [English](Legal/en/support.md) · [Русский](Legal/ru/support.md)
- Privacy Policy: [English](Legal/en/privacy.md) · [Русский](Legal/ru/privacy.md)
- Terms of Use: [English](Legal/en/terms.md) · [Русский](Legal/ru/terms.md)

The same pages are in the app, under About and licenses.

## Licence

The lessons are part of Lean Playground. Copyright 2026 Sergii Ziborov. All
rights reserved; see [LICENSE](LICENSE).
