<p align="center">
  <img src="assets/icons/ico.png" alt="GiSing! logo" width="320">
</p>

# GiSing! Karaoke

> Grab the mic. Let's sing!

GiSing! is an Android karaoke player. It plays MIDI karaoke files with lyrics, shows background videos or your phone camera behind the lyrics, scores your singing, and can be controlled from your phone over Wi-Fi.

## Features

- **Song selection** with a 6-digit song code, a typing keypad, and a search page with an on-screen keyboard (landscape)
- **Song list, artist list, rankings, favorites, and a new songs page**
- **Reservation queue** shown at the top of the karaoke screen, with next song and now playing
- **MIDI playback** with a SoundFont (`.sf2`) engine, key and tempo control, and a per-channel mixer
- **Word-by-word lyrics** with a countdown, interlude screen, and an end-of-song score screen
- **Scoring** (random, or from your microphone pitch)
- **Background videos** grouped by folder, background photos, or the live camera
- **MP3 and MP4 songs** with `.lrc` lyrics
- **Web remote control** over Wi-Fi, opened by scanning a QR code on the karaoke screen
- **Mic monitor and voice effects** (echo, reverb, clarity)
- **Recording** of the song and your mic
- **Themes** for the lyrics, idle screen, queue, score, and interlude, all set in Settings

## Requirements

- Android 5.0 (API 21) or newer
- Storage access for the song and background folders
- Microphone and camera access, only if you use those features

## Install

Download the latest `.apk` from the [Releases](../../releases) page, open it on your phone, and allow installation from unknown sources if asked.

If an update says the app conflicts with an existing package, uninstall the old version first. This happens only when the signing key changed.

## Folder setup

On first run, GiSing! creates its app folder on the device. You can move it from Settings. Put your files in these folders:

| Folder | What goes in it |
| --- | --- |
| `songs/midi/` | MIDI (`.mid`, `.midi`, `.kar`) files and ZIP packs |
| `songs/mp3/`, `songs/mp4/` | MP3 and MP4 songs, with a `.lrc` of the same name for lyrics |
| `songs/packs/` | Megaoke-style packs (`.idx` + `.dat`) |
| `bgv/<FolderName>/` | Background videos, one folder per group |
| `bgphoto/` | Background photos |
| `sf/` | SoundFont (`.sf2`) files for MIDI playback |
| `assets/digits/` | Custom typing sounds `n0.mp3` to `n9.mp3` (optional) |
| `assets/score/` | Custom score sounds `score_1` to `score_5` as `.mp3` or `.mid` (optional) |

Song file names follow the pattern `code_title_artist.mid`. After adding files, rescan the songs in Settings.

## Remote control

The karaoke screen shows a QR code when the remote server is on. Scan it with your phone to open the remote in a browser. The phone and the device must be on the same Wi-Fi network. The default port is `8765` and can be changed in Settings. You can turn the remote off completely in Settings.

## Verification

Release APKs are signed with the developer's release key. To confirm an APK really came from this project, check that its signing certificate matches these fingerprints:

- **MD5:** `C1A8ED8A21C3F3F219E2623FBC80D619`
- **SHA-1:** `450B0BF2518AC510FDDDA0AAA675545F4CC40133`
- **SHA-256:** `1FDB1E8660A371D27782EC6A09299B36B79B7248825278209FC21AFC237FBBC7`

Check an APK with Android's build tools:

```bash
apksigner verify --print-certs app-release.apk
```

Each release is also scanned with VirusTotal. The link is in the release notes.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.