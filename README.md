# Media Group Renamer 🖼️📹

[![npm version](https://img.shields.io/npm/v/content-renamer.svg?logo=npm)](https://www.npmjs.com/package/content-renamer)
[![npm downloads](https://img.shields.io/npm/dm/content-renamer.svg?logo=npm)](https://www.npmjs.com/package/content-renamer)
[![GitHub stars](https://img.shields.io/github/stars/is-harshul/content-renamer.svg?logo=github)](https://github.com/is-harshul/content-renamer/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/is-harshul/content-renamer.svg?logo=github)](https://github.com/is-harshul/content-renamer/network/members)
[![license](https://img.shields.io/npm/l/content-renamer.svg)](https://github.com/is-harshul/content-renamer/blob/main/LICENSE)
[![node version](https://img.shields.io/node/v/content-renamer.svg?logo=node.js)](https://www.npmjs.com/package/content-renamer)

A CLI tool to organize media files by timestamp and geolocation metadata

## Demo
![Demo](assets/demo.gif)

## Features
- Groups media files by time and location metadata
- Configurable time window (default 15 minutes)
- Configurable distance threshold (default 100 meters)
- Supports common photo/video formats
- Prevents filename conflicts
- Preserves file extensions

## Installation
```bash
npm install -g content-renamer
```

## Usage

### Interactive Mode
```bash
content-renamer --interactive
```
OR Simply write
```bash
content-renamer --i
```

### Non-Interactive Mode
```bash
content-renamer <directory> [duration_minutes] [distance_meters]
```

### Examples
1. Organize photos in the ~/Pictures folder:
```bash
# Basic usage with defaults
content-renamer --directory ~/Pictures
```

2. Group files with a 30-minute window and 200-meter distance:
```bash
content-renamer --directory ~/Videos --duration 30 --distance 200
```

3. Use interactive mode:
```bash
content-renamer --interactive
```

4. Organize files in a relative path:
```bash
content-renamer --directory ../Trip/Photos
```

## Configuration
| Parameter | Default | Description |
|-----------|---------|-------------|
| directory | - | Path to media files (required) |
| duration_minutes | 15 | Max minutes between files in a group |
| distance_meters | 100 | Max distance between files in a group |

## Output
Files will be renamed in the format:
```text
Location1_001.jpg
Location1_002.mp4
Location2_001.png
```

## Notes
- Files without valid timestamps will be ignored
- Requires ExifTool installed on system
- Always backup files before processing

## License
MIT © [Harshul Kansal](https://github.com/is-harshul)


## Support
If you find this project helpful, consider supporting my work:

- [☕ Buy Me a Coffee](https://www.buymeacoffee.com/is.harshul)
- [💖 GitHub Sponsors](https://github.com/sponsors/is-harshul)
- [💰 PayPal](https://paypal.me/itsharshul)
