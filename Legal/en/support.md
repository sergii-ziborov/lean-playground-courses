# Lean Playground support

Lean Playground teaches Lean 4 on iPhone and iPad: lessons, flashcards, labs, and an editor where Lean checks your proofs right on the device.

**Contact:** sergii.ziborov@gmail.com. Publisher: Serhii Ziborov. We usually reply within two working days. Please mention your device model, the iOS version and the app version (shown in About and licenses), and if a proof behaves oddly, paste its code.

## Common questions

- **Does it need the internet?** Only to download course packs and Mathlib basics, and to import from GitHub. Lean runs on the device, so your files and the lessons you have work offline.
- **Why is the first check slow?** Lean loads its library when the app starts. The first time takes a few seconds longer; the "Preparing Lean" card shows how it goes.
- **Can I use Mathlib?** Yes, with Mathlib basics: an optional 418.5 MB download in Playground → Libraries (about 2.4 GB on the device). It has the everyday part of Mathlib, such as `ring`, `linarith`, `norm_num` and ℕ ℤ ℚ ℝ ℂ, but no topology or analysis. A file that needs more is marked "Needs full Mathlib".
- **Can a file import another file of my project?** Not yet. Each file is checked on its own, and the app marks files that import other files.
- **Where are my files?** In the app, on your device. Share a file from Playground or export it as .lean from the editor. On a Mac, connect the device and open the app's files in Finder.
- **How do I start over?** Delete the app; iOS removes its data. Export the files you want to keep first.

Privacy Policy: [privacy.md](privacy.md). Terms of Use: [terms.md](terms.md).
