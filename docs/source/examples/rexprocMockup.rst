Mockup Label: REX ApID 0x7B1, Processed Data
##################################################

This label is a mockup created for design purposes. The data file
it describes contains processed data REX radio output frame data with
ApID 0x7B1.

The mockup shows the entire *<Product_Observational>* structure
including the New Horizons dictionary classes, which are found in the
*<Mission_Area>* of the structure. It is a valid label, except for the
specified path/location of the mission dictionary .xsd file, which should
be updated prior to attempting to validate it.

  **Note** that the New Horizons (nh:) and Small Bodies (sb:) dictionaries are in 
  active development. Consult the current release documentation for changes
  to these namespaces-in-development before attempting and real-would applications,
  or the Github repo for latest development versions. 

.. code-block:: XML
    
    <Product_Observational
        xmlns="http://pds.nasa.gov/pds4/pds/v1"
        xmlns:disp="http://pds.nasa.gov/pds4/disp/v1"
        xmlns:geom="http://pds.nasa.gov/pds4/geom/v1"
        xmlns:nh="http://pds.nasa.gov/pds4/mission/nh/v1"
        xmlns:sb="http://pds.nasa.gov/pds4/sb/v1"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://pds.nasa.gov/pds4/pds/v1 https://pds.nasa.gov/pds4/pds/v1/PDS4_PDS_1J00.xsd
                            http://pds.nasa.gov/pds4/geom/v1 https://pds.nasa.gov/pds4/geom/v1/PDS4_GEOM_1J00_1960.xsd
                            http://pds.nasa.gov/pds4/sb/v1 https://pds.nasa.gov/pds4/sb/v1/PDS4_SB_1J00_1000.xsd
                            http://pds.nasa.gov/pds4/mission/nh/v1 https://pds.nasa.gov/pds4/mission/nh/v1/PDS4_NH_1L00_1000.xsd">
        
        <Identification_Area>
            <logical_identifier>urn:nasa:pds:nh_rex:kem1_cal:rex_0408622814_0x7b1_sci</logical_identifier>
            <version_id>1.0</version_id>
            <title>REX Calibrated Data Product: rex_0408622814_0x7b1_sci</title>
            <information_model_version>1.19.0.0</information_model_version>
            <product_class>Product_Observational</product_class>
        </Identification_Area>
    
        <Observation_Area>
            <Time_Coordinates>
                <start_date_time>2019-01-01T04:28:16.148378Z</start_date_time>
                <stop_date_time>2019-01-01T04:28:17.172378Z</stop_date_time>
            </Time_Coordinates>
    
            <Primary_Result_Summary>
                <purpose>Science</purpose>
                <processing_level>Calibrated</processing_level>
                <Science_Facets>
                    <wavelength_range>Radio</wavelength_range>
                    <discipline_name>Radio Science</discipline_name>
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
                    <name>REX</name>
                    <type>Instrument</type>
                    <description>Radio Science Experiment</description>
                    <Internal_Reference>
                        <lid_reference>urn:nasa:pds:context:instrument:nh.rex</lid_reference>
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
                        <nh:telemetry_apid>0x7b1</nh:telemetry_apid>
                        <nh:sequence_id>KERX_MU69_CA03-TEMP_REX_2019001__RADIOMETRIC</nh:sequence_id>
                        <nh:observation_description>Radiometric Measurement</nh:observation_description>
                        <nh:Mission_Elapsed_Time>
                            <nh:clock_partition>3</nh:clock_partition>
                            <nh:start_clock_count>0408622814:00000</nh:start_clock_count>
                            <nh:stop_clock_count>0408622815:01200</nh:stop_clock_count>
                        </nh:Mission_Elapsed_Time>
                        <nh:Detector>
                            <nh:detector_name>Radio Science Experiment</nh:detector_name>
                            <nh:detector_type>Local oscillator vs. uplink signal phase comparator</nh:detector_type>
                        </nh:Detector>
                        <nh:Spacecraft_State>
                            <nh:pointing_method>CB1</nh:pointing_method>
                            <nh:spacecraft_spin_state>3-Axis</nh:spacecraft_spin_state>
                        </nh:Spacecraft_State>
                    </nh:Observation_Parameters>
                    
                    <nh:REX_Radiometry_Information>
                        <nh:frame_data_source>0x00</nh:frame_data_source>
                        <nh:agc_gain_setting>169.0</nh:agc_gain_setting>
                        <nh:agc_setting_source>ULCMD</nh:agc_setting_source>
                        <nh:agc_gain_provenance>18359.ssf:KERX_MU69_CA03-TEMP_REX_2019001__RADIOMETRIC$</nh:agc_gain_provenance>
                        <nh:base_agc_gain>167.0</nh:base_agc_gain>
                        <nh:base_power unit="dBm">-176.852</nh:base_power>
                        <nh:radio_bandwidth unit="MHz">4.5</nh:radio_bandwidth>
                        <nh:radiometry_response_step unit="dBm">-0.475</nh:radiometry_response_step>
                        <nh:radiometry_response_offset unit="dBm">-101.03</nh:radiometry_response_offset>
                        <nh:iq_calibration_constant unit="mV">0.1221</nh:iq_calibration_constant>
                        <nh:time_tag_calibration_constant unit="s">0.1024</nh:time_tag_calibration_constant>
                    </nh:REX_Radiometry_Information>
                
                </nh:Mission_Parameters>
            </Mission_Area>
    
            <Discipline_Area>
                <geom:Geometry/>
                <sb:SB_Metadata/>
                <!-- etc. -->
            </Discipline_Area>
        
        </Observation_Area>
    
        <Reference_List>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_rex:kem1_raw:rex_0408622814_0x7b1_eng</lid_reference>
                <reference_type>data_to_raw_product</reference_type>
            </Internal_Reference>
            <Internal_Reference>
                <lid_reference>urn:nasa:pds:nh_documents:rex:rex_ssr</lid_reference>
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
            <!-- other references as relevant -->
        </Reference_List>
        
        <File_Area_Observational>
            <File>
                <file_name>rex_0408622814_0x7b1_sci.fit</file_name>
                <local_identifier>data_file</local_identifier>
                <creation_date_time>2021-05-27T05:33:26Z</creation_date_time>
                <file_size unit="byte">86400</file_size>
                <md5_checksum>a394985fbe64075d1ca21952878ca529</md5_checksum>
            </File>
            <Header>
                <offset unit="byte">0</offset>
                <object_length unit="byte">23040</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_1D>
                <name>REX Output Frame</name>
                <local_identifier>ROF</local_identifier>
                <offset unit="byte">23040</offset>
                <axes>1</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <Element_Array>
                    <data_type>UnsignedByte</data_type>
                    <scaling_factor>1</scaling_factor>
                    <value_offset>0</value_offset>
                </Element_Array>
                <Axis_Array>
                    <axis_name>bytestream</axis_name>
                    <elements>5088</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
            </Array_1D>
            <Header>
                <offset unit="byte">28800</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Table_Binary>
                <name>In-Phase/Quadrature-Phase Values</name>
                <offset unit="byte">31680</offset>
                <records>1250</records>
                <Record_Binary>
                    <fields>2</fields>
                    <groups>0</groups>
                    <record_length unit="byte">8</record_length>
                    <Field_Binary>
                        <name>I Value</name>
                        <field_number>1</field_number>
                        <field_location unit="byte">1</field_location>
                        <data_type>IEEE754MSBSingle</data_type>
                        <field_length unit="byte">4</field_length>
                        <unit>mV</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>Q Value</name>
                        <field_number>2</field_number>
                        <field_location unit="byte">5</field_location>
                        <data_type>IEEE754MSBSingle</data_type>
                        <field_length unit="byte">4</field_length>
                        <unit>mV</unit>
                    </Field_Binary>
                </Record_Binary>
            </Table_Binary>
            <Header>
                <offset unit="byte">43200</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Table_Binary>
                <name>Radiometer &amp; Time Tags</name>
                <offset unit="byte">46080</offset>
                <records>10</records>
                <Record_Binary>
                    <fields>3</fields>
                    <groups>0</groups>
                    <record_length unit="byte">12</record_length>
                    <Field_Binary>
                        <name>Radiometer</name>
                        <field_number>1</field_number>
                        <field_location unit="byte">1</field_location>
                        <data_type>IEEE754MSBSingle</data_type>
                        <field_length unit="byte">4</field_length>
                        <unit>dBm</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>Time Tag</name>
                        <field_number>2</field_number>
                        <field_location unit="byte">5</field_location>
                        <data_type>IEEE754MSBSingle</data_type>
                        <field_length unit="byte">4</field_length>
                        <unit>s</unit>
                    </Field_Binary>
                    <Field_Binary>
                        <name>Quality flag</name>
                        <field_number>3</field_number>
                        <field_location unit="byte">9</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                    </Field_Binary>
                </Record_Binary>
            </Table_Binary>
            <Header>
                <offset unit="byte">48960</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Table_Binary>
                <name>Housekeeping (0x004)</name>
                <offset unit="byte">51840</offset>
                <records>1</records>
                <Record_Binary>
                    <fields>3</fields>
                    <groups>0</groups>
                    <record_length unit="byte">7</record_length>
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
                        <name>CDH_PLL_OPEN_CLOSED_LOOP_1</name>
                        <field_number>2</field_number>
                        <field_location unit="byte">5</field_location>
                        <data_type>UnsignedByte</data_type>
                        <field_length unit="byte">1</field_length>
                    </Field_Binary>
                    <Field_Binary>
                        <name>CDH_PLL_AGCV_1</name>
                        <field_number>3</field_number>
                        <field_location unit="byte">6</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                </Record_Binary>
            </Table_Binary>
            <Header>
                <offset unit="byte">54720</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Header>
                <offset unit="byte">57600</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Header>
                <offset unit="byte">60480</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Header>
                <offset unit="byte">63360</offset>
                <object_length unit="byte">11520</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Table_Binary>
                <name>Thrusters</name>
                <offset unit="byte">74880</offset>
                <records>45</records>
                <Record_Binary>
                    <fields>28</fields>
                    <groups>0</groups>
                    <record_length unit="byte">110</record_length>
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
                        <name>GC1_SH_VERNIER</name>
                        <field_number>2</field_number>
                        <field_location unit="byte">5</field_location>
                        <data_type>SignedMSB2</data_type>
                        <field_length unit="byte">2</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>32768</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_DATA_VALID_MET</name>
                        <field_number>3</field_number>
                        <field_location unit="byte">7</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_0</name>
                        <field_number>4</field_number>
                        <field_location unit="byte">11</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_1</name>
                        <field_number>5</field_number>
                        <field_location unit="byte">15</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_2</name>
                        <field_number>6</field_number>
                        <field_location unit="byte">19</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_3</name>
                        <field_number>7</field_number>
                        <field_location unit="byte">23</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_4</name>
                        <field_number>8</field_number>
                        <field_location unit="byte">27</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_5</name>
                        <field_number>9</field_number>
                        <field_location unit="byte">31</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_6</name>
                        <field_number>10</field_number>
                        <field_location unit="byte">35</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_7</name>
                        <field_number>11</field_number>
                        <field_location unit="byte">39</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_8</name>
                        <field_number>12</field_number>
                        <field_location unit="byte">43</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_9</name>
                        <field_number>13</field_number>
                        <field_location unit="byte">47</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_10</name>
                        <field_number>14</field_number>
                        <field_location unit="byte">51</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_11</name>
                        <field_number>15</field_number>
                        <field_location unit="byte">55</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_12</name>
                        <field_number>16</field_number>
                        <field_location unit="byte">59</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_13</name>
                        <field_number>17</field_number>
                        <field_location unit="byte">63</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_14</name>
                        <field_number>18</field_number>
                        <field_location unit="byte">67</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_15</name>
                        <field_number>19</field_number>
                        <field_location unit="byte">71</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_16</name>
                        <field_number>20</field_number>
                        <field_location unit="byte">75</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_17</name>
                        <field_number>21</field_number>
                        <field_location unit="byte">79</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_18</name>
                        <field_number>22</field_number>
                        <field_location unit="byte">83</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_19</name>
                        <field_number>23</field_number>
                        <field_location unit="byte">87</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_20</name>
                        <field_number>24</field_number>
                        <field_location unit="byte">91</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_21</name>
                        <field_number>25</field_number>
                        <field_location unit="byte">95</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_22</name>
                        <field_number>26</field_number>
                        <field_location unit="byte">99</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_23</name>
                        <field_number>27</field_number>
                        <field_location unit="byte">103</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                    <Field_Binary>
                        <name>GC1_RCS_FIRE_MINOR_24</name>
                        <field_number>28</field_number>
                        <field_location unit="byte">107</field_location>
                        <data_type>SignedMSB4</data_type>
                        <field_length unit="byte">4</field_length>
                        <scaling_factor>1</scaling_factor>
                        <value_offset>2147483648</value_offset>
                    </Field_Binary>
                </Record_Binary>
            </Table_Binary>
            <Header>
                <offset unit="byte">80640</offset>
                <object_length unit="byte">2880</object_length>
                <parsing_standard_id>FITS 4.0</parsing_standard_id>
            </Header>
            <Array_1D>
                <name>SSR Sector Headers</name>
                <offset unit="byte">83520</offset>
                <axes>1</axes>
                <axis_index_order>Last Index Fastest</axis_index_order>
                <description>[TBD]</description>
                <Element_Array>
                    <data_type>UnsignedByte</data_type>
                </Element_Array>
                <Axis_Array>
                    <axis_name>NAXIS1</axis_name>
                    <elements>336</elements>
                    <sequence_number>1</sequence_number>
                </Axis_Array>
            </Array_1D>
        </File_Area_Observational>
    
    </Product_Observational>
    