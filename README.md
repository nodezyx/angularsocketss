
<div align="center">  
  <h1>✨ @angularsockets/elaina-bail</h1>  
  <p><em>Custom WhatsApp library built upon Baileys — enhanced, modernized, and elegant ✨</em></p>
  
  <img src="https://files.catbox.moe/dmz2fn.jpg" width="300" alt="Elaina Bail Banner" />  

---

  <p>  
    <a href="https://www.npmjs.com/package/@angularsockets/elaina-bail">  
      <img src="https://img.shields.io/npm/v/@angularsockets/elaina-bail?color=blueviolet&label=version&logo=npm" alt="npm version" />  
    </a>  
    <a href="https://www.npmjs.com/package/@angularsockets/elaina-bail">  
      <img src="https://img.shields.io/npm/dt/@angularsockets/elaina-bail?color=blueviolet&label=downloads&logo=npm" alt="npm downloads" />  
    </a>  
    <a href="https://whatsapp.com/channel/0029VapYyKEGufIpsd3Rja2C">  
      <img src="https://img.shields.io/badge/Join-WhatsApp%20Channel-25D366?logo=whatsapp&logoColor=white" alt="WhatsApp Channel" />  
    </a>  
  </p>  
</div>

<p align="center">  
  <a href="https://elaina-bail.vercel.app">  
    <img src="https://img.shields.io/badge/Documentation-Baileys-blue?style=for-the-badge&logo=readthedocs&logoColor=white" alt="View Documentation">  
  </a>  
</p>

---

## 📌 Overview

> **elaina-bail** is a refined version of the Baileys library with cleaner API usage, exclusive features like album messaging, newsletter controls, and full-size profile uploads — tailored for modern WhatsApp automation needs.

### Current Version: **1.4.0**

> **Update Information**

All update information is now redirected to the WhatsApp channel:

<a href="https://whatsapp.com/channel/0029VapYyKEGufIpsd3Rja2C">
  <img src="https://img.shields.io/badge/Join-WhatsApp%20Channel-25D366?logo=whatsapp&logoColor=white" alt="WhatsApp Channel" />
</a>

---

## 📦 Installation

### Via package.json Fork Baileys (NPM)

**@whiskeysockets/baileys**

```json
"dependencies": {  
  "@whiskeysockets/baileys": "npm:@angularsockets/elaina-bail"  
}
```

**@adiwajsing/baileys**

```json
"dependencies": {  
  "@adiwajshing/baileys": "npm:@angularsockets/elaina-bail"  
}
```

### Or via terminal

```bash
npm install elaina-bail@npm:@angularsockets/elaina-bail
```

### Importing (for those who don't fork another repository)

**ESM**

```javascript
import makeWASocket from '@angularsockets/elaina-bail'
```

**CJS**

```javascript
const { default: makeWASocket } = require('@angularsockets/elaina-bail')
```

---

## 🌟 Key Features

| Category | Description |
|----------|-------------|
| 📢 Channels | Seamlessly send messages to WhatsApp Channels |
| 🖱️ Buttons | Create interactive messages with button options and quick replies |
| 🖼️ Albums | Send grouped images or videos as an album (carousel-like format) |
| 👤 LID Grouping | Handle group operations using the latest @lid addressing style |
| 🤖 AI Message Style | Add a stylized "AI" icon to messages |
| 📷 HD Profile Pics | Upload full-size profile pictures without cropping |
| 🔐 Pairing Code | Generate custom alphanumeric pairing codes |
| 🛠️ Dev Experience | Reduced noise from logs with optimized libsignal printouts |

---

## 💡 Use Case Examples

<details>  
<summary><strong>📬 Newsletter Control</strong></summary>

```javascript
// Create a newsletter  
await sock.newsletterCreate("Elaina Updates");  
  
// Change description  
await sock.newsletterUpdateDescription("elaina@newsletter", "Fresh updates weekly");  
  
// Send a reaction to a channel message  
await sock.newsletterReactMessage("elaina@newsletter", "175", "🔥");
```

</details>

<details>  
<summary><strong>📌 Interactive Messaging</strong></summary>

```javascript
const buttons = [  
  { buttonId: 'btn1', buttonText: { displayText: 'Click Me' }, type: 1 },  
  { buttonId: 'btn2', buttonText: { displayText: 'Visit Site' }, type: 1 }  
];  
  
const msg = {  
  text: "Choose one:",  
  footer: "From Elaina with love 💜",  
  buttons,  
  headerType: 1  
};  
  
await sock.sendMessage(id, msg, { quoted: null });
```

</details>

<details>  
<summary><strong>🖼️ Send Album</strong></summary>

```javascript
const media = [  
  { image: { url: "https://example.com/pic1.jpg" } },  
  { video: { url: "https://example.com/clip.mp4" } }  
];  
  
await sock.sendMessage(id, { album: media, caption: "Memories 💫" }, { quoted: null });
```

</details>

<details>  
<summary><strong>🔐 Pairing with Custom Code</strong></summary>

```javascript
const code = await sock.requestPairingCode("62xxxxxxxxxx", "ELAINA01");  
console.log("Your Pairing Code:", code);
```

</details>

<details>  
<summary><strong>📊 Poll Creation</strong></summary>

```javascript
const pollMessage = {  
  name: "Favorite Color?",  
  values: ["Red", "Blue", "Green"],  
  selectableCount: 1  
};  
  
await sock.sendMessage(id, { poll: pollMessage });
```

</details>

<details>  
<summary><strong>📍 Location Sharing</strong></summary>

```javascript
const locationMessage = {  
  degreesLatitude: 37.422,  
  degreesLongitude: -122.084,  
  name: "Googleplex",  
  address: "1600 Amphitheatre Pkwy, Mountain View, CA 94043"  
};  
  
await sock.sendMessage(id, { location: locationMessage });
```

</details>

<details>  
<summary><strong>👥 Group Management</strong></summary>

```javascript
// Create group  
const group = await sock.groupCreate("My New Group", [number1, number2]);  
  
// Add participants  
await sock.groupAdd(group.id, [number3, number4]);  
  
// Change group description  
await sock.groupUpdateDescription(group.id, "This is our awesome group!");
```

</details>

---

**Note:** Replace `id` with the actual recipient ID and `sock` with your WhatsApp socket connection variable.

---

## 🐞 Found a Bug?

Please contact the maintainer directly via WhatsApp:

<p align="center">  
  <a href="https://wa.me/263719647303" target="_blank">  
    <img alt="WhatsApp" src="https://img.shields.io/badge/Chat%20on%20WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white">  
  </a>  
</p>

---

## 🙏 Credits

**Creator:** MR FRANK OFC

- 🌐 Website: [mrfrankofc.gleeze.com](https://mrfrankofc.gleeze.com)
- 💻 GitHub: [@mrfr8nk](https://github.com/mrfr8nk)

**Special Thanks:**
- RexyHayanais
- Nystar

> [!CAUTION]
> Built on top of the WhiskeySockets/Baileys project. All original core logic credits go to their team. elaina-bail extends it with thoughtful UX and DX improvements.

---

<div align="center">
  <p>Made with 💜 by MR FRANK OFC</p>
</div>



