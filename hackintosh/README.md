# PC specs & parts
- Mainboard: Gigabyte gaming 7
- CPU: Coffee lake core i5-8400
- VGA: GTX 650 (native support)
- RAM: Corsair 16GB
- SSD: Samsung SSD 960 Evo
- Monitor: Dual monitor Dell

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

# Tool
- Clover configurator

# Audio & Micro
- Micro: Buy a usb micro
