# Changelog

All notable changes to this project will be documented in this file.  
This project follows [Semantic Versioning](https://semver.org/).

---

## [1.2] - 2025-10-06

### Added
- Automatic removal of panels previously spawned in the same position before generating new ones.  

### Changed
- **“reset colors”** renamed to **“clear”**, now restoring both the number’s colors and removing panels if they are in their original spawn position.  
- Updated internal **README** with clarified behavior and new instructions.

### Fixed
- Fixed a bug where the flag could mix elements from **ver.1** and **ver.2** when the *umenu* was not used after loading the patcher
  *(added `loadmess` initialization)*.

---

## [1.1] - 2025-10-05

### Added
- Compatibility with objects using `@presentation 1`.
- Visual arrows indicating connection outlets.
- "Reset colors" option to restore default number box appearance.

### Changed
- Rewritten internal logic using `uzi`, `sprintf`, and `deferlow`  
  (replacing `zl.join` and `delay`).
- Introduced **variant 2** with `triscale 1.8` for more accurate flag proportions.

### Fixed
- Corrected red tone from `255 0 0` to `238 42 53`.

---

## [1.0] - 2025-10-03

### Initial release
- First public version of the *freepalestine* patch.
- Created custom number box skin stylised as the Palestinian flag.
- Added automatic scripting of three `panel` objects (black, white, green).
- Included recolored triangle (chevron) and styled number text.

---
