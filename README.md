# ArtemisLuaLoader


https://github.com/user-attachments/assets/9170c696-7629-4c26-b8e5-d735e084fc01



Artemis is a modified cross-platform Visual Novel game engine that uses Lua scripting, supporting platforms like Windows, Android, iOS, Web, Nintendo Switch, and PlayStation.

In this version, the system can detect the PS4's IP address, facilitating custom script loading. Most Artemis-based games automatically load a `save9999.dat` file at boot. By editing this save file, it’s possible to chain-load custom scripts directly from the save folder, following this sequence:

**Game Boot** -> **Load Save File "save9999.dat"** -> **Load IET Script "inject.iet"** -> **Load Lua Script "inject.lua"**

This modified setup has been successfully tested on Windows and PS4, and it’s expected to work on other platforms as well.

The repository includes a custom save file for the PS4 game CUSA16074 (Raspberry Cube). This game was selected for convenience as an easily accessible physical disc. Other physical games compatible with Artemis include CUSA27389 (ハミダシクリエイティブ) and CUSA13303 (ノラと皇女と野良猫ハート HD). Alternatively, you can purchase a trial version through the [PlayStation Store](https://store.playstation.com/ja-jp/product/JP2551-CUSA27390_00-HAMIDASHITR00001/) to test the functionality.

Note that you may need to create a custom `save9999.dat` file for each game. While Windows allows full access to `luasocket` and `os.execute`, PS4 access is more restricted. For guidance on copying PS4 save files, refer to online resources.
