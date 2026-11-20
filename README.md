# Convertr

Convertr is a macOS utility for converting files and making common edits from Finder. Select files, drag them, and hold a modifier key to open the right set of choices beside the pointer. Converted files are saved next to the originals; when a name is already taken, Convertr adds a number instead of overwriting it.

## What it handles

Convertr works with images, audio, video, documents, spreadsheets, presentations, archives, and subtitles. Available output formats depend on the source file; the wheel only shows conversions Convertr can perform.

- **Images:** JPEG, PNG, WebP, HEIC/HEIF, TIFF, AVIF, and BMP. SVG can be used as an input.
- **Audio:** MP3, M4A/AAC, WAV, FLAC, OGG, Opus, and AIFF. WMA is input-only.
- **Video:** MP4/M4V, MOV, MKV, WebM, and GIF. AVI and WMV are input-only.
- **Documents:** PDF, DOC/DOCX, Markdown, plain text, EPUB, HTML, RTF, and Pages. RTFD is input-only.
- **Spreadsheets:** XLSX, ODS, CSV, and TSV. XLS is input-only.
- **Presentations:** PPTX. PPT is input-only.
- **Archives:** ZIP, TAR, and TGZ. RAR is input-only.
- **Subtitles:** SRT and VTT.

Several files can be converted together when they share an available destination format.

## Convert and edit

The **Tools** wheel offers file-specific operations, including:

- Compress or shrink images, audio, and video; crop, rotate, adjust, add a background, annotate, or redact images.
- Make collages and PDFs from image selections; read text or QR codes; create searchable PDFs.
- Trim, split, join, change speed, extract audio, mute, or capture frames from video; normalize audio, change channels, or trim silence.
- Compress, split, merge, reorder, and rotate PDF pages; remove metadata and extract text.
- Extract supported archives.

The **Actions** wheel can float a file, copy or move it, copy its path, or open its location in Terminal.

## How it works

1. Select one or more supported files in Finder and begin dragging.
2. Hold **Shift** for Convert, **Command** for Tools, or **Control** for Actions. These keys can be changed in Settings.
3. Choose a destination format or operation from the wheel.
4. Convertr runs the job and saves the result beside the source file.

You can also open the wheel from the menu bar or use the system-wide Open Wheel shortcut with a Finder selection. For batches, Convertr plans every output name before starting so same-named results do not overwrite each other.

## Local processing

Conversions run on the Mac. macOS frameworks handle image and PDF work and provide utilities such as `textutil` and `tar`. Bundled tools handle the formats that need them: FFmpeg for audio and video, Pandoc for document conversion, LibreOffice in headless mode for Office files, and dedicated encoders for AVIF and WebP.

The app does not upload files, send usage reports, or download engines. The GitHub page hosts the installer; it does not receive conversion data. The engines are included in the zip, so the other Mac does not need Homebrew.

## Folder permissions

Choose **Folder Access Guide…** from the menu bar to check access to a folder and see the relevant macOS privacy setting if access is blocked. The guide does not open the conversion wheel or start a job. macOS controls the permission; Full Disk Access is usually unnecessary.

## Download and install

The current build is for Apple silicon Macs running macOS 26 or later. Download [Convertr.zip](https://github.com/grphxdsign-ops/Convertr/releases/latest/download/Convertr.zip), open it in Finder, and drag `Convertr.app` to Applications. The zip is about 220 MB because it includes the conversion engines.

This test build is ad-hoc signed and is not notarized. On first launch, macOS may block it; Control-click Convertr, choose **Open**, and confirm. Then approve the folder and Finder permissions requested by macOS.

## License and notices

Convertr is based on the MIT-licensed Clementine project. See [LICENSE](LICENSE), [NOTICE](NOTICE), and [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) for attribution and bundled engine details. This repository publishes the installer and release notes, not the app's source code.
