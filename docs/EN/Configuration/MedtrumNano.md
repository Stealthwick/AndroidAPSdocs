# Medtrum Nano

## Outline (to be removed later)

Do mention pump type (nano) as less as possible as we want to support other pump models as well in the future

- Pump capabilities with AAPS
    - Automatic DST and timezone change
    - Temp Basal Rate
    - Bolus and SMB
    - etc
- Hardware and Software Requirements
    > PumpBase with ref: 
        > For other refs contact us @Discord
- Before you begin
    - Patch session is coupled to AAPS, cannot be used with PDM or Official medtrum app
    - Your pump will not stop delivering insulin when it is not connected to AAPS
    - See dash page
- Setup
    - Enable driver
        > Setup wizard
        > Config builder
    - Medtrum configuration
        > MUST enter SN (only change this when no patch is activated!)
        > Refer to <Settings> below
    - Activate patch
    - Deactivate patch
- Medtrum TAB
    - Fields
    - Buttons
        > Refresh
        > Reset Alarms
        > Change patch
- Medtrum Settings
    - Serial Number
    - Patch expiration
    - Alarm Settings
    - Hourly Maximum Insulin
    - Daily Maximum Insulin
- Actions (ACT) Tab
    > Copy from dash?
- Troubleshooting
    > Activation interrupted
    > Preventing Occlusions and patch faults
        > Make sure pump base is properly seated
        > Do not try to fill the patch to the maximum
- Where to get help
    > Needed? Copy from dash?

## Pump capabilities with AAPS
* Automatic DST and timezone handling
* All loop functionality support (Bolus + Temporary basal)
* Extended bolus not support by AAPS driver

## Hardware and Software Requirements
* **Compatible Android phone** with a BLE Bluetooth connection 
    - See AAPS requirements (TODO Link)
* **Compatible Medtrum pumpbase and patches**
    - Currently Medtrum Nano pumpbase refs: **MD0201** and **MD8201** are supported. If you have an unsupported model and can donate the hardware or you can help with testing contact us at discord (TODO: Hyperlink) for support.

## Before you begin

**SAFETY FIRST** Do not attempt this process in an environment where you cannot recover from an error (extra pods, insulin, and phone devices are must-haves).

**The PDM and Medtrum App will not work with a patch that is activated by AAPS.**
Previously you used your PDM or Medtrum app to send commands to your pump. For security reasons you can only use the activated patch with the device you have activated it.

*This does NOT mean you should throw away your PDM, it is recommended to keep it around as a backup and for emergencies, for instance when your phone gets lost or AAPS is not working correctly.*

**Your pump will not stop delivering insulin when it is not connected to AAPS**
Default basal rates are programmed on the pump on activation as defined in the current active profile.
As long as AAPS is operational it will send basal rate commands that run for a maximum of 120 minutes. When for some reason the pod does not receive any new commands (for instance because communication was lost due to Pod - phone distance) the pump will automatically fall back to default basal rates.

**30 min Basal Rate Profiles are NOT supported in AAPS.**
**The AAPS Profile does not support a 30 minute basal rate time frame**
If you are new to AAPS and are setting up your basal rate profile for the first time, please be aware that basal rates starting on a half-hour basis are not supported, and you will need to adjust your basal rate profile to start on the hour. For example, if you have a basal rate of 1.1 units which starts at 09:30 and has a duration of 2 hours ending at 11:30, this will not work. You will need to change this 1.1 unit basal rate to a time range of either 9:00-11:00 or 10:00-12:00. Even though the Medtrum pump hardware itself supports the 30 min basal rate profile increments, AAPS is not able to take them into account with its algorithms currently.

**0U/h profile basal rates are NOT supported in AAPS**
While the Medtrum pump does support a zero basal rate, since AAPS uses multiples of the profile basal rate to determine automated treatment it cannot function with a zero basal rate. A temporary zero basal rate can be achieved through the "Disconnect pump" function or through a combination of Disable Loop/Temp Basal Rate or Suspend Loop/Temp Basal Rate. 

