<h1 align="center">File Opener Script</h1>

<p align="center">A simple shell script to interactively select and open files using appropriate applications based on their MIME type.</p>

##

<p align="center">
<img src="./open.gif" alt="File Opener Script Example" width="2000px">
</p>

## Features
- Uses `fzf` for interactive file selection if no argument is provided.
- Automatically detects the MIME type of the selected file.
- Opens the file with the most suitable application:
  - Images: `nsxiv`
  - Videos & Audio: `mpv`
  - PDFs: `mupdf`
  - Text files: `vim`
  - Other file types: `xdg-open`

## Prerequisites
Ensure the following programs are installed on your system:
- [`fzf`](https://github.com/junegunn/fzf) - Fuzzy Finder for interactive selection.
- [`nsxiv`](https://codeberg.org/nsxiv/nsxiv) - Lightweight image viewer.
- [`mpv`](https://mpv.io/) - Media player for videos and audio.
- [`mupdf`](https://mupdf.com/) - PDF viewer.
- [`vim`](https://www.vim.org/) - Text editor.
- [`xdg-open`](https://linux.die.net/man/1/xdg-open) - Opens files with the default system application.

## Installation
Download and install the script with:

```sh
doas curl -sL "https://raw.githubusercontent.com/ganeshkumar0x/File-opener-script/refs/heads/main/open" -o /usr/local/bin/open
doas chmod +x /usr/local/bin/open
```

## Usage
Run the script in the terminal:

```sh
open [filename]
```

- If no filename is provided, `fzf` will be used to select one.
- The script then determines the file type and opens it with the appropriate application.

## Uninstallation
To remove the script, run:

```sh
doas rm /usr/local/bin/open
```

## License
This project is licensed under the [MIT License](LICENSE).
