------------------------------

These are separate registry files that changes various settings for the game. Please select one under each folder, from 1 to 5.

The registry files are mostly independent except for folder 4 and 5, since the graphics presets includes pre-defined values for vertical sync. So always enable/disable vertical sync manually through the registry files under folder 5 after having selected a graphics preset.

These aren't all the registry keys the game uses, but these seem to be the most important ones.

------------------------------

ASM2Launcher.exe and Game.exe also sets a couple of other register keys as well, which are mentioned below:

------------------------------------------------------------------------------------------------------
Set by Game.exe itself:
------------------------------------------------------------------------------------------------------
[HKEY_CURRENT_USER\Software\Activision\The Amazing Spider-Man 2 (TM)\Settings\Display]
"PerfHUD"=dword:00000000
"Brightness"=dword:00000000
"Gamma"=dword:00000000
"Contrast"=dword:00000000
"AutoFlushShaders"=dword:00000001
"RefreshRate"=dword:00000000
"Cameras"=hex:01,00,00,0a,a0,05,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,\
  00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,00,\
  00,00,00,00,00,00,00,00,04,00

[HKEY_CURRENT_USER\Software\Activision\The Amazing Spider-Man 2 (TM)\Settings\Game]
"CleanQuit"=dword:00000001

------------------------------------------------------------------------------------------------------
Set by ASM2Launcher.exe: (Seems to be useless?)
------------------------------------------------------------------------------------------------------
[HKEY_CURRENT_USER\Software\Activision\The Amazing Spider-Man 2 (TM)\GameConfig]
"AlreadyRun"=dword:00000001

[HKEY_CURRENT_USER\Software\Activision\The Amazing Spider-Man 2 (TM)\Settings]
"AssertIgnorePrefix"=""
"WinX"=dword:00000000
"WinY"=dword:00000000
