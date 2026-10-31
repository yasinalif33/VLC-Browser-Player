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
- Network streams: the player no longer sends a CORS preflight for
  playback, so streams from servers without CORS headers can play.
  Two browser limits remain and cannot be worked around in-page:
  (1) an `http://` stream is blocked on an `https://` page (mixed
  content) — the player retries the same URL over `https://` once,
  and if that fails, download the file and open it locally, or use a
  `https://` link; (2) MKV files whose audio track is AC3/DTS (common
  in dual-audio releases) will fail to decode even when the video is
  H.264 — use desktop VLC for those, or an MP4/WebM version.
