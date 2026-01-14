# Game Portfolio Setup Guide

## Overview
This is a professional game portfolio home page similar to CrazyGames.com with:
- Dark gaming-themed UI with cyan accents
- Responsive grid layout
- Hover video previews
- Support for HTML/CSS/JS and external Unity games
- Built-in search functionality

## Quick Start

### 1. Open the Home Page
Open `index.html` in your browser to see your game portfolio.

### 2. Add Games to Your Portfolio

Edit `index.html` and find the `gamesData` object (around line 250). Add your games to these arrays:

**Featured Games** - Shows first
**HTML Games** - Local HTML/CSS/JS games
**Unity Games** - External links to itch.io or GameJolt

### 3. Game Data Structure

Each game entry needs:
```javascript
{
    id: 1,
    title: "Game Name",
    thumbnail: "./path/to/thumbnail.jpg",
    video: "./path/to/preview.mp4",
    badge: "hot", // or "new", "updated", "top" (optional)
    type: "html", // or "external"
    link: "./games/game-name/index.html" // or external URL
}
```

## Examples

### HTML Game Example
```javascript
html: [{
    id: 1,
    title: "Snake Game",
    thumbnail: "./games/snake/thumb.jpg",
    video: "./games/snake/preview.mp4",
    badge: "new",
    type: "html",
    link: "./games/snake/index.html"
}]
```

### Unity Game Example (itch.io)
```javascript
unity: [{
    id: 1,
    title: "My Unity Game",
    thumbnail: "https://img.itch.io/game.jpg",
    video: "https://itch.io/preview.mp4",
    badge: "hot",
    type: "external",
    link: "https://your-name.itch.io/your-game"
}]
```

### Unity Game Example (GameJolt)
```javascript
unity: [{
    id: 2,
    title: "GameJolt Game",
    thumbnail: "https://gamejolt.com/img.jpg",
    video: "https://gamejolt.com/preview.mp4",
    badge: "updated",
    type: "external",
    link: "https://gamejolt.com/games/your-game/123456"
}]
```

## File Organization

```
HTML-PROJECT/
├── index.html
├── GAMES_SETUP.md
└── games/
    ├── snake-game/
    │   ├── index.html
    │   ├── style.css
    │   ├── script.js
    │   ├── thumbnail.jpg
    │   └── preview.mp4
    └── another-game/
        └── ...
```

## Badge Types
- **hot** - Red/Orange badge
- **new** - Cyan badge
- **updated** - Green badge
- **top** - Orange badge

## Customization

### Colors (in CSS)
- Primary: `#00d4ff` (cyan)
- Background: `#0f0f0f` (dark)
- Text: `#fff` (white)

### Grid Layout
Change `minmax(250px, 1fr)` to adjust card width.

## Tips

1. **Video Format**: Use MP4 files
2. **Optimize**: Compress images and videos
3. **Relative Paths**: Use `./` for local files
4. **Full URLs**: Use `https://` for external links
5. **Test**: Open index.html locally before uploading

## Support
Both itch.io and GameJolt support web games, so any Unity game deployed there will work fine with external type links.
