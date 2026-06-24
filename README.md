# Multilingual Agent Call — ElevenLabs API Demo

I built the "declined card / fraud hold" support call from my [ElevenAgents financial-services concept]([https://github.com/aliyasaiyed/elevenagents-finserv-concept]) as real audio, using the ElevenLabs API, in three languages: **English, Spanish, and German**.

## Why

The concept claims ElevenAgents can resolve financial support calls in any language. I wanted to test whether the product actually delivers that, and to hear what an enterprise buyer would hear. German is deliberate: Deutsche Telekom is a named ElevenLabs customer, so it's a realistic enterprise language to prove the product on.

## What's here

- `elevenlabs_multilingual_call.ipynb` — the notebook that generates the calls. Runs in Google Colab, nothing to install.
- call_english.mp3, call_spanish.mp3, call_german.mp3 — the generated calls.

## How it works

Two ElevenLabs voices play the caller and the support agent. The notebook generates each line with the multilingual model, then stitches the lines into one continuous call per language.

## What I noticed

Across all three languages the conversation kept a natural pace, and the turn-taking in Spanish and German sounded like a real call rather than a robotic read, whereas English sounded slightly robotic to me personally. The voice quality surprised me most: Spanish sounded the most natural to me as the agent carried a calm, competent tone that a financial caller would want.
 
One honest limitation: because I generated each line separately and joined them, the speakers run straight into each other with no pause, so the rhythm is a little tighter than a real call. In production I'd add natural gaps and let the agent's tone shift between hearing the problem and resolving it. Maybe because English is my native language, I noticed the tone of the voices in that audio seemed to change a little unnaturally to me personally, whereas Spanish and German felt more steady-toned.

What it changed about how I'd position it: the multilingual quality is strong enough that language coverage isn't a footnote, it's a wedge. The worry enterprise buyers have is that non-English voices degrade. I found the opposite: the Spanish and German held up as well as the English, and to my ear they were steadier. So for multinational and EU financial buyers, I'd lead with that proof directly, that the agent sounds as composed and trustworthy in every language, rather than burying language support as a feature.

## Run it yourself

1. Open `elevenlabs_multilingual_call.ipynb` in [Google Colab](https://colab.research.google.com).
2. Get a free ElevenLabs API key (elevenlabs.io → Profile → API Keys).
3. Run the cells top to bottom. It will prompt for your key at runtime; the key is never saved in the notebook or this repository.
