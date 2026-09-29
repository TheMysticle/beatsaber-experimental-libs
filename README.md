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


## A note on how this fork was made

I'm not a professional programmer. I do some Android development, but Unity/Harmony
modding is new to me, so I know just enough to spot when something has gone wrong and
roughly how to fix it.

This fork's changes were made with AI assistance. I direct the work, review what it
produces, and test everything on real hardware before it goes into a release. I'm
sharing this because I'd rather be upfront about it than have you wonder. This
disclaimer covers this fork's own changes only — the original mod is the work of its
original author(s).

I understand not everyone is comfortable with AI-assisted code, and that's a fair
position; a lot of people here have spent years building real expertise. If you'd
rather check things yourself, everything is open and the commits are small. Bug
reports, reviews and corrections are very welcome, and I'll fix what I get wrong.
