# Note 8 & Galaxy s8 Low Temp Charging Bypass

Simple Magisk module that bypasses the "temperature too low" charging pause on the Samsung Galaxy Note 8.

Made for people who want to remove the wireless charging coil or who have a broken temprature sensor like me inside their note 8 and get annoyed when it refuses to charge even though its not dangerous, i created this as i was building a "gaming phone" project and my phone i was using was already damanged.

### Compatibility
- **Primary**: Galaxy Note 8 (SM-N950F / SM-N950N / SM-N950FD)
- **Possibly**: Galaxy S8 / S8+ (same generation battery driver)
- **Will NOT work** on newer Samsung phones (especially past 2018) or any other brands

### Requirements
- Magisk (v20.4+)
- Rooted Note 8 or samsung galaxy s8

### Installation
1. Download the latest release zip
2. Flash it in Magisk Manager → Modules → Install from storage
3. Reboot
4. Done

The module applies the bypass a few seconds after boot and re-applies it a couple more times just to be safe.

### What it does
Writes to these nodes:
- `/sys/class/power_supply/battery/batt_tune_temp_low_normal`
- `/sys/class/power_supply/battery/batt_tune_temp_low_rec_normal`
- `/sys/class/power_supply/battery/batt_temp_table`

This lowers the temperature threshold so the phone will charge even when it thinks it's too cold.

### Warning
Use at your own risk.  
Charging a lithium battery when it's very cold can still damage it over time. This module only removes Samsung's software block — it doesn't make physics go away.

I'm not responsible if your battery swells, dies early, or anything else. You flashed it, you own it.
I hope this helps you because it took me a week to develop this solution for this very neiche issue. 
You do require a rooted phone for this!! otherwise it cant write to the nodes in the restricted area.

### Credits
Made by AutisticFloppa. 

### Changelog
**v1.1**
- Initial public release
