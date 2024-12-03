# Regression Test Directory

This directory contains regression tests for specific issues resolved, as
well as simple examples of the structures included in the New Horizons
Mission dictionary. Note that examples show structure only - the values
should not be taken as examples of what should be expected in real 
observational labels.

The issue-related tests include:

**ConversionConstantsUnits_Fail.xml**

  Verify that incorrect values for *nh:units_of_conversion_constants* produce errors.

**MVICmc0Proc_DEPREC_FAIL.xml**

**MVICmpfProv_DEPREC_FAIL.xml**

  Verify that the original MVIC_Calibration_Constants class is now deprecated in 
  favor of the Radiometric_Conversion_Constants class.

## *examples/* Directory

This directory contains the following VALID-only test files:
  
**AliceClasses.xml**

  An abbreviated label that tests the Alice-related schema structures.
  
**LEISAClasses.xml**

  An abbreviated label that tests the LEISA-related schema structures.
  
**LORRIClasses.xml**

  An abbreviated label that tests the LORRI-related schema structures.
  
**MVICmc0Proc_VALID.xml**

  A stripped-down label mockup that shows only the NH mission classes (no discipline 
  classes) for a processed MVIC color channel TDI observation. 
  
**MVICmpfProc_VALID.xml**

  A stripped-down label mockup that shows only the NH mission classes for a 
  processed MVIC panchromatic frame array framing observation.
  
**LEISAProc_VALID.xml**

  A design mockup of a LEISA label showing only mission classes for a processing
  data product.
    
**SWAPhistProc_VALID.xml**

  A mock-up of a SWAP histogram product, testing the SWAP-related schema 
  structures.
 