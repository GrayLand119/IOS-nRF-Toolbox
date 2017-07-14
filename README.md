# IOS-nRF-Toolbox

Modify DFU moudle for Odun and Icomwell company.


* **Cycling Speed and Cadence**
* **Running Speed and Cadence** 
* **Heart Rate Monitor**
* **Blood Pressure Monitor**
* **Health Thermometer Monitor** 
* **Glucose Monitor**
* **Proximity Monitor** 

### Device Firmware Update (DFU)

The **Device Firmware Update (DFU)** profile allows you to update the application, bootloader and/or the Soft Device image over-the-air (OTA). It is compatible with Nordic Semiconductor nRF5x devices that have the S-Series SoftDevice and bootloader enabled. From version 1.5 onward, the nRF Toolbox has allowed to send the required init packet. More information about the init packet may be found here: [init packet handling](https://github.com/NordicSemiconductor/nRF-Master-Control-Panel/tree/master/init%20packet%20handling).

nRF Toolbox is using the iOSDFULibrary framework, available here: [IOS-Pods-DFU-Library](https://github.com/NordicSemiconductor/IOS-Pods-DFU-Library). The library is packaged with the project so no extra work is needed, if you would like to manually update it or modify it, it is bundled via cocoapods so a simple `pod update` will handle updating the library for you. 

The DFU profile has the following features:
- Scans for devices that are in DFU mode.
- Connects to devices in DFU mode and uploads the selected firmware (Softdevice, Bootloader and/or application).
- Allows HEX or BIN file updates
- Allows to update a Softdevice and/or bootloader and application from a distribution ZIP file automatically.
- Pause, resume, and cancel firmware updates.
- Includes pre-installed examples that consist of the Bluetooth Smart heart rate service and running speed and cadence service.

### Secure Device Firmware Update (Secure DFU)

The **Secure Device Firmware Update (Secure DFU)** profile allows you to **securely** update your Nordic Semiconductor nRF5x S-Seriese devices.
This works by verifying that your firmware files are signed by the vendor that released the code and has not been tampered with, also this means that the peripherals will only accept updates from
the intended developers and reject any firmwares that are not properly signed with the matching key.

As an applications developer, the frontend for the DFU Library is agnostic of the DFU protocol in use, so there are no changes to be done on the mobile application's side to support Secure DFU. 

### Requirements

- iOS 8.0 and above.
- iPhone 4S or newer.
- iPad 3 or newer.
- Compatible with nRF5x devices with S-Series Softdevice and DFU Bootloader flashed.

### Resources

- nRF51 and nRF52 Development kits can be ordered from [nordicsemi.com/eng/Buy-Online](http://www.nordicsemi.com/eng/Buy-Online).
- The SDK and SoftDevices are available online at [developer.nordicsemi.com](http://developer.nordicsemi.com).
