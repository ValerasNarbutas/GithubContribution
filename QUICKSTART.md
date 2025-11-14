# GitHub Waves - Quick Start Guide

## 🚀 Getting Started in 30 Seconds

1. **Download**: Clone or download this repository
2. **Open**: Double-click `index.html` (or right-click → Open with → your browser)
3. **Explore**: Your music visualizer is ready!

That's it! No installation, no build steps, no dependencies.

## 🎮 How to Use

### Navigation
- **Choose Visualization**: Click mode buttons (📊 Bars, 〰️ Wave, ⭕ Circular)
- **Pause/Play**: Click the pause button to stop/start animations
- **Explore Details**: Hover over bars to see date and contribution count (Bars mode)
- **Check Stats**: View your contribution statistics in the top-left panel

### Understanding Your Visualizer

#### Colors Mean Activity
- 🟣 **Purple**: Low contribution days (1-10 contributions)
- 💜 **Purple-Pink**: Medium contribution days (11-20 contributions)  
- 💗 **Pink**: High contribution days (21+ contributions)
- ⚫ **Dim/Small**: Days with no contributions

#### Visualization Modes

**📊 Bars Mode**
- Frequency bars extending from center
- Height represents contribution intensity
- Bars pulse with animation
- Hover to see details

**〰️ Wave Mode**
- Multiple layered sine waves
- Wave amplitude based on contributions
- Flowing, organic motion
- Creates audio waveform effect

**⭕ Circular Mode**
- Concentric rings radiating outward
- Particles positioned in circular patterns
- Pulsating center core
- Creates radial symmetry

### Statistics Panel

The info panel shows:
- **Total Contributions**: Your complete 2025 count
- **Current Streak**: How many consecutive days you've contributed
- **Longest Streak**: Your best streak of the year
- **Loudest Day**: The day with the most contributions

## 🔧 Customization

Want to personalize your visualizer? Open `index.html` in a text editor:

### Change Animation Speed
Find this line (~line 207):
```javascript
this.animationTime += 0.02;
```
Change `0.02` to a larger number for faster animation (e.g., `0.05`)

### Modify Colors
Find the color section (~line 252):
```javascript
const hue = 280 - (normalizedValue * 60); // Purple to Pink
```
Change `280` (base hue) or `60` (range) for different color schemes

### Adjust Wave Count
Find this line (~line 295):
```javascript
const waveCount = 5;  // Number of wave layers
```
Change to 3-10 for fewer/more waves

### Modify Circular Rings
Find this line (~line 321):
```javascript
const rings = 3;  // Number of concentric rings
```
Change to 2-5 for different patterns

## 🌐 Deploy to GitHub Pages

Share your galaxy online:

1. Push this repository to GitHub
2. Go to **Settings** → **Pages**
3. Select **main** branch as source
4. Your galaxy will be at: `https://yourusername.github.io/GithubContribution/`

## 📱 Browser Compatibility

Works in all modern browsers:
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Opera

Requires: CSS 3D transforms and Canvas API support (available in all browsers since 2015)

## 🎨 Tips for Best Experience

1. **Use a larger screen** for the full immersive effect
2. **Pause rotation** to explore specific time periods
3. **Hover over bright stars** to see your most productive days
4. **Check stats** to understand your coding patterns
5. **Share screenshots** of your beautiful galaxy!

## 🔮 Future Integration

This prototype uses generated sample data. To connect to your real GitHub contributions:

### Using GitHub API

1. Get a GitHub Personal Access Token
2. Fetch contribution data using GitHub's GraphQL API
3. Replace the `generateContributionData()` function with API calls

Example query:
```graphql
query {
  user(login: "yourusername") {
    contributionsCollection(from: "2025-01-01T00:00:00Z", to: "2025-12-31T23:59:59Z") {
      contributionCalendar {
        totalContributions
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

### Privacy Note
The current implementation runs entirely in your browser with no external calls. Your data stays private!

## 🐛 Troubleshooting

**Q: The galaxy isn't showing**
- A: Make sure you're using a modern browser (Chrome, Firefox, Safari, Edge)
- A: Try refreshing the page (Ctrl/Cmd + R)

**Q: Stars are overlapping weirdly**
- A: This is normal! It creates depth in the 3D space

**Q: Performance is slow**
- A: The galaxy renders 365+ objects. Try closing other tabs or using a more powerful device

**Q: I want to see my real contributions**
- A: Currently uses sample data. See "Future Integration" section above for GitHub API integration

## 💡 Fun Ideas

- Screenshot different modes for comparison
- Watch how patterns emerge in different visualizations
- Use it in presentations about your coding journey
- Share screenshots of interesting patterns
- Compare wave patterns across different time periods

## 🌟 Enjoy Your Music Visualizer!

Your contributions create rhythm and patterns - like music, each one adds to the symphony of your coding year. 

Happy exploring! 🎵✨
