# Changelog

All notable changes to KYN Lux are documented here. The app follows semantic versioning.

## [4.5] — April 2026 (Current)

### Added
- **Backlog feature**: Log past sun sessions with full parameter control
  - Date/time picker for when session occurred
  - Duration, location, sky conditions, clothing, activity, meal, SPF
  - Real-time earnings estimation as parameters change
  - Smart location defaulting to app's current geolocation
  - Automatically updates daily progress for today's backlog sessions
  
- **Enhanced location handling**
  - Backlog modal pre-loads current GPS location from app settings
  - Option to change location without re-setting global location
  - Display of current location with easy override mechanism

### Improved
- Backlog form UX with collapsible location editor
- Real-time calculation accuracy with improved modifiers
- Modal styling and responsiveness across devices

### Fixed
- Syntax errors in function declarations
- Brace balancing in JavaScript sections

## [4.4] — March 2026

### Added
- **Circadian Rhythm Scheduler**
  - Three daily light windows: Cortisol Reset (6:30–7:30 AM), Peak Vitamin D (12:00–1:00 PM), DLMO Wind-down (6:30–7:30 PM)
  - iPhone push notifications for each window
  - Visual indicator of current/next window

- **Dynamic theme support**
  - Dark Luxury (default) — premium, warm aesthetic
  - Light & Clean — bright, minimal design
  - Auto — follows iOS system preference

### Improved
- Animated accordion-style dropdowns for clothing and activity selection
- Mid-session inline adjustments preserve earned nutrients
- Gold dot selection indicators in dropdown menus

## [4.3] — February 2026

### Added
- **Live session stats bar**
  - Current UV Index
  - IU/min rate calculation
  - Burn time countdown (color-coded by risk)
  - Sky condition emoji indicator

- **Real-time nutrient earning display**
  - Live Vitamin D, Nitric Oxide, Serotonin counters
  - Animated dial ring showing session progress (0–60 min)
  - Per-nutrient rate calculations

### Improved
- Session drawer UX with cleaner parameter controls
- Effective rate calculation based on all active conditions

## [4.2] — January 2026

### Added
- **Full science engine** per nutrient
  - Vitamin D: UVB-based, clothing + SPF + meal modifiers
  - Nitric Oxide: UVA-based, activity multiplier
  - Serotonin: Retinal exposure, activity boost, daily cap at 100%

- **SPF differential blocking**
  - Separate UVB/UVA block rates per SPF level
  - Realistic sunscreen effectiveness modeling

- **Activity multipliers**
  - Still (0.9×) / Moving (1.0×) / Active (1.1×)
  - Affects NO and Serotonin rates

- **Pre-session meal boost**
  - None (1.0×) / Light (1.15×) / Fatty (1.35×)
  - Only affects Vitamin D absorption

### Improved
- Accuracy of all nutrient calculations
- Weather API integration with fallback logic

## [4.1] — December 2025

### Added
- **Multi-period history view**
  - Today / Week / Month / All Time filters
  - Daily accumulation display
  - Stacked bar chart for visual trends

- **Session metadata storage**
  - Full condition snapshot per session
  - Location, sky, clothing, activity, meal, SPF
  - Timestamp and duration logging

### Improved
- History rendering performance
- Daily reset logic at midnight
- Chart accuracy and readability

## [4.0] — November 2025 (Major Release)

### Added
- **Onboarding flow**
  - First-time user setup with profile questions
  - Skin type (I–VI Fitzpatrick scale)
  - Age, biological sex, health goal
  - Daily nutrient targets

- **Profile system**
  - Editable user information
  - Daily target customization per nutrient
  - Goal-based recommendations

- **Home screen redesign**
  - Progress rings (3-ring VD/NO/Serotonin display)
  - Daily summary stats
  - Next window indicator

- **Burn time calculator**
  - Fitzpatrick-based MED calculation
  - SPF-adjusted burn times
  - Live countdown during session

- **Conditions panel**
  - Real-time weather from OpenMeteo API
  - Cloud cover percentage
  - Manual location override
  - UV Index display

### Improved
- Typography system (Bebas Neue + DM Sans)
- Dark Luxury aesthetic refinement
- iOS PWA optimization
- Session state management

## [3.5] — October 2025

### Added
- **Pause/Resume session** functionality
  - Preserves already-earned nutrients
  - Pause time tracking with tolerance
  - Visual pause indicator

### Improved
- Session accuracy with pause logic
- UI responsiveness during long sessions

## [3.0] — September 2025

### Added
- **Core session tracking**
  - Start/stop timer with millisecond precision
  - Real-time VD, NO, Serotonin calculation
  - Animated progress dial

- **Session conditions**
  - Clothing coverage (face-arms, t-shirt, tank, swimwear)
  - Activity level (still, moving, active)
  - Sky condition (clear, partly, mostly, overcast)
  - SPF sunscreen selection

- **Nutrient rate engine**
  - Base rates: 200 IU/min VD, 0.8 μmol/min NO, 0.5%/min SER
  - Sky modifiers
  - Clothing exposure fractions

- **Daily progress tracking**
  - Midnight reset
  - Cumulative daily totals
  - localStorage persistence

### Improved
- CSS variable system for theming
- Font loading and fallbacks
- Mobile viewport optimization

## [2.0] — August 2025

### Added
- **Navigation system**
  - Bottom nav bar (Home, Session, Schedule, History, Profile)
  - Screen routing and state persistence

- **History view**
  - Session list with metadata
  - Session details modal
  - Date-based grouping

- **Profile view**
  - User information display
  - Goal settings
  - Daily targets

### Improved
- Overall app structure and modularity

## [1.0] — July 2025 (Initial Release)

### Added
- Single-file HTML PWA
- Basic session tracking
- localStorage integration
- Responsive mobile design
- iOS home screen installability

---

## Planned Features (Future Versions)

### v5 (Q2 2026)
- **Multi-device sync** via Supabase (optional)
- **Export/import** (CSV, JSON)
- **Batch session upload**
- **Apple Health** integration
- **Weather archive** for past accuracy

### v6 (Q4 2026)
- **Genetic variants** in vitamin D metabolism
- **Latitude-adjusted** calculations
- **Seasonal trends** analysis
- **Deficiency detection** thresholds
- **Community goals** and leaderboards

---

## Version History at a Glance

| Version | Date | Key Addition |
|---------|------|--------------|
| 4.5 | Apr 2026 | Backlog feature + smart location defaulting |
| 4.4 | Mar 2026 | Circadian scheduler + theme support |
| 4.3 | Feb 2026 | Live stats bar + nutrient counters |
| 4.2 | Jan 2026 | Full science engine + activity/meal modifiers |
| 4.1 | Dec 2025 | Multi-period history view |
| 4.0 | Nov 2025 | Major UI redesign + profile system |
| 3.5 | Oct 2025 | Pause/resume sessions |
| 3.0 | Sep 2025 | Core tracking + conditions engine |
| 2.0 | Aug 2025 | Navigation system |
| 1.0 | Jul 2025 | Initial release |
