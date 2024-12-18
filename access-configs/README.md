---
description: >-
  Optionally gate your game's release branches with access codes or on chain
  asset balances
---

# 🔑 Access Configs

## Access Configurations

HyperPlay provides multiple ways to gate access to your game, called Access Configs.

You can use string-based Access Codes similar to license keys that Steam, Epic, and the majority of traditional stores provide. This provides a familiar & friendly onboarding to players where token-gating is not yet possible or is not necessary.

Token Gating your game is also possible both at the download level, which we handle automatically, and within your game's Runtime, which is handled within your game via the Wallet Overlay APIs (i.e., performing balance checks within the game as an additional security step).

## Access Codes

Game downloads can be gated with 12 digit alphanumeric codes on a per channel basis.&#x20;

**Each access code can only be claimed by 1 user by default.**

After a user claims a channel's access code, all future releases to that channel will be downloadable by the user.&#x20;

One caveat is if the game developer changes the access config for the channel, the user's access will now be determined by the new access config associated with the channel.

Here is a walkthrough for creating a new access config using access codes:

{% content-ref url="how-to-create-access-codes.md" %}
[how-to-create-access-codes.md](how-to-create-access-codes.md)
{% endcontent-ref %}

### Instant Access mode

Many game developers need a TestFlight-style mode that makes their latest builds immediately available to a subset of users.

This allows immediate testing of the build while HyperPlay reviews & approves your build for public use.

HyperPlay automatically provides instant access to all gated release branches that meet the following criteria:

* The Access Config must contain **less than or equal to 300** Access Codes
* The build must still pass the security scan once the scan is complete, or it will be auto-denied
* The Access Config must not contain "Unlimited Use" Access Codes

### Unlimited Use Codes

By default, each Access Code can only be used their set number of uses.

Each Access Code is also linked to the HyperPlay account that claimed

However, in some circumstances, it's necessary to allow keys to be used an unlimited number of times, whether for internal-only use, special events, or quickly setting up a LAN party.

This feature is only available by request. To enable Unlimited Use keys, please contact your HyperPlay account representative and we'll help you get it setup right away.

## Token Gating

Game downloads can also be gated with on chain token balances on arbitrary chains.

ERC20, ERC721, and ERC1155 are supported.

Here is a walkthrough for creating a new access config using token gating:

{% content-ref url="how-to-token-gate-a-release-branch.md" %}
[how-to-token-gate-a-release-branch.md](how-to-token-gate-a-release-branch.md)
{% endcontent-ref %}
