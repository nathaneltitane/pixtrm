![pixtrm](https://raw.githubusercontent.com/nathaneltitane/pixtrm/main/pixtrm.svg)

[![Donate](https://img.shields.io/badge/Paypal-2f343f.svg?style=for-the-badge&logo=paypal&label=Donate)](https://www.paypal.com/donate?hosted_button_id=ZW3CDCANHJCWJ)

[[ PixTrm // Project Page ]](https://github.com/nathaneltitane/pixtrm) [ Version // 01-18-2025 ]

---

### NOTICE

01-18-2025 ↴

- Initial release

---

### Welcome to PixTrm

Display images in terminal using base64-encoded inline image display protocol!

This script enables displaying images directly in the terminal using a base64-encoded inline image display protocol.

It provides various options for resizing, stretching, and parsing image files, whether local or remote. Users can adjust the dimensions of the displayed image and specify the input type, ensuring flexibility and ease of use.

---

### Usage:
```

bash pixtrm -i | -n | -h [Height] -w [Width] | -s | -f [File] | -u | -t [File Type] | [-b]

---

Options

-i, --inline
Display the image inline in the terminal.

-n, --name
Display the filename after parsing the image.

-h, --height [Height]
Set the image height in terminal character cells.

-w, --width [Width]
Set the image width in terminal character cells.

-s, --stretch
Stretch the image to the specified width and height.

-f, --file
Treat following arguments as local file paths.

-u, --url
Treat following arguments as remote URLs.

-t, --type [File Type]
Provide a type hint to assist with parsing or processing, especially for piped input.

-b, --block
Use the standard protocol to transfer the image as a single monolithic block or control sequence.

-h, --help
Show help and usage information.
```

---

### Usage Examples:

Display a local image with specific dimensions:

```
bash pixtrm -w 250px -h 250px -s image.png
```

Display an image from a pipe with percentage-based width:

```
cat image-01.png | bash pixtrm -w 75%
```


Display an image with percentage-based height:

```
cat image-02.jpg | bash pixtrm -h 30%
```


Parse and display a remote URL and a local file:

```
bash pixtrm -n -w 500px -u http://host.url/path/to/image.gif -w 80 -f image.png
```


Display images from a list of URLs:

```
cat url-list[.txt] | xargs bash pixtrm -n -w 40 -u
```

Display a JSON configuration file:

```
bash pixtrm -t application/json config.json
```

---

### Image Sizing:

If width or height are not specified, the script will automatically determine appropriate values:

Numeric (n): Specifies the number of terminal character cells.

Pixels (npx): Specifies the size in pixels.

Percentage (n%): Specifies a percentage of the terminal session's width or height.

Automatic (auto): Automatically calculates dimensions based on the image size.

---

### File Type:

The file type can be:

A MIME type (e.g., text/markdown).

A language name (e.g., Java).

A file extension (e.g., .sh).

When the filename is unavailable (e.g., piped input), the --type option helps to disambiguate the file's type. Generally, the script infers file type from the extension or content.

---

### Notes:

Ensure your terminal supports inline image display protocols.

Use appropriate dimension formats for better control over the display.

### Projects:

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/dextop?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=DEXTOP)](https://github.com/nathaneltitane/dextop)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/frobulator?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=FROBULATOR)](https://github.com/nathaneltitane/frobulator)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/gutengrab?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=GutenGrab)](https://github.com/nathaneltitane/gutengrab)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/l2cu?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=L²CU)](https://github.com/nathaneltitane/l2cu)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/terminal?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=TERMINAL)](https://github.com/nathaneltitane/terminal)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/mechablocks?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=MECHA%20//%20BLOCKS)](https://github.com/nathaneltitane/mechablocks)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/pixtrm?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=PIXTRM)](https://github.com/nathaneltitane/pixtrm)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/nathaneltitane?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=NATHANEL%20%2b%20TITANE)](https://github.com/nathaneltitane/nathaneltitane)

[![GitHub Repo stars](https://img.shields.io/github/stars/nathaneltitane/pewpewprints?style=for-the-badge&logo=gnubash&logoColor=ffffff&label=PEW%21%20PEW%21%20PRINTS)](https://github.com/nathaneltitane/pewpewprints)

---

[[ PixTrm // Project Page ]](https://github.com/nathaneltitane/pixtrm) [ Version // 01-18-2025 ]

### Enjoying Dextop? Buy me a coffee to show your appreciation!

[![Donate](https://img.shields.io/badge/Paypal-2f343f.svg?style=for-the-badge&logo=paypal&label=Donate)](https://www.paypal.com/donate?hosted_button_id=ZW3CDCANHJCWJ)
