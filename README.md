# Boldclaim Chat

Bring your own AI. Wir sehen deine Counter nie.

Single-file vanilla HTML chat-UI für faktenbasierte Counter-Speech. Inferenz läuft im Browser direkt gegen den Provider deiner Wahl (Anthropic, OpenAI, Moonshot, OpenRouter, Ollama). Kein Server zwischen dir und dem Modell, kein Tracking, keine Cookies.

## Status

- v2.0 Phase A — Skeleton, lokal testbar
- BYOK-only Architektur (kein Server-LLM-Fallback)
- Multi-Provider Streaming, Vision-fähig (Anthropic + OpenAI)

## Lokal testen

```sh
python3 -m http.server 8765
# http://localhost:8765
```

API-Key in Settings (Gear-Icon oben rechts) eintragen, "Verbindung testen", los.

## Privacy

- API-Key bleibt im Browser localStorage, niemals auf einem Server
- Counter-Text geht direkt vom Browser zum Provider, nicht über uns
- Kein Pinecone, kein externer Worker (in dieser Phase)
- Quellcode ist die Wahrheit, lies `index.html`

## Stack

- Vanilla HTML + Alpine.js + Tailwind CDN
- Single file, ~917 Zeilen
- Zero build, zero dependencies bei Deploy
