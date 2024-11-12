---
description: >-
  HyperPlay provides multiple out-of-the-box methods for launching Browser games
  with the HyperPlay Overlay.
---

# 🌐 API for Browser Games (EVM)

## Two Clients: Out-of-the-box Compatibility

HyperPlay provides multiple out-of-the-box methods for launching Browser games with the HyperPlay Overlay:

* HyperPlay Browser Client (within existing browsers, launched directly from the game's HyperPlay [Store](https://store.hyperplay.xyz/) page)
* HyperPlay Desktop Client (within the native HyperPlay app)

Our Browser Client allows you to launch your game directly within your HyperPlay [Store](https://store.hyperplay.xyz/) Page, without needing to install the Desktop Client.

Our Desktop Client allows you to launch your game within a WebView with WebGPU support, and upgrades your browser game to feel like a full screen native game experience.

**Browser-based games receive a number of advantages by being listed in HyperPlay.**&#x20;

* Greater distribution and discovery by web3 players
* Built-in Quests via the HyperPlay Overlay
* Games can opt to use HyperPlay's authentication to simplify player onboarding
* Graphics card acceleration through WebGPU ensures that games perform well
* Games are opened in a full-screen view, making them feel more like native games
* Developers get access to the full-suite of tools, incentives, and features that the HyperPlay ecosystem provides to game developers.

**If your game is already compatible with MetaMask, either through `window.ethereum` or the MetaMask SDK, your game is already compatible with HyperPlay's wallet overlay.**&#x20;

The HyperPlay application injects the player's wallet into browser pages much in the same way that a typical web browser running the MetaMask browser extension would. Any calls made to the wallet on your page will be relayed to the user's selected wallet.

If you're new to implementing MetaMask, we recommend starting with MetaMask's developer docs. There are multiple ways to integrate MetaMask, including both MetaMask's new SDK or utilizing a convenience library and `window.ethereum` directly.

**Check out the MetaMask developer docs** [**here**](https://docs.metamask.io/wallet/how-to/connect/)**.**

## Testing Your Game with the Desktop Client

To test your game, we recommend opening the HyperPlay desktop application, navigating to Library, and then Add Game. Here you can side-load the game and test for compatibility as if your game were already listed in the HyperPlay Store.

## Testing Your Game with the Browser Client

Please proceed with listing your game through the HyperPlay Developer Portal (see below). Once you've submitted your game's listing info, please reach out to your HyperPlay account representatives to enable the Browser Client functionality for your game.

## Listing your Browser Game in the Store

Once you're ready to list, reach out to the HyperPlay team via the Submit a Listing link on hyperplay.xyz. We'll get you connected to the HyperPlay Developer Portal so you'll be able to manage your listing. The whole process is quick and easy.

## Limitations

### Desktop Client

While there are currently no known limitations for the Desktop Client, if your game has a fullscreen button within its UI, we recommend adopting the [`@hyperplay/browser-sdk`](https://www.npmjs.com/package/@hyperplay/browser-sdk) to ensure it works seamlessly with HyperPlay's Overlay. Please see [below](api-for-browser-games-evm.md#in-game-fullscreen-button-integration) for more details.

### Browser Client

**Security Headers**:

* Ensure the **X-Frame-Options** header is not set to `"SAMEORIGIN"` or `"DENY"`.
* Set the **Content-Security-Policy** header to include `'store.hyperplay.xyz'` or `'*.hyperplay.xyz'`
  * For example: `Content-Security-Policy: frame-ancestors 'self' https://store.hyperplay.xyz https://*.hyperplay.xyz;`

This will give permission to the only the HyperPlay Browser Client to render your website within an iframe.

#### In-game fullscreen button integration

If your game has a fullscreen button within the UI, a small one-line change is needed to make it work with the HyperPlay Overlay.

Since the fullscreen button on the HyperPlay Overlay affects the parent frame, and the fullscreen button within the iframe affects the child frame only, the following code will automatically detect and handle this case when launching your game within the HyperPlay Browser Client:

```javascript
import { requestFullscreen } from '@hyperplay/browser-sdk'

...

  <button onClick={() => {requestFullscreen({ elementId: 'gameCanvas', setStyle: true })}}>Request Fullscreen</button>
  ...
  <div id="gameCanvas">Some Content</div>
```

This will not affect your game's default behavior, it will only apply this change when we detect it is launched within the Browser Client.

To integrate this fix, please install the following NPM package and follow the steps within the README:

{% embed url="https://www.npmjs.com/package/@hyperplay/browser-sdk" %}

#### OAuth not possible within iframe&#x20;

If your game **requires** OAuth at any step in the sign-in or registration flow, due to third-party security practices, OAuth providers like Google, Discord, etc, block signing in within iframes of a different origin to prevent websites from hijacking your session.

In these cases, there are two possible solutions:

* Allow players to use Sign-in With Ethereum or a similar web3 signature-based authentication, and hide the OAuth options for these users.
* Fallback to using the HyperPlay Desktop Client only for launching your game.

Since the Desktop Client acts like a native browser, it does not use an iframe to inject the Overlay, and therefore, this issue is avoided.

If your game requires OAuth, please give the HyperPlay team a heads up during onboarding so we can double check this configuration during the QA process.

