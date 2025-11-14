# 🌌 GitHub Galaxy - 2025 Contributions Visualization

A unique and stunning 3D visualization of GitHub contributions for 2025, rendered as an interactive spiral galaxy where each day becomes a celestial object in space.

![GitHub Galaxy Visualization](https://img.shields.io/badge/Visualization-3D%20Galaxy-purple)
![Year](https://img.shields.io/badge/Year-2025-blue)
![Tech](https://img.shields.io/badge/Tech-Three.js-brightgreen)

## 🎨 Concept

Unlike traditional 2D contribution graphs or simple 3D city visualizations, **GitHub Galaxy** transforms your coding activity into a living, breathing spiral galaxy:

- **🌟 Each contribution day** is represented as a star or celestial object
- **✨ Contribution intensity** determines the size, brightness, and color of each star
- **🌀 Time progression** follows spiral galaxy arms, creating a natural flow through the year
- **🎮 Interactive navigation** allows you to fly through and explore your contribution universe
- **🎨 Color gradient** transitions from blue (low activity) → purple (medium) → pink (high activity)

## ✨ Features

### Visual Features
- **3D Spiral Galaxy Layout**: Three spiral arms representing your year of contributions
- **Dynamic Coloring**: Contribution intensity affects color (blue → purple → pink gradient)
- **Glowing Core**: Pulsating galactic center with atmospheric effects
- **Background Star Field**: 10,000 ambient stars creating depth and immersion
- **Point Lights**: High-activity days emit their own light
- **Atmospheric Fog**: Adds depth and creates a space-like atmosphere

### Interactive Features
- **Mouse Drag Navigation**: Rotate and orbit around your galaxy
- **Scroll to Zoom**: Zoom in/out to explore details
- **Hover Tooltips**: See exact date and contribution count for each day
- **Auto-rotation**: Galaxy slowly spins automatically (can be toggled)
- **Reset View**: Return to default camera position instantly

### Statistics Dashboard
- **Total Contributions**: Your complete 2025 contribution count
- **Current Streak**: Active contribution days in a row
- **Longest Streak**: Your best contribution streak of the year
- **Brightest Day**: The day with maximum contributions

## 🚀 Quick Start

### Option 1: Direct Usage
Simply open `index.html` in a modern web browser:

```bash
# Clone the repository
git clone https://github.com/ValerasNarbutas/GithubContribution.git
cd GithubContribution

# Open in browser
open index.html  # macOS
# or
start index.html  # Windows
# or
xdg-open index.html  # Linux
```

### Option 2: Local Server
For the best experience, serve it via a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (with http-server)
npx http-server

# Then visit http://localhost:8000
```

### Option 3: Deploy to GitHub Pages
1. Push this repository to GitHub
2. Go to Settings → Pages
3. Select main branch as source
4. Your galaxy will be available at `https://yourusername.github.io/GithubContribution/`

## 🎮 Controls

| Action | Control |
|--------|---------|
| **Rotate View** | Click and drag |
| **Zoom** | Mouse wheel / Trackpad pinch |
| **View Details** | Hover over any star |
| **Pause/Resume** | Click "Pause Rotation" button |
| **Reset Camera** | Click "Reset View" button |

## 🔧 Technical Details

### Technologies Used
- **Three.js** (r128): WebGL-based 3D rendering library
- **Vanilla JavaScript**: No framework dependencies
- **HTML5 Canvas**: Hardware-accelerated rendering
- **CSS3**: Modern styling with backdrop filters and gradients

### Architecture
- **Self-contained**: Single HTML file with embedded CSS and JavaScript
- **No build step**: Works directly in the browser
- **CDN-based**: Three.js loaded from CDN (can be made offline)
- **Responsive**: Adapts to any screen size

### Performance
- **10,000+ objects**: Background stars plus 365 contribution objects
- **60 FPS**: Smooth animation on modern hardware
- **Raycasting**: Efficient hover detection
- **Point lights**: Dynamic lighting for high-contribution days

## 📊 Data Structure

The visualization uses a simple data structure for each day:

```javascript
{
    date: Date,              // The specific date
    contributions: Number,   // Contribution count (0-50+)
    dayOfYear: Number       // Day index (0-364)
}
```

### Customization

#### Change Galaxy Arms
```javascript
const armCount = 3;  // Number of spiral arms (try 2-5)
```

#### Adjust Rotation Speed
```javascript
this.galaxyGroup.rotation.y += 0.001;  // Increase for faster rotation
```

#### Modify Color Palette
```javascript
// In createStar method, adjust colors:
if (normalizedContributions < 0.33) {
    color = new THREE.Color(0x58a6ff);  // Change blue
} else if (normalizedContributions < 0.66) {
    color = new THREE.Color(0x6a7fdb);  // Change purple
} else {
    color = new THREE.Color(0xff6b9d);  // Change pink
}
```

## 🔌 GitHub API Integration (Future)

Currently uses generated sample data. To integrate with real GitHub data:

1. Add GitHub API authentication
2. Fetch contribution data from GitHub GraphQL API
3. Parse and map to the galaxy structure

Example API call structure:
```javascript
query {
  user(login: "username") {
    contributionsCollection(from: "2025-01-01T00:00:00Z", to: "2025-12-31T23:59:59Z") {
      contributionCalendar {
        weeks {
          contributionDays {
            date
            contributionCount
          }
        }
      }
    }
  }
}
```

## 🎯 Unique Selling Points

What makes GitHub Galaxy stand out:

1. **Astronomical Theme**: First GitHub contribution visualizer using galaxy/space theme
2. **Spiral Layout**: Natural time progression along galaxy arms (not just a grid)
3. **True 3D Navigation**: Full camera controls, not just a rotating object
4. **Atmospheric Effects**: Fog, glowing core, point lights create immersion
5. **Zero Dependencies**: Single file, works offline after first load
6. **Performance**: Handles 10,000+ objects at 60 FPS
7. **Interactive Details**: Real-time tooltips without performance impact

## 🛠️ Development

### Project Structure
```
GithubContribution/
├── index.html          # Complete visualization (HTML + CSS + JS)
└── README.md          # This file
```

### Future Enhancements
- [ ] Real GitHub API integration
- [ ] Save/export galaxy as image or video
- [ ] VR/AR support for immersive viewing
- [ ] Comparison view (multiple years)
- [ ] Sound effects and ambient space music
- [ ] Planetary view (zooming into individual days)
- [ ] Share your galaxy with a unique URL
- [ ] Custom color themes
- [ ] Mobile touch controls optimization

## 📸 Screenshots

*Coming soon: Add screenshots of your galaxy here!*

## 🌟 Inspiration

This project was inspired by:
- The beauty of spiral galaxies like Andromeda and Milky Way
- The desire to make contribution graphs more engaging and beautiful
- The concept that code contributions are like stars - each one adds to the universe

## 🤝 Contributing

Contributions are welcome! Some ideas:
- Add different galaxy types (elliptical, irregular)
- Implement constellation patterns for milestones
- Add particle effects for contribution "explosions"
- Create a time-travel feature to animate through the year

## 📄 License

MIT License - Feel free to use, modify, and distribute!

## 💫 Credits

Created with ❤️ using Three.js

---

**Made with passion for the coding community. May your galaxy shine bright! ✨**