---
description: An overview of common questions about HyperPlay
---

# ❓ FAQ

#### **Q: What is HyperPlay?**

A: HyperPlay is a desktop application that provides both a web3-native game store and an aggregator of other game stores. HyperPlay allows players to install games from the Epic Store, GOG, Amazon Prime Gaming, or our own HyperPlay store. Players can connect their MetaMask or WalletConnect wallet to our native desktop application, and then use their wallet inside of every game launched from within HyperPlay, even in native desktop games. HyperPlay was developed in partnership with [**MetaMask**](https://metamask.io) and was incubated by [**Game7**](https://game7.io/), a DAO focused on accelerating the adoption of sustainable web3-native gaming. In June of 2023, we closed a capital raise and became an independent company.



#### **Q: What are HyperPlay Quests? What can I win by completing these quests?**

A: HyperPlay has built-in questing used by the games in the HyperPlay Store. Players can win tokens, NFTs, and off-chain points by completing the various quests created by the game developers who compose the HyperPlay community.&#x20;

Available Quests appear both in the Quest directory, the game's Store listing, and in the HyperPlay overlay while the player in in-game. You can browser the HyperPlay Store here, or open up the HyperPlay app and select "Quests" on the left sidebar. Once you've earned quest rewards, the quest rewards are claimed in-game, using the HyperPlay overlay.



#### **Q: Is HyperPlay related to MetaMask?**

We are built in close partnership with MetaMask, and our founder was previously Lead of Operations for MetaMask. MetaMask wrote a [case study](https://metamask.io/news/developers/how-hyperplay-is-building-a-web-3-game-store-with-the-metamask-developer/) about how we work together and you can see some of their[ tweet threads](https://twitter.com/MetaMask/status/1630995052402016256) about the collaboration as well.



#### **Q: Does HyperPlay have a token?**

A: Not yet. :smile:\


#### **Q: Is HyperPlay open source?**&#x20;

A: Yes. HyperPlay is open source, mainly under a GPL license. A small number of our products like the HyperPlay developer portal, game hosting, and the wallet overlay plugin are issued under a separate proprietary license, although we are working to progressively be more open source over time.\


#### **Q: How do games list in the HyperPlay Store?**

A: Developers seeking to list in the HyperPlay Store should get in contact with us through [**this form**](https://forms.gle/A3mQ8A7CTWrDo8LD6). Once your application is processed, we'll schedule an onboarding call and grant you access to the HyperPlay developer portal where you can manage your game builds.&#x20;

Since HyperPlay aggregates other game stores like the Epic Games Store, we also offer an option to create a "Forwarder Listing" inside the HyperPlay Store that will download the game from the Epic Games Store. Games looking to create a forwarder listing inside the HyperPlay Store should get in contact using the [same listing form](https://docs.google.com/forms/d/e/1FAIpQLSdR-nIKJp-ZeqiaoXKlXK8kWISPwkyk0Y898YAvUbcSbY4K9w/viewform) above. For listing in the Epic Games Store or GOG, we recommend reaching out to those stores directly.



#### **Q: As a game developer, how do I create quests for my game?**

A: You can build quests directly inside of the HyperPlay developer portal where you manage you game's listing. Most quest types require no engineering effort, and can even be built by a non-technical team member! The quests are all handled by HyperPlay and decentralized smart contracts end-to-end. HyperPlay's developer portal will deploy your game's quest smart contract, the HyperPlay overlay tracks player eligibility, and players claim the quest reward while in-game, through the HyperPlay overlay.

At launch, we support Play Streak quests, but other quest types are coming like Reputation Airdrops, Leaderboards, and In-game Achievements are all coming soon. Play Streak Quests and Reputation Airdrops can be created with no engineering effort from game teams, while the Leaderboards and In-game Achievement quests can be implemented by integrating with a simple API for tracking player progress.



#### **Q: What does HyperPlay charge developers to be included? Steam and Apple are charging 30% fees. Will HyperPlay charge similar fees?**

A: HyperPlay takes no listing fee or in-game transaction fees. HyperPlay is free for game developers. For developers releasing through Epic or GOG, the fees of those stores still apply, but we add no additional fees.&#x20;



#### **Q: Are both native games and browser games supported?**

A: Yes, both are supported! For browser games, we work some UX magic to give these a better user experience than playing a in traditional browser. We also provide graphics card acceleration of browser based games through WebGPU.



#### **Q: Which wallets are supported?**

A: Players can use MetaMask Mobile, the MetaMask browser extension, or any WalletConnect based wallet like Sequence, TrustWallet, or others. MetaMask Mobile and WalletConnect are connected by scanning a simple QR code, and the MetaMask browser extension can even be imported from your existing browser install.



#### **Q: How will HyperPlay keep players safe from scams, malware, and other attack vectors? Does HyperPlay have access to my secret recovery phrase?**

A: HyperPlay does not have access to your secret recovery phrase. To understand HyperPlay's security model, it is first important to understand how HyperPlay works. From a technical perspective, HyperPlay is actually a gaming-focused Electron-based web browser that includes built-in wallet implementations like MetaMask and WalletConnect.&#x20;

HyperPlay functions very similarly to the way Chrome does in relationship to the MetaMask browser extension. If you select the MetaMask browser extension as your wallet method, HyperPlay can import your extension MetaMask installation from your current web browser to the MetaMask installation included within HyperPlay. Your secret recovery phrase remains encrypted within the wallet vault file, and only you can access them by using your MetaMask password. For advanced users and developers, we also support importing a wallet with a 12 or 24 word secret recovery phrase. From a security perspective, this feature is essentially identical to setting up a new MetaMask install within Chrome.  If you lose your 12 or 24 word secret recovery phrase, there is nothing the HyperPlay team can do to help you recover it as we never had access to your keys or funds.

Overall, there are four critical components to HyperPlay’s security strategy.&#x20;

1. **Store review:** all stores included in our app (HyperPlay, Epic, GOG) do extensive malware testing and diligence on the development teams for any software submitted through our store, including both static analysis and dynamic analysis. We never allow any title to be published without security review.
2. **Game sandboxes:** Because it is impossible to ensure that no malware will ever slip through a store review process (see the many news stories about malware included in Steam), we’re introducing game sandboxes that prevent a malicious game that slipped through a store review process from acting outside of its own context. We aim to launch this feature soon.
3. **Key segregation:** HyperPlay never exposes a user’s keys to games. The wallet lives within our desktop application or on an external mobile device. Games can submit transaction requests to HyperPlay, which we show to the user. The game cannot access the user’s keys or sign on behalf of the user without user consent.
4. **External signer:** It isn’t a coincidence that we support MetaMask Mobile and WalletConnect. Keeping the keys off of one’s device, and having transactions pop up on an external mobile device is an inherently more secure pattern. For security conscious users, we strongly recommend the MetaMask Mobile integration as the most secure connection method. Even in the event that a user's computer becomes compromised, this pattern should keep the malware from being able to access the keys.

A word of warning here: other "web3 game launchers" have often marketed themselves as a safer solution to download games. At the time of writing, we are aware of extremely alarming poor security practices in some of these products. We urge those teams to look to our example and take user safety and protection of user funds more seriously.

\


#### **Q: What is the process of bringing an existing MetaMask wallet to HyperPlay?**

A: For MetaMask Mobile or WalletConnect users, players will scan a QR code within the HyperPlay app from MetaMask Mobile to link their wallet. For browser extension users, HyperPlay makes it super simple to import any MetaMask wallet (including custom networks, tokens, and settings) already found on the local device by importing the install from their browser extension folder. We only import your existing install with explicit user consent, however.



#### **Q: Which networks are supported?**

A: All EVM networks are supported, including Ethereum, zkSync, Polygon, Mantle, Linea, Avalanche, Arbitrum, Optimism, BSC, and Harmony. Non-EVM networks like Sui, Starkware, Solana and Cosmos are supported through MetaMask’s Snaps plugin system, but will require the user to use a MetaMask browser extension wallet for compatibility.\


#### **Q: What operating systems are supported?**

A: HyperPlay supports Windows, SteamDeck, MacOS, and Linux. We are also integrated with GPTK and Wine-Crossover, providing game compatibility on Mac. For SteamDeck and Linux players, HyperPlay integrates with the [Proton compatibility library](https://www.protondb.com/), allowing Windows games to run natively. We can't promise that Windows game will run perfectly on Mac or Linux through these compatibility libraries, but we do our best to provide this kind of support.



#### **Q: What kinds of interactions between games and the integrated wallets are possible?**

A: All major web3 APIs can be passed through to the game, and back to the wallet. This is accomplished using a combination of the MetaMask Mobile SDK, the MetaMask browser extension, and the HyperPlay client-side API. This includes transaction requests, signature requests, propose custom networks, and propose custom tokens.&#x20;



#### **Q: Is HyperPlay related to the Heroic Games Launcher?**

A: Yes! HyperPlay's co-founder Flavio Lima is also the founder of the Heroic Games Launcher. Heroic was created to allow people to play Epic Games Store games on Steam Deck and Linux, but isn’t necessarily a web3 product. We are developing both products, and share a great deal of the same tech.



#### **Q: What are some of the benefits for developers launching their games through this platform?**

A: HyperPlay is the most-developer loyal game distribution platform. We solve many developer experience problems (ie. the wallet-to-game interaction problem) to make it easier to build great web3 game experiences. Additionally, our model of aggregating many stores provides a safe haven for web3 game developers who have been constantly de-platformed and exploited by monopolistic web2 companies. We are a developer loyal platform that aims to promote freedom and permissionless innovation. Many user acquisition features are coming for our developer community as well.\


#### **Q: How does HyperPlay make money?**

A: We are not monetized at this time. We plan to introduce optional monetized features to our users at a later date.

#### Q: What is HyperPlay's CDN coverage?

A: HyperPlay's CDN coverage is global. We block the following countries to comply with US laws:

* **CU**: Cuba
* **IR**: Iran
* **KP**: North Korea
* **SY**: Syria

#### Q: How long does it take my project release to go live?

A: For the first release for a project, it typically takes 1-3 days for the full testing process. If your game passes all tests, it will go live, and you will receive a notification email.&#x20;

For subsequent releases, it typically takes 30 to 60 minutes for a release to go live if no issues are found with your submitted build.

#### Q: What is the difference between the admin and release manager roles?

A: An admin role can perform all sensitive actions regarding a project. A release manager can only create new releases for channels.\
