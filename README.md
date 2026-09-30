![pixtrm](https://raw.githubusercontent.com/nathaneltitane/pixtrm/main/pixtrm.svg)

[![Donate](https://img.shields.io/badge/Paypal-2f343f.svg?style=for-the-badge&logo=paypal&label=Donate)](https://www.paypal.com/donate?hosted_button_id=ZW3CDCANHJCWJ)

[[ PixTrm // Project Page ]](https://github.com/nathaneltitane/pixtrm) [ Version // 2026-09-30 ]

---

### NOTICE

09-30-2026 ↴

- Options reworked: '-f' / '--file' selects the image, '-d' / '--download' replaces '-i' / '--inline'
- Width and height options are '-x' / '--width' and '-y' / '--height'
- Multipart transfer inside tmux or screen, '-b' / '--block' forces a single block

01-18-2025 ↴

- Initial release

---

### Welcome to PixTrm

PixTrm is a Bash terminal utility that lets you display images directly in your terminal, using a base64-encoded inline image protocol.

It provides various options for parsing image files, whether local, remote or piped:

Users can adjust the dimensions of the displayed image and specify the input type, ensuring flexibility and ease of use.

### TL;DR

The script automatically installs and manages what it needs:

- curl
- frobulator (auto-downloaded to ~/.local/bin/frobulator if missing)

Clone the repository ↴

```
git clone https://github.com/nathaneltitane/pixtrm.git
```

Move into the directory ↴

```
cd pixtrm
```

Make it executable ↴

```
chmod +x pixtrm
```

Run it ↴

```
bash pixtrm -f image.png -x 250px -y 250px
```

Or install globally ↴

```
sudo install -m 755 pixtrm /usr/local/bin/pixtrm
```

Example ↴

```
bash pixtrm -f image.jpg -x 75% -y auto -s
cat photo.png | pixtrm -x 50%
```

---

### Features

- Display images inline in terminal using base64-encoded OSC protocol
- Support for local files, URLs, and stdin pipelines
- Adjustable width and height in characters, pixels, or percentages
- Stretch or preserve aspect ratio control
- Optional filename display after render
- Optional file download instead of display
- MIME-type and format hinting ('-t' / '--type') for disambiguation
- Multipart transfer inside tmux and screen multiplexers
- Uses [frobulator](https://github.com/nathaneltitane/frobulator) for logging, progress, and error handling

---

### Usage

```
pixtrm -f [File] -d | -n | -x [Width] -y [Height] | -s | -t [Type] | -b | -h
```

### Options

| Flag     | Long Option       | Description                                             |
| -------- | ----------------- | ------------------------------------------------------- |
| `-f`     | `--file [File]`   | Image file or URL to display - reads stdin when omitted |
| `-d`     | `--download`      | Send image as a file download instead of displaying it  |
| `-n`     | `--name`          | Display filename after image render                     |
| `-x`     | `--width [n]`     | Set image width (in character cells, px, %, or auto)    |
| `-y`     | `--height [n]`    | Set image height (in character cells, px, %, or auto)   |
| `-s`     | `--stretch`       | Stretch image to specified width and height             |
| `-t`     | `--type [Type]`   | Provide type hint (application/json, .sh, Python)       |
| `-b`     | `--block`         | Send image as a single block sequence                   |
| `-h`     | `--help`          | Show help and usage information                         |

Examples:

Display a local image with specific dimensions ↴

```
pixtrm -f image.png -x 250px -y 250px -s
```

Display an image from stdin ↴

```
cat image.png | pixtrm -x 75%
```

Display an image from a remote URL ↴

```
pixtrm -f https://example.com/photo.jpg -n -x 500px
```

Display images from a URL list ↴

```
cat url-list.txt | xargs -n 1 pixtrm -n -x 40 -f
```

Send an image as a file download ↴

```
pixtrm -f image.png -d
```

Display a JSON configuration file ↴

```
pixtrm -f config.json -t application/json
```

---

### Image Sizing

If width or height are not specified, PixTrm automatically determines appropriate values.

| Unit   | Meaning                                        |
| ------ | ---------------------------------------------- |
| `n`    | Character cells                                |
| `npx`  | Pixel value                                    |
| `n%`   | Percentage of terminal width or height         |
| `auto` | Automatically scale to image’s intrinsic ratio |

---

### File Type Hints

File type hints ('-t' / '--type' argument) improve handling of files or streams where the extension is unavailable.

Examples ↴

| Input              | Type Hint Example |
| ------------------ | ----------------- |
| JSON configuration | application/json  |
| Script             | .sh               |
| Markdown           | text/markdown     |
| Language           | Python            |

---

### Protocol

PixTrm implements the OSC 1337 inline image protocol:

- Detects tmux or screen multiplexer and adapts control sequences.
- Sends multipart (512-byte) encoded chunks inside tmux or screen, a single monolithic block otherwise - '--block' forces a single block.
- Encodes data via base64 before inline transmission.
- Local files are read directly, URLs require 'http://' or 'https://'.

---

### Notes

- Requires a terminal that supports the OSC 1337 inline image protocol (e.g., iTerm2, WezTerm).
- Ideal for displaying previews, diagrams, or assets directly within the CLI.
- Fully portable and compatible with Debian-based and Termux environments.

---

### Other Projects:

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/dextop?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=DEXTOP)](https://github.com/nathaneltitane/dextop)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/frobulator?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=FROBULATOR)](https://github.com/nathaneltitane/frobulator)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/l2cu?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=L²CU)](https://github.com/nathaneltitane/l2cu)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/terminal?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=TERMINAL)](https://github.com/nathaneltitane/terminal)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/legolinux?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=LEGO//LINUX)](https://github.com/nathaneltitane/legolinux)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/nathaneltitane?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=NATHANEL+TITANE)](https://github.com/nathaneltitane/nathaneltitane)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/pewpewprints?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=PEWPEWPRINTS)](https://github.com/nathaneltitane/pewpewprints)

---

[[ PixTrm // Project Page ]](https://github.com/nathaneltitane/pixtrm) [ Version // 2026-09-30 ]

### Enjoying PixTrm? Buy me a coffee to show your appreciation!

[![Donate](https://img.shields.io/badge/Paypal-2f343f.svg?style=for-the-badge&logo=paypal&label=Donate)](https://www.paypal.com/donate?hosted_button_id=ZW3CDCANHJCWJ)
