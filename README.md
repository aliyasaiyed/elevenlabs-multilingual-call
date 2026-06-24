# Multilingual Agent Call — ElevenLabs API Demo

I built the "declined card / fraud hold" support call from my [ElevenAgents financial-services concept]([https://github.com/aliyasaiyed/elevenagents-finserv-concept]) as real audio, using the ElevenLabs API, in three languages: **English, Spanish, and German**.

## Why

The concept claims ElevenAgents can resolve financial support calls in any language. I wanted to test whether the product actually delivers that, and to hear what an enterprise buyer would hear. German is deliberate: Deutsche Telekom is a named ElevenLabs customer, so it's a realistic enterprise language to prove the product on.

## What's here

- `elevenlabs_multilingual_call.ipynb` — the notebook that generates the calls. Runs in Google Colab, nothing to install.
- `audio/` — the generated calls: English, Spanish, and German.

## How it works

Two ElevenLabs voices play the caller and the support agent. The notebook generates each line with the multilingual model, then stitches the lines into one continuous call per language.

## What I noticed

> **[ Fill this in after you run it. ]** Two or three honest, specific observations: how natural the turn-taking felt, where pronunciation or pacing was strong or weak across the three languages, anything that surprised you, and one concrete thing it changed about how you would position the product. This section is the most important part of the repo. Be specific, and be honest, including about any limitations.

## Run it yourself

1. Open `elevenlabs_multilingual_call.ipynb` in [Google Colab](https://colab.research.google.com).
2. Get a free ElevenLabs API key (elevenlabs.io → Profile → API Keys).
3. Run the cells top to bottom. It will prompt for your key at runtime; the key is never saved in the notebook or this repository.
