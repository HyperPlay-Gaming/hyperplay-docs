---
description: >-
  Optionally gate your game's channels with access codes or on chain asset
  balances
---

# 🔑 Access Configs

## Access Codes

Game downloads can be gated with 12 digit alphanumeric codes on a per channel basis.&#x20;

Each access code can only be claimed by 1 user. After a user claims a channel's access code, all future releases to that channel will be downloadable by the user.&#x20;

One caveat is if the game developer changes the access config for the channel, the user's access will now be determined by the new access config associated with the channel.

Here is a walkthrough for creating a new access config using access codes:

{% content-ref url="how-to-create-access-codes.md" %}
[how-to-create-access-codes.md](how-to-create-access-codes.md)
{% endcontent-ref %}

## Token Gating

Game downloads can also be gated with on chain token balances on arbitrary chains.

ERC20, ERC721, and ERC1155 are supported.

Here is a walkthrough for creating a new access config using token gating:

{% content-ref url="how-to-token-gate-a-channel.md" %}
[how-to-token-gate-a-channel.md](how-to-token-gate-a-channel.md)
{% endcontent-ref %}
