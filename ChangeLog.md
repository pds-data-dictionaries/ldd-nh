# New Horizons Mission Dictionary Change Log

## Version 1.1.0.0

Upgrades and modifications to support ongoing migration of PDS3 data and developement of
the PDS4 pipeline for the second extended mission.

* MVIC_Conversion_Constants has been deprecated in favor of Radiometric_Conversion_Constants
(for all instruments that need them). The new class includes a constant for Arrokoth.

* Classes have been added to support SWAP and LEISA as well as spacecraft state and 
engineering/housekeeping data included with the observational data. Examples for these
new classes have been added to the documentation set.

## Version 1.0.0.0

This is the first configured version of the mission namespace, created as part of the
migration of MVIC KEM1 observations from PDS3 to PDS4. Many versions are expected as
additional missions, phases, and instruments are migrated.
