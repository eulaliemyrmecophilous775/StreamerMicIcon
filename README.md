# StreamerMicIcon

A lightweight, always-on-top Windows overlay that shows your default microphone's mute status as a floating icon. Built for streamers who forget to unmute.

![Windows](https://img.shields.io/badge/platform-Windows-blue)

## Preview

<p align="center">
  <img src="images/mic_live.png" alt="Mic Live" width="128">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="images/mic_muted.png" alt="Mic Muted" width="128">
</p>

<p align="center">
  <b>Live</b> (green) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <b>Muted</b> (red, flashing)
</p>

## Features

- **Transparent floating icon** — only the mic shape is visible, no window chrome
- **Real-time status** — polls the Windows default microphone every 250ms
- **Color-coded** — green when live, red when muted, gray if no mic detected
- **Flashing alert** — the icon pulses when muted so you never miss it
- **Draggable** — click and drag to reposition anywhere on screen
- **Always on top** — stays visible over games, OBS, browsers, etc.
- **Double-click to quit**

## Quick Start (portable exe)

Download `StreamerMicIcon.exe` from [Releases](https://github.com/michaelnemtsev/StreamerMicIcon/releases) and run it. No installation or Python needed.

## Run from Source

```bash
pip install -r requirements.txt
python streamer_mic_icon.py
```

## Build Portable exe

```bash
pip install pyinstaller
python -m PyInstaller --onefile --noconsole --name StreamerMicIcon streamer_mic_icon.py
```

The standalone exe will be in `dist/StreamerMicIcon.exe`.

## Dependencies

- [PyQt5](https://pypi.org/project/PyQt5/) — transparent window and rendering
- [pycaw](https://pypi.org/project/pycaw/) — Windows Core Audio API bindings
- [comtypes](https://pypi.org/project/comtypes/) — COM interface support

## License

MIT
