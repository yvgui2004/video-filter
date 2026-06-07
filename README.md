# Video Filter / 视频筛选器

A desktop video file scanner and statistics analyzer built with Python and CustomTkinter.
基于 Python + CustomTkinter 的桌面端视频文件扫描统计工具。

## Features / 功能

- **Folder scanning / 文件夹扫描** — recursively scans a folder for video files, extracts size, duration, video/audio bitrate using ffprobe / 递归扫描文件夹中的视频文件，通过 ffprobe 提取大小、时长、视频/音频码率
- **Multi-threaded / 多线程** — configurable thread count for fast scanning of large folders / 可配置线程数，快速扫描大量文件
- **Sort & filter / 排序筛选** — sort by name, size, duration, bitrate; filter by file format / 按名称、大小、时长、码率排序，按格式筛选
- **Selection statistics / 选择统计** — select multiple files to see total count, duration, and size / 多选文件查看总数量、总时长、总大小
- **Batch commands / 批量命令** — built-in presets for video transcoding (x265 CRF, NVENC HEVC, NVENC H.264) with customizable commands / 内置视频转码预设（x265 CRF 软编、NVENC HEVC、NVENC H.264），支持自定义命令
- **Dark/Light theme / 深浅主题** — smooth animated theme switching / 流畅动画切换深浅色主题
- **Bilingual / 双语界面** — Chinese and English UI with one-click toggle / 中英文界面一键切换
- **Drag-select / 拖拽选择** — click-and-drag to select multiple rows quickly / 点击拖拽快速批量选择

## Requirements / 环境要求

### 1. Python 3.10+

[python.org](https://www.python.org/downloads/) 下载安装，安装时勾选 **"Add Python to PATH"**。

```bash
python --version   # 确认版本 ≥ 3.10
```

### 2. CustomTkinter

```bash
pip install customtkinter
```

或使用国内镜像加速：

```bash
pip install customtkinter -i https://pypi.tuna.tsinghua.edu.cn/simple
```

### 3. FFmpeg（包含 ffprobe）

程序依赖 `ffprobe` 读取视频的时长和码率信息，必须安装 FFmpeg 并添加到系统 PATH。

**Windows：**
1. 下载 [ffmpeg-master-latest-win64-gpl.zip](https://github.com/BtbN/FFmpeg-Builds/releases)
2. 解压到任意目录（如 `C:\ffmpeg`）
3. 将 `bin` 目录（如 `C:\ffmpeg\bin`）添加到系统 PATH：
   - 右键"此电脑" → 属性 → 高级系统设置 → 环境变量
   - 在"系统变量"中找到 `Path`，添加 `C:\ffmpeg\bin`
4. 重启终端，验证：

```bash
ffprobe -version   # 确认可用
```

**macOS：**

```bash
brew install ffmpeg
```

**Linux (Debian/Ubuntu)：**

```bash
sudo apt install ffmpeg
```

### 4. 验证环境

```bash
python -c "import customtkinter; print('OK')"   # 应输出 OK
ffprobe -version | head -1                       # 应显示版本号
```

## Usage / 使用方式

```bash
python 3.py
```

1. Click **Open Folder** to select a video directory / 点击"选择文件夹"
2. Sort and filter the results as needed / 根据需要排序和筛选
3. Select files and optionally apply batch commands / 选择文件，可选应用批量命令
4. Copy selected file paths or execute command presets / 复制选中文件路径或执行命令预设

## Screenshots / 截图

| Dark / 深色 | Light / 浅色 |
|------------|-------------|
| *(screenshot)* | *(screenshot)* |

## License / 许可证

MIT
