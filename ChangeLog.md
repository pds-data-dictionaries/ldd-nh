# New Horizons Mission Dictionary Change Log

## Version 1.2.0.0

* Add Alice door_position attribute

* Add REX-specific class and attributes

## Version 1.1.0.0

Upgrades and modifications to support ongoing migration of PDS3 data and developement of
the PDS4 pipeline for the second extended mission.

* MVIC_Conversion_Constants has been deprecated in favor of Radiometric_Conversion_Constants
(for all instruments that need them). The new class includes a constant for Arrokoth.

* Classes have been added to support ALICE, LEISA, LORRI, and SWAP as well as spacecraft state and 
engineering/housekeeping data included with the observational data. Examples for these
new instrument classes have been added to the *test/* directory set.

* Added *examples/* directory under *test/* for simple, valid labels that show schema structures 
(i.e., the classes) for specific instruments.

* Updated *docs/* to remove the full examples that were causing build failures because of their size.
The documents will now link directly to the smaller examples in the *test/examples/* location.

* Added *Notes_for_Developers" file to src/ for common reference. This is intended as
a "best practices" reference for the NH LDD developers [Issue #17](https://github.com/pds-data-dictionaries/ldd-nh/issues/17).

## Version 1.0.0.0

This is the first configured version of the mission namespace, created as part of the
migration of MVIC KEM1 observations from PDS3 to PDS4. Many versions are expected as
additional missions, phases, and instruments are migrated.
