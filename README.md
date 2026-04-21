<div align="center">

# 🔐 Mila

### Private messaging, rebuilt from first principles.

![Status](https://img.shields.io/badge/status-coming%20soon-blueviolet?style=for-the-badge)
![Crypto](https://img.shields.io/badge/crypto-zero%20dependencies-ff6b6b?style=for-the-badge)
![Post Quantum](https://img.shields.io/badge/post--quantum-ready-00c9a7?style=for-the-badge)
![License](https://img.shields.io/badge/license-open%20source-4ecdc4?style=for-the-badge)

</div>

---

> Most messaging apps ask you to **trust them.**
> Mila asks you to **read the code.**

---

## 🚨 The Problem with Everyone Else

| | WhatsApp | Telegram | Signal | **Mila** |
|---|---|---|---|---|
| Owned by surveillance ad company | ✅ Meta | ❌ | ❌ | ❌ |
| E2E encrypted by default | ✅ | ❌ | ✅ | ✅ |
| Server sees sender identity | ✅ | ✅ | ✅ | ❌ |
| Third-party crypto libraries | ✅ | ✅ | ✅ | ❌ |
| Post-quantum encryption | ❌ | ❌ | ✅ | ✅ |
| Metadata-blind relay | ❌ | ❌ | ❌ | ✅ |
| Keys encrypted on device | ⚠️ | ❌ | ✅ | ✅ |
| E2E encrypted group calls | ❌ | ❌ | ✅ | ✅ |

**WhatsApp** is owned by Meta — the largest surveillance advertising company on the planet. Every contact list, every "who talked to whom and when," feeds their data graph even if message content is encrypted.

**Telegram** isn't end-to-end encrypted by default, stores your messages on their servers in plaintext, and has handed over user data to governments on request.

**Signal** is the gold standard — but it still knows you exist. It sees your phone number, your registration timestamp, and which servers your messages route through.

---

## 🏗️ Mila is Different at the Architecture Level

### 🙈 The Server is Blind

Mila's relay is a **dumb mailbox** — it stores encrypted blobs and routes them by ID. It has no message logic, no contact graph, no metadata to subpoena.

**Sealed Sender** encryption means the relay never learns who sent a message to whom.

> Not *"we promise not to look."* — **Technically cannot look.**

---

### 🔬 No Borrowed Crypto

Every cryptographic protocol is implemented **from scratch** using low-level primitives:

- 🔑 **X3DH** — Asynchronous key agreement
- 🔄 **Double Ratchet** — Forward-secret message encryption
- 🫥 **Sealed Sender** — Anonymous delivery
- 👥 **SenderKey** — Efficient group encryption
- ⚛️ **PQXDH + ML-KEM** — Post-quantum key exchange

No Signal library. No OpenSSL. No third-party black box to audit or trust. **The math is in the open, in the code, readable by anyone.**

---

### ⚛️ Post-Quantum Ready

Mila integrates post-quantum key exchange using **ML-KEM** so that conversations started today are safe against future quantum computers.

Signal added this in 2023. WhatsApp and Telegram haven't.

---

### 🔒 Your Keys, Your Device

Identity keys never leave your device unencrypted. Local storage is protected by:

- **Argon2id** — Memory-hard key derivation
- **ChaCha20-Poly1305** — Authenticated encryption

There is no cloud backup that can be court-ordered.

---

### 📞 Group Calls, Fully Encrypted

Voice and video calls — 1:1 and group — are end-to-end encrypted through a **self-hosted SFU**. No call metadata routed through a third-party CDN.

---

<div align="center">

## 🚀 Coming Soon

*Built for people who don't just want to be told their messages are private —*
*but want to know exactly why.*

![Rust](https://img.shields.io/badge/built%20with-Rust-f74c00?style=flat-square&logo=rust)
![TypeScript](https://img.shields.io/badge/mobile-TypeScript-3178c6?style=flat-square&logo=typescript)
![React Native](https://img.shields.io/badge/app-React%20Native-61dafb?style=flat-square&logo=react)

</div>
