New Horizons Mission Namespace Outline
##################################################

*<nh:Mission_Parameters>* is the public entry point to the New Horizons Mission 
namespace. This class contains all other NH classes and must be included to gain
access to them. Below is a summary outline of all classes and attributes 
currently available in the NH mission dictionary, in the order in which they 
would appear in a label if every single one was used. 

Note that there are no real cases in which every single mission class and 
attribute would appear in a single label. The point of this outline is primarily
to catalog what is present and show the required ordering within classes when
they are included in a label.

::

  <nh:Mission_Parameters>
      <nh:mission_phase_name>
      
      <nh:Observation_Parameters>
          <nh:telemetry_apid>
          <nh:sequence_id>
          <nh:observation_description>
          
          <nh:Mission_Elapsed_Time>
              <nh:clock_parition>
              <nh:start_clock_count>
              <nh:stop_clock_count>
          
          <nh:Detector>
              <nh:detector_name>
              <nh:detector_type>
              
              <nh:Alice_Details>
                  <nh:aperture>
                  <nh:door_position>
              
              <nh:Ralph_Details>
                  <nh:met510>
                  <nh:hk_packet_is_real>
              
              <nh:LEISA_Details>
                  <nh:scan_type>
                  <nh:leisa_mode>
                  <nh:leisa_offset_1>
                  <nh:leisa_offset_2>
                  <nh:leisa_offset_3>
                  <nh:leisa_offset_4>
                  <nh:leisa_rate>
                  <nh:leisa_side>
                  <nh:leisa_temperature>

              <nh:MVIC_Details>
                  <nh:scan_type>
                  <nh:tdi_rate>
              
              <nh:SWAP_Details>
                  <nh:sweep_samples_count>
          
          <nh:Spacecraft_State>
              <nh:thruster_x_enabled>
              <nh:thruster_y_enabled>
              <nh:thruster_z_enabled>
              <nh:gc_scan_rate>
              <nh:target_motion_rate>
              <nh:relative_control_mode_active>
              <nh:pointing_method>
              <nh:spacecraft_spin_state>

      <nh:MVIC_Calibration_Information>
          <nh:physical_pixel_size>
          <nh:read_noise>
          <nh:gain>
          <nh:tdi_median_bias_level>
          
          <nh:Framing_Biases>
              <nh:Frame_Bias_Levels>
                  <nh:frame_number>
                  <nh:left_side_median_bias>
                  <nh:right_side_median_bias>
      
      <nh:Radiometric_Conversion_Constants>
          <nh:pivot_wavelength>
          
          <nh:Resolved_Source>
              <nh:units_of_conversion_constants>
              <nh:solar_constant>
              <nh:jupiter_constant>
              <nh:pholus_constant>
              <nh:pluto_constant>
              <nh:charon_constant>
              <nh:arrokoth_constant>
          
          <nh:Unresolved_Source>
              <nh:units_of_conversion_constants>
              <nh:solar_constant>
              <nh:jupiter_constant>
              <nh:pholus_constant>
              <nh:pluto_constant>
              <nh:charon_constant>
              <nh:arrokoth_constant>
    
      <nh:REX_Radiometry_Information>
          <nh:frame_data_source>
          <nh:agc_gain_setting>
          <nh:agc_setting_source>
          <nh:agc_gain_provenance>
          <nh:base_agc_gain>
          <nh:base_power>
          <nh:radio_bandwidth>
          <nh:radiometry_response_step>
          <nh:radiometry_response_offset>
          <nh:iq_calibration_constant>
          <nh:time_tag_calibration_constant>
