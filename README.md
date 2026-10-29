# We in here being nice 💗

A lightweight party game about giving genuine compliments without giving away your secret mission.

One device runs the **host screen** (TV, projector, or computer). Everyone else scans the QR code on their phone, joins by name, and gets a secret target when the host starts.

## How to play

1. Open the published website on the host device.
2. Leave the host screen open so the QR code remains visible.
3. Players scan the QR code, enter their names, and join the lobby.
4. With at least three players, the host starts the round.
5. Each player privately reveals their target, works a genuine compliment into conversation, and taps **Mark done**.
6. Debrief, reveal targets if desired, and reshuffle for another round.

The host view is made for a TV/desktop screen; the private mission view is designed for phones.

## Publish with GitHub Pages

This is a plain static HTML site. No build or API key is needed.

1. Open **[Settings → Pages](https://github.com/tbenitz/we-in-here-being-nice/settings/pages)** in this repository.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose **main** and **/(root)**, then click **Save**.
4. After GitHub finishes publishing, open **https://tbenitz.github.io/we-in-here-being-nice/**.

The on-screen QR code links back to the published page with its room identifier. Keep the host tab open during a live game.

## Notes

- Live joins use **PeerJS signaling and WebRTC**, so devices need internet connectivity. PeerJS is loaded from a CDN for live rooms.
- The game can also run as a standalone HTML file with a shared/pass-the-phone experience.
- Host state is stored in the host browser's local storage. Clearing site data or closing the host during a game can interrupt play.
- Mission assignments are intended for casual party-game privacy; the game does not provide account-based authentication.
- No databases, cloud AI APIs, or paid services are required.

## Implementation

Everything is in **index.html**: HTML, CSS, vanilla JavaScript, and an embedded QR encoder. The QR encoder includes its license attribution in the code.
