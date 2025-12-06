# Ernest Tech House Session Generator

Professional WhatsApp session generator for **Ellie v1**, **A.C.E.P.H.A.R**, and **ERNEST V2** bots.

## 🤖 About

This session generator is created by **Pease Ernest** of **Ernst Tech House** to provide a secure and reliable way to generate WhatsApp bot sessions.

## ✨ Features

- 🔗 **Pair Code Method** - Quick pairing using 8-digit code
- 📱 **QR Code Method** - Traditional QR scanning
- 📦 **Direct File Transfer** - Sends creds.json file directly (no base64)
- 🎵 **Welcome Package** - Includes avatar image and welcome audio
- 🔒 **Secure** - Encrypted session data
- ⚡ **Fast** - Lightning-fast generation

## 🚀 Supported Bots

- Ellie v1
- A.C.E.P.H.A.R
- ERNEST V2

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/mauricegift/gifted-session.git
cd gifted-session
```

2. Install dependencies:
```bash
npm install
```

3. Create assets folder and add files:
```bash
mkdir assets
# Add avatar.jpeg and welcome.mp3 to the assets folder
```

4. Start the server:
```bash
npm start
```

## 🔧 Usage in Your Bot

```javascript
const fs = require('fs');
const path = require('path');
const sessionDir = path.join(__dirname, 'session');
const credsPath = path.join(sessionDir, 'creds.json');

// Simply use the creds.json file directly
async function loadSession() {
    try {
        if (!fs.existsSync(sessionDir)) {
            fs.mkdirSync(sessionDir, { recursive: true });
        }

        // Copy your received creds.json to the session directory
        // The file is sent directly, no decompression needed!
        
        console.log("✅ Session loaded successfully");
    } catch (e) {
        console.error("❌ Session Error:", e.message);
        throw e;
    }
}

// In your bot startup
const { state, saveCreds } = await useMultiFileAuthState(sessionDir);
```

## 🌐 Deployment

### Heroku
[![Deploy to Heroku](https://img.shields.io/badge/Deploy%20To%20Heroku-purple?style=for-the-badge&logo=heroku)](https://dashboard.heroku.com/new?template=https://github.com/mauricegift/gifted-session)

### Render
[![Deploy to Render](https://img.shields.io/badge/Deploy%20To%20Render-black?style=for-the-badge&logo=render)](https://dashboard.render.com)

### Koyeb
[![Deploy to Koyeb](https://img.shields.io/badge/Deploy%20To%20Koyeb-blue?style=for-the-badge&logo=koyeb)](https://app.koyeb.com)

## 📁 Required Files

Place these files in the `assets` folder:
- `avatar.jpeg` - Bot avatar image
- `welcome.mp3` - Welcome audio file

## 👨‍💻 Creator

**Pease Ernest**  
Ernst Tech House

## 📱 Connect With Us

- 📢 [Telegram Channel](https://t.me/ernesttechhouse)
- 💬 [WhatsApp Channel](https://whatsapp.com/channel/0029VayK4ty7DAWr0jeCZx0i)
- 🐙 [GitHub](https://github.com/Ernest12287/gifted-session)

## 📝 License

GPL-3.0 License

## 🙏 Credits

Special thanks to:
- Baileys Library
- WhiskeySockets
- All contributors

---

Made with ❤️ by Ernst Tech House