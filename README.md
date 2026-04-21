# Mila — Private messaging, rebuilt from first principles.

Most messaging apps ask you to trust them. WhatsApp is owned by Meta — the largest surveillance advertising company on the planet. Every contact list, every "who talked to whom and when," feeds their data graph even if message content is encrypted. Telegram isn't end-to-end encrypted by default, stores your messages on their servers in plaintext, and has handed over user data to governments. Signal is the gold standard — but it still knows you exist. It sees your phone number, your registration timestamp, and which servers your messages route through.

Mila is different at the architecture level.

## The server is blind.

Mila's relay is a dumb mailbox — it stores encrypted blobs and routes them by ID. It has no message logic, no contact graph, no metadata to subpoena. Sealed Sender encryption means the relay never learns who sent a message to whom. Not "we promise not to look." *Technically cannot look.*

## No borrowed crypto.

Every cryptographic protocol — X3DH key agreement, Double Ratchet message encryption, Sealed Sender, group SenderKey, post-quantum key exchange (PQXDH) — is implemented from scratch using low-level primitives. No Signal library. No OpenSSL. No third-party black box to audit or trust. The math is in the open, in the code, readable by anyone.

## Post-quantum ready.

Mila integrates post-quantum key exchange using ML-KEM so that conversations started today are safe against future quantum computers. Signal added this in 2023. WhatsApp and Telegram haven't.

## Your keys, your device.

Identity keys never leave your device unencrypted. Local storage is protected by Argon2id key derivation and ChaCha20-Poly1305 encryption — the same primitives used in modern TLS. There is no cloud backup that can be court-ordered.

## Group calls, fully encrypted.

Voice and video calls — 1:1 and group — are end-to-end encrypted through a self-hosted SFU. No call metadata routed through a third-party CDN.

---

*Mila is coming. Built for people who don't just want to be told their messages are private — but want to know exactly why.*
