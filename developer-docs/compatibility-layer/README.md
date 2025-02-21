# 🍷 Compatibility Layer

## Compatibility Layer Overview

### Overview

The Compatibility Layer in HyperPlay is a unique feature, not only in Web3 but also in traditional gaming, designed to help developers extend the reach of their applications across multiple operating systems with minimal effort.&#x20;

By abstracting platform-specific details, the Compatibility Layer allows developers to build a game for Windows only and have it run seamlessly on other operating systems like macOS and Linux, and devices like the SteamDeck.&#x20;

This is particularly useful for achieving a broader audience without the need for extensive OS-specific modifications. It works similarly to what Steam does with Steam Play on Linux, but on HyperPlay, it also works on macOS, automatically setting up Apple's Gaming Porting Toolkit (GPTK) for maximum compatibility.

#### Benefits

* **Cross-Platform Support**: Write your code for Windows, and HyperPlay will enable it to run on macOS, Linux, and the Steam Deck.
* **Reduced Development Time**: Focus on building features rather than dealing with OS-specific issues.
* **Consistency**: Ensure a uniform user experience across all supported platforms.

#### Implementation

The Compatibility Layer is integrated into HyperPlay through a set of APIs and tools, like Proton on Linux and GPTK on macOS, that handle the underlying differences between platforms. These tools automatically adjust the application's behavior to match the target environment, allowing developers to concentrate on core functionality. By leveraging this layer, developers can ensure their applications are accessible to a wider audience, enhancing their potential reach and impact.
