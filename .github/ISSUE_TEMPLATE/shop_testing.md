---
name: Shop Testing Checklist
about: A checklist for in house testing
title: 'Shop Testing Checklist'
labels: ''
assignees: ''

---
## Shop Testing Checklist - "System Name"

### Admin

- [ ] Confirm that all gear required for testing is in the shop
- [ ] Inform PM of any gear that has been erroneously shipped to site.  This includes any/all peripherals required for complete system testing (touch panels/transmitters/receivers/mics/cameras)  
- [ ] Review equipment rack for proper cable/equipment labeling  
- [ ] Review drawings to ensure that all fabrication punches have been cleared/implemented by Engineering  
- [ ] Review completed and approved IT workbook and put into GitHub  
- [ ] Review project scope of work  
- [ ] Review programming scope of work and approved GUI screenshots  
- [ ] Inform programmer of proposed schedule for In House testing to confirm availability  

### Device/Network Configuration

- [ ] Update all firmware to latest approved release
- [ ] Set IP addresses and host-names of all equipment according to IT Workbook
- [ ] If all networking is internal, verify IT workbook conforms to published standards
- [ ] Record all serial numbers/mac addresses in IT Workbook
- [ ] Set IPID's for all touch panels
- [ ] If necessary, request iPad gift certificates and set up iTunes account
- [ ] Download and license Crestron application on new iPad's
- [ ] Disable energy efficient Ethernet on switch
- [ ] Review and familiarize yourself with any new gear.  Assume that you may be called upon to assist      in onsite configuration of specialty gear (video wall processors, signage players, etc)

### Video Testing

- [ ] Test video routing from all inputs/outputs with Transmitters and Receivers at highest possible video resolution (test 4k if there is 4k gear)
- [ ] Set EDID table on video switcher
- [ ] All inputs and outputs on Video Switch physically labelled and labelled in software
- [ ] HDCP Sources tested (MAC's)
- [ ] All scalers configured to enable scaling and scale to native resolution of connected displays
- [ ] Any wireless presentation devices are configured per client documentation (if none is provided request from PM)
- [ ] Wireless presentation tested with all possible devices (laptop, IOS, android)

### Audio Testing

- [ ] Load DSP files
- [ ] Review amplifier specification to ensure that output blocks will not clip amplifier 
    1. [Biamp Guide](https://support.biamp.com/General/Audio/Gain_structure%3A_input_and_output_levels)
- [ ] Connect all microphones and set gain appropriately
- [ ] Add any manufacturer recommended mic settings to DSP
    1. [Tesira <-> Shure](https://support.biamp.com/Tesira/Miscellaneous/Using_the_Shure_MXA910_microphone_array_with_Tesira)
- [ ] Configure any Dante routes/switch settings as required
- [ ] Set NOM and Decay time on any Automixers
- [ ] Ensure a test generator has been added to DSP file
- [ ] Ensure meters have been added to all inputs and output and that Hold Time is set properly
- [ ] Check that input levels on all sources is appropriate
- [ ] Set levels and mute appropriately in system shutdown and startup presets
- [ ] Make sure amplifier channels are physically labelled
- [ ] Pair and label any wireless microphones and verify wireless frequencies for installed location
- [ ] Connect DSP to test phone line and perform a test call

### Video Conferencing

- [ ] Configure video conferencing codec per client provided specifications (if none have been provided, request from PM)
- [ ] Verify input/output audio levels and settings from codec
- [ ] Disable any unused codec features(proximity mode etc.)
- [ ] Make test calls with PPI Zoom meeting
- [ ] Test content presentation from all available sources
- [ ] If client is to configure onsite, make note of all settings used during successful testing so that they may be applied once client has configured the codec
- [ ] Save codec settings to a file locally

### Control

- [ ] Load all Control and Configuration files to the processor
- [ ] Load touch panel files to all touch panels
- [ ] Load iPad files to processor
- [ ] Verify time/timezone is correct on control processor
- [ ] If Crestron disable cloud status
- [ ] If using control subnet, set to manual and configure subnet for 192.168.1.0/24 (must verify does not conflict with client LAN)
- [ ] Review entire GUI for any text errors or misspellings
- [ ] Verify all source routing
- [ ] Verify all audio control
- [ ] Verify shutdown and startup audio presets are being properly recalled
- [ ] Verify mic mute logic and color is synced across all devices
- [ ] Verify all video displays route to correct source at shutdown (usually none)
- [ ] Test all startup presets route correct source
- [ ] Test all other device control as needed
- [ ] Any room combining/overflow scenarios should be extensively tested with both video and audio present
- [ ] Reboot rack to ensure that system boots up in a usable state
- [ ] Review error log and resolve any non-Crestron related errors

### Documentation

- [ ] Ensure any rack changes are punched in Plan Grid
- [ ] Document all serial number, MAC addresses, and hostnames in IT Workbook
- [ ] Save any additional configuration files (RoomConfig.json, Switch, VTC, WAP) in a config folder labelled by room/systems in the repository
- [ ] Ensure any externally configured devices have be physically labelled so they may be installed properly in the field
- [ ] Add notes to Fabrication Test Notes section in Project wiki.  The following information is most pertinent:
    1. Equipment missing or untested
    2. Custom equipment configuration information (video wall processors, signage, etc.)
    3. General notes or information for Field Engineer in the field
- [ ] Email summary of testing to Integration Manager, Project Programmer, and Field Engineer
- [ ] After the summary is reviewed, the Project Programmer will give approval.  Once given, inform PM/Fabrication Manager of shop testing completion.