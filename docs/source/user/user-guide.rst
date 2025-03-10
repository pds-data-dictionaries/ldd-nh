.. 2023-01-28, by Anne Raugh

##################################################
Introduction
##################################################

This *User's Guide* provides a brief overview of the 
New Horizons Mission (NH or "nh:") namespace for those working with data from
New Horizons primary or extended missions. The primary New Horizons mission 
was to the Pluto system. The extended missions to date have been called
the "Kuiper Belt Extended Missions 1 and 2", or "KEM1" and "KEM2", in the
mission documentation and metadata.

----

   **Note** *that the New Horizons legacy data migration is in its early stages, with* 
   *labels being designed for each instrument in turn. This namespace is in active* 
   *development and will continue to be so for the forseeable future.* 

----

Data from the primary and first extended ("KEM1")
missions were archived in PDS3 format and migration is underway to convert the 
legacy data into PDS4. These migrated products will also serve as templates for the
second extended ("KEM2") mission, which will be delivered in PDS4 format.

This guide presents the major features of the namespace.

################################################################
Overview of the New Horizons (NH) Mission Dictionary
################################################################

.. include:: ../intro.md

- **Primary Steward:** Anne Raugh, Small Bodies Node, University of Maryland (@acraugh on Github)
- **Dictionary Repo:** https://github.com/pds-data-dictionaries/ldd-nh
- **Namespace Prefix:** nh:

Corrections, changes, and additions should be submitted through 
the `PDS LDD Issue Repo <https://github.com/pds-data-dictionaries/PDS4-LDD-Issue-Repo>`_.

##################################################
Organization of Classes and Attributes
##################################################

The New Horizons dictionary has a single top-level class that must be used to
access any of the NH metadata classes. Below that, there are major subclasses
for metadata that is common to all (or multiple instruments), as well as
classes specific to particular instruments. Processed and calibrated data will
generally have additional classes to provide instrument-specific processing
details.

The following sections describe the major divisions of the New Horizons Mission
namespace, in the order in which they occur in the schema (and thus, labels).

**************************************************
Top-Level Class: <nh:Mission_Parameters>
**************************************************

The *<nh:Mission_Parameters>* class acts as a wrapper for all other NH classes.
It contains one required attribute and (as of this writing) two optional classes
for data specific to the Multispectral Visible Imaging Camera (MVIC) part of
in the Ralph instrument package.

The class contains a single required attribute, *<nh:mission_phase_name>*, with the
string identifying the mission phase. Mission phase names are unique to the
primary or extended mission in which they occur. Specifically, the phases in the
extended missions contain the extended mission acronym ("KEM1 Encounter", for 
example).

The major subclasses of the *<nh:Mission_Parameters>* class are:

- :ref:`<nh:Observation_Parameters><observation-parameters>`
- :ref:`<nh:MVIC_Calibration_Information><mvic-calibration-information>`
- :ref:`<nh:Radiometric_Converstion_Constants><radiometric-conversion-constants>`
- :ref:`<nh:REX_Radiometry_Information><rex-radiometry-information>`

You can see a complete outline of the namespace under the
:doc:`../detailed/outline` topic.

.. _observation-parameters:

**************************************************
Subclass: <nh:Observation_Parameters>
**************************************************

The *<nh:Observation_Parameters>* class provides details specific to the New 
Horizons mission and the instrument used to make the observation comprising the
data product. It provides three attributes and two classes. As in the PDS
common namespace, in the NH dictionary attributes names are all lowercase; 
class names are in title case.

This class contains:

- <nh:telemetry_appid>
- <nh:sequence_id>
- <nh:observation_description>
- <nh:Mission_Elapsed_Time>
- <nh:Detector>
- <nh:Spacecraft_State>

None of these components is repeatable; all are expected to be present in all raw
and processed/calibrated data labels.

<nh:telemetry_appid>, <nh:sequence_id>, and <nh:observation_description>
  These attributes are provided primarily for provenance and to provide some minimal
  description of planned activities for the end user. The *nh:telementry_appid* is
  tied to instrument operating mode and to onboard processing like data compression. 
  The mission documentation for each instrument will provide further detail 
  if desired. The *<nh:sequence_id>* ties into the instrument observing plan, and
  the codes comprising that ID are roughly translated into something approaching
  English in the *<nh:observation_description>* string.

