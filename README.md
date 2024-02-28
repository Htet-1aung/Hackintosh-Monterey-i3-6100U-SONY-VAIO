# Hackintosh-Monterey-i3-6100U-SONY VAIO

This is an overview of running Hackintosh MacOS Monterey 12.7.3 on my SONY VAIO with an Intel i3-6100U processor.

## Hardware

- CPU: Intel Core i3-6100U 2.3Ghz
- GPU:
  - Chipset Model: Intel HD Graphics 520
  - Type: GPU
  - Bus: Built-In

## What's Not Working

The following features are not currently working:

- WiFi(Recommended to use Airportitwlm.kext for Intel wifi cards or itwlm.kext + heliport can be a solution too).
- Bluetooth
- Battery indicator(Which can be fixed by upgrading SMCBatteryIndicator.kext)
- Sleep and hibernation

## Fixing Issues

To address the issues mentioned above, you can follow these steps:

- WiFi: Add `itlwm`(Remember to download Heliport to work with it) or `Airportitlwm.kext` to fix WiFi functionality.
- Bluetooth: Install `BluetoothFixUp.kext` and `IntelBluetoothFirmware.kext` to resolve Bluetooth-related dependencies.
  Here: https://github.com/OpenIntelWireless/itlwm
- Battery Indicator: Update `VirtualSMC.kext` and its dependencies to fix the battery indicator.
- Other Issues: For any additional issues, add the necessary kext files to the `EFI/OC/KEXTS` directory.
- ACPI Solution: Add SSDT-PLUG.aml and SSDT-USBX.aml to the /EFI/OC/ACPI directory.


Note: Make sure to research and download the appropriate kext files for your specific hardware configuration.

That's it! With these steps, you should be able to address the mentioned issues and have a functional Hackintosh setup on your SONY VAIO with an Intel i3-6100U processor running MacOS Monterey 12.7.3.

Feel free to customize and tweak the configuration as needed. Good luck!

