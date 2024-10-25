# Tick Manager

[![Modrinth](https://img.shields.io/modrinth/dt/tick-manager?color=00AF5C&label=downloads&logo=modrinth)](https://modrinth.com/datapack/tick-manager)
![Minecraft](https://img.shields.io/badge/Minecraft-1.20.x-blue)
![License](https://img.shields.io/github/license/Astra_Caelum/tick-manager)

A lightweight Minecraft datapack that automatically manages server random tick speed based on player presence to optimize performance.

## Features

- 🚀 Automatically freezes random ticks when no players are online
- ⚡ Instantly unfreezes when players join
- 📊 Server console logging for easy monitoring
- 🪶 Minimal performance impact
- ⚙️ Zero configuration needed

## Installation

1. Download the latest release from [Modrinth](https://modrinth.com/datapack/tick-manager) or the [Releases](../../releases) page
2. Place the datapack file in your world's `datapacks` folder
   ```
   world/
   └── datapacks/
       └── tick_manager.zip
   ```
3. Run `/reload` in-game or restart your server
4. That's it! The datapack will now automatically manage your server's tick speed

## How It Works

The datapack monitors player presence on your server. When the last player leaves, it starts a 1-minute timer. After this timer expires, it sets the `randomTickSpeed` to 0, effectively freezing random ticks to reduce server load. As soon as a player joins, it immediately restores the default tick speed (3) for normal gameplay.

All state changes are logged to the server console for easy monitoring.

## Commands

There are no commands needed to use this datapack. It works automatically!

## Compatibility

- Works with Minecraft Java Edition 1.20.x
- Compatible with most other datapacks and mods
- Can be safely added to or removed from existing worlds

## Performance Impact

The datapack is designed to be as lightweight as possible:
- Only runs necessary checks when state changes might occur
- Uses minimal scoreboard objectives
- No continuous player scanning
- No redstone or entities used

## For Developers

The datapack structure is organized as follows:
```
tick_manager/
├── pack.mcmeta
└── data/
    ├── minecraft/
    │   └── tags/
    │       └── functions/
    │           ├── tick.json
    │           └── load.json
    └── tick_manager/
        └── functions/
            ├── load.mcfunction
            ├── tick.mcfunction
            ├── start_empty_check.mcfunction
            ├── freeze_ticks.mcfunction
            └── unfreeze_ticks.mcfunction
```

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions:
1. Check the [Issues](../../issues) page for known problems
2. Create a new issue if your problem isn't already listed
3. Provide as much detail as possible, including:
   - Minecraft version
   - Server type (Paper, Vanilla, etc.)
   - Any relevant logs
   - Steps to reproduce the issue

## Credits

Created and maintained by [Astra_Caelum](https://github.com/Astra_Caelum)

---
<div align="center">
  
[![GitHub Profile](https://img.shields.io/badge/GitHub-Astra__Caelum-blue?style=flat&logo=github)](https://github.com/Astra_Caelum)
[![Modrinth Profile](https://img.shields.io/badge/Modrinth-Astra__Caelum-00AF5C?style=flat&logo=modrinth)](https://modrinth.com/user/Astra_Caelum)

</div>
