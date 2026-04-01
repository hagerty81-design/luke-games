# Luke Games

HTML5 canvas games by Luke Hagerty, built with Claude Code.

## Project Info
- **Repo**: github.com/hagerty81-design/luke-games
- **Live URL**: https://hagerty81-design.github.io/luke-games/
- **Hosting**: GitHub Pages (auto-deploys from `main` branch in ~30 seconds)
- **Git user**: hagerty81-design

## Architecture
- Single-file HTML5 games (no build tools)
- Canvas with DPI scaling (`devicePixelRatio`)
- Pixel-art sprites drawn with `fillRect()` calls
- Web Audio API for procedural sound effects
- Game state machine: start → playing → gameover

## Deploy Workflow
```bash
git add index.html
git commit -m "description"
git push
# Auto-deploys to GitHub Pages in ~30 seconds
```

## Key Technical Notes
- ALWAYS use DPI scaling on canvas (see html5-game-dev skill)
- ALWAYS clearRect at start of each render frame
- ALWAYS resume AudioContext on first user interaction
- Use `image-rendering: pixelated` CSS for crisp pixel art
- Mouse coordinates must be mapped from CSS rect to game space
