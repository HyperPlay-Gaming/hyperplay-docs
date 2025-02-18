# Compatibility Layer

## Overview

The Compatibility Layer in HyperPlay is a unique and exclusive feature, not only in Web3 but also in Web2 launchers, designed to help developers extend the reach of their applications across multiple platforms with minimal effort. By abstracting platform-specific details, the Compatibility Layer allows developers to write code once and have it run seamlessly on various operating systems and devices. This is particularly useful for achieving a broader audience without the need for extensive platform-specific modifications. It works similarly to what Steam does with Steam Play on Linux, but on HyperPlay, it also works on macOS, automatically setting up Apple's Gaming Porting Toolkit (GPTK) for maximum compatibility.

### Benefits

- **Cross-Platform Support**: Write your code for Windows, and HyperPlay will figure out how to run it on macOS, Linux, and the Steam Deck.
- **Reduced Development Time**: Focus on building features rather than dealing with platform-specific issues.
- **Consistency**: Ensure a uniform user experience across all supported platforms.

### Implementation

The Compatibility Layer is integrated into HyperPlay through a set of APIs and tools, like Proton on Linux and GPTK on macOS, that handle the underlying differences between platforms. These tools automatically adjust the application's behavior to match the target environment, allowing developers to concentrate on core functionality. By leveraging this layer, developers can ensure their applications are accessible to a wider audience, enhancing their potential reach and impact.