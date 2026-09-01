# Changelog

## Historical

Everything below predates this fork's own release tagging and the adoption of
[Conventional Commits](https://www.conventionalcommits.org). It was generated
once with [git-cliff](https://git-cliff.org) from the commit history, using the
upstream release tags as version boundaries, and is preserved verbatim.

`aio-v1.0.0` is the baseline release: everything this fork carried at the point
release automation was adopted. Releases *after* it are managed by
release-please and appear above this section. Do not hand-edit below this line.

## aio-v1.0.0 (2026-09-02)


### Features

- Added Fusion360 file. This is just a zip archive containing several f3d files and accessory JSONs.
- Added pcb-3.0 case draft. Included adjustable wall mount.
- Added sliding window filter to temperature, humidity, pressure from BME280
- Added support for ESP32-S3 mini with speaker-media player. RGB light platform changes for ESP-IDF framework.
- Added speaker-media player introduced in 2025.2.0. ESPHome min version bumped up to 2025.2.0
- Added Fast Pulse and Slow Pulse light effects. Should also now set framework correctly depending on media_player and VA sensors. Added no-PSRAM config for media_player.
- Added esp32 section back in to MP
- Added additional LED effects for media player announcements
- Added wake_word_engine selector. Added micro_wake_word with alexa and hey_jarvis.
- Added speaker to voice assist sensor. Renamed i2s component IDs to improve clarity.
- Added optional media_player sensor
- Status_led ([#288](https://github.com/Schluggi/AIOsense/issues/288))
- Added abilitiy to stop RTTTL playback

### Fixes

- Update LED configuration to use output reference
- Output is a required parameter for light.monochromatic
- Corrected led_invert from bool to str.
- Corrected invert LED back and added arduino framework for C3
- Yaml lint
- Fix: amp swapped terminal label
- Fix pcb version number

### Refactoring

- Renamed i2s_audio to avoid clash with esphome. Removed ESPhome min version declaration
- Switching framework in media_player is problematic
- Python action
- Move to requirements.in
- Move GY-302

### Removals

- Removed esp32 from media_player
- Removed use_wake_word switch
- Removed obsolete boards.
- Tindie link

### Maintenance

- Update esp-idf framework version from latest to recommended
- Enforce arduino frameword for media_player
- Update board for s2 and c3
- Updated pin assignments for rc1. Added i2s_dout_pin for amplifier/speaker.

### Other

- Change to status_led platform for onboard LED
- Do not start voice assist on boot.
- ESPhome 2025.2 changes. Removed declaration of framework in VA instead inherit from parent config for board.
- On device micro wake word crashes on ESP32-S2 mini. HA only.
- PSRAM required
- Typo in platform name
- LED effects not supported on GPIO platform. Switched to monochromatic and ledc
- Invert LED on C3 mini
- OTABackend separation due to PR 6459 in esphome
- OTABackend separation due to https://github.com/esphome/esphome/pull/6459
- Bring back sensor IO positions from V2.1
- Undo project settings
- Initial PCB V3.0.0 commit

## esphome-v3.0.1 (2024-02-25)


### Maintenance

- Update bme280.yaml

### Other

- Release esphome-v3.0.1
- Remake README.md
- Yaml lint

## esphome-v3.0.0 (2023-11-27)


### Features

- Add support for voice assistant with single color leds
- Adding unit_of_measurement
- Adding distance segment zones (closes [#107](https://github.com/Schluggi/AIOsense/issues/107))
- Add basic support for S3 mini
- Add substitutions for voice assistant
- Add pulse effect for booting
- Adding min_version for bsec
- Adding on_boot priority
- Adding default temperature offset
- Adding voice assistant
- Add effects to RGB LED ([#102](https://github.com/Schluggi/AIOsense/issues/102))
- Adding hint to docs for LD2410(c)

### Fixes

- Fixing mmwave_segments
- Fixing S3 led type
- Fixing S3 led colors
- Fixing defaults
- Fixing comments
- Fix breaking changes in 2023.08 ([#105](https://github.com/Schluggi/AIOsense/issues/105))
- Added mmWave to BOM

### Refactoring

- Rename comments

### Removals

- Remove line-length from linting ([#103](https://github.com/Schluggi/AIOsense/issues/103))

### Maintenance

- Bump remote_package version
- Bump s3 framework version
- Bump Ld2410  ([#118](https://github.com/Schluggi/AIOsense/issues/118))

### Other

- Improve mmwave_segments
- Replacing the sen0395 component the new official one (closes [#125](https://github.com/Schluggi/AIOsense/issues/125))
- Led debugging
- Revert "add pulse effect for booting"
- Set version to 3.0.0
- Testing
- Set v3 as package ref
- New docs theme
- BSEC Quickfix ([#122](https://github.com/Schluggi/AIOsense/issues/122))
- Changed github Name from MeisterGig to lukas-holzner ([#127](https://github.com/Schluggi/AIOsense/issues/127))
- Offset improvements ([#111](https://github.com/Schluggi/AIOsense/issues/111))
- Yaml lint
- Swapping rx & tx (closes [#97](https://github.com/Schluggi/AIOsense/issues/97))
- Hanging restore_state to restore_mode  (fixes [#95](https://github.com/Schluggi/AIOsense/issues/95))

## v2.1.0 (2023-06-20)


### Features

- **case**: Files for the upright stand mount ([#80](https://github.com/Schluggi/AIOsense/issues/80))
- Quickstart guide for flashing ([#48](https://github.com/Schluggi/AIOsense/issues/48))
- Tindie shop link
- Bme address note
- Make bme i²c address configurable
- 3d printable case (closes [#9](https://github.com/Schluggi/AIOsense/issues/9))
- Safe_mode & cpu temperature
- Sensors for wifi signal and status
- PCBWay references
- Support for HLK-LD2410C ([#33](https://github.com/Schluggi/AIOsense/issues/33))
- BOM ([#48](https://github.com/Schluggi/AIOsense/issues/48))
- Pulldown for PIR ([#52](https://github.com/Schluggi/AIOsense/issues/52))
- Step files for PIR an socket
- PIR description
- 3D image for buzzer
- Own PIR footprint
- RTTTL Buzzer (closes [#32](https://github.com/Schluggi/AIOsense/issues/32))

### Fixes

- Yaml lint
- S2 config (fixes [#79](https://github.com/Schluggi/AIOsense/issues/79)) ([#82](https://github.com/Schluggi/AIOsense/issues/82))
- CPU Temperature sensor only for ESP8266 ([#78](https://github.com/Schluggi/AIOsense/issues/78))
- PIR pin mode for ESP8266 ([#78](https://github.com/Schluggi/AIOsense/issues/78))
- Led invert for ESP8266 ([#78](https://github.com/Schluggi/AIOsense/issues/78))
- MmWave naming
- Fixing reference in demo config
- BOM links
- Debugging I²C based on new package mode
- Kicad error caused by old library
- Fix doc links in README.md
- BME header pin orientation (closes [#55](https://github.com/Schluggi/AIOsense/issues/55))

### Refactoring

- Moved case files to v1.0 sub dir (related to [#57](https://github.com/Schluggi/AIOsense/issues/57))

### Removals

- Restart duplication
- Disable bluetooth_proxy by default (performance problems)
- _pcb.md
- Disable web_server by default

### Other

- 2.1.0
- Safe_mode category to diagnostic
- Yaml lint
- Versioning
- MmWave config is now entity_category: config
- Release 2.1.0-rc1
- Autoformat
- New amazon links
- Resistors footprint to handsolder
- Change resistors from THT to SMD and add LCSC references ([#65](https://github.com/Schluggi/AIOsense/issues/65))
- Use packages to cleanup ESPhome configs ([#70](https://github.com/Schluggi/AIOsense/issues/70))
- Yaml lint for yaml lint
- Cleanup mkdocs
- More strict yaml rules
- ESPHome config updates for HLK-LD2410 ([#45](https://github.com/Schluggi/AIOsense/issues/45))
- Automerge also for minor versions
- Cleanup requirements.txt
- Yaml lint only on yaml changes
- Requirements test only on changes
- Kicad default text width to fix some warnings
- Swapped GND and SDA at the IO port

## v2.0.0 (2023-03-28)


### Features

- Python_requirements.yaml workflow
- Version to bug report
- Debugging for I²C ([#44](https://github.com/Schluggi/AIOsense/issues/44))
- TO-5 digi-key link ([#48](https://github.com/Schluggi/AIOsense/issues/48))
- Added missing bsec config (fixes [#43](https://github.com/Schluggi/AIOsense/issues/43))
- Yaml lint (closes [#39](https://github.com/Schluggi/AIOsense/issues/39))
- Issue templates (closes [#38](https://github.com/Schluggi/AIOsense/issues/38))
- Contributors listing
- Venv
- Add renovate.json
- Docs badge
- Add readthedocs
- Added fillet to bottom hole edge for fit
- Added STL and STEP case models for v1.0.
- Add LCSC part number for JLCPCB SMT services.
- 3s LED while booting (no green, because does not work)
- 3s green LED while booting
- Control for ESP32C3 onboard LED
- BME680 support for EPS32-C3
- Added MH-ET Live as commented out option for board.
- Added ESPHome yaml config for generic ESP32 D1 Mini
- Off_delay for PIR
- Info about the power consumption
- Support for BME680 bsec
- Web_server
- Support for bluetooth_proxy for the esp32-c3
- Project & version
- Order images
- PIR not working note
- Static ip option
- Doc images
- Create ESP Home config for S2 Mini
- Config for esp32 c3 mini
- Reschandreas to special thanks list
- Step file to gitignore
- Qrcode ([#5](https://github.com/Schluggi/AIOsense/issues/5))
- Added: pin header for HLK-LD2410 (closes [#10](https://github.com/Schluggi/AIOsense/issues/10))

### Fixes

- Yaml lint
- Syntax
- Fixed typo - it's not "pulluted" but "polluted"
- PIR pin since PIR changes
- Footprint for LD2410
- Fixed IO labeling (closes [#17](https://github.com/Schluggi/AIOsense/issues/17))
- Typo
- Sensor Modules link
- PIR is now in the center and does not block the mmWave
- PIR sensor pin
- Yaml layout
- Some layout fixes
- Top corners
- PIR label is not in the center of the ESP
- PIR GPIO for S2
- Unify esphome files
- Kicad paths in gitignore

### Refactoring

- Moved the ESP closer to the edge
- Refactor README.md

### Documentation

- Readme rework

### Removals

- Title prefix from doc template
- DependencyDashboard
- Changelog (look at releases)
- Password for fallback ap
- Bluetooth_proxy (no tested yet)
- Everything v1 related

### Maintenance

- Requirements.txt
- Updated model to correct problems from test print
- Updated step file to mirror changes in top/bottom
- Updated top component to shorten pins
- Updated part numbers for as many parts as possible for Mouser, Farnell, Digikey (and the HiLink LD2410 with Aliexpress Link)
- Images & schematic
- Pcb images
- Date on schematic
- Schematic and date

### Other

- Release of v2.0.0
- Yaml lint
- YAML lint
- Automerge patches (renovate)
- Closes [#47](https://github.com/Schluggi/AIOsense/issues/47) - new light for esp32 d1 mini that is trigerred on boot
- Downgrade markdown
- Improve docs ([#31](https://github.com/Schluggi/AIOsense/issues/31))
- Improve docs (closes [#31](https://github.com/Schluggi/AIOsense/issues/31))
- Anyway... all yaml files
- Yaml lint only for esphome/
- Myst-parser to 1.0.0
- Filename
- Note not to buy v1
- Migration to kicad 7.0
- Restored group id
- Power pins replaced with terminal block (closes [#18](https://github.com/Schluggi/AIOsense/issues/18))
- PIR-Jumper removed & port labels changed
- MmWave Distance: box is now a slider
- Illuminance update_interval
- Small layout changes
- Product images added, badges changed
- Mounting holes now are grounded
- Changed: PCB size reduced
- Back to THT resistors (closes [#12](https://github.com/Schluggi/AIOsense/issues/12))
- Switch to SMD (closes [#12](https://github.com/Schluggi/AIOsense/issues/12))
- PCB review changes
- All-in-one-sensor is now AIOsense
- Closes [#3](https://github.com/Schluggi/AIOsense/issues/3): m3 mounting holes

## v1.0 (2022-11-07)


### Documentation

- README.md

### Other

- First release


