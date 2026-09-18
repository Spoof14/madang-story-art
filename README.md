# madang-story-art

Public CDN host for Madang (countryCapitals) story-art images.

## Purpose

This repository serves as a **public CDN** for premium story art images used by the Madang app (countryCapitals). By hosting these assets publicly, the app can lazy-load premium images on demand, keeping the Play Store and App Store installation size small.

## Contents

- **585 JPG files** (~84 MB total)
- Located in `story-art/` directory
- Original filenames preserved from source

**All files in this repository are PUBLIC.**

## Usage

### Canonical URL Patterns

#### jsDelivr CDN (Preferred)
```
https://cdn.jsdelivr.net/gh/Spoof14/madang-story-art@main/story-art/{filename}
```

**Example:**
```
https://cdn.jsdelivr.net/gh/Spoof14/madang-story-art@main/story-art/frog-prince-1.jpg
```

#### GitHub Raw (Fallback)
```
https://raw.githubusercontent.com/Spoof14/madang-story-art/main/story-art/{filename}
```

**Example:**
```
https://raw.githubusercontent.com/Spoof14/madang-story-art/main/story-art/cinderella-1.jpg
```

### Integration

Set `REMOTE_ART_BASE` in your app to:
```
https://cdn.jsdelivr.net/gh/Spoof14/madang-story-art@main/story-art
```

Then construct full URLs by appending `/{filename}` as needed.

## Notes

- jsDelivr may take 1-2 minutes to cache new files after initial push
- jsDelivr provides automatic global CDN with edge caching
- GitHub raw URLs work immediately but have stricter rate limits
- This is an assets-only repository - all commits go directly to `main`

## Source

Files sourced from the private [countryCapitals](https://github.com/Spoof14/countryCapitals) repository at `public/story-art/`.