<nh:Mission_Elapsed_Time>
  The *<nh:Mission_Elapsed_Time>* class provides the spacecraft clock partition and
  count at the start and end of the observation comprising the data product.
  The translation from spacecraft clock to UTC is dependent on the hardware and is
  usually described in the mission documentation. Many missions and end-users use
  the publicly available Navigation and Ancillary Information (NAIF) Toolkit to 
  perform this conversion.
  
<nh:Detector>
  The *<nh:Detector>* class identifies the detector used to make the observation,
  and includes classes to provide detector-specific parameters. "Detector" may
  mean an instrument, or it may mean literally one of several detectors available
  within an instrument (as is the case of the MVIC instrument, for example). This
  class will contain detector-specific subclasses where needed to provide specific
  observational settings for the detector.
  
<nh:Spacecraft_State>
  The *<nh:Spacecraft_State>* class provides information about thruster firings,
  spin state, scan rate, and spacecraft motion at the time of the observation.
  For cases where none of the attributes of this class are relevant to the data
  product, this class should be omitted.
  
  
.. _mvic-calibration-information:
  
************************************************
Subclass: <nh:MVIC_Calibration_Information>
************************************************
  
The *<nh:MVIC_Calibration_Information>* class is used in labels for processed
data from all seven MVIC detectors. It provides detector-specific quantities
used in processing the data, and in the case of the MVIC framing camers, it
provides the specific left- and right-side biases used to process each frame.
  
This class contains:
  
- <nh:physical_pixel_size>
- <nh:read_noise>
- <nh:gain>
- <nh:tdi_median_bias_level>
- <nh:Framing_Biases>
  
<nh:physical_pixel_size>, <nh:read_noise> and <nh:gain>
  The *<nh:physical_pixel_size>* value is constant for all pixels on all MVIC
  detectors. It is provided explicitly for the convenience of users 
  further analyzing to the data. The *<nh:read_noise>* and *<nh:gain>* are 
  also provided for all MVIC observations.
    
<nh:tdi_median_bias_level>
  The *<nh:tdi_median_bias_level>* appears only in processed time delay integration
  (TDI) observations, from the color channels and the two panchromatic TDI channels.
  Bias levels for the TDI channels are determined during cruise operations and 
  may be updated through the course of the mission.
    
<nh:Framing_Biases>
  The *<nh:Framing_Biases>* class only appears in processing sequences from the MVIC
  framing array. It contains one *<nh:Frame_Bias_Levels>* class for each frame
  comprising the observation that identifies the frame by number and lists the 
  left- and right-side bias levels applied
  in processing that particular frame. For framing observations, bias is measured 
  during each observations using shielded pixels on either edge of the array.


.. _radiometric-conversion-constants:
 
*************************************************
Subclass: <nh:Radiometric_Conversion_Constants>
*************************************************

**NOTE:** *As of version 1.1.0, this class replaces the deprecated
<nh:MVIC_Conversion_Constants> class. The content of that class is included in this
one, with additional constants added as needed. This class is used by multiple instruments.*

The *<nh:Radiometric_Conversion_Constants>* class is used in labels for processed
data from all seven MVIC detectors. The MVIC pipeline does not produce "calibrated"
data in the sense that PDS defines "calibrated" - specifically, "Data reduced to 
physical units". The final reduction step depends on both the spectal characteristics
of the target and whether that target is resolved. Instead, the calibration 
documentation provided with the archive includes formulae for applying the absolute 
calibration for specific targets, and the constants needed to plug into the
formulae are provided in this class.

This class contains:

- <nh:pivot_wavelength>
- <nh:Resolved_Source>
- <nh:Unresolved_Source>

<nh:pivot_wavelength>
  The *<nh:pivot_wavelength>* attribute contains the pivot wavelength of the
  filter/dectector combination. 
  
<nh:Resolved_Source>
  The *<nh:Resolved_Source>* class provides the units of measure (units of radiance, 
  in the case of resolved targets) applicable to the resulting pixel values.
  Other attributes contain the conversion constants for five targets:
  
    - The Sun
    - Jupiter
    - \(5145\) Pholus, a centaur
    - Pluto
    - Charon
    - Arrokoth

