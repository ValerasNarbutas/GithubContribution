# 🎵 GitHub Waves - 2025 Contributions Visualization

A unique and stunning music visualizer for GitHub contributions in 2025, transforming your coding activity into beautiful animated sound waves and frequency bars.

![GitHub Waves Visualization](https://img.shields.io/badge/Visualization-Music%20Waves-purple)
![Year](https://img.shields.io/badge/Year-2025-blue)
![Tech](https://img.shields.io/badge/Tech-Canvas%202D-brightgreen)

## 🎨 Concept

Unlike traditional 2D contribution graphs, **GitHub Waves** transforms your coding activity into a dynamic audio-visual experience:

- **🎵 Each contribution day** creates a frequency bar or wave point
- **✨ Contribution intensity** determines the height, brightness, and color
- **〰️ Multiple visualization modes** - Bars, Waves, and Circular patterns
- **🎮 Interactive controls** to switch modes and pause/play animations
- **🎨 Color gradient** transitions from blue (low activity) → purple (medium) → pink (high activity)

## ✨ Features

### Visual Modes
- **📊 Bars Mode**: Frequency bars that pulse vertically with glow effects
- **〰️ Wave Mode**: Multiple layered sine waves flowing across the screen
- **⭕ Circular Mode**: Concentric rings radiating from center with particle effects
- **🎨 Dynamic Coloring**: Purple-to-pink gradient based on contribution intensity
- **✨ Smooth Animations**: Canvas-based rendering with pulsing and flowing effects

### Interactive Features
- **Mode Switching**: Toggle between Bars, Wave, and Circular visualizations
- **Play/Pause**: Control animation playback
- **Hover Tooltips**: See exact date and contribution count (in Bars mode)
- **Responsive Design**: Adapts to any screen size
- **Smooth Transitions**: Fluid animations at 60 FPS

### Statistics Dashboard
- **Total Contributions**: Your complete 2025 contribution count
- **Current Streak**: Active contribution days in a row
- **Longest Streak**: Your best contribution streak of the year
- **Loudest Day**: The day with maximum contributions

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
| **Switch to Bars** | Click "📊 Bars" button |
| **Switch to Waves** | Click "〰️ Wave" button |
| **Switch to Circular** | Click "⭕ Circular" button |
| **Pause/Play** | Click "⏸️ Pause" / "▶️ Play" button |
| **View Details** | Hover over bars (Bars mode only) |

## 🔧 Technical Details

### Technologies Used
- **Canvas 2D API**: Hardware-accelerated 2D rendering
- **Vanilla JavaScript**: No framework dependencies
- **HTML5 Canvas**: Real-time animation rendering
- **CSS3**: Modern styling with backdrop filters and gradients

### Architecture
- **Self-contained**: Single HTML file with embedded CSS and JavaScript
- **No build step**: Works directly in the browser
- **No external dependencies**: Pure web standards
- **Responsive**: Adapts to any screen size

### Performance
- **365 contribution bars/points**: One for each day of the year
- **60 FPS**: Smooth animation on modern hardware
- **Canvas rendering**: Efficient 2D graphics
- **Real-time effects**: Pulsing, glowing, and flowing animations

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

#### Change Animation Speed
```javascript
this.animationTime += 0.02;  // Increase for faster animation
```

#### Modify Color Palette
```javascript
// In drawing methods, adjust hue values:
const hue = 280 - (normalizedValue * 60); // Purple to Pink
// Change base hue (280) or range (60) for different colors
```

#### Adjust Visualization Modes
```javascript
// Add new modes or modify existing ones in the draw methods
drawBarsMode() { /* bars rendering */ }
drawWaveMode() { /* wave rendering */ }
drawCircularMode() { /* circular rendering */ }
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

What makes GitHub Waves stand out:

1. **Music Visualizer Theme**: First GitHub contribution visualizer using audio-reactive aesthetics
2. **Multiple Modes**: Three distinct visualization styles (Bars, Wave, Circular)
3. **Canvas-Based**: Smooth 2D animations without complex 3D libraries
4. **Zero Dependencies**: Single file, works offline after first load
5. **Performance**: Renders 365+ elements at 60 FPS smoothly
6. **Interactive**: Real-time mode switching and tooltips

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
- The beauty of music visualizers and audio-reactive art
- The rhythm and flow of coding activity throughout the year
- The desire to make contribution graphs more engaging and dynamic
- The concept that contributions have rhythm - peaks, valleys, and patterns

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