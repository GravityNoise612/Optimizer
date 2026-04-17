# Gaming Settings Optimizer

A powerful browser-based tool that scans your installed games and recommends optimal in-game settings based on your PC hardware.

🎮 **[Open the App →](#how-to-use)**

## Features

- ✅ **Hardware Detection** - Automatically detects your GPU, CPU, RAM, and display settings
- ✅ **Game Scanner** - Scans your game folders for installed titles
- ✅ **Smart Recommendations** - Provides detailed setting recommendations (Low/Medium/High/Ultra) for 100+ games
- ✅ **Executable-Based Detection** - Uses actual game .exe files for accurate detection (no false positives)
- ✅ **Persistent Storage** - Saves your specs and game library locally in your browser
- ✅ **No Installation Required** - Runs entirely in your browser, no downloads or setup needed
- ✅ **Offline Compatible** - Works without internet after first load
- ✅ **Windows Compatible** - Optimized for Windows with File System Access API support

## How to Use

### 1. **Check Your Hardware**
The app automatically detects:
- GPU model and tier (Low/Medium/High/Ultra)
- CPU cores
- System RAM
- Display resolution and refresh rate
- Performance tier badge

### 2. **Scan Your Games**
Click "Browse & Scan Games" and select your game installation folder (usually `C:\Program Files\Steam\steamapps\common` or similar).

The scanner will:
- Scan only top-level game folders
- Look for game executable files (.exe)
- Match executables to a database of 100+ games
- Add discovered games to your list

### 3. **View Game Settings**
Click on any game to see recommended settings across 4 performance tiers:
- **Low** - 1080p, 60 FPS
- **Medium** - 1440p, 60 FPS  
- **High** - 1440p, 60-120 FPS
- **Ultra** - 4K, 120+ FPS

## Supported Games (100+)

### AAA Titles
Cyberpunk 2077, Elden Ring, Starfield, Black Myth: Wukong, Dragon Age: The Veilguard, Final Fantasy XVI, Alan Wake 2, S.T.A.L.K.E.R. 2, Warhammer 40K: Space Marine 2, Palworld, HELLDIVERS 2, and more...

### Competitive/Multiplayer
Fortnite, VALORANT, Counter-Strike 2, Dota 2, League of Legends, Apex Legends, Overwatch 2, Destiny 2, World of Warcraft, Rainbow Six Siege, and more...

### Survival/Sandbox
Minecraft, Rust, Valheim, Grounded, Subnautica, No Man's Sky, DayZ, Conan Exiles, and more...

### RPG/Action
The Witcher 3, Grand Theft Auto V, Red Dead Redemption 2, Skyrim, Fallout 4, God of War, Ghost of Tsushima, Spider-Man, and more...

### Indie Games
Stardew Valley, Hollow Knight, Celeste, Terraria, Factorio, RimWorld, Undertale, Cuphead, and more...

## Game Detection Method

The scanner uses **exact executable filename matching** to ensure accuracy:
- Looks for specific .exe files (e.g., `fortnite.exe`, `eldenring.exe`)
- Only matches top-level game folders
- No substring or keyword matching
- Zero false positives

## Browser Requirements

- **Chrome/Edge/Opera** - Full support with File System Access API
- **Firefox/Safari** - Limited support (cannot use folder picker, but can still view settings)

## Data Storage

All data is stored **locally in your browser**:
- ✅ Your hardware specs
- ✅ Discovered game list
- ✅ No data sent to servers
- ✅ Clear browser data to reset

## GPU Tier Detection

The app automatically categorizes your GPU:

| Tier | Examples |
|------|----------|
| **ULTRA** | RTX 5090, 4090, RTX 4080 Super, RX 9070 XT, 9080 |
| **HIGH** | RTX 5080, 5070 Ti, RTX 4070, 4070 Ti, RX 7800 XT |
| **MEDIUM** | RTX 4060, 3070, 3060 Ti, RX 7600, 6700 |
| **LOW** | RTX 3050, 2060, GTX 1660, 1650, RX 5500 |

## Installation

### Option 1: Use the Live Version
Visit the app directly in your browser

### Option 2: Self-Host on GitHub Pages

1. **Fork this repository** to your GitHub account
2. **Enable GitHub Pages** in repository settings:
   - Go to Settings → Pages
   - Source: Deploy from branch
   - Branch: `main` (or your default branch)
3. **Access your site** at: `https://yourusername.github.io/gaming-settings-optimizer/`

### Option 3: Local Use
1. Download `index.html`
2. Open in Edge, Chrome, or Opera browser
3. Click "Browse & Scan Games" to get started

## Limitations

- **File System Access API** only works in Chromium browsers (Chrome, Edge, Opera)
- **Scanner requires read access** to your game folders
- **DirectStorage API limitations** - cannot access drive letters directly, shows relative paths
- **Some games may not be detected** if they use unusual folder structures or executable names

## Troubleshooting

### Games not showing up in scan?
- Ensure the game folder is at the top level (not nested in subfolders)
- Check if the game has a matching .exe file
- Try selecting the parent directory and scanning again

### Performance tier showing as "Medium"?
- Your GPU may not be in the database
- Manual override available in the Edit Specs button

### Settings showing "Coming soon"?
- That game is detected but doesn't have detailed settings yet
- Check back for updates as the database grows

## Contributing

Have a game not in the database? Or better settings recommendations?

1. Open an issue with the game name and your PC specs
2. Include what settings you use and your FPS targets
3. PRs welcome to add new games!

## Technology Stack

- **HTML5** - Structure
- **CSS3** - Dark mode UI
- **Vanilla JavaScript** - No dependencies
- **WebGL** - GPU detection
- **File System Access API** - Folder scanning
- **localStorage** - Data persistence

## License

MIT License - Feel free to use, modify, and distribute

## Disclaimer

These are **recommended baseline settings** based on GPU tier. Actual performance depends on:
- Your specific CPU and RAM
- Driver updates
- Game updates and patches
- Background processes
- Monitor refresh rate

Always test settings in-game and adjust to your preferences!

## Support

Found a bug or have a feature request?  
Open an issue on GitHub

---

Made with ⚡ for gamers who want optimal performance without the guesswork.
