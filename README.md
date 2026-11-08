# WhisperCrypt

A tiny, offline-capable web app (PWA) for scrambling text messages between two people who share one secret key. Install it on your phone's home screen, agree on a key, and send scrambled messages over any channel.

## Features

- AES-256-GCM encryption (PBKDF2 key derivation, 200k iterations)
- Shared secret stored only on each device (localStorage)
- Scramble / Descramble tabs
- Copy, Share, and QR-code for scrambled text
- Recent-message history
- Works offline once installed

## Usage

1. Host the folder (e.g. GitHub Pages) and open the URL on both phones.
2. Install to home screen (Safari: Share → Add to Home Screen; Chrome: menu → Install app).
3. Both open the app → **Key** tab → enter the same secret phrase → Save. Agree on the key out of band (in person or by voice call).
4. To send: **Scramble** tab → type → Scramble → copy/share/QR.
5. To read: **Descramble** tab → paste → Descramble.

## Security notes

- The key never leaves the device; encryption happens locally.
- Without the shared key, the scrambled text cannot be read.
- No forward secrecy or sender authentication — fine for casual privacy, not high-threat scenarios.
- If you lose the key, messages cannot be recovered.

## License

MIT
