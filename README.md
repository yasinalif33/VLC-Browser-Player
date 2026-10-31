# VLC Browser Player

A VLC-style media player that runs entirely in the browser.

Open local video and audio files (button or drag & drop — files are never
uploaded), paste a network stream URL, or play a sample stream. Features
include a playlist sidebar, loop/shuffle, playback speed, subtitle files
(.srt / .vtt, with SRT converted in-page), live brightness / contrast /
saturation / hue controls, PNG snapshot, picture-in-picture, fullscreen,
media info, and VLC-style keyboard shortcuts.

## Run it

Open `index.html` in a browser, or serve this repository with GitHub Pages
(Source: Deploy from a branch, branch `main`, folder `/ (root)`).

## Notes

- This is an original browser player inspired by VLC's interface and
  feature set. It is not VLC itself and does not bundle VLC code.
- Local-file playback uses standard browser object URLs. Format support
  depends on the browser's built-in codecs, unlike desktop VLC which
  ships its own decoders.
