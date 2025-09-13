# 🎵 K Music Bot

**K Music Bot** is an advanced Discord music bot designed for your Discord servers. It offers a perfect music experience with YouTube music streaming, bass control, volume adjustment, and bilingual support.

## 🌟 Features

### 🎼 Music Features
- 🎵 **YouTube Music Support** - Supports YouTube links and song searches
- 🔊 **Volume Control** - Volume adjustment (0-100%)
- 🎚️ **Bass Control** - Bass adjustment (-10 to +10 range)
- ⏸️ **Playback Control** - Stop, pause, resume, skip commands
- 📝 **Queue Management** - Music queue display and management

### 🌍 Language Support
- 🇹🇷 **Turkish** - Full Turkish language support
- 🇺🇸 **English** - Complete English language support
- 🔄 **Dynamic Language Switching** - Per-user language preferences

### 🔒 Privacy & Security
- ✅ **GDPR/KVKV Compliant** - Safely handles user data
- 🚫 **Data Minimization** - Collects no unnecessary data
- 🔐 **Secure Logging** - Removes personal data from logs

## 📦 Installation

### Requirements
- Node.js 18.0.0 or higher
- Discord Bot Token
- FFmpeg (automatically installed)

### 1. Project Setup
```bash
# Clone the repository
git clone https://github.com/mda-team/k-music-bot.git
cd k-music-bot

# Install dependencies
npm install
```

### 2. Discord Bot Settings

#### Bot Permissions (Required):
- `Send Messages` - Send messages in channels
- `Use Slash Commands` - Use slash commands
- `Connect` - Connect to voice channels
- `Speak` - Speak in voice channels
- `Use Voice Activity` - Use voice activity detection

#### Intent Settings:
Enable these intents for your bot in Discord Developer Portal:
- `MESSAGE CONTENT INTENT`
- `GUILD MESSAGES`
- `GUILD VOICE STATES`

### 3. Starting the Bot

#### Windows:
```batch
start.bat
```

#### Linux/macOS:
```bash
chmod +x start.sh
./start.sh
```

#### Manual Start:
```bash
npm start
# or
node index.js
```

## 🎮 Commands

### 🎵 Music Commands (k! prefix)

| Command | Description | Usage |
|---------|-------------|-------|
| `k!play <song/link>` | Play music from YouTube | `k!play Deacon Blue Istanbul` |
| `k!stop` | Stop music and clear queue | `k!stop` |
| `k!pause` | Pause current track | `k!pause` |
| `k!resume` | Resume playback | `k!resume` |
| `k!skip` | Skip to next song | `k!skip` |
| `k!queue` | Show music queue | `k!queue` |
| `k!volume <0-100>` | Set volume level | `k!volume 50` |
| `k!bass <-10 to +10>` | Adjust bass level | `k!bass +5` |

### 🌍 Language Commands (k! prefix)

| Command | Description | Usage |
|---------|-------------|-------|
| `k!tr` | Switch to Turkish | `k!tr` |
| `k!en` | Switch to English | `k!en` |

### ⚡ Slash Commands (/ prefix)

| Command | Description | Usage |
|---------|-------------|-------|
| `/help` | Show all commands | `/help` |
| `/support` | Get support server link | `/support` |

## 🛠️ Development

### Project Structure
```
k-music-bot/
├── commands/          # Bot commands
│   ├── play.js        # Music playback
│   ├── volume.js      # Volume control
│   ├── bass.js        # Bass control
│   └── ...
├── events/            # Bot events
│   └── ready.js       # Bot ready event
├── utils/             # Utility functions
│   └── musicUtils.js  # Music operations
├── index.js           # Main bot file
├── config.json        # Bot configuration
├── language.js        # Language system
├── safelog.js         # GDPR compliant logging
└── package.json       # Project dependencies
```

### Technologies
- **discord.js v14** - Discord API wrapper
- **@discordjs/voice** - Voice channel management
- **ytdl-core & play-dl** - YouTube music streaming
- **ffmpeg-static** - Audio processing
- **Node.js 18+** - JavaScript runtime

## 🔧 Troubleshooting

### Common Issues

#### Bot not joining voice channel:
- Ensure the bot has `Connect` and `Speak` permissions
- Check if the voice channel has a user limit

#### YouTube videos not playing:
- Check your internet connection
- The bot automatically tries different YouTube sources

#### Commands not working:
- Make sure `MESSAGE CONTENT INTENT` is enabled
- Verify that the bot token is set correctly

#### Poor audio quality:
- Use `k!volume` and `k!bass` commands to adjust
- Check your internet connection speed

### Log Checking
```bash
# View logs
tail -f logs/bot-$(date +%Y-%m-%d).log

# Filter error logs
grep "ERROR" logs/bot-$(date +%Y-%m-%d).log
```

## 📄 License

This project is licensed under the [MIT License](https://github.com/Monsdea/K-Music/blob/main/LICENSE.md).

## 👥 Contact

- 🌐 **Website**: [GitHub](https://github.com/Monsdea/K-Music)
- 🐛 **Bug Reports**: [Issues](https://discord.gg/ZFDzgWynct)
- 📧 **Support**: Use the `/support` command in the Discord bot

## 🎯 Roadmap

- [ ] Spotify support
- [ ] Playlist saving
- [ ] Web dashboard
- [ ] More language support
- [ ] Lyrics display

---

**K Music Bot** - Developed with ❤️ by MDA Team.