<nh:Unresolved_Source>
  The *<nh:Unresolved_Source>* class provides the units of measure (units of 
  irradiance, in the case of unresolved targets) applicable to the resulting pixel
  values. Other attributes contain the conversion constants for five targets:
  
    - The Sun
    - Jupiter
    - \(5145\) Pholus, a centaur
    - Pluto
    - Charon
    - Arrokoth


.. _rex-radiometry-information:
 
*************************************************
Subclass: <nh:REX_Radiometry_Information>
*************************************************

The *<nh:REX_Radiometry_Information>* class is used in labels for data from the Radio
Science Experiment. The attributes in this class provide important instrument
parameters and coefficients used to translate raw radiometer counts into physical
units for a given product.

This class contains:

- <nh:frame_data_source>
- <nh:agc_gain_setting>
- <nh:agc_setting_source>
- <nh:agc_gain_provenance>
- <nh:base_agc_gain>
- <nh:base_power>
- <nh:radio_bandwidth>
- <nh:radiometry_response_step>
- <nh:radiometry_response_offset>
- <nh:iq_calibration_constant>
- <nh:time_tag_calibration_constant>

<nh:frame_data_source>
  The *<nh:frame_data_source>* attribute indicates the source of the input as a two-
  digit hexadecimal number (i.e., one octet), represented as a string prefixed by
  '0x'. 0x00 is the default source when taking data of external 7.2 GHz signal or
  external radiometry. All other values indicate REX-internal sources intended for
  diagnostics. The 4 least significant bits and the single most significant bit are
  not used.
  
<nh:agc_gain_setting>
  The *<nh:agc_gain_setting>* attribute supplies the value of the AGC gain setting
  used in the radiometry calibration.

<nh:agc_setting_source>
  The *<nh:agc_setting_source>* attribute provides the source of the
  *<nh:agc_gain_setting>* value. This attribute will have a value of either 'AUX' or
  'ULCMD'.

<nh:agc_gain_provenance>
  The *<nh:agc_gain_provenance>* attribute supplies the provenance for the
  *<nh:agc_gain_setting>* attribute. If *<nh:agc_setting_source>* = 'ULCMD', this value
  will take the form 'YYDOY.ssf:...', where YY is the two-digit year, DOY is the
  day-of-year, and '...' represents a string that indicates the source sequence file.
  Otherwise (if *<nh:agc_setting_source>*='AUX'), this value will be 'Nominal'. The
  nominal AGC gain values are 167 for side A and 163 for side B.

<nh:base_agc_gain> and <nh:base_power>
  The *<nh:base_agc_gain>* and *<nh:base_power>* contain the nominal/base AGC gain
  setting and the base/offset dBm value for the active side of the REX electronics,
  respectively. The base power is equivalent to the output power when
  RAW = (10^(-Ro/10))/Bandwidth and AGC = AGCOF, given the formula
  
    Power[dBm] = Rbase + 10*log10(Bandwidth*RAW) + dBstep*(AGC-AGCOF) + Ro
  
  The nominal values for this attribute are -176.852 for right circular polarization
  (side A) and -177.177 for left circular polarization (side B).

<nh:radio_bandwidth>
  The *<nh:radio_bandwidth>* attribute provides the active bandwidth of the REX radio.

<nh:radiometry_response_step> and <nh:radiometry_response_offset>
  The *<nh:radiometry_response_step>* and *<nh:radiometry_response_offset>* attributes
  contain the slope and intercept, for converting from raw counts to physical/
  radiometric quantities. These two attributes' values are represented by 'dBstep' and
  'Ro', respectively, in the formula

    Power[dBm] = Rbase + 10*log10(Bandwidth*RAW) + dBstep*(AGC-AGCOF) + Ro

<nh:iq_calibration_constant>
  The *<nh:iq_calibration_constant>* attribute supplies the I and Q response of the
  REX instrument, used to convert between raw counts and an I/Q value in mV. This
  constant has a nominal value of (1000 / (2^13)) mV/count.

<nh:time_tag_calibration_constant>
  The *<nh:time_tag_calibration_constant>* attribute provides the coefficient to be
  used when converting between raw counts and time tag seconds, e.g. 'DT' in the
  formula
  
    timetag[s] = DT * RAW
