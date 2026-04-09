# KYN Lux — Intelligent Sun Therapy Tracking

A premium iPhone PWA for tracking and optimizing sun exposure for Vitamin D synthesis, nitric oxide production, and serotonin elevation.

## Features

### Core Tracking
- **Real-time sun session tracking** with live nutrient rate calculation
- **Three photobiological nutrients**:
  - Vitamin D (IU) — via UVB exposure
  - Nitric Oxide (μmol) — via UVA exposure
  - Serotonin (%) — via retinal light exposure
- **Science-backed calculation engine** based on peer-reviewed research (Holick, Weller, Lambert)

### Session Control
- **Live session stats bar**: UV Index, IU/min rate, burn time countdown
- **Pause/resume** without losing earned nutrients
- **Mid-session adjustments**: Change clothing or activity with forward-only nutrient updates
- **Burn time calculator** based on Fitzpatrick skin type

### Personalization
- **Profile system** with skin type, age, biological sex, and primary health goal
- **Daily targets** customized per nutrient and goal
- **Circadian rhythm scheduler** with three daily light windows (Cortisol Reset, Peak Vitamin D, DLMO Wind-down)
- **iPhone notification reminders** for each window

### Backlog Feature
- **Log past sessions** if you forgot to track in real-time
- Set date, time, duration, and all session parameters
- Real-time earnings estimation based on conditions
- Automatically updates daily progress if session is for today

### Data & Insights
- **Multi-period history** (Today / Week / Month / All Time)
- **Session replay** with full condition metadata
- **Progress rings** (3-ring display) showing VD, NO, and Serotonin toward daily targets
- **Daily accumulation** with midnight reset
- **Theme support**: Dark Luxury, Light & Clean, Auto (follows iOS)

### Circadian Scheduling
- **Morning window** (Cortisol Reset): 6:30–7:30 AM
- **Midday window** (Peak Vitamin D): 12:00–1:00 PM
- **Evening window** (DLMO Wind-down): 6:30–7:30 PM
- Visual indicator showing current/next active window
- Push notifications at each window start

## Installation

### iPhone (Recommended)
1. Open this PWA in **Safari** on your iPhone
2. Tap the **Share** icon → "Add to Home Screen"
3. Name it "KYN Lux" and tap **Add**
4. The app installs as a full-screen PWA without App Store submission

### Browser
Open the `index.html` file directly in any modern web browser (Chrome, Safari, Firefox, Edge).

## Technical Stack

- **Single-file HTML/CSS/JavaScript** — No build process required
- **localStorage** for persistent data (no server needed)
- **OpenMeteo API** (free, no key) for real-time weather/UV data
- **GitHub Pages** for zero-cost hosting

### File Size
- **~301 KB** — Single HTML file includes all logic, styles, and assets

## Data Storage

All data is stored locally in your browser:
- `kyn_profile` — User profile (skin type, age, sex, goals)
- `kyn_sessions` — Array of past sun sessions with metadata
- `kyn_today` — Daily progress (VD, NO, Serotonin, minutes)
- `kyn_reminders` — Circadian window reminder settings
- `kyn_theme` — Theme preference (dark / light / auto)

**No cloud sync, no analytics, no tracking.**

## Science Behind KYN

### Vitamin D (IU)
**Formula**: Base rate × Sky modifier × Clothing exposure × SPF reduction × Pre-meal boost

- **Base rate**: ~200 IU/min (peak midday conditions)
- **Sky modifier**: Clear (1.0×) → Partly (0.75×) → Mostly (0.5×) → Overcast (0.25×)
- **Clothing**: Face & arms (18%) → T-shirt (35%) → Tank (55%) → Swimwear (85%)
- **SPF blocking**: SPF 15 (93.3% UVB block) → SPF 50+ (98% block)
- **Meal boost**: None (1.0×) → Light (1.15×) → Fatty (1.35×)

*Source: Holick, M.F. (2007) "Vitamin D deficiency." NEJM. Holick, M.F. (2015) JCEM.*

### Nitric Oxide (μmol)
**Formula**: Base rate × Sky modifier × Clothing exposure × SPF reduction × Activity modifier

- **Base rate**: ~0.8 μmol/min (UVA-dependent)
- **Activity boost**: Still (0.9×) → Moving (1.0×) → Active (1.1×)
- **Blocked by**: UVA-blocking sunscreen (less effective than UVB)

*Source: Weller, R.B., Wang, Y., He, J., et al. (2014) "Does oral ingestion of nitrite increase plasma nitrite in fasted subjects?" Br J Clin Pharmacol.*

### Serotonin (%)
**Formula**: Base rate × Activity modifier × Clothing exposure (capped at 100% daily)

- **Base rate**: ~0.5%/min per minute of sun exposure
- **Activity boost**: Still (0.9×) → Moving (1.0×) → Active (1.1×)
- **Light exposure**: Impacts retinal illuminance, independent of UVB/UVA
- **Daily cap**: Cannot exceed 100% in a single day

*Source: Lambert, G.W., Reid, C., Kaye, D.M., et al. (2002) "Effect of sunlight and season on serotonin turnover in the brain." Lancet.*

## Usage

