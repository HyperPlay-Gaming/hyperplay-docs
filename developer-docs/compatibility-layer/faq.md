## Compatibility Layer FAQ

#### **Q: What do I need to do in order for my games to run using the compatibility layer on HyperPlay?**
A: Nothing, the compatibility layer is enabled for all users on macOS and Linux automatically. So whenever the player installs a Windows game, when clicking Play, HyperPlay will do all the necessary steps to make it work out of the box.

#### **Q: Is it guaranteed that my game will work through the compatibility layer?**
A: Unfortunately, the compatibility layer won't work on 100% of games and not on 100% of systems. Right now, we have some good numbers, and on Linux, more than 90% of our Windows library is playable and around 85% on macOS. But this may vary. The HyperPlay team is always improving it, so if your game doesn't work, contact us, and we can investigate ways to improve compatbility for your specific use case.

#### **Q: Are there any specific system requirements that the players should know about?**
A: On Linux, they should be the same as for Windows systems. For macOS, the recommendation is a Mac with at least 16GB of RAM running Apple silicon like M1 or newer.

#### **Q: I want to implement an anti-cheat in my game, what are the recommendations?**
A: If you aim to have your Windows game working on macOS and Linux, it is recommended that you look for server-side anti-cheat software rather than client-side software. Specifically, kernel-level anti-cheat software suffers significant compatbility issues. If you still want to run a client-side anti-cheat, the recommended ones are Easy Anti-Cheat or BattleEye since they have support for our Linux compatibility layer. However, at this time, this support only works on Linux. We believe MacOS will be supported in the future.

#### **Q: My game doesn't launch through the compatibility layer, what can I do?**
A: The first step for troubleshooting is to determine if your game needs things like DotNet, VCRedist, or other Windows libraries and DLLs installed for it to work. HyperPlay has support to install external EXEs inside the Wine prefix. For that, follow these steps:
1. Open the game settings.
2. In the Wine tab, click on the `RUN EXE ON PREFIX` button.
3. Select the desired EXE and follow the steps, then try again.

If you wish, you can also open WineTricks on the same screen, and there you can select `default prefix` and then `install a Windows DLL or component`. Be aware that WineTricks has external dependencies that might need to be installed if they are missing from your system. HyperPlay will alert you about that, and they can be installed using `brew` on macOS or the package manager on Linux.

#### **Q: My game launches but is too slow and unresponsive**
A: Since the compatibility layer needs to make translation calls, it might need more resources than when running through Windows natively. So if a system doesn't meet the recommended specs or is on the same level, some performance might be lost, leading to issues like lags and slowdowns.
