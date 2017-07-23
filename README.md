# Skip-ASM2Launcher
Custom launcher to skip the bundled C# launcher in The Amazing Spider-Man 2 on PC.


## Introduction

The default launcher is coded in older C# and have a tendency to break on all kinds of computers.
Hence, this workaround.

* ASM2Launcher.exe is a really simple C++ application that only does one thing and one thing only: launches Game.exe.
* The real ASM2Launcher.exe takes care of all kinds of things, such as validating settings according to the reported VRAM of the primary GPU (can cause issues with hybrid platforms such as Nvidia Optimus) as well as allows keybinds to be reconfigured.

This custom launcher can be used to skip the launcher completely, and hopefully also manages to make the game playable on computers that fail to start the original launcher properly. Please be aware that settings must instead be manually changed through the registry and/or input.dat. Refer to the various subfolders under Settings for how to do so.


## Installation

1. Navigate to the game folder.
2. Rename/remove the original ASM2Launcher.exe
3. Move the included custom launcher from here to the game folder.
4. Use the various registry files in the Settings subfolder in this archive to tweak the settings of the game.


## Source code

```
// ASM2Launcher.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"
#include <Windows.h>

VOID startup(LPCTSTR lpApplicationName)
{
	// https://stackoverflow.com/questions/15435994/how-do-i-open-an-exe-from-another-c-exe/15440094
  
	// additional information
	STARTUPINFO si;
	PROCESS_INFORMATION pi;

	// set the size of the structures
	ZeroMemory(&si, sizeof(si));
	si.cb = sizeof(si);
	ZeroMemory(&pi, sizeof(pi));

	// start the program up
	CreateProcess(
		lpApplicationName, // the path
		NULL, // Command line
		NULL, // Process handle not inheritable
		NULL, // Thread handle not inheritable
		FALSE, // Set handle inheritance to FALSE
		0, // No creation flags
		NULL, // Use parent's environment block
		NULL, // Use parent's starting directory 
		&si, // Pointer to STARTUPINFO structure
		&pi // Pointer to PROCESS_INFORMATION structure (removed extra parentheses)
	);
	// Close process and thread handles. 
	CloseHandle(pi.hProcess);
	CloseHandle(pi.hThread);
}

int main()
{
	LPCTSTR ASM2Game = L"Game.exe";
	startup(ASM2Game);
	return 0;
}
```


## License

https://github.com/Idearum/Skip-ASM2Launcher/blob/master/LICENSE