### Begin a Session
1. Tap **"Begin Sun Session"** on home screen
2. Set conditions: location, clothing, activity, meal, sunscreen
3. View current UV Index and estimated IU/min rate
4. Tap **"Start"** to begin tracking

### During a Session
- **Live timer** counts elapsed time
- **Nutrient counter** shows real-time IU, μmol, and % earned
- **Pause/Resume** to pause without losing progress
- **Adjust clothing/activity** mid-session — forward rate updates, past earnings preserved
- **Live stats bar** shows UV Index, burn time remaining, sky condition

### Log a Past Session
1. Tap **"Log Past Session"** on home screen
2. Set date, time, duration, and conditions
3. Real-time estimate shows expected earnings
4. Tap **"Log Session"** — updates history and daily progress if applicable

### View History
1. Tap **"History"** in bottom navigation
2. Filter by period (Today / Week / Month / All Time)
3. View daily accumulation with VD, NO, and Serotonin totals
4. Tap individual sessions to see full metadata

### Customize Profile
1. Tap **"Profile"** in bottom navigation
2. Set skin type (I–VI)
3. Set age and biological sex
4. Set primary health goal (VD optimization, Mood, Cardio, Immunity, General)
5. Set daily targets for each nutrient

### Schedule Reminders
1. Tap **"Schedule"** in bottom navigation
2. Enable/disable reminders for each circadian window
3. View next recommended window and countdown timer

### Change Theme
1. Tap **"Profile"** → **"Appearance"**
2. Choose: **Dark Luxury** (default), **Light & Clean**, or **Auto** (follows iOS)

## Browser Compatibility

- ✅ **iOS Safari 13+** (primary target)
- ✅ **Android Chrome**
- ✅ **Desktop browsers** (Chrome, Safari, Firefox, Edge)
- ⚠️ **Older browsers**: Requires ES6 support, CSS Variables, localStorage

## Deployment

### GitHub Pages
1. Push all files to a GitHub repository
2. Go to **Settings → Pages → Build and deployment**
3. Set source to `main` branch (or your branch)
4. Your PWA is live at `https://yourusername.github.io/kyn-lux/`

### Custom Domain
Point your domain to GitHub Pages and configure CNAME in repository settings.

### Self-Hosting
Any static web server works:
- **Netlify**: Drag and drop the HTML file
- **Vercel**: Import GitHub repo
- **Apache/Nginx**: Serve the HTML file directly

## File Structure

```
kyn-lux/
├── index.html              # Single-file PWA (main app)
├── README.md               # This file
├── LICENSE                 # MIT license
├── CHANGELOG.md            # Version history
├── FEATURES.md             # Detailed feature documentation
└── ICONS.md                # SVG icon reference guide
```

**All logic, styles, fonts, and assets are embedded in `index.html`.** No external dependencies except:
- Google Fonts (Bebas Neue, DM Sans) — CDN loaded
- OpenMeteo API — Free, no authentication required

## Future Roadmap

### v5 Features
- **Supabase integration** for multi-device sync (optional, v2 feature)
- **Export/import** sessions (CSV, JSON)
- **Batch upload** of historical sessions
- **Weather archive** integration for past session accuracy
- **Notes** field for session details
- **Photos** attached to sessions
- **Apple Health** integration for step/activity data

### Advanced Calculations
- **Real-time UV index** from location (currently supported via OpenMeteo)
- **Personalized vitamin D targets** based on deficiency status
- **Genetic vitamin D metabolism** variants (future research)
- **Seasonal adjustment** for latitude and time of year

## Contributing

This is a personal health project. Contributions welcome:
- Bug reports and feature requests via GitHub Issues
- Pull requests for improvements (code, design, UX)
- Documentation and translation improvements
- Icon/design system enhancements

## License

MIT License — Free for personal and commercial use. See LICENSE file.

## Disclaimer

**KYN Lux is not medical advice.** This app is for personal sun exposure tracking and estimation only. Consult a dermatologist or healthcare provider before making changes to sun exposure, especially if you have:

- Skin cancer history
- Photosensitivity disorders
- Medication interactions with sunlight
- Vitamin D deficiency (diagnosed)
- Mood disorders being treated with light therapy

UV exposure carries health risks. The calculations in this app are based on peer-reviewed research but should not replace professional medical guidance.

## Support

For issues, questions, or feedback:
- Open a GitHub Issue
- Check existing issues for solutions
- Review the FEATURES.md documentation

## Credits

**Research References:**
- Holick, M.F. (2007) "Vitamin D deficiency." NEJM 357:266–281.
- Weller, R.B., et al. (2014) "Does oral ingestion of nitrite increase plasma nitrite?" Br J Clin Pharmacol 77(2):357–366.
- Lambert, G.W., et al. (2002) "Effect of sunlight and season on serotonin turnover in the brain." Lancet 360(9348):1840–1842.
- Holick, M.F. (2015) "The vitamin D deficiency pandemic and consequences for non-skeletal health." Molecules 20(12):21961–21976.

**Design Inspiration:**
- Oura Ring (health metrics presentation)
- Apple Health (iOS integration patterns)
- Dark Luxury aesthetic (premium health tracking)

---

**Version**: 4.5  
**Last Updated**: April 2026  
**Status**: Actively maintained
