# System Monitor Cinnamon

A small tool to display CPU usage, memory usage, and real-time network speed in the Cinnamon desktop panel.
Inspired by [RunCat365](https://github.com/Kyome22/RunCat365)


## Features

- 📊 Real-time display of CPU usage
- 💾 Shows memory usage
- 🌐 Shows network upload/download speed
- 🎨 Customizable icon themes (cat/horse)
- 🌓 Supports auto/dark/white icon themes
- ⚙️ Adjustable refresh rate
- 🎯 Lightweight, low resource consumption

## Installation

1. Download the project files to your local machine.
2. Copy the entire folder to the Cinnamon applets directory:
   ```bash
   mkdir -p ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/;
   cp -r system-monitor-cinnamon ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/;
   # Install translation files
   mkdir -p ~/.local/share/locale/zh_CN/LC_MESSAGES/;
   msgfmt -o ~/.local/share/locale/zh_CN/LC_MESSAGES/system-monitor-cinnamon@MainPoser.mo ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/po/zh_CN.po
   ```
3. Enable the applet in Cinnamon settings.
4. Right-click the panel → Add applets → Select "System Monitor Cinnamon"

## Usage

After installation, the applet will automatically display system monitoring information on the panel. The default format is:

```
CPU: 45% | MEM: 2.1G/8G | ↑ 1.2MB/s ↓ 500KB/s
```

## Configuration Options

Right-click the applet and select "Configure" to adjust the following options:

- **Show network speed**: Controls whether to display network speed on the panel.
- **Refresh rate**: Sets the data update interval (1-60 seconds).
- **Icon theme**: Choose the icon color theme (follow system/white/black).
- **Animation icon**: Choose the animation icon type (cat/horse).

## Project Structure

```
system-monitor-cinnamon/
├── applet.js              # Main program file
├── metada.json            # Applet metadata
├── setting-schema.json    # Configuration options definition
├── stylesheet.css         # Style file
├── icons/                 # Icon resources
│   └── runners/
│       ├── cat/          # Cat animation icons
│       └── horse/        # Horse animation icons
├── LICENSE                # License file
└── README.md              # Project description
```

## Technical Implementation

- Written in JavaScript (ES6)
- Based on the Cinnamon Applet framework
- Reads CPU, memory, and network data from system files
- Uses GdkPixbuf for animation effects

## Troubleshooting

If the applet is not working correctly, try the following solutions:

1. Restart Cinnamon: Press `Ctrl+Alt+Esc` or run `cinnamon --replace`
2. Check system logs: View error messages in `~/.xsession-errors`
3. Make sure necessary dependencies are installed on your system.

## Contribution Guide

Bug reports and feature requests are welcome! If you want to contribute code:

1. Fork this project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

MainPoser - 2026
