# yt-dlp Flutter Android

An Android (11+) Flutter application that allows downloading audio and video from YouTube
using **yt-dlp** and converting media formats with **ffmpeg** — fully offline, with all
required binaries bundled directly inside the APK.

> ⚠️ This project is intended **for educational and personal use only**.

---

## Overview

This project demonstrates how a Flutter application can execute native command-line tools
(`yt-dlp` and `ffmpeg`) directly on an Android device without relying on any external server,
cloud service, or third-party application such as Termux.

The app provides a simple single-screen interface where a user can paste a YouTube link,
choose an output format, and download or convert media files directly on the device.

---

## Features

### Audio
- Download audio in the following formats:
  - MP3
  - FLAC
  - WAV
- Embedded metadata:
  - title
  - artist
  - album
  - thumbnail (cover art)

### Video
- Download video in:
  - MP4
  - MKV

### General
- yt-dlp and ffmpeg binaries bundled inside the APK
- Fully offline processing
- No backend server
- No Termux dependency
- Single-screen UI
- Android 11+ support (Scoped Storage compliant)
- Step-by-step GitHub commits for learning purposes

---

## Architecture

The Flutter application launches `yt-dlp` and `ffmpeg` as external processes using
Dart's `Process.run` / `Process.start`, captures their output, and displays progress
and errors in the UI.

---

## Requirements

### Development
- Windows 11
- Flutter (stable channel)
- Android Studio
- Android SDK
- Android device or emulator (Android 11+)

### Runtime
- Android 11 or newer
- Storage access permission

---

## Building the APK

To build a release APK:

## The generated APK will be located at
build/app/outputs/flutter-apk/app-release.apk

```bash
flutter build apk --release

