# wallhaven_crawl

[English](./README.md) | [简体中文](./README.zh-CN.md)

A lightweight Node.js crawler script for downloading wallpapers from Wallhaven search/result pages.

## Features

- Parse wallpaper detail links from Wallhaven list/search pages.
- Build direct image URLs for both `.jpg` and `.png`.
- Download files to a local folder.
- Fallback to `.png` if `.jpg` is unavailable.
- Support one-page download and multi-page batch download workflows.

## Requirements

- Node.js 14+ (recommended)
- npm

## Install

```bash
npm install
```

## Usage

The current script is configured in `index.js` and starts immediately via:

```bash
node index.js
```

By default, it runs `downAllImg()` at the bottom of the file.

## Configuration

This project is currently script-driven (no CLI args yet).  
Edit these parts in `index.js` based on your target:

- Source URLs in `getImgUrl()`
- Page range in the `for` loop
- Download output folder (e.g. `./wallhaven_plants/`)

## Notes

- Ensure the target download directory already exists before running.
- Download speed/frequency should be moderated to avoid overloading the source site.
- This project is for learning and personal use. Respect Wallhaven terms and copyright policies.
