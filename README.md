# Video Filter

A desktop video file scanner and statistics analyzer built with Python and CustomTkinter.

## Features

- **Folder scanning** — recursively scans a folder for video files, extracts size, duration, video/audio bitrate using ffprobe
- **Multi-threaded** — configurable thread count for fast scanning of large folders
- **Sort & filter** — sort by name, size, duration, bitrate; filter by file format
- **Selection statistics** — select multiple files to see total count, duration, and size
- **Batch commands** — built-in presets for video transcoding (x265 CRF, NVENC HEVC, NVENC H.264) with customizable commands
- **Dark/Light theme** — smooth animated theme switching
- **Bilingual** — Chinese and English UI with one-click toggle
- **Drag-select** — click-and-drag to select multiple rows quickly

## Requirements

- Python 3.10+
- [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter)
- FFmpeg (ffprobe) in PATH

```bash
pip install customtkinter
```

## Usage

```bash
python 3.py
```

1. Click **Open Folder** to select a video directory
2. Sort and filter the results as needed
3. Select files and optionally apply batch commands
4. Copy selected file paths or execute command presets

## Screenshots

| Dark | Light |
|------|-------|
| *(screenshot)* | *(screenshot)* |

## License

MIT
