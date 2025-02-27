# New Horizons Mission Dictionary Change Log

## Version 1.2.0.0

Continuing development to support migration, KEM2 extended mission, and to clean up some details.

* The LORRI_Target_Information class was ultimately not used for migrating the KEM1 data, and
  has been removed from the dictionary.
* The Observational_Parameters class was made optional to accommodate some cases where the class
  is not relevant but other Mission_Parameters are.
* The Spacecraft_State class was made optional within Observational_Parameters for cases where
  the state attributes would otherwise all be omitted.
* Updated the online document reference to the PDS Dictionary webhelp site to the 1M00 version, 
  which includes the version 1.1 contents of this dictionary. Users should note that there is a 
  version lag between in this facility relative to the release of the latest version of the NH dictionary.
* Update nh:detector_name for SWAP and deprecated previous detector name. Added regression test for the FAIL condition.
* The pointing_method attributein the Spacecraft_State class has been deprecated. The encoded 
  information in this attribute was used for pipeline control and is not relevant to end user 
  applications.
* The definitions of gc_scan_rate, target_motion_rate, radio_bandwidth, and 
  radiometry_response_offset have been checked and finalized.
* The target_motion_rate attribute definition was finalized, units of measure were added, and a
  min/max range defined to help ensure that the right unit (rad/s) will appear in PDS labels. 
  (The FITS header value is in μrad/s.)
* The mission_phase permissible value list was extended to cover all primary and extended 
  mission phases to date.
* Reconciled the definition of agc_gain_provenance with the permissible value list of the 
  referenced attribute agc_setting_source.
* Expanded undefined acronyms "TDI" and "ULDB" in all places they occurred.
* Clarified the English in the "check_bias" Schematron rule output.
* Added a pds:Internal_Reference to the ICD document in definitions that cited that document
  specifically (for an equation or additional details).
* Modified the definition of time_tag_calibration_constant based on consultation with the
  NH archiving team and the REX chapter of the ICD.
* Modified the definition of the Radiometric_Conversion_Constants class to explicitly note 
  that it is used for both MVIC and LORRI data.
* Updated regression tests and examples to correspond to the 1.2.0.0 version of the NH mission 
* Updated documentation


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

* Added *Notes_for_Developers* file to src/ for common reference. This is intended as
a "best practices" reference for the NH LDD developers [Issue #17](https://github.com/pds-data-dictionaries/ldd-nh/issues/17).

## Version 1.0.0.0

This is the first configured version of the mission namespace, created as part of the
migration of MVIC KEM1 observations from PDS3 to PDS4. Many versions are expected as
additional missions, phases, and instruments are migrated.
