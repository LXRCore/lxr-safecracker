# lxr-safecracker ![Version](https://img.shields.io/badge/version-1.0.0-blue) ![Status](https://img.shields.io/badge/status-active-brightgreen) ![License](https://img.shields.io/github/license/LXRCore/lxr-safecracker)

**lxr-safecracker** is a safe cracking minigame for **LXRCore**. This minigame is a fun and engaging addition for RedM servers running on the **LXRCore** framework. The goal is to simulate cracking safes as a part of various roleplay scenarios, providing an immersive experience for players.

## Features

- Fully customizable safe cracking minigame.
- Immersive lockpicking and cracking mechanics.
- Adjustable difficulty levels based on the lock type.
- Can be integrated with heist missions, roleplay events, or treasure hunts.

## Installation

1. Clone or download the repository into your `lxr` directory.
2. Ensure that **LXRCore** is installed and running.
3. Add the following to your `server.cfg`:

```bash
ensure lxr-core
ensure lxr-safecracker
```

## Configuration

The safe cracking configuration can be customized in the `config.lua` file. Below is a summary of the main options:

### Basic Configuration

```lua
Config = Config or {}

Config.Difficulty = {
    Easy = 1,
    Medium = 2,
    Hard = 3,
}

Config.CrackerTypes = {
    "Standard", -- Basic lock cracking
    "Advanced", -- Advanced lock cracking with additional steps
}

Config.MinigameDuration = {
    Easy = 30, -- 30 seconds for easy locks
    Medium = 60, -- 60 seconds for medium locks
    Hard = 90 -- 90 seconds for hard locks
}

Config.Rewards = {
    Easy = {cash = 100, items = {"GoldBar"}},
    Medium = {cash = 500, items = {"Diamond"}},
    Hard = {cash = 1000, items = {"Emerald"}}
}
```

### Example Setup

Here’s an example setup where the cracking difficulty is set to medium, with a 60-second timer and a reward system of $500 cash and a diamond:

```lua
Config = {
    Difficulty = "Medium",
    CrackerTypes = {"Advanced"},
    MinigameDuration = {
        Easy = 30,
        Medium = 60,
        Hard = 90
    },
    Rewards = {
        Medium = {cash = 500, items = {"Diamond"}}
    }
}
```

## License

This project is licensed under the MIT License.

## Credits

- Special thanks to [JAM_SafeCracker](https://github.com/JustAnotherModder/JAM_SafeCracker) for providing the original inspiration for this minigame.
- This version is specifically optimized for **LXRCore** and **RedM** integration.