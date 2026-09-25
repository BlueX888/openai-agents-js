---
'@openai/agents-realtime': patch
---

fix: Send `response.cancel` when the WebSocket Realtime transport is interrupted while a response is in progress but no audio is being played, e.g. before the first audio delta of the response or after its audio has already finished, so the response no longer keeps generating after an interrupt.
