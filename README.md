# HP Pavilion X360 14-dh0023nl Hackintosh
EFI folder for Opencore boot-loader for HP Pavilion X360 model 14-dh0023nl
### Last update - Discontinued
**April 2023**, MacOS Ventura
### Last checked MacOS version
13.2.1
## Disclaimer
This repo will be update yearly one month or so after the release of new version of MacOS (unless differently specified)
### PC spec
Quick pc spec to ensure hardware is the same
# TODO: Tabella degli specs

## Does it work?
# TODO: tabella di cosa funziona
## Usage
### Recommended
**General Advise** : use this repo as a mirror to correct your mistakes during the creation of your own EFI folder
- create your own EFI directory by following the excelent Dortania's guide\
 https://dortania.github.io/OpenCore-Install-Guide/
- boot up your efi to see what is not working
- if something is not working use this provided EFI as a mirror to detect differecens and make changes accordingly
- **do not directly copy kext files** as they may be outdated and not working anymore with your Opencore version 
- **You can copy ACPI files** in your ACPI directory to fix harware compatibility issue\
**Waning**: sometimes ACPI files alone will not fix your problems, you will have to manually add to the config.plist in ACPI/Patch the correct patches to make them work

### Discouraged
- Use the provided efi as it is to install MacOS\
**Warning** you will have to generate personal device info as stated in Dortania's guide, such as serial number\
In config.plist -> PlatformInfo.\

```

	<key>MLB</key>
	<string>INSERT HERE</string>
	<key>MaxBIOSVersion</key>
	<false/>
	<key>ProcessorType</key>
	<integer>0</integer>
	<key>ROM</key>
	<data>INSERT HERE</data>
	<key>SpoofVendor</key>
	<true/>
	<key>SystemMemoryStatus</key>
	<string>Auto</string>
	<key>SystemProductName</key>
	<string>MacBookPro15,4</string>
	<key>SystemSerialNumber</key>
	<string>INSERT HERE</string>
	<key>SystemUUID</key>
	<string>INSERT HERE</string>
```
You can use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to automate the process

---
Feel free to open up issues if you encounter some problems, I will answer as soon as possible.