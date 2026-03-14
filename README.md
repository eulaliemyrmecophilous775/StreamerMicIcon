# StreamerMicIcon

A lightweight, always-on-top Windows overlay that shows your default microphone's mute status as a floating icon. Built for streamers who forget to unmute.

![Windows](https://img.shields.io/badge/platform-Windows-blue)

## Features

- **Transparent floating icon** — only the mic shape is visible, no window chrome
- **Real-time status** — polls the Windows default microphone every 250ms
- **Color-coded** — green when live, red when muted, gray if no mic detected
- **Flashing alert** — the icon pulses when muted so you never miss it
- **Draggable** — click and drag to reposition anywhere on screen
- **Always on top** — stays visible over games, OBS, browsers, etc.
- **Double-click to quit**

## Quick Start (portable exe)

Download `MicMute.exe` from [Releases](https://github.com/michaelnemtsev/StreamerMicIcon/releases) and run it. No installation or Python needed.

## Run from Source

```bash
pip install -r requirements.txt
python mic_monitor.py
```

## Build Portable exe

```bash
pip install pyinstaller
python -m PyInstaller --onefile --noconsole --name MicMute mic_monitor.py
```

The standalone exe will be in `dist/MicMute.exe`.

## Dependencies

- [PyQt5](https://pypi.org/project/PyQt5/) — transparent window and rendering
- [pycaw](https://pypi.org/project/pycaw/) — Windows Core Audio API bindings
- [comtypes](https://pypi.org/project/comtypes/) — COM interface support

## License

MIT
