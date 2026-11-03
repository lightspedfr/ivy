static-ivy — hosted games edition

Upload this entire folder to a static HTTPS host and open index.html or the
folder URL ending in /. It also works on localhost HTTP. It discovers its
base path automatically and uses hash navigation, with no SPA rewrite needed.

Games load in an isolated iframe from:
https://games.ivy.rest/static/games/index.html
The hosted library provides Lumin, UGS and GN-Math. Game HTML, thumbnails and
catalogues are not included in this smaller download. Games require access to
the hosted service. Existing local game-save messages remain bound to the
expected iframe source and exact game origin; saves stay on your static host.

tejmarcs/teiloivartlu, their WASM and transports remain bundled locally.
Edit wisp.json to change the ordered WebSocket Wisp server list. API base is
https://ivy.rest. Secure account/chat/billing features open on central Ivy.

Serve .mjs/.js as JavaScript and .wasm as application/wasm. Service worker
scope is this folder. Avoid blanket COEP=require-corp headers because they can
block externally hosted games. HTTPS or localhost is required for the proxy.

Keep this folder structure intact. No Node process, npm install, private key,
server source, account database or runtime secret is part of this deployment.
Original dependency license notices are retained in licenses/.
