# GitHub Galaxy - Quick Start Guide

## 🚀 Getting Started in 30 Seconds

1. **Download**: Clone or download this repository
2. **Open**: Double-click `index.html` (or right-click → Open with → your browser)
3. **Explore**: Your galaxy is ready!

That's it! No installation, no build steps, no dependencies.

## 🎮 How to Use

### Navigation
- **View the Galaxy**: The galaxy automatically rotates to show all angles
- **Pause/Resume**: Click the "⏸️ Pause Rotation" button to stop/start
- **Explore Stars**: Hover over any star to see the date and contribution count
- **Check Stats**: View your contribution statistics in the top-left panel

### Understanding Your Galaxy

#### Colors Mean Activity
- 🔵 **Blue Stars**: Low contribution days (1-10 contributions)
- 🟣 **Purple Stars**: Medium contribution days (11-20 contributions)  
- 🟠 **Pink Stars**: High contribution days (21+ contributions)
- ⚫ **Dim Stars**: Days with no contributions

#### Size Matters
- Larger, brighter stars = more contributions that day
- Each star has a glow effect proportional to activity
- The galactic core pulses at the center

#### The Spiral Structure
- **3 Spiral Arms**: Your year flows through three galaxy arms
- **Time Progression**: Starts near the center, expands outward
- **Natural Flow**: Like a real spiral galaxy (Milky Way, Andromeda)

### Statistics Panel

The info panel shows:
- **Total Contributions**: Your complete 2025 count
- **Current Streak**: How many consecutive days you've contributed
- **Longest Streak**: Your best streak of the year
- **Brightest Day**: The day with the most contributions

## 🔧 Customization

Want to personalize your galaxy? Open `index.html` in a text editor:

### Change Animation Speed
Find this line (~line 67):
```css
animation: rotate 120s linear infinite;
```
Change `120s` to a smaller number for faster rotation (e.g., `60s`)

### Modify Colors
Find the color section (~line 260):
```javascript
if (normalizedContributions < 0.33) {
    color = '#58a6ff';  // Blue - change this hex code
} else if (normalizedContributions < 0.66) {
    color = '#6a7fdb';  // Purple - change this hex code
} else {
    color = '#ff6b9d';  // Pink - change this hex code
}
```

### Adjust Galaxy Arms
Find this line (~line 207):
```javascript
const armCount = 3;  // Change to 2, 4, or 5 for different patterns
```

### Increase Spiral Tightness
Find this line (~line 208):
```javascript
const rotationsPerArm = 2.5;  // Increase for tighter spirals
```

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

- Screenshot your galaxy at different angles
- Compare different years (create multiple versions)
- Print it as poster art
- Use it in presentations about your coding journey
- Share with your team to compare galaxies

## 🌟 Enjoy Your Galaxy!

Your contributions are like stars in the universe - each one matters and together they create something beautiful. 

Happy exploring! 🚀✨
