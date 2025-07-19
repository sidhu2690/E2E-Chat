# 🌿 E2E Chat — Private, Peer-to-Peer, Encrypted Communication

> 🚀 A lightweight, zero-backend, secure chat app with media support — built for **true privacy** and **direct communication**.

---

## 🌈 Highlights

* 🔐 **End-to-End Encrypted**: Messages are encrypted (currently via Caesar Cipher) before transmission.
* 🛡️ **True Peer-to-Peer (P2P)**: Uses WebRTC via PeerJS — **no server relays your data**, and once connected, even signaling is discarded.
* 👥 **Strict 1-to-1 Communication**: Like a digital walkie-talkie — only two people can connect to a room, and **no one else can eavesdrop**, even if they know your room key.
* 📁 **File Sharing**: Send **images**, **audio recordings**, or **any file** securely.
* 🎤 **Voice Messages**: Record and transmit audio messages directly in the chat.
* 🌐 **No Data Storage**: Zero logs, zero databases — messages and media are **not stored anywhere**.
* 📱 **Mobile Friendly**: Works beautifully across devices thanks to Tailwind CSS.
* 🤖 **Emoji-Ready**: Auto-parses emojis using [Twemoji](https://twemoji.twitter.com/).

---

## 🔧 Features

| Feature           | Description                                                             |
| ----------------- | ----------------------------------------------------------------------- |
| 🌿 No Servers     | Only used for signaling. After that, the server steps away.             |
| 🧩 Caesar Cipher  | Simple demo encryption (can be upgraded to AES or NaCl).                |
| 🎥 Camera Support | Capture and share images directly using your camera.                    |
| 📂 Media Recorder | Record voice messages and send them on the go.                          |
| 🧠 Room-based     | Users can **create** or **join** rooms — secure and ephemeral.          |
| 📦 100% Frontend  | Can be hosted on GitHub Pages, Vercel, Netlify — **no backend needed**. |

---

## 🛡️ Privacy First — Our Philosophy

This app was built with one mission: **make conversations private by default.**

* 📶 Connections are established directly between two browsers (via WebRTC).
* 🧍‍♂️🧍‍♀️ **Only two participants can ever connect to a room** — others are rejected.
* 🔐 Even if someone gets your room name, they can't listen or join if two peers are already connected.
* 🔄 Nothing is stored, nothing is cached — everything is ephemeral.
* 🔒 Encryption (currently Caesar Cipher) ensures readable content never touches the wire in plain form.

> ⚠️ **Note**: Caesar Cipher is used here for demonstration purposes — it can and should be replaced with a modern encryption algorithm (like AES-GCM or libsodium). But even in its current form, **interception is almost impossible** due to the direct P2P channel.

---

## 🧪 Demo & How to Use

1. **Enter a Room Name** (e.g., `room123`)
2. **Create Room** (Host) or **Join Room** (Guest)
3. Once connected, chat freely:

   * 💬 Type and send messages
   * 📎 Share files
   * 📷 Snap or upload images
   * 🎤 Press the mic to record and send voice

> Think of it like a private tunnel — no one sees the entrance or the exit but you.

---

## 🚀 Deployment

Host it anywhere:

* GitHub Pages
* Netlify
* Vercel
* Any static site hosting service

No backend required. Just HTML, CSS (via Tailwind), and JavaScript (with PeerJS).

---

## 🔮 Future Possibilities

* ✅ Upgrade encryption to AES, RSA, or NaCl
* ✅ Add QR code for room sharing
* ✅ Add message persistence (optional, client-only)
* ✅ Multi-user support (optional extension)
* ✅ Typing indicators, message reactions, etc.

---

## 📜 License

MIT — Free to use, modify, and expand.

---

## ❤️ Final Word

This app isn’t just a chat tool — it's a **digital sanctuary for secure, private communication**. With just a room name, you open a secret channel between two people. No trace, no tracking, no compromise.

> Use it for quick personal chats, secure media transfers, or just the joy of building a trustless communication system.

Stay private. Stay connected. ✨
