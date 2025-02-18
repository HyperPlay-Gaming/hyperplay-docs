## Compatibiliy Layer FAQ

#### **Q:  What do I need to do in order for my games to run using the compatibility layer on HyperPlay?**
A: Nothing, the compatibiliy layer is enabled for all users on macOS and Linux automatically. So whenever the player installs a Windows game, when clicking Play HyperPlay will do all the necessary steps to make it work out of the box.

#### **Q: It is guarantee that my game will work through the compatibility layer?**
A: Unfortunatelly the compatibiliy layer won't work on 100% of games and not on 100% of systems. Right now we have some good numbers and on Linux more than 90% of our Windows library is playable and around 85% on macOS. But this may vary. The HyperPlay team is always improving it so if your game won't work contact us and we can take a look on what is possible to do.

#### **Q: There is any specific system requirements that the players should know about?**

A: On Linux they should be the same as for Windows systems. For macOS the recommended is a Mac with at least 16GB of RAM running Apple silicon like M1 or newer.

#### **Q: I Want to implement a Anti-Cheat on my game, what are the recomendations?**

A: If you aim to have your Windows game working on macOS and Linux, is recommended that you looks for Server Side Anti-Cheats and not client-side ones. Especially Kernel-Level Anti-Cheats which doesn't support Wine. <br>
If you still want to run a Client-Side AntiCheat the recommended ones are EasyAnticheat or BattleEye since they have Support for Wine. <br>
But as far as we know, this support only works on Linux.

#### **Q: My game doesn't launch through the compatibiliy layer, what can I do?**
A: As we know, Windows is a complex operating systems and the compatibiliy layer cannot replicate everything with it. What you should do is to see if your game needs things like DotNet, VCRedist or other Windows libraries and DLLs installed for it to work. <br>
HyperPlay has support to install external EXEs inside the Wine Prefix. For that, follow these steps:
1. open the game settings.
2. the Wine Tab click on the `RUN EXE ON PREFIX` Button. 
3. Select the desired EXE and follow the steps then try again.

If you wish, you can also open WineTricks on the same screen and there you can select `default prefix` and then `install a Windows DLL or component`. <br>
Beware that Winetricks has external dependecies that might need to be installed in case they are missing from your system. HyperPlay will alert on that and they can be installed using `brew` on macOS or the package manager on Linux.

#### **Q: My game launches but is too slow and unresposive**
A: Since the compatibility layer needs to make translations calls it might need more resources than when running through Windows nativelly. So if a system doesn't meet the recommended specs or are on the same level, some performance might get lost leading to issues like lags and slowdowns.