# PC specs & parts
- Mainboard: Gigabyte gaming 7
- CPU: Coffee lake core i5-8400
- VGA: GTX 650 (native support)
- RAM: Corsair 16GB
- SSD: Samsung SSD 960 Evo
- Monitor: Dual monitor Dell

## Hackintosh Working

# How to install
1. Download macOS
  - [macOS Sierra!](http://appstore.com/mac/macossierra)
  - macOS High Sierra (from AppStore)
2. Format USB
  - Name: macOS
  - Format: Mac OS Extended (Journaled)
  - Scheme: GUID Partition Map
3. Copy macOS to USB
  - Sierra
  ```
  sudo /Applications/Install\ macOS\ Sierra.app/Contents/Resources/createinstallmedia --applicationpath /Applications/Install\ macOS\ Sierra.app  --volume /Volumes/macOS/
  ```
  - High Sierra
  ```
  sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --applicationpath /Applications/Install\ macOS\ High\ Sierra.app  --volume /Volumes/macOS/
  ```
4. Make Boot loader (Create EFI folder)
  - Open clover configurator
  - Mount Partition for Install macOS… then click Open Partition
  - Delete EFI folder here
  - Copy Base EFI folder (inclued in this project)
5. Config config.plist
  - Samsung SSD 960 EVO
    - High Sierra: you don't need to do anything
    - Sierra

    Put that in the “KernelAndKextPatches” section of your Clover config.plist
    ```
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily IONameMatch</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>InfoPlistPatch</key>
        <true/>
        <key>Find</key>
        <data>PHN0cmluZz5wY2kxNDRkLGE4MDQ8L3N0cmluZz4=</data>
        <key>Replace</key>
        <data>PHN0cmluZz5wY2kxNDRkLGE4MDI8L3N0cmluZz4=</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#1</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>ibPoAgAAweAMBQAQAACJgw==</data>
        <key>Replace</key>
        <data>ibPoAgAAweAJBQAQAACJgw==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#2</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>D7aMiIIAAACD+QwPhTIBAA==</data>
        <key>Replace</key>
        <data>D7aMiIIAAACD+QkPhTIBAA==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#3</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>AMeDpAAAAAAQAABIi0gISA==</data>
        <key>Replace</key>
        <data>AMeDpAAAAAACAABIi0gISA==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#4</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>SYnGTYX2dGFBwecMSWP/vg==</data>
        <key>Replace</key>
        <data>SYnGTYX2dGFBwecJSWP/vg==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#5</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>hv8PAABIwegMD7cPgeH/Dw==</data>
        <key>Replace</key>
        <data>hv8PAABIwegJD7cPgeH/Dw==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#6_7</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>icGB4f8PAABIAdFIgfn/DwAAdzs=</data>
        <key>Replace</key>
        <data>icGB4f8BAABIAdFIgfn/AQAAdzs=</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#8</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>SYHF/w8AAEnB7QxJiwQkSA==</data>
        <key>Replace</key>
        <data>SYHF/w8AAEnB7QlJiwQkSA==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#9_10</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>BgIAAEyNuAAQAABMiflIgeEA8P//SYmGGgEAAEmJjiIBAABBvAAQAABJKfQ=</data>
        <key>Replace</key>
        <data>BgIAAEyNuAACAABMiflIgeEA8P//SYmGGgEAAEmJjiIBAABBvAACAABJKfQ=</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#11</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>AABJiY4iAQAAugAQAABIKQ==</data>
        <key>Replace</key>
        <data>AABJiY4iAQAAugACAABIKQ==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#12</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>yAAAAEkp17gAEAAATYskJA==</data>
        <key>Replace</key>
        <data>yAAAAEkp17gAAgAATYskJA==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#13</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>4b+AQBUGTYnWugAQAABFMQ==</data>
        <key>Replace</key>
        <data>4b+AQBUGTYnWugACAABFMQ==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#14</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>iWTY+EmBxAAQAABJgccA8A==</data>
        <key>Replace</key>
        <data>iWTY+EmBxAACAABJgccA8A==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#15</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>Bf8PAABIwegMZvfB/w8PlQ==</data>
        <key>Replace</key>
        <data>Bf8PAABIwegJZvfB/w8PlQ==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#16</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>weIIQQ+2wcHgDEQJ0EQJwA==</data>
        <key>Replace</key>
        <data>weIIQQ+2wcHgCUQJ0EQJwA==</data>
    </dict>
    <dict>
        <key>Comment</key>
        <string>IONVMeFamily Pike R. Alpha Patch#17</string>
        <key>Disabled</key>
        <false/>
        <key>Name</key>
        <string>IONVMeFamily</string>
        <key>Find</key>
        <data>RYTJD5XAD7bAweAMRAnYRA==</data>
        <key>Replace</key>
        <data>RYTJD5XAD7bAweAJRAnYRA==</data>
    </dict>
    ```
# Tool
- Clover configurator

# Audio & Micro
- Micro: Buy a usb micro
