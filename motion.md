# Motion Issues
## Z-axis moving up just fine, but once it reaches halfway past the gantry, it's not going down!
### BLTouch/CR Touch/Other ABL users
Your probe cable is loose, check both ends (motherboard side and probe side)
### Everyone else
#### ⚠️ This is just speculation, since I've never had this problem without ABL ⚠️
- A) Your Z-axis limit switch cable is loose, check both ends
- B) Your Z-axis limit switch is stuck, try loosening it
## Printer freezing/doing an M112 shutdown after heating up/during homing
### BlTouch/CR Touch/Other ABL users
#### ⚠️ This is just speculation, since I've never had this problem with ABL ⚠️
Your probe cable is loose, check both ends (motherboard side and probe side)
### Everyone else
This is actually a homing problem in disguise, let me explain:

In the stock firmware, an M112 shutdown manifests as a full freeze (which is why I recommend the [E3V2/S1 Professional Firmware](https://github.com/mriscoc/Ender3V2S1/releases/latest)). A homing error will result in an M112 shutdown.

Because homing usually happens after heating up, the problem disguises itself as a problem with heating, but is actually a homing problem.

**In my case, my Z-limit switch was completely unplugged**, although the problem might happen with **other limit switches being unplugged/loosened**
