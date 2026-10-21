# VidoByte — Third-party source and licenses (Windows x64)

This is the source/build information for the separately distributed command-line FFmpeg components used in VidoByte Smart Video Compressor 0.3.4. **This document does not certify patent or license clearance.**

## FFmpeg

- FFmpeg source version: **9.0.2**, unmodified upstream archive
- [Download exact upstream FFmpeg 9.0.2 source](https://ffmpeg.org/releases/ffmpeg-9.0.2.tar.xz)
- [FFmpeg upstream repository](https://github.com/FFmpeg/FFmpeg)
- [FFmpeg legal and LGPL requirements](https://ffmpeg.org/legal.html)
- Our Windows build instructions: [build-ffmpeg-9.0.2-ucrt64.sh](build-ffmpeg-9.0.2-ucrt64.sh)

The build config disables GPL-licensed x264/x265 and OpenH264 and enables Windows Media Foundation H.264 encoding plus SVT-AV1 encoding and dav1d decoding. The app launches FFmpeg as a separate local executable. The delivered binary reports the full build configuration via `ffmpeg.exe -version`.

## Dynamically linked components

| Component | Version | Source and license |
| --- | --- | --- |
| dav1d | 1.5.4 | [VideoLAN dav1d](https://code.videolan.org/videolan/dav1d), BSD-style license and AOM patent terms |
| SVT-AV1 | 4.2.0 | [AOMediaCodec SVT-AV1](https://gitlab.com/AOMediaCodec/SVT-AV1), BSD-style license and patent terms |
| GCC libgcc / libstdc++ | GCC 16.2.0 | [MSYS2 UCRT64 toolchain](https://packages.msys2.org/), GNU GPL and GCC Runtime Library Exception |
| MinGW-w64 winpthreads | MSYS2 UCRT64 package | [MinGW-w64](https://www.mingw-w64.org/), COPYING/redistribution terms |

The VidoByte MSIX includes third-party license notices alongside the executables. Corresponding source/build records are maintained by the publisher; publicly accessible upstream links and this build script are supplied here.

## Distribution notice

VidoByte media processing occurs locally. The software may involve codec patents; LGPL/BSD notices and the absence of OpenH264 alone **do not** establish commercial patent licensing rights in all countries. The publisher must review obligations and the final shipped binary before release.

For inquiries or a copy of build/source materials, email **lebao1462@gmail.com**.
