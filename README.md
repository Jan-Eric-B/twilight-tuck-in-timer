# <img src="docs/images/AppIcon.png" width="30" height="30" alt="Twilight Tuck-In Timer icon"> Twilight Tuck-In Timer

[![Latest release](https://img.shields.io/github/v/release/Jan-Eric-B/twilight-tuck-in-timer)](https://github.com/Jan-Eric-B/twilight-tuck-in-timer/releases/latest)
[![License](https://img.shields.io/github/license/Jan-Eric-B/twilight-tuck-in-timer)](LICENSE)
[![.NET 11](https://img.shields.io/badge/.NET-11-512BD4)](https://dotnet.microsoft.com/download/dotnet/11.0)
[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://paypal.me/JanEricBe)

A tiny Windows app for setting a sleep timer. Set a time when the PC should shut down.

Originally made for my girlfriend, who likes to have something play in the background on the PC while trying to sleep.

<img src="docs/images/Showcase_MainWindow.png" alt="Twilight Tuck-In Timer - Main window">

Built with WPF, .NET 11 and [WPF UI](https://github.com/lepoco/wpfui). 
It uses the built-in Windows `shutdown` command and it can be cancelled in the app as well.

## Features

- **Simple sleep timer** - Set time (hours and minutes) and press start!
- **Cancelable** - You can cancel it again directly in the app.
- **Remembers your last timer** - The hours and minutes you used last time are loaded on start.
- **No installation** - A single portable `.exe`, no .NET runtime required.

## Requirements

- Windows 10 or Windows 11 (x64)

## Installation

Download `TTIT.exe` from the [Releases](../../releases) page and run it.

> [!NOTE]
> The exe is not code-signed, so Windows SmartScreen may show a warning on first launch. Click **More info** → **Run anyway**.

## Usage

1. Enter the **hours** and **minutes** until the PC should shut down.
2. Click **Schedule Shutdown**.
3. To stop it, click **Cancel Shutdown**.

Scheduling a new timer replaces any shutdown that was already scheduled.

> [!WARNING]
> When the timer runs out, Windows shuts down and unsaved work in other applications may be lost.

## Building from Source

**Prerequisites:**

- [.NET 11 SDK](https://dotnet.microsoft.com/download/dotnet/11.0)

```bash
git clone https://github.com/Jan-Eric-B/twilight-tuck-in-timer.git
cd twilight-tuck-in-timer
dotnet publish src/TTIT/TTIT.csproj -c Release -o publish
```

This produces a self-contained single-file `publish/TTIT.exe`.

## Dependencies

| Library                                                             | License    | Purpose                         |
| ------------------------------------------------------------------- | ---------- | ------------------------------- |
| [WPF UI](https://github.com/lepoco/wpfui)                           | MIT        | Fluent UI controls              |
| [WpfAnimatedGif](https://github.com/XamlAnimatedGif/WpfAnimatedGif) | Apache 2.0 | Animated GIF in the help window |

## License

Twilight Tuck-In Timer is licensed under the **GNU General Public License v3.0**. See [LICENSE](LICENSE) for the full text.
