Mockup Label: MVIC Red Channel, Processed Data
##################################################

This label mockup has been updated for version 1.1.0.0 of the mission
dictionary. Namespace references have been updated, and the older
MVIC_Calibration_Constants class has been replaced by the 
Radiometric_Calibration_Constants class, which applies to multipl
instruments. The data file correspunding to this label would contain
processed data from a TDI observation through the MVIC Red Channel 
(identified as "mc0" in file names).

The mockup shows the entire *<Product_Observational>*
structure including the New Horizons dictionary classes, which are 
found in the *<Mission_Area>* of the structure.

  **Note** that the New Horizons (nh:) and Small Bodies (sb:) dictionaries are in 
  active development. Consult the current release documentation for changes
  to these namespaces-in-development before attempting and real-would applications,
  or the Github repo for latest development versions. 

.. code-block:: XML

  <Product_Observational xmlns="http://pds.nasa.gov/pds4/pds/v1" 
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:disp="http://pds.nasa.gov/pds4/disp/v1" 
    xmlns:geom="http://pds.nasa.gov/pds4/geom/v1" 
    xmlns:img="http://pds.nasa.gov/pds4/img/v1" 
    xmlns:sb="http://pds.nasa.gov/pds4/sb/v0" 
    xmlns:nh="http://pds.nasa.gov/pds4/mission/nh/v1" 
    xsi:schemaLocation="http://pds.nasa.gov/pds4/pds/v1 https://pds.nasa.gov/pds4/pds/v1/PDS4_PDS_1L00.xsd
    http://pds.nasa.gov/pds4/disp/v1 https://pds.nasa.gov/pds4/disp/v1/PDS4_DISP_1L00_1510.xsd
    http://pds.nasa.gov/pds4/geom/v1 https://pds.nasa.gov/pds4/geom/v1/PDS4_GEOM_1L00_1970.xsd
    http://pds.nasa.gov/pds4/img/v1  https://pds.nasa.gov/pds4/img/v1/PDS4_IMG_1L00_1890.xsd
    http://pds.nasa.gov/pds4/sb/v1   https://pds.nasa.gov/pds4/sb/v0/PDS4_SB_1L00_1000.xsd
    http://pds.nasa.gov/pds4/mission/nh/v1 https://pds.nasa.gov/pds4/mission/nh/v1/PDS4_NH_1L00_1100.xsd">

    <Identification_Area>
        <logical_identifier>urn:nasa:pds:nh_mvic:kem1_cal:mc0_0408625487_0x545_sci</logical_identifier>
        <version_id>1.0</version_id>
        <title>New Horizons MVIC Red Channel Observation mc0_0408625487_0x545_sci (Processed Data)</title>
        <information_model_version>1.21.0.0</information_model_version>
        <product_class>Product_Observational</product_class>

        <Modification_History>
            <Modification_Detail>
                <modification_date>2022-12-26</modification_date>
                <version_id>1.0</version_id>
                <description>
                    A.C.Raugh: Migrated from PDS3 product NH-A-MVIC-3-KEM1-V6.0:MC0_0408625487_0X545_SCI
                </description>
            </Modification_Detail>
        </Modification_History>
    </Identification_Area>

    <Observation_Area>
        <Time_Coordinates>
            <start_date_time>2019-01-01T05:12:55.280Z</start_date_time>
            <stop_date_time>2019-01-01T05:14:34.148Z</stop_date_time>
        </Time_Coordinates>

        <Primary_Result_Summary>
            <purpose>Science</purpose>
            <processing_level>Partially Processed</processing_level>
            <Science_Facets>
                <wavelength_range>Visible</wavelength_range>
                <discipline_name>Imaging</discipline_name>
                <facet1>Grayscale</facet1>
            </Science_Facets>
        </Primary_Result_Summary>

        <Investigation_Area>
            <name>New Horizons Kuiper Belt Extended Mission 1</name>
            <type>Mission</type>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:context:investigation:mission.new_horizons_kem1</lid_reference>
                <reference_type>data_to_investigation</reference_type>
            </Internal_Reference>
        </Investigation_Area>

        <Observing_System>
            <Observing_System_Component>
                <name>New Horizons Spacecraft</name>
                <type>Host</type>
                <Internal_Reference>
                    <lid_reference>urn:nasa:pds:context:instrument_host:spacecraft.nh</lid_reference>
                    <reference_type>is_instrument_host</reference_type>
                </Internal_Reference>
            </Observing_System_Component>
            <!-- There is no "Instrument Package" in PDS4 as yet
            <Observing_System_Component>
                <name>RALPH</name>
                <type>Instrument Package</type> 
                <description>
                    RALPH is an instrument package supporting two independent instrument,
                    the Multispectral Visible Imaging Camera (MVIC) and the Linear Etalon
                    Imaging Spectral Array (LEISA), that share a boresight, a focal plane, 
                    and electronics. Detectors and pipeline processing are unique to each
                    instrument.
                </description>
            </Observing_System_Component>
            -->            
            <Observing_System_Component>
                <name>Multispectral Visible Imaging Camera (MVIC)</name>
                <type>Instrument</type>
                <description>
                    Note that the MVIC instrument has seven distinct detectors, identified by
                    the "nh:Detector" class metadata.
                </description>
                <Internal_Reference>
                    <lid_reference>urn:nasa:pds:context:instrument:nh.mvic</lid_reference>
                    <reference_type>is_instrument</reference_type>
                </Internal_Reference>
            </Observing_System_Component>
        </Observing_System>

        <Target_Identification>
            <name>(486958) Arrokoth</name>
            <alternate_designation>2014 MU69</alternate_designation>
            <type>Trans-Neptunian Object</type>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:context:target:trans-neptunian_object.486958_2014_mu69</lid_reference>
                <reference_type>data_to_target</reference_type>
            </Internal_Reference>
        </Target_Identification>

        <Mission_Area>
            <nh:Mission_Parameters>
                <nh:mission_phase_name>KEM1 Encounter</nh:mission_phase_name>
                <nh:Observation_Parameters>
                    <nh:telemetry_apid>0x545</nh:telemetry_apid>
                    <nh:sequence_id>KEMV_MU69_CA05_HIRES_MC_2019001</nh:sequence_id>
                    <nh:observation_description>MVIC Color CA Scan, LORRI Rider</nh:observation_description>
                    <nh:Mission_Elapsed_Time>
                        <nh:clock_partition>3</nh:clock_partition>
                        <nh:start_clock_count>0408625493:06600</nh:start_clock_count>
                        <nh:stop_clock_count>0408625592:00000</nh:stop_clock_count>
                    </nh:Mission_Elapsed_Time>
                    <nh:Detector>
                        <nh:detector_name>MVIC Red (RED) Channel</nh:detector_name>
                        <nh:detector_type>CCD</nh:detector_type>
                        <nh:MVIC_Details>
                            <nh:scan_type>TDI - Time Delay Integration Mode</nh:scan_type>
                            <nh:tdi_rate unit="Hz">40.4694</nh:tdi_rate>
                        </nh:MVIC_Details>
                    </nh:Detector>
                </nh:Observation_Parameters>
                <nh:MVIC_Calibration_Information>
                    <nh:physical_pixel_size unit="micrometer">13.0000</nh:physical_pixel_size>
                    <nh:read_noise>30.000</nh:read_noise>
                    <nh:gain unit="electron/DN">58.6000</nh:gain>
                    <nh:tdi_median_bias_level unit="DN">25</nh:tdi_median_bias_level>
                </nh:MVIC_Calibration_Information>
                <nh:Radiometric_Conversion_Constants>
                    <nh:pivot_wavelength unit="micrometer">0.624</nh:pivot_wavelength>
                    <nh:Resolved_Source>
                        <nh:units_of_conversion_constants>(DN/s)/(erg/cm^2/s/Angstrom/sr)</nh:units_of_conversion_constants>
                        <nh:solar_constant>30910.883</nh:solar_constant>
                        <nh:jupiter_constant>32852.793</nh:jupiter_constant>
                        <nh:pholus_constant>32509.977</nh:pholus_constant>
                        <nh:pluto_constant>30908.678</nh:pluto_constant>
                        <nh:charon_constant>30856.479</nh:charon_constant>
                    </nh:Resolved_Source>
                    <nh:Unresolved_Source>
                        <nh:units_of_conversion_constants>(DN/s)/(erg/cm^2/s/Angstrom)</nh:units_of_conversion_constants>
                        <nh:solar_constant>7.880E+13</nh:solar_constant>
                        <nh:jupiter_constant>8.375E+13</nh:jupiter_constant>
                        <nh:pholus_constant>8.287E+13</nh:pholus_constant>
                        <nh:pluto_constant>7.879E+13</nh:pluto_constant>
                        <nh:charon_constant>7.866E+13</nh:charon_constant>
                    </nh:Unresolved_Source>
                </nh:Radiometric_Conversion_Constants>
            </nh:Mission_Parameters>
        </Mission_Area>

        <Discipline_Area>
            <disp:Display_Settings>
                <Local_Internal_Reference>
                    <local_identifier_reference>Image</local_identifier_reference>
                    <local_identifier_reference>ErrorEstimate</local_identifier_reference>
                    <local_identifier_reference>Quality</local_identifier_reference>
                    <local_reference_type>display_settings_to_array</local_reference_type>
                </Local_Internal_Reference>
                <disp:Display_Direction>
                    <disp:horizontal_display_axis>Sample</disp:horizontal_display_axis>
                    <disp:horizontal_display_direction>Left to Right</disp:horizontal_display_direction>
                    <disp:vertical_display_axis>Line</disp:vertical_display_axis>
                    <disp:vertical_display_direction>Bottom to Top</disp:vertical_display_direction>
                </disp:Display_Direction>
            </disp:Display_Settings>

            <img:Exposure>
                <img:exposure_duration unit="s">0.79072</img:exposure_duration>
            </img:Exposure>
            <img:Onboard_Compression>
                <img:onboard_compression_class>Lossless</img:onboard_compression_class>
            </img:Onboard_Compression>
            
            <geom:Geometry>

                <geom:comment>
                    Note that the geometry parameters in this label were calculated by the
                    mission using an unpublished kernel set still in development at the time 
                    of archiving. These parameters are based on "predict geometry", which is
                    generally not as accurate as metadata available at a later date.
                </geom:comment>

                <geom:Image_Display_Geometry>
                    <geom:geometry_reference_time_utc>2019-01-01T05:13:44.714Z</geom:geometry_reference_time_utc>
                    <Local_Internal_Reference>
                        <local_identifier_reference>Image</local_identifier_reference>
                        <local_reference_type>display_to_data_object</local_reference_type>
                    </Local_Internal_Reference>
                    <geom:Geometry_Target_Identification>
                        <geom:body_spice_name>2486958</geom:body_spice_name>
                        <geom:name>(486958) Arrokoth</geom:name>
                    </geom:Geometry_Target_Identification>
                    <geom:Object_Orientation_RA_Dec>
                        <geom:reference_pixel_location>Center</geom:reference_pixel_location>
                        <geom:right_ascension_angle unit="deg">276.8</geom:right_ascension_angle>
                        <geom:declination_angle unit="deg">-33.8</geom:declination_angle>
                        <geom:celestial_north_clock_angle unit="deg">351.57838</geom:celestial_north_clock_angle>
                        <geom:Reference_Frame_Identification>
                            <geom:name>EME J2000</geom:name>
                        </geom:Reference_Frame_Identification>
                    </geom:Object_Orientation_RA_Dec>
                    <geom:Object_Orientation_Clock_Angles>
                        <geom:target_positive_pole_clock_angle unit="deg">264.7</geom:target_positive_pole_clock_angle>
                        <geom:sun_direction_clock_angle unit="deg">133.8</geom:sun_direction_clock_angle>
                    </geom:Object_Orientation_Clock_Angles>
                    <geom:Quaternion_Plus_To_From>
                        <geom:qcos>0.3391999442067836</geom:qcos>
                        <geom:qsin1>0.5793975569923115</geom:qsin1>
                        <geom:qsin2>0.3215769780838686</geom:qsin2>
                        <geom:qsin3>0.6677051115334547</geom:qsin3>
                        <geom:Rotate_From>
                            <geom:name>MVIC Instrument Frame</geom:name>
                        </geom:Rotate_From>
                        <geom:Rotate_To>
                            <geom:name>EME J2000</geom:name>
                        </geom:Rotate_To>
                    </geom:Quaternion_Plus_To_From>
                </geom:Image_Display_Geometry>

                <geom:Geometry_Orbiter>
                    <geom:geometry_reference_time_utc>2019-01-01T05:13:44.714Z</geom:geometry_reference_time_utc>
                    <geom:Orbiter_Identification>
                        <geom:Geometry_Target_Identification>
                            <geom:body_spice_name>2486958</geom:body_spice_name>
                            <geom:name>(486958) Arrokoth</geom:name>
                        </geom:Geometry_Target_Identification>
                    </geom:Orbiter_Identification>
                    <geom:Pixel_Dimensions>
                        <geom:pixel_field_of_view_method>Constant</geom:pixel_field_of_view_method>
                        <geom:horizontal_pixel_field_of_view unit="mrad">.0198065</geom:horizontal_pixel_field_of_view>
                        <geom:vertical_pixel_field_of_view unit="mrad">.0198065</geom:vertical_pixel_field_of_view>
                    </geom:Pixel_Dimensions>
                    <geom:Distances>
                        <geom:Distances_Specific>
                            <geom:spacecraft_geocentric_distance unit="km">6620524663.557333</geom:spacecraft_geocentric_distance>
                            <geom:spacecraft_heliocentric_distance unit="km">6474349486.445694</geom:spacecraft_heliocentric_distance>
                            <geom:spacecraft_target_center_distance unit="km">17364.42363680587</geom:spacecraft_target_center_distance>
                            <geom:target_geocentric_distance unit="km">6620676566.778128</geom:target_geocentric_distance>
                            <geom:target_heliocentric_distance unit="km">6474366229.430338</geom:target_heliocentric_distance>
                        </geom:Distances_Specific>
                    </geom:Distances>
                    <geom:Surface_Geometry>
                        <geom:Surface_Geometry_Specific>
                            <geom:subsolar_latitude unit="deg">-61.85812998743076</geom:subsolar_latitude>
                            <geom:subsolar_longitude unit="deg">87.24761404769193</geom:subsolar_longitude>
                            <geom:subspacecraft_latitude unit="deg">-53.47274657874268</geom:subspacecraft_latitude>
                            <geom:subspacecraft_longitude unit="deg">111.6557853166782</geom:subspacecraft_longitude>
                        </geom:Surface_Geometry_Specific>
                    </geom:Surface_Geometry>
                    <geom:Illumination_Geometry>
                        <geom:Illumination_Specific>
                            <geom:reference_location>Boresight Intercept Point</geom:reference_location>
                            <geom:phase_angle unit="deg">15.4</geom:phase_angle>
                            <geom:solar_elongation unit="deg">164.6</geom:solar_elongation>
                        </geom:Illumination_Specific>
                    </geom:Illumination_Geometry>
                    <geom:Vectors>
                        <geom:Vectors_Cartesian_Specific>
                            <geom:Vector_Cartesian_Position_Spacecraft_To_Target>
                                <geom:x_position unit="km">1656.2122</geom:x_position>
                                <geom:y_position unit="km">-14549.6368</geom:y_position>
                                <geom:z_position unit="km">-9332.1077</geom:z_position>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Position_Spacecraft_To_Target>
                            <geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Target>
                                <geom:x_velocity unit="km/s">1.113444</geom:x_velocity>
                                <geom:y_velocity unit="km/s">-13.442996</geom:y_velocity>
                                <geom:z_velocity unit="km/s">-5.139864</geom:z_velocity>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Target>
                            <geom:Vector_Cartesian_Position_Sun_To_Target>
                                <geom:x_position unit="km">1801863012.047373</geom:x_position>
                                <geom:y_position unit="km">-5789632811.265433</geom:y_position>
                                <geom:z_position unit="km">-2269550543.460596</geom:z_position>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Position_Sun_To_Target>
                            <geom:Vector_Cartesian_Velocity_Target_Relative_To_Sun>
                                <geom:x_velocity unit="km/s">4.370272</geom:x_velocity>
                                <geom:y_velocity unit="km/s">1.336516</geom:y_velocity>
                                <geom:z_velocity unit="km/s">0.445148</geom:z_velocity>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Velocity_Target_Relative_To_Sun>
                            <geom:Vector_Cartesian_Position_Earth_To_Target>
                                <geom:x_position unit="km">1828821837.219335</geom:x_position>
                                <geom:y_position unit="km">-5922292146.245399</geom:y_position>
                                <geom:z_position unit="km">-2327063519.570272</geom:z_position>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Position_Earth_To_Target>
                            <geom:Vector_Cartesian_Velocity_Target_Relative_To_Earth>
                                <geom:x_velocity unit="km/s">34.156224</geom:x_velocity>
                                <geom:y_velocity unit="km/s">6.405462</geom:y_velocity>
                                <geom:z_velocity unit="km/s">2.642036</geom:z_velocity>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Velocity_Target_Relative_To_Earth>
                            <geom:Vector_Cartesian_Position_Sun_To_Spacecraft>
                                <geom:x_position unit="km">1801956296.599184</geom:x_position>
                                <geom:y_position unit="km">-5789592074.710976</geom:y_position>
                                <geom:z_position unit="km">-2269532636.079516</geom:z_position>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Position_Sun_To_Spacecraft>
                            <geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Sun>
                                <geom:x_velocity unit="km/s">5.483717</geom:x_velocity>
                                <geom:y_velocity unit="km/s">-12.1064806</geom:y_velocity>
                                <geom:z_velocity unit="km/s">-4.694715</geom:z_velocity>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Sun>
                            <geom:Vector_Cartesian_Position_Earth_To_Spacecraft>
                                <geom:x_position unit="km">1827405810.34603</geom:x_position>
                                <geom:y_position unit="km">-5922522508.111715</geom:y_position>
                                <geom:z_position unit="km">-2327157486.28979</geom:z_position>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Position_Earth_To_Spacecraft>
                            <geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Earth>
                                <geom:x_velocity unit="km/s">35.316729</geom:x_velocity>
                                <geom:y_velocity unit="km/s">-7.283111</geom:y_velocity>
                                <geom:z_velocity unit="km/s">-2.604148</geom:z_velocity>
                                <geom:light_time_correction_applied>Received_Light_Time_Stellar_Abb</geom:light_time_correction_applied>
                            </geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Earth>
                        </geom:Vectors_Cartesian_Specific>
                    </geom:Vectors>
                </geom:Geometry_Orbiter>
            </geom:Geometry>
            
            <sb:SB_Metadata>
                <sb:Observation_Parameters>
                    <sb:Exposure>
                        <sb:exposure_duration unit="s">0.79072</sb:exposure_duration>
                        <sb:exposure_description>
                            The exposure duration is the amount of time that data was collected
                            for each pixel in the array. For details of how the MVIC TDI scanning
                            observations collected data, see "Ralph: A Visible/Infrared Imager for
                            the New Horizons Pluto/Kuiper Belt Mission" (Reuter, et al. 2008), a 
                            preprint copy of which is included in the mission archive and 
                            referenced below.
                        </sb:exposure_description>
                    </sb:Exposure>
                    <sb:Filter>
                        <sb:filter_name>Red</sb:filter_name>
                        <sb:filter_type>Broadband</sb:filter_type>
                        <sb:short_wavelength_limit unit="nm">540</sb:short_wavelength_limit>
                        <sb:long_wavelength_limit unit="nm">700</sb:long_wavelength_limit>
                    </sb:Filter>
                    <sb:Timing>
                        <sb:midobservation_time_UTC_YMD>2019-01-01T05:13:44.714Z</sb:midobservation_time_UTC_YMD>
                        <sb:midobservation_time_UTC_JD unit="julian day">2458484.7178786</sb:midobservation_time_UTC_JD>
                    </sb:Timing>
                </sb:Observation_Parameters>
                
                <sb:Calibration_Information>
                    <sb:Raw_Data_Product>
                        <Internal_Reference>
                            <lidvid_reference>urn:nasa:pds:nh_mvic:kem1_cal:mc0_0408625487_0x545_eng::1.0</lidvid_reference>
                            <reference_type>processed_data_to_raw_data</reference_type>
                        </Internal_Reference>
                    </sb:Raw_Data_Product>
                    
                    <sb:Calibration_Applied>
                        <sb:comment>
                            The conversion to physical units depends on the spectral characteristics of the 
                            object and whether it is resolved. Conversion constants are provided as part of
                            the mission attributes in this label.
                        </sb:comment>
                        <sb:bias_subtraction>true</sb:bias_subtraction>
                        <sb:flat_field_applied>true</sb:flat_field_applied>
                    </sb:Calibration_Applied>
                    
                    <sb:Calibration_Reference_Files>
                        <sb:Flat_Field>
                            <sb:file_name>mc0_flat_20160120.fits</sb:file_name>
                            <Internal_Reference>
                                <lidvid_reference>urn:nasa:pds:nh_mvic:calibration_files:mc0_flat::4.0</lidvid_reference>
                                <reference_type>image_to_flat_field_file</reference_type>
                            </Internal_Reference>
                        </sb:Flat_Field>
                    </sb:Calibration_Reference_Files>
                </sb:Calibration_Information>
                
                <sb:Additional_Image_Metadata>
                    <Local_Internal_Reference>
                        <local_identifier_reference>Image</local_identifier_reference>
                        <local_reference_type>image_to_additional_metadata</local_reference_type>
                    </Local_Internal_Reference>
                    
                    <sb:image_observation_type>Single Image</sb:image_observation_type>
                    
                    <sb:Ancillary_Data_Objects>
                        <sb:Quality_Map>
                            <Local_Internal_Reference>
                                <local_identifier_reference>Quality</local_identifier_reference>
                                <local_reference_type>image_to_quality_map</local_reference_type>
                            </Local_Internal_Reference>
                            <sb:Quality_Map_Definition>
                                <sb:flags_are_bit_flags>true</sb:flags_are_bit_flags>
                                <sb:best_quality_value>0</sb:best_quality_value>
                                <sb:Quality_Flag_Definition>
                                    <sb:flag_value>1</sb:flag_value>
                                    <sb:flag_meaning>Housekeeping keyword out of yellow limits</sb:flag_meaning>
                                </sb:Quality_Flag_Definition>
                                <sb:Quality_Flag_Definition>
                                    <sb:flag_value>2</sb:flag_value>
                                    <sb:flag_meaning>Defect in one of the reference calibration files</sb:flag_meaning>
                                </sb:Quality_Flag_Definition>
                                <sb:Quality_Flag_Definition>
                                    <sb:flag_value>4</sb:flag_value>
                                    <sb:flag_meaning>Permanent CCD defect (e.g., dead pixel)</sb:flag_meaning>
                                </sb:Quality_Flag_Definition>
                                <sb:Quality_Flag_Definition>
                                    <sb:flag_value>8</sb:flag_value>
                                    <sb:flag_meaning>DN level in non-linear regime of detector</sb:flag_meaning>
                                </sb:Quality_Flag_Definition>
                                <sb:Quality_Flag_Definition>
                                    <sb:flag_value>16</sb:flag_value>
                                    <sb:flag_meaning>Zero-value pixel</sb:flag_meaning>
                                </sb:Quality_Flag_Definition>
                                <sb:Quality_Flag_Definition>
                                    <sb:flag_value>32</sb:flag_value>
                                    <sb:flag_meaning>Bad pixel not in any of the above categories</sb:flag_meaning>
                                </sb:Quality_Flag_Definition>
                            </sb:Quality_Map_Definition>
                        </sb:Quality_Map>
                        <sb:Error_Estimates_Map>
                            <Local_Internal_Reference>
                                <local_identifier_reference>ErrorEstimate</local_identifier_reference>
                                <local_reference_type>image_to_error_map</local_reference_type>
                            </Local_Internal_Reference>
                        </sb:Error_Estimates_Map>
                    </sb:Ancillary_Data_Objects>
                    
                    <sb:Additional_Geometry_Metadata>
                        <sb:comment>
                            Note that the geometry parameters in this label were calculated by the
                            mission using an unpublished kernel set still in development at the time 
                            of archiving. These parameters are based on "predict geometry", which is
                            generally not as accurate as metadata available at a later date.
                            
                            The instrument position angles are calculated at the midpoint of the 
                            observing sequence.
                        </sb:comment>
                        <sb:Instrument_Position_Angles>
                            <sb:y_axis_position_angle unit="deg">351.5783804696931</sb:y_axis_position_angle>
                            <sb:z_axis_position_angle unit="deg">81.57838046969316</sb:z_axis_position_angle>
                        </sb:Instrument_Position_Angles>
                    </sb:Additional_Geometry_Metadata>
                </sb:Additional_Image_Metadata>
            </sb:SB_Metadata>

        </Discipline_Area>
    </Observation_Area>
    
    <Reference_List>
        <Internal_Reference>
            <lid_reference>urn:nasa:pds:nh_documents:ralph:ralph_ssr</lid_reference>
            <reference_type>data_to_document</reference_type>
            <comment>
                This document from Space Science Reviews describes technical and operational 
                details of the RALPH instruments and detectors.
            </comment>
        </Internal_Reference>
    </Reference_List>
    
    <File_Area_Observational>
        <File>
            <file_name>mc0_0408625487_0x545_sci.fit</file_name>
            <comment>
                This file contains a single observation from one of the MVIC color channel detectors.
                The image dimensions reflect the full area of the detector, not all of which contains
                data in all cases. Pixels for which data was not downloaded are filled with the 
                "missing_constant" value.
            </comment>
        </File>
        
        <!-- Primary ("extension 0" in some applications) header and data unit -->
        
        <Header>
            <offset unit="byte">0</offset>
            <object_length unit="byte">25920</object_length>
            <parsing_standard_id>FITS 3.0</parsing_standard_id>
            <description>
                Primary FITS header unit. The New Horizons pipeline produced data in FITS format.
            </description>
        </Header>
        <Array_2D_Image>
            <name>Observational Data (DN)</name>
            <local_identifier>Image</local_identifier>
            <offset unit="byte">25920</offset>
            <axes>2</axes>
            <axis_index_order>Last Index Fastest</axis_index_order>
            <description>
                This array contains data only for pixels within the window(s) defined by the
                Subframe(s) listed for this product. Other pixels have been set to -1.0, the
                defined "missing_constant". 
            </description>
            <Element_Array>
                <data_type>IEEE754MSBSingle</data_type>
                <unit>DN</unit>
            </Element_Array>
            <Axis_Array>
                <axis_name>Line</axis_name>
                <elements>3984</elements>
                <sequence_number>1</sequence_number>
            </Axis_Array>
            <Axis_Array>
                <axis_name>Sample</axis_name>
                <elements>5024</elements>
                <sequence_number>2</sequence_number>
            </Axis_Array>
            <Special_Constants>
                <missing_constant>-1.000</missing_constant>
            </Special_Constants>
        </Array_2D_Image>
        
        <!-- First extension header and data unit -->
        
        <Header>
            <offset unit="byte">80089920</offset>
            <object_length unit="byte">2880</object_length>
            <parsing_standard_id>FITS 3.0</parsing_standard_id>
            <description>
                FITS IMAGE extension header - a minimal header.
            </description>
        </Header>
        <Array_2D_Image>
            <name>Per-pixel Error Estimate (DN)</name>
            <local_identifier>ErrorEstimate</local_identifier>
            <offset unit="byte">80092800</offset>
            <axes>2</axes>
            <axis_index_order>Last Index Fastest</axis_index_order>
            <description>
                This array provides per-pixel error estimates in DN for each of the corresponding
                pixels in the primary data. It contains data only for pixels within the window(s) 
                defined by the Subframe(s) listed for this product. Other pixels have been set to 
                -1.0, the defined "missing_constant". 
            </description>
            <Element_Array>
                <data_type>IEEE754MSBSingle</data_type>
                <unit>DN</unit>
            </Element_Array>
            <Axis_Array>
                <axis_name>Line</axis_name>
                <elements>3984</elements>
                <sequence_number>1</sequence_number>
            </Axis_Array>
            <Axis_Array>
                <axis_name>Sample</axis_name>
                <elements>5024</elements>
                <sequence_number>2</sequence_number>
            </Axis_Array>
            <Special_Constants>
                <missing_constant>-1.00</missing_constant>
            </Special_Constants>
        </Array_2D_Image>
        
        <!-- Second extension header and data unit -->
        
        <Header>
            <offset unit="byte">160156800</offset>
            <object_length unit="byte">2880</object_length>
            <parsing_standard_id>FITS 3.0</parsing_standard_id>
            <description>
                FITS IMAGE extension header - minimal header. COMMENT cards include terse
                quality code definitions.
            </description>
        </Header>
        <Array_2D_Image>
            <name>Per-pixel Quality Assessment</name>
            <local_identifier>Quality</local_identifier>
            <offset unit="byte">160159680</offset>
            <axes>2</axes>
            <axis_index_order>Last Index Fastest</axis_index_order>
            <Element_Array>
                <data_type>SignedMSB2</data_type>
            </Element_Array>
            <Axis_Array>
                <axis_name>Line</axis_name>
                <elements>3984</elements>
                <sequence_number>1</sequence_number>
            </Axis_Array>
            <Axis_Array>
                <axis_name>Sample</axis_name>
                <elements>5024</elements>
                <sequence_number>2</sequence_number>
            </Axis_Array>
            <Special_Constants>
                <missing_constant>-1</missing_constant>
            </Special_Constants>
        </Array_2D_Image>
    </File_Area_Observational>
    
   </Product_Observational>
