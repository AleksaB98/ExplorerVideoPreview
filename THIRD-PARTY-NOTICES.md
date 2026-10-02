# Third-party notices

ExplorerVideoPreview itself is released under the MIT licence (see `LICENSE`). It is distributed together with, and built from, the software below.

## FFmpeg

The `ffmpeg` folder holds `ffmpeg.exe`, `ffprobe.exe` and the FFmpeg libraries they need, unmodified, from this build:

- Build: `ffmpeg-n9.0.1-11-ge47273f4d9-win64-lgpl-shared-9.0`, published by the BtbN FFmpeg-Builds project as `autobuild-2026-08-31-13-27` (https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-08-31-13-27).
- Licence: **GNU Lesser General Public License, version 3** (the build is configured with `--enable-version3` and without `--enable-gpl` or `--enable-nonfree`). The licence text is in `ffmpeg\LICENSE.txt`.
- Source: FFmpeg at commit `e47273f4d9` of the `release/9.0` branch (https://github.com/FFmpeg/FFmpeg/tree/e47273f4d9). The scripts that produced the build, and the list of libraries it includes, are in the BtbN FFmpeg-Builds repository at the tag above. `ffmpeg\ffmpeg.exe -version` prints the exact configuration, and `ffmpeg\ffmpeg.exe -L` prints the licence.
- How it is used: ExplorerVideoPreview starts `ffmpeg.exe` and `ffprobe.exe` as separate programs. It is not linked with FFmpeg. You may replace the files in the `ffmpeg` folder with another build, or point the app at another folder under Settings > Advanced > FFmpeg folder.

FFmpeg is a trademark of Fabrice Bellard, originator of the FFmpeg project. This project is not affiliated with FFmpeg.

## Rust crates compiled into `evp.exe`

| Crate | Licence |
|---|---|
| windows, windows-core, windows-collections, windows-future, windows-link, windows-numerics, windows-result, windows-strings, windows-threading, windows-implement, windows-interface (Microsoft) | MIT OR Apache-2.0 |
| zune-jpeg, zune-core | MIT OR Apache-2.0 OR Zlib |

Used while building only (not part of the program): proc-macro2, quote, syn (MIT OR Apache-2.0), unicode-ident ((MIT OR Apache-2.0) AND Unicode-3.0), embed-resource and its dependencies (MIT or Apache-2.0).

These crates are used under the MIT licence, whose text is the same as in `LICENSE` with each crate's own copyright holders. Their sources are on https://crates.io under the names above.

## Rust standard library

`evp.exe` contains parts of the Rust standard library, licensed MIT OR Apache-2.0 (https://www.rust-lang.org/policies/licenses).
