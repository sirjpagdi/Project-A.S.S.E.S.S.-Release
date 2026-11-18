# Project A.S.S.E.S.S.

Android educational assessment app, adapted from the existing MCQ Quick Check v1.2.5 codebase.

**Status:** Source conversion candidate; not compiled or device-validated.

Includes assessment-sheet generation, camera-based scanning and grading, test sets, competency analytics, classes, learner matching and exports. Licensing and subscription restrictions were removed from this edition.

See `PROJECT_ASSESS_CONVERSION.md` for changes, testing obligations, and signing notes. The historical `CHANGELOG.md` documents upstream development and is retained as provenance; it is not this edition's release history.

Developer: Sir_JPagdi. Third-party licenses remain under `licenses/` and the existing `LICENSE`.

## Building without Android Studio

Pushing to GitHub runs `.github/workflows/build.yml`, which builds a debug APK (download it from the run's Artifacts). Add the four signing secrets listed at the top of that file and it also builds a signed release APK named `project_assess_v<versionName>.apk`.

## Releases and updates

The app can check for a newer version (once a day on launch, and on demand from About > Check for Updates). It only reads the latest release of `sirjpagdi/Project-A.S.S.E.S.S.-Release`; no learner or test data is sent, and nothing is needed for routine offline use. To publish an update:

1. Tag the release `v<versionName>` (for example `v1.0.1`) and publish it (not a draft or pre-release).
2. Put a line `versionCode: <number>` in the release notes. It must be higher than the installed app's `versionCode`.
3. Attach the signed APK, named `project_assess_v<versionName>.apk`.

