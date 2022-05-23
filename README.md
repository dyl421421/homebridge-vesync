# homebridge-vesync

[Homebridge](https://github.com/nfarina/homebridge) platform plugin for Etekcity Wifi Smart Plugs
https://www.amazon.com/dp/B01M3MYIFS/

This plugin uses the existing VeSync app infrastructure to allow you to control your Etekcity smart plugs.

Provide your username and password and register as a platform, and it will auto-detect the plugs you have registered.

Power usage data is not synced over, but is still available in the Vesync app.

# Installation

1. Install homebridge using: npm install -g homebridge
2. Install this plugin using: npm install -g homebridge-vesync
3. Update your configuration file. See below for a sample.

# Configuration

Configuration sample:

 ```
        "platforms": [
          {
            "platform": "VesyncPlug",
            "name": "VesyncPlug",
            "username": "***",
            "password": "***",
            "exclude": "deviceId1,deviceId2"
          }
        ]
```
## Optional parameters

- debug, this will enable more logging information from the plugin

  "debug": "True"
- exclude, this will exclude devices with given IDs from showing in the home
  
  "exclude": "7af4d35-23fac3243212312,7af4d35-23fac3243212315"

## Credits

- AlakhaiVaynard   - Inital Code
- KaidenR - Bug Fix, Issue #1
- rossmckelvie - Code Improvements, Bug Fix Issue #3
- Danimal4326 / NorthernMan54  - Used [homebridge-ecoplug](https://github.com/NorthernMan54/homebridge-ecoplug) as a template for platform registration and required operations for on/off
- dirwin517 / keatontaylor - Used [etekcity-smartplug](https://github.com/arupex/etekcity-smartplug) as a template for sending the commands to vesync to control the outlet
- micktron - Updated api to version 2, added support for ESO15-TB
- dyl421421 - added exclusion list to limit devices shown in the home app