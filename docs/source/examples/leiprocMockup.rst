#######################################################################
Mockup Label: LEISA Spectral Image, Processed Data
#######################################################################

This label is a mockup created for design purposes. The data file
it describes contains processed LEISA spectral image data (identified
by telemetry ApID 0x53c).

The mockup shows the entire *<Product_Observational>*
structure, including the New Horizons dictionary classes, which are 
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
        http://pds.nasa.gov/pds4/sp/v1   https://pds.nasa.gov/pds4/sp/v1/PDS4_SP_1L00_1311.xsd
        http://pds.nasa.gov/pds4/sb/v1   https://pds.nasa.gov/pds4/sb/v1/PDS4_SB_1L00_1000.xsd
        http://pds.nasa.gov/pds4/mission/nh/v1 https://pds.nasa.gov/pds4/mission/nh/v1/PDS4_NH_1L00_1100.xsd>
        <Identification_Area>
            <logical_identifier>urn:nasa:pds:nh_leisa:kem1_cal:lsb_0408606595_0x53c_sci</logical_identifier>
            <version_id>1.0</version_id>
            <title>LEISA Calibrated Data Product: lsb_0408606595_0x53c_sci</title>
            <information_model_version>1.21.0.0</information_model_version>
            <product_class>Product_Observational</product_class>
        </Identification_Area>

        <Observation_Area>
            <Time_Coordinates>
                <start_date_time>2018-12-31T23:57:57.148195Z</start_date_time>
                <stop_date_time>2019-01-01T00:04:46.148199Z</stop_date_time>
            </Time_Coordinates>

            <Primary_Result_Summary>
                <purpose>Science</purpose>
                <processing_level>Calibrated</processing_level>
                <Science_Facets>
                    <wavelength_range>Near Infrared</wavelength_range>
                    <discipline_name>Spectroscopy</discipline_name>
                    <facet1>Spectral Image</facet1>
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
                <Observing_System_Component>
                    <name>LEISA</name>
                    <type>Instrument</type>
                    <description>Linear Etalon Imaging Spectral Array</description>
                    <Internal_Reference>
                        <lid_reference>urn:nasa:pds:context:instrument:nh.leisa</lid_reference>
                        <reference_type>is_instrument</reference_type>
                    </Internal_Reference>
                </Observing_System_Component>
            </Observing_System>

            <Target_Identification>
                <name>Asteroid 486958 (2014 MU69)</name>
                <alternate_designation>Arrokoth</alternate_designation>
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
                        <nh:telemetry_apid>0x53c</nh:telemetry_apid>
                        <nh:sequence_id>KELE_MU69_APROTH_LE_2018365J</nh:sequence_id>
                        <nh:observation_description>LEISA Composition and System Scan</nh:observation_description>
                        <nh:Mission_Elapsed_Time>
                            <nh:clock_partition>3</nh:clock_partition>
                            <nh:start_clock_count>0408606595:00000</nh:start_clock_count>
                            <nh:stop_clock_count>0408607004:00000</nh:stop_clock_count>
                        </nh:Mission_Elapsed_Time>
                        <nh:Detector>
                            <nh:detector_name>Linear Etalon Imaging Spectral Array</nh:detector_name>
                            <nh:detector_type>HgCdTe PICNIC array</nh:detector_type>
                            <nh:Ralph_Details>
                                <nh:met510 unit="s">408606595</nh:met510>
                                <nh:true510>true</nh:true510>
                            </nh:Ralph_Details>
                            <nh:LEISA_Details>
                                <nh:scan_type>LEISA</nh:scan_type>
                                <nh:leisa_mode>SUBTRACTED</nh:leisa_mode>
                                <nh:leisa_offset_1 unit="DN">2951</nh:leisa_offset_1>
                                <nh:leisa_offset_2 unit="DN">2950</nh:leisa_offset_2>
                                <nh:leisa_offset_3 unit="DN">2957</nh:leisa_offset_3>
                                <nh:leisa_offset_4 unit="DN">2945</nh:leisa_offset_4>
                                <nh:leisa_rate unit="ms">1521</nh:leisa_rate>
                                <nh:leisa_side>B</nh:leisa_side>
                                <nh:leisa_temperature unit="degC">-161.77116450294238</nh:leisa_temperature>
                            </nh:LEISA_Details>
                        </nh:Detector>
                        <nh:Spacecraft_State>
                            <nh:thruster_x_enable>true</nh:thruster_x_enable>
                            <nh:thruster_y_enable>true</nh:thruster_y_enable>
                            <nh:thruster_z_enable>true</nh:thruster_z_enable>
                            <nh:gc_scan_rate>-40.0</nh:gc_scan_rate>
                            <nh:target_motion_rate>40.0</nh:target_motion_rate>
                            <nh:relative_control_mode>false</nh:relative_control_mode>
                            <nh:pointing_method>CB1</nh:pointing_method>
                            <nh:spacecraft_spin_state>3-Axis</nh:spacecraft_spin_state>
                        </nh:Spacecraft_State>
                    </nh:Observation_Parameters>
                </nh:Mission_Parameters>
            </Mission_Area>
            <Discipline_Area>
                <disp:Display_Settings>
                    <Local_Internal_Reference>
                        <local_identifier_reference>data_array</local_identifier_reference>
                        <local_reference_type>display_settings_to_array</local_reference_type>
                    </Local_Internal_Reference>
                    <disp:Display_Direction>
                        <disp:horizontal_display_axis>xtrack</disp:horizontal_display_axis>
                        <disp:horizontal_display_direction>Left to Right</disp:horizontal_display_direction>
                        <disp:vertical_display_axis>atrack</disp:vertical_display_axis>
                        <disp:vertical_display_direction>Bottom to Top</disp:vertical_display_direction>
                    </disp:Display_Direction>
                </disp:Display_Settings>
                <geom:Geometry>
                    <geom:SPICE_Kernel_Files>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20060119_20100101_od032.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20061001_20100101_od040.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20070307_20100101_od041.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20070319_20150901_od077.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20120501_20160913_od091.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20150801_20190901_od126.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20161201_20250101_od132.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20161202_20250101_od134.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20180601_20250101_od146.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20190101_20260101_od153.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pred_20190101_20270101_od154.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>17258_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18226_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18240_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18254_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18270_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18287_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18302_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18315_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18330_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18344_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>18359_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>19003_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>19059_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>19073_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>19234_cmd.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>LSK</geom:kernel_type>
                            <geom:spice_kernel_file_name>naif0012.tls</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SCLK</geom:kernel_type>
                            <geom:spice_kernel_file_name>new-horizons_2437.tsc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>PCK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_stars_kbo_centaur_ppinp.tpc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>PCK</geom:kernel_type>
                            <geom:spice_kernel_file_name>pck00010.tpc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>FK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_v220.tf</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_allinstruments_v002.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_alice_v200.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_lorri_v201.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_pepssi_v110.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_ralph_v100.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_rex_v100.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_sdc_v101.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>IK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_swap_v200.ti</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>FK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_soc_misc_v001.tf</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Provenance Not Applicable</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>sb-2002jf56-2.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>jup260.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>kbo_centaur_horizons_20131129.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>kbo_centaur_20170422.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>kbo_centaur_20200430.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_extras.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_stars.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>2002_KX14_20160411.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2011_HJ103_20170920.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2012_HE85_20170808.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2012_HZ84_20170808.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2011_JY31_20190804.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2013_LU35_20171205.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2020KU11_20201029a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_B6600475_20201029a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_P4856186_20210204a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2020KR11_20210204a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2020KP11_20210305a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2020KT11_20201216a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_2020KO11_20201029a_type5.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>Huya_20160411.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>Pholus_20160411.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_nep081.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_ura111.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>NavPE_de433_od154.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>NavSE_plu047_od123.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>NavSBE_2014MU69_od154.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_nep_ura_000.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_recon_e2j_v1.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Reconstructed</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_recon_j2sep07_prelimv1.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Reconstructed</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>SPK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nh_recon_pluto_od122_v01.bsp</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Reconstructed</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2006_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2007_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2008_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2009_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2010_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2011_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2012_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2013_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2014_v001.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2015_v039.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2016_v003.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2017_v014.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2018_v100.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2019_v029.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2020_v010.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2021_01_v006.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2021_02_v024.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2021_03_v003.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>merged_nhpc_2021_04_v004.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_122_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_124_01.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_125_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_126_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_127_01.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_128_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_129_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_130_04.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_133_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_136_01.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_137_02.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                        <geom:SPICE_Kernel_Identification>
                            <geom:kernel_type>CK</geom:kernel_type>
                            <geom:spice_kernel_file_name>nhpc_2021_140_01.bc</geom:spice_kernel_file_name>
                            <geom:kernel_provenance>Predicted</geom:kernel_provenance>
                        </geom:SPICE_Kernel_Identification>
                    </geom:SPICE_Kernel_Files>
                    <geom:Image_Display_Geometry>
                        <Local_Internal_Reference>
                            <local_identifier_reference>data_array</local_identifier_reference>
                            <local_reference_type>display_to_data_object</local_reference_type>
                        </Local_Internal_Reference>
                        <geom:Display_Direction>
                            <geom:horizontal_display_axis>xtrack</geom:horizontal_display_axis>
                            <geom:horizontal_display_direction>Left to Right</geom:horizontal_display_direction>
                            <geom:vertical_display_axis>atrack</geom:vertical_display_axis>
                            <geom:vertical_display_direction>Bottom to Top</geom:vertical_display_direction>
                        </geom:Display_Direction>
                        <geom:Object_Orientation_RA_Dec>
                            <geom:reference_pixel_location>Center</geom:reference_pixel_location>
                            <geom:right_ascension_angle unit="deg">274.7232413307675</geom:right_ascension_angle>
                            <geom:declination_angle unit="deg">-21.35784423851748</geom:declination_angle>
                            <geom:celestial_north_clock_angle unit="deg">262.3566981473393</geom:celestial_north_clock_angle>
                            <geom:Reference_Frame_Identification>
                                <geom:frame_spice_name>J2000</geom:frame_spice_name>
                            </geom:Reference_Frame_Identification>
                        </geom:Object_Orientation_RA_Dec>
                        <geom:Object_Orientation_Clock_Angles>
                            <geom:celestial_north_clock_angle unit="deg">262.3566981473393</geom:celestial_north_clock_angle>
                            <geom:ecliptic_north_clock_angle unit="deg">354.23485935732054</geom:ecliptic_north_clock_angle>
                        </geom:Object_Orientation_Clock_Angles>
                        <geom:Quaternion_Plus_To_From>
                            <geom:qcos>0.6732431746429188</geom:qcos>
                            <geom:qsin1>0.0916500147893187</geom:qsin1>
                            <geom:qsin2>-0.1734229754467548</geom:qsin2>
                            <geom:qsin3>0.7129294314117186</geom:qsin3>
                            <geom:Rotate_From>
                                <geom:name>Instrument</geom:name>
                            </geom:Rotate_From>
                            <geom:Rotate_To>
                                <geom:name>J2000</geom:name>
                            </geom:Rotate_To>
                        </geom:Quaternion_Plus_To_From>
                        <geom:Quaternion_Plus_To_From>
                            <geom:qcos>0.666729356129307</geom:qcos>
                            <geom:qsin1>0.09067215654542525</geom:qsin1>
                            <geom:qsin2>-0.1722976286820616</geom:qsin2>
                            <geom:qsin3>0.7194192469300081</geom:qsin3>
                            <geom:Rotate_From>
                                <geom:name>Spacecraft</geom:name>
                            </geom:Rotate_From>
                            <geom:Rotate_To>
                                <geom:name>J2000</geom:name>
                            </geom:Rotate_To>
                        </geom:Quaternion_Plus_To_From>
                    </geom:Image_Display_Geometry>
                    <geom:Geometry_Orbiter>
                        <geom:geometry_reference_time_utc>2019-01-01T00:01:21.648Z</geom:geometry_reference_time_utc>
                        <geom:geometry_reference_time_tdb unit="s">599572950.8321096</geom:geometry_reference_time_tdb>
                        <geom:Orbiter_Identification>
                            <geom:Geometry_Target_Identification>
                                <geom:body_spice_name>ASTEROID 486958 (2014 MU69)</geom:body_spice_name>
                                <geom:name>ASTEROID 486958 (2014 MU69)</geom:name>
                            </geom:Geometry_Target_Identification>
                        </geom:Orbiter_Identification>
                        <geom:Distances>
                            <geom:Distances_Specific>
                                <geom:spacecraft_geocentric_distance unit="km">6620201636.994308</geom:spacecraft_geocentric_distance>
                                <geom:spacecraft_heliocentric_distance unit="km">6474087120.780692</geom:spacecraft_heliocentric_distance>
                                <geom:spacecraft_target_center_distance unit="km">287581.1118812975</geom:spacecraft_target_center_distance>
                                <geom:target_geocentric_distance unit="km">6620623490.016938</geom:target_geocentric_distance>
                                <geom:target_heliocentric_distance unit="km">6474368757.251996</geom:target_heliocentric_distance>
                            </geom:Distances_Specific>
                        </geom:Distances>
                        <geom:Illumination_Geometry/>
                        <geom:Vectors>
                            <geom:Vectors_Cartesian_Specific>
                                <geom:Vector_Cartesian_Position_Spacecraft_To_Target>
                                    <geom:x_position unit="km">-22525.66368780454</geom:x_position>
                                    <geom:y_position unit="km">266513.5999357428</geom:y_position>
                                    <geom:z_position unit="km">105669.2549211838</geom:z_position>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Position_Spacecraft_To_Target>
                                <geom:Vector_Cartesian_Position_Sun_To_Spacecraft>
                                    <geom:x_position unit="km">-1801853514.78909</geom:x_position>
                                    <geom:y_position unit="km">5789365161.508654</geom:y_position>
                                    <geom:z_position unit="km">2269444642.508496</geom:z_position>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Position_Sun_To_Spacecraft>
                                <geom:Vector_Cartesian_Position_Sun_To_Target>
                                    <geom:x_position unit="km">-1801781095.301896</geom:x_position>
                                    <geom:y_position unit="km">5789657861.18177</geom:y_position>
                                    <geom:z_position unit="km">2269558886.645064</geom:z_position>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Position_Sun_To_Target>
                                <geom:Vector_Cartesian_Position_Earth_To_Spacecraft>
                                    <geom:x_position unit="km">1826743717.661557</geom:x_position>
                                    <geom:y_position unit="km">-5922385017.230049</geom:y_position>
                                    <geom:z_position unit="km">-2327108251.056487</geom:z_position>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Position_Earth_To_Spacecraft>
                                <geom:Vector_Cartesian_Position_Earth_To_Target>
                                    <geom:x_position unit="km">-1828181419.217183</geom:x_position>
                                    <geom:y_position unit="km">5922411243.338773</geom:y_position>
                                    <geom:z_position unit="km">2327112622.923008</geom:z_position>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Position_Earth_To_Target>
                                <geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Target>
                                    <geom:x_velocity unit="km/s">1.113445726473272</geom:x_velocity>
                                    <geom:y_velocity unit="km/s">-13.44300730598812</geom:y_velocity>
                                    <geom:z_velocity unit="km/s">-5.139864239396772</geom:z_velocity>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Target>
                                <geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Sun>
                                    <geom:x_velocity unit="km/s">-5.48373278562833</geom:x_velocity>
                                    <geom:y_velocity unit="km/s">12.10654710345172</geom:y_velocity>
                                    <geom:z_velocity unit="km/s">4.694737612498981</geom:z_velocity>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Sun>
                                <geom:Vector_Cartesian_Velocity_Target_Relative_To_Sun>
                                    <geom:x_velocity unit="km/s">-4.37028705896105</geom:x_velocity>
                                    <geom:y_velocity unit="km/s">-1.336460202247877</geom:y_velocity>
                                    <geom:z_velocity unit="km/s">-0.4451266267813521</geom:z_velocity>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Velocity_Target_Relative_To_Sun>
                                <geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Earth>
                                    <geom:x_velocity unit="km/s">35.33594607665277</geom:x_velocity>
                                    <geom:y_velocity unit="km/s">-7.387470661001551</geom:y_velocity>
                                    <geom:z_velocity unit="km/s">-2.649320625505575</geom:z_velocity>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Velocity_Spacecraft_Relative_To_Earth>
                                <geom:Vector_Cartesian_Velocity_Target_Relative_To_Earth>
                                    <geom:x_velocity unit="km/s">-34.17652442681917</geom:x_velocity>
                                    <geom:y_velocity unit="km/s">-6.301227209591479</geom:y_velocity>
                                    <geom:z_velocity unit="km/s">-2.596910012461239</geom:z_velocity>
                                    <geom:light_time_correction_applied>None</geom:light_time_correction_applied>
                                </geom:Vector_Cartesian_Velocity_Target_Relative_To_Earth>
                            </geom:Vectors_Cartesian_Specific>
                        </geom:Vectors>
                    </geom:Geometry_Orbiter>
                </geom:Geometry>

                <img:Imaging>
                    <Local_Internal_Reference>
                        <local_identifier_reference>data_array</local_identifier_reference>
                        <local_reference_type>imaging_parameters_to_image_object</local_reference_type>
                    </Local_Internal_Reference>
                    <img:Exposure>
                        <img:exposure_duration unit="s">1.521</img:exposure_duration>
                    </img:Exposure>
                    <img:Onboard_Compression>
                        <img:onboard_compression_class>Lossless</img:onboard_compression_class>
                    </img:Onboard_Compression>
                </img:Imaging>

                <sp:Spectral_Characteristics>
                    <Local_Internal_Reference>
                        <local_identifier_reference>data_array</local_identifier_reference>
                        <local_reference_type>spectral_characteristics_to_array_object</local_reference_type>
                    </Local_Internal_Reference>
                    <sp:spectrum_format>3D</sp:spectrum_format>
                    <sp:spectral_bin_type>wavelength</sp:spectral_bin_type>
                    <sp:Observation_Parameters>
                        <sp:number_of_exposures>1</sp:number_of_exposures>
                        <sp:net_integration_time unit="s">1.521</sp:net_integration_time>
                    </sp:Observation_Parameters>
                    <sp:Field_of_View>
                        <sp:description>FOV</sp:description>
                        <sp:Rectangular_FOV>
                            <sp:width_angle unit="deg">0.9</sp:width_angle>
                            <sp:length_angle unit="deg">0.9</sp:length_angle>
                        </sp:Rectangular_FOV>
                    </sp:Field_of_View>
                    <sp:Bin_Description>
                        <sp:bin_profile_description>TBS</sp:bin_profile_description>
                        <sp:Spectral_Lookup>
                            <sp:Bin_Center_Lookup>
                                <Internal_Reference>
                                    <lid_reference>urn:nasa:pds:nh_leisa:calibration_files:wave_map</lid_reference>
                                    <reference_type>spectral_characteristics_to_bin_center_values</reference_type>
                                </Internal_Reference>
                            </sp:Bin_Center_Lookup>
                            <sp:Bin_Width_Lookup>
                                <Internal_Reference>
                                    <lid_reference>urn:nasa:pds:nh_leisa:calibration_files:wave_map</lid_reference>
                                    <reference_type>spectral_characteristics_to_bin_width_values</reference_type>
                                </Internal_Reference>
                            </sp:Bin_Width_Lookup>
                            <sp:comment>The wavelength map ancillary product contains an array of bin
                                center wavelengths and bin widths for each pixel. Each pixel index in
                                the array contains a pair of (bin center, bin width) values in units of
                                microns. This information is also duplicated in the first FITS extension
                                (after the primary HDU) in level 2 LEISA products.
                            </sp:comment>
                        </sp:Spectral_Lookup>
                    </sp:Bin_Description>
                </sp:Spectral_Characteristics>
                
                <sb:SB_Metadata/>
                
                <proc:Processing_Information>
                    <Local_Internal_Reference>
                        <local_identifier_reference>data_file</local_identifier_reference>
                        <local_reference_type>processing_information_to_data_object</local_reference_type>
                    </Local_Internal_Reference>
                    <proc:Process>
                        <proc:name>NH SOC Data Processing Pipeline</proc:name>
                        <proc:process_owner_name>TSOC</proc:process_owner_name>
                        <proc:process_owner_institution_name>Southwest Research Institute</proc:process_owner_institution_name>
                        <proc:Software>
                            <proc:software_id>L1</proc:software_id>
                            <proc:software_version_id>6.4</proc:software_version_id>
                        </proc:Software>
                        <proc:Software>
                            <proc:software_id>L2</proc:software_id>
                            <proc:software_version_id>1.0</proc:software_version_id>
                        </proc:Software>
                    </proc:Process>
                </proc:Processing_Information>
            </Discipline_Area>
        </Observation_Area>
        
        <Reference_List>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_leisa:kem1_raw:lsb_0408606595_0x53c_eng</lid_reference>
                <reference_type>data_to_raw_product</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_leisa:calibration_files:pixel_map_20160824</lid_reference>
                <reference_type>data_to_calibration_product</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_leisa:calibration_files:flat_map_pflat4x</lid_reference>
                <reference_type>data_to_calibration_product</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_leisa:calibration_files:cal_map_pflat4x</lid_reference>
                <reference_type>data_to_calibration_product</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_documents:leisa:leisa_ssr</lid_reference>
                <reference_type>data_to_document</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_documents:mission:payload_ssr</lid_reference>
                <reference_type>data_to_document</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_documents:mission:soc_inst_icd</lid_reference>
                <reference_type>data_to_document</reference_type>
            </Internal_Reference>
        </Reference_List>
        <File_Area_Observational>
            <File>
                <file_name>lsb_0408606595_0x53c_sci.fit</file_name>
                <local_identifier>data_file</local_identifier>
                <creation_date_time>2021-05-23T07:56:33Z</creation_date_time>
                <file_size unit="byte">189800640</file_size>
                <md5_checksum>3eaa4cc63ed4fe9fbe0b22b5333b0477</md5_checksum>
            </File>
            <Header>
                <offset unit="byte">0</offset>
                <object_length unit="byte">25920</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_3D_Spectrum>
                <name>Observational Image</name>
                <local_identifier>data_array</local_identifier>
                <offset unit="byte">25920</offset>
                <axes>3</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>IEEE754MSBSingle</data_type>
                    <scaling_factor>1</scaling_factor>
                    <value_offset>0</value_offset>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>frame</axis_name>
                    <elements>285</elements>
                    <sequence_number>3</sequence_number>
                </Axis_Array>
            </Array_3D_Spectrum>
            <Header>
                <offset unit="byte">74738880</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_3D>
                <name>Per-pixel spectral properties</name>
                <local_identifier>bin_properties</local_identifier>
                <offset unit="byte">74741760</offset>
                <axes>3</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>IEEE754MSBSingle</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>property</axis_name>
                    <elements>2</elements>
                    <sequence_number>3</sequence_number>
                </Axis_Array>
            </Array_3D>
            <Header>
                <offset unit="byte">75268800</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_3D>
                <name>Per-pixel pointing vectors</name>
                <offset unit="byte">75271680</offset>
                <axes>3</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>IEEE754MSBDouble</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>dimension</axis_name>
                    <elements>3</elements>
                    <sequence_number>3</sequence_number>
                </Axis_Array>
            </Array_3D>
            <Header>
                <offset unit="byte">76847040</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_2D>
                <name>Per-pixel flat field corrections</name>
                <offset unit="byte">76849920</offset>
                <axes>2</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>IEEE754MSBSingle</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
            </Array_2D>
            <Header>
                <offset unit="byte">77114880</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_3D>
                <name>Per-pixel gains and offsets</name>
                <offset unit="byte">77117760</offset>
                <axes>3</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>IEEE754MSBSingle</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>quantity</axis_name>
                    <elements>2</elements>
                    <sequence_number>3</sequence_number>
                </Axis_Array>
            </Array_3D>
            <Header>
                <offset unit="byte">77644800</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_3D>
                <name>Per-pxel error estimates</name>
                <offset unit="byte">77647680</offset>
                <axes>3</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>IEEE754MSBSingle</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>frame</axis_name>
                    <elements>285</elements>
                    <sequence_number>3</sequence_number>
                </Axis_Array>
            </Array_3D>
            <Header>
                <offset unit="byte">152360640</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_3D>
                <name>Per-pixel data quality flags</name>
                <offset unit="byte">152363520</offset>
                <axes>3</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>TBS</description>
                <Element_Array>
                    <data_type>SignedMSB2</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>xtrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>atrack</axis_name>
                    <elements>256</elements>
                    <sequence_number>2</sequence_number>
                </Axis_Array>
                <Axis_Array>
                    <axis_name>frame</axis_name>
                    <elements>285</elements>
                    <sequence_number>3</sequence_number>
                </Axis_Array>
            </Array_3D>
            <Header>
                <offset unit="byte">189720000</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Table_Binary>
                <name>Et Quaternion</name>
                <offset unit="byte">189722880</offset>
                <records>285</records>
                <Record_Binary>
                    <fields>5</fields>
                    <groups>0</groups>
                    <record_length unit="byte">36</record_length>
                    <Field_Binary>
                        <name>ET</name>
                        <field_number>1</field_number>
                        <field_location unit="byte">1</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <unit>seconds</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>QUATERNION A</name>
                        <field_number>2</field_number>
                        <field_location unit="byte">5</field_location>
                        <data_type>IEEE754MSBDouble</data_type>
                        <field_length unit="byte">8</field_length>
                        <unit>none</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>QUATERNION X</name>
                        <field_number>3</field_number>
                        <field_location unit="byte">13</field_location>
                        <data_type>IEEE754MSBDouble</data_type>
                        <field_length unit="byte">8</field_length>
                        <unit>none</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>QUATERNION Y</name>
                        <field_number>4</field_number>
                        <field_location unit="byte">21</field_location>
                        <data_type>IEEE754MSBDouble</data_type>
                        <field_length unit="byte">8</field_length>
                        <unit>none</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>QUATERNION Z</name>
                        <field_number>5</field_number>
                        <field_location unit="byte">29</field_location>
                        <data_type>IEEE754MSBDouble</data_type>
                        <field_length unit="byte">8</field_length>
                        <unit>none</unit>
                    </Field_Binary>
                </Record_Binary>
            </Table_Binary>
            <Header>
                <offset unit="byte">189734400</offset>
                <object_length unit="byte">17280</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Table_Binary>
                <name>Housekeeping Table</name>
                <offset unit="byte">189751680</offset>
                <records>414</records>
                <Record_Binary>
                    <fields>75</fields>
                    <groups>0</groups>
                    <record_length unit="byte">115</record_length>
                    <Field_Binary>
                        <name>MET</name>
                        <field_number>1</field_number>
                        <field_location unit="byte">1</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>AcqStart</name>
                        <field_number>2</field_number>
                        <field_location unit="byte">5</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CMDEXE_CNT</name>
                        <field_number>3</field_number>
                        <field_location unit="byte">6</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CMDREJ_CNT</name>
                        <field_number>4</field_number>
                        <field_location unit="byte">7</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>VERSION</name>
                        <field_number>5</field_number>
                        <field_location unit="byte">8</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>STATE</name>
                        <field_number>6</field_number>
                        <field_location unit="byte">9</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MODE</name>
                        <field_number>7</field_number>
                        <field_location unit="byte">10</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>POS_12V</name>
                        <field_number>8</field_number>
                        <field_location unit="byte">11</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>NEG_12V</name>
                        <field_number>9</field_number>
                        <field_location unit="byte">13</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>POS_5V</name>
                        <field_number>10</field_number>
                        <field_location unit="byte">15</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>NEG_5V</name>
                        <field_number>11</field_number>
                        <field_location unit="byte">17</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>POS_30V</name>
                        <field_number>12</field_number>
                        <field_location unit="byte">19</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MVIC_TEMP</name>
                        <field_number>13</field_number>
                        <field_location unit="byte">21</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_TEMP</name>
                        <field_number>14</field_number>
                        <field_location unit="byte">23</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DE_NOT_DONE</name>
                        <field_number>15</field_number>
                        <field_location unit="byte">25</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>EEPTAB</name>
                        <field_number>16</field_number>
                        <field_location unit="byte">26</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>SPARE0</name>
                        <field_number>17</field_number>
                        <field_location unit="byte">27</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>PPS</name>
                        <field_number>18</field_number>
                        <field_location unit="byte">28</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>SIDE</name>
                        <field_number>19</field_number>
                        <field_location unit="byte">29</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>WDT_EXP</name>
                        <field_number>20</field_number>
                        <field_location unit="byte">30</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RLY_ERR</name>
                        <field_number>21</field_number>
                        <field_location unit="byte">31</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>OPCODE</name>
                        <field_number>22</field_number>
                        <field_location unit="byte">32</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>XMT_AFF</name>
                        <field_number>23</field_number>
                        <field_location unit="byte">33</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>XMT_FF</name>
                        <field_number>24</field_number>
                        <field_location unit="byte">34</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RCV1_OVRN</name>
                        <field_number>25</field_number>
                        <field_location unit="byte">35</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RCV1_AFF</name>
                        <field_number>26</field_number>
                        <field_location unit="byte">36</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RCV1_FF</name>
                        <field_number>27</field_number>
                        <field_location unit="byte">37</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RCV2_OVRN</name>
                        <field_number>28</field_number>
                        <field_location unit="byte">38</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RCV2_AFF</name>
                        <field_number>29</field_number>
                        <field_location unit="byte">39</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RCV2_FF</name>
                        <field_number>30</field_number>
                        <field_location unit="byte">40</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>EE_WEN</name>
                        <field_number>31</field_number>
                        <field_location unit="byte">41</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>IEM_ACTIVE</name>
                        <field_number>32</field_number>
                        <field_location unit="byte">42</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>IEM_SELECT</name>
                        <field_number>33</field_number>
                        <field_location unit="byte">43</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>WDT_EN</name>
                        <field_number>34</field_number>
                        <field_location unit="byte">44</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RLY_BSY</name>
                        <field_number>35</field_number>
                        <field_location unit="byte">45</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>SPARE1</name>
                        <field_number>36</field_number>
                        <field_location unit="byte">46</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>EXP_CNT</name>
                        <field_number>37</field_number>
                        <field_location unit="byte">47</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>FPGA_VER</name>
                        <field_number>38</field_number>
                        <field_location unit="byte">48</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>OSC_CNT</name>
                        <field_number>39</field_number>
                        <field_location unit="byte">49</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>TDI_RATE</name>
                        <field_number>40</field_number>
                        <field_location unit="byte">51</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>FRAME_RATE</name>
                        <field_number>41</field_number>
                        <field_location unit="byte">53</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MEMDP_STATE</name>
                        <field_number>42</field_number>
                        <field_location unit="byte">55</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MEMLD_STATE</name>
                        <field_number>43</field_number>
                        <field_location unit="byte">56</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DRAM_WIN</name>
                        <field_number>44</field_number>
                        <field_location unit="byte">57</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DE_FPGA</name>
                        <field_number>45</field_number>
                        <field_location unit="byte">58</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DISCRETE</name>
                        <field_number>46</field_number>
                        <field_location unit="byte">59</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GRP_RLY3</name>
                        <field_number>47</field_number>
                        <field_location unit="byte">60</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GRP_RLY2</name>
                        <field_number>48</field_number>
                        <field_location unit="byte">61</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GRP_RLY1</name>
                        <field_number>49</field_number>
                        <field_location unit="byte">62</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DE_SEL_RLY</name>
                        <field_number>50</field_number>
                        <field_location unit="byte">63</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GO_STATE</name>
                        <field_number>51</field_number>
                        <field_location unit="byte">64</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CODE</name>
                        <field_number>52</field_number>
                        <field_location unit="byte">65</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>TABLE_AREA</name>
                        <field_number>53</field_number>
                        <field_location unit="byte">66</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MVIC_VRD</name>
                        <field_number>54</field_number>
                        <field_location unit="byte">67</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MVIC_VOD</name>
                        <field_number>55</field_number>
                        <field_location unit="byte">69</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MVIC_VOG</name>
                        <field_number>56</field_number>
                        <field_location unit="byte">71</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>MVIC_BSPAR</name>
                        <field_number>57</field_number>
                        <field_location unit="byte">73</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_VRST</name>
                        <field_number>58</field_number>
                        <field_location unit="byte">75</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_VDDA</name>
                        <field_number>59</field_number>
                        <field_location unit="byte">77</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_DSUB</name>
                        <field_number>60</field_number>
                        <field_location unit="byte">79</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_GATE</name>
                        <field_number>61</field_number>
                        <field_location unit="byte">81</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_BSPAR</name>
                        <field_number>62</field_number>
                        <field_location unit="byte">83</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>RPT_SHFTRTE</name>
                        <field_number>63</field_number>
                        <field_location unit="byte">85</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>SHFTRTE_OFF</name>
                        <field_number>64</field_number>
                        <field_location unit="byte">89</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>OBS_TABLE</name>
                        <field_number>65</field_number>
                        <field_location unit="byte">93</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_OFF1</name>
                        <field_number>66</field_number>
                        <field_location unit="byte">94</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_OFF2</name>
                        <field_number>67</field_number>
                        <field_location unit="byte">96</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_OFF3</name>
                        <field_number>68</field_number>
                        <field_location unit="byte">98</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>LEISA_OFF4</name>
                        <field_number>69</field_number>
                        <field_location unit="byte">100</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CDH_THERM</name>
                        <field_number>70</field_number>
                        <field_location unit="byte">102</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DE_SPARE_50</name>
                        <field_number>71</field_number>
                        <field_location unit="byte">104</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>DE_SPARE_51</name>
                        <field_number>72</field_number>
                        <field_location unit="byte">106</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>ANA_GRND</name>
                        <field_number>73</field_number>
                        <field_location unit="byte">108</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CHECKSUM</name>
                        <field_number>74</field_number>
                        <field_location unit="byte">110</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CalcChecksum</name>
                        <field_number>75</field_number>
                        <field_location unit="byte">112</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                </Record_Binary>
            </Table_Binary>
        </File_Area_Observational>
    </Product_Observational>
