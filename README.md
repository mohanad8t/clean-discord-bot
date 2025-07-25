# ⚡ Clean Discord Bot Template

A clean and minimal starter template for a modern Discord bot using `discord.js`.

## 📦 Features

- 🧱 Modular structure (commands & events)
- 💬 Slash commands support
- 🚀 Easy deployment
- 🧼 Clean code & fully customizable
- 📁 Auto command loader

---

## 🔧 Requirements

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- A Discord bot token from the [Discord Developer Portal](https://discord.com/developers/applications)

---

## 📁 Folder Structure

```
clean-discord-bot/
│
├── commands/           # All slash commands
│   └── ping.js
│
├── events/             # All event listeners
│   └── ready.js
│
├── config.js           # Bot configuration
├── deploy-commands.js  # Script to register slash commands
└── index.js            # Bot entry point
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/mohanad8t/clean-discord-bot
cd clean-discord-bot
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set your bot token
Edit `config.js`:
```js
module.exports = {
  token: 'YOUR_BOT_TOKEN_HERE',
  clientId: 'YOUR_CLIENT_ID',
  guildId: 'YOUR_GUILD_ID' // Optional for testing
};
```

### 4. Deploy commands
```bash
node deploy-commands.js
```

### 5. Start the bot
```bash
npm start
```

---

## ✨ Example Command

```js
// commands/ping.js
const { SlashCommandBuilder } = require('discord.js');

module.exports = {
  data: new SlashCommandBuilder().setName('ping').setDescription('Replies with Pong!'),
  async execute(interaction) {
    await interaction.reply('🏓 Pong!');
  },
};
```

---

## 🤝 Contribution

Feel free to fork and improve this template. PRs are welcome!

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
