# Downsides and Limitations of the Compatibility Layer

Unfortunately, compatibility layers are not perfect and do not support every Windows or DirectX call yet. While compatibility is quite mature and stable on Linux, it still rapidly improving on macOS. Some issues might be found, and some games might not work at all, although this is a small number. Some of these limitations include, but are not limited to:

1. **Performance Impact** Games running on Linux may experience up to a 10% performance decrease, while macOS users could see a reduction of up to 25%. On the other hand, some games might have better performance depending on how they were developed.
2. **Shader Lag** DX9/10/11 games might exhibit lag due to real-time shader caching. Once the shaders are cached, they persist until a game or driver update.
3. **Anti-Cheat Incompatibility** Kernel-level anti-cheat systems (e.g., Vanguard, Easy Anti-Cheat) suffer compatibility issues. While Easy Anti-Cheat and BattleEye offer support for compatibility layers, this must be enabled by game developers and requires a specific library file within the game folder to work on Linux. macOS support for these anti-cheat products is not yet available when using compatibility layers.
4. **Bugs and Glitches** Users may encounter bugs and glitches when some system or DirectX calls are not fully supported by the compatibility layer.
5. **Additional Workarounds** In some cases, installing additional Windows libraries (e.g., vcrun, dotnet) may be necessary to run certain games. On Mac and Linux, HyperPlay ships with Winetricks, making it easy to install these tools. An automated way to install these workarounds is planned for a future HyperPlay release.
