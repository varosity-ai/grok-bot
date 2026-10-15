# Varosity for Grok Bot

Give your Grok Bot a studio. This plugin connects [Varosity](https://varosity.ai) — 60+ video, image, voice and
music models behind one account — to Grok Bot as a remote MCP server. The same files work in Cursor and Grok Build.

**Guide and examples:** https://varosity.ai/grok-bot

## What your Bot can make

| | Models |
|---|---|
| Video | Veo 3.1, Kling 3.0, Seedance, Grok Imagine, Runway, Luma |
| Images | FLUX, GPT Image 2, Nano Banana Pro, Ideogram, Grok Imagine |
| Voice | ElevenLabs narration, multi-voice scenes, voice design and cloning |
| Music | Suno, Lyria, ElevenLabs Music |

Live prices: `list_models` (from the Bot) or https://varosity.ai/pricing. Images start at 1¢; a draft video clip
on Veo 3.1 Lite is about 21¢.

## Connect

1. Ask your Bot: *"Connect to Varosity.ai — remote MCP server https://varosity.ai/api/mcp."* Grok Bot adds the
   server and asks for your Varosity key in a secure box.
2. Create an account at https://varosity.ai/signup (most new accounts get a small starter credit), create a key at
   https://varosity.ai/app/keys/api-keys and paste it into that box.
   Adding the server by hand: name `varosity`, URL `https://varosity.ai/api/mcp`, header
   `Authorization: Bearer vsk_…`. Clients that support OAuth sign-in can skip the key.
3. Ask for something small first: *"Make a 1¢ test image of a paper boat on a pond with Varosity."*

On a team plan, an admin may need to allow the server first: Grok Bot follows the team's connector policy.

## Jobs to hand your Bot

- *Every Monday, read our changelog, write a 5-second shot for the biggest change, render it on Veo 3.1 Lite as a
  draft, and send it to me. If I approve, re-render it on Kling 3.0.*
- *For each post in my drafts folder, make two 16:9 images with FLUX and one with GPT Image 2.*
- *When a new product video lands, write a 20-second script, voice it with ElevenLabs, and add a quiet music bed.*

## What this plugin contains

- `mcp.json` / `.mcp.json` — one remote MCP server, `https://varosity.ai/api/mcp`. No local code, no hooks,
  no telemetry.
- `.grok-plugin/plugin.json`, `.cursor-plugin/plugin.json`, `.claude-plugin/plugin.json` — manifests.
- `assets/icon.svg` — logo.

## Network and credentials

All calls go to `https://varosity.ai/api/mcp` over HTTPS. Authentication is OAuth sign-in to your Varosity
account, or a Varosity API key (`vsk_…`) you create. Generations spend your prepaid Varosity credits (provider
price +5%, charged for what is produced; failed renders are not billed) or run on your own provider keys if you
add them. Each result reports your remaining balance.

## Support

support@varosity.ai · https://varosity.ai/support

Grok and Grok Bot are products of xAI. Varosity is independent and not affiliated with or endorsed by xAI.

MIT licensed.
