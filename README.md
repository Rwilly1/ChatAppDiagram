# ChatAppDiagram

Three interactive diagrams of [Rwilly1/ChatApp](https://github.com/Rwilly1/ChatApp), a real-time end-to-end encrypted chat app (Flask + Flask-SocketIO + AES-256). Rendered client-side with [dagre-d3](https://github.com/dagrejs/dagre-d3), laid out from the actual event names and file/line references in `app.py`, `crypto_utils.py`, and `static/app.js`.

- **Architecture** — the browser/server split, colored by trust boundary: which side of the wire can see plaintext and which only ever touches ciphertext.
- **Router / room topology** — how `send_message` broadcasts within a Socket.IO room versus how `send_dm` targets one socket id directly.
- **Direct-message flow** — the full path of a DM, including the branch where an offline recipient silently drops the message while the sender still gets an echo.

## View it

Open `index.html` directly, or enable GitHub Pages for this repo (Settings → Pages → deploy from `main` branch) to get a hosted link.

## Notes

- Single self-contained HTML file — no build step.
- Hovering a node or edge lights up its connected arrows.
- Each diagram card has zoom controls (`−` / `⟲` / `+`); zooming in past the card width makes the card scrollable.
