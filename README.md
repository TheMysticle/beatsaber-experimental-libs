# beatsaber-experimental-libs

Redistributed third-party libraries needed for the experimental Beat Saber
1.45.1 mod set (see https://github.com/TheMysticle/bs-manager-steam-frame,
branch `experimental-1.45.1-support`).

## INIFileParser.dll (v2.5.2.0)

Source: [rickyah/ini-parser](https://github.com/rickyah/ini-parser) (MIT
licensed). BS_Utils's `BS_Utils.Utilities.IniFile` references the assembly
by its exact identity `INIFileParser, Version=2.5.2.0`. BeatMods' current
"Ini Parser" listing ships a newer, renamed build (assembly `INIParser`
v2.5.9.0) that does NOT satisfy that reference - loading it produces:

```
System.TypeLoadException: Could not load file or assembly 'INIFileParser,
Version=2.5.2.0, Culture=neutral, PublicKeyToken=79af7b307b65cf3c'
```

This is the older build, kept under its original assembly name/version so
existing BS_Utils builds resolve it correctly.
