# Quick Start Guide

Get KYN Lux up and running in 5 minutes.

## Installation

### iPhone (Recommended)
1. Open this link in **Safari** on your iPhone
2. Tap the **Share** icon (square with arrow)
3. Scroll down and tap **"Add to Home Screen"**
4. Name it **"KYN Lux"** and tap **"Add"**
5. The app installs instantly — no App Store needed!

### Desktop/Browser
- Simply open `index.html` in any modern web browser

---

## First Launch

### Step 1: Set Your Profile (2 min)
When you first open the app, you'll see an **onboarding flow**:

1. **Name** — Enter your first name
2. **Age** — Your current age
3. **Biological Sex** — Male or Female
4. **Skin Type** — Choose I–VI (Fitzpatrick scale)
   - If unsure, start with **Type III** (moderate sensitivity)
5. **Primary Goal** — Pick one:
   - Vitamin D Optimization (if deficient)
   - Mood & Wellbeing (seasonal depression, alertness)
   - Cardiovascular Health (heart health priority)
   - Immune Support (infection prevention)
   - General Wellness (balanced approach)

This takes ~60 seconds. You can change these anytime in **Profile**.

### Step 2: Grant Location Permission (1 min)
The app asks for your location to fetch real-time weather and UV Index. You'll see:
```
"KYN Lux would like to access your location"
[Don't Allow] [Allow Once] [Allow]
```

Tap **"Allow"** so the app can:
- Detect your geographic position
- Fetch local cloud cover and UV Index
- Estimate burn times accurately

**If you deny**: You can manually enter a city or coordinates in the **Conditions panel** anytime.

### Step 3: Take Your First Session (2 min)

1. Tap **"Begin Sun Session"** on the home screen
2. Check the **Conditions panel**:
   - ✓ Location auto-detected (e.g., "Phoenix, Arizona")
   - ✓ Sky condition from weather (e.g., "Clear ☀️")
   - ✓ UV Index showing (e.g., "8 High")
3. Set your clothing:
   - Default is **"T-shirt & Shorts"** (35% exposure)
   - Change if you're in swimwear, light clothing, etc.
4. Set sunscreen:
   - Default is **"None"**
   - Change if you applied SPF
5. Review **Effective Rate** (e.g., "~220 IU/min")
6. Tap **"Start"** — timer begins!
7. Stay outside for **10–30 minutes**
8. Watch the live counters show nutrients earned
9. Tap **✕** to end — your session is saved!

After your first session, you'll see:
- Progress rings start filling (gold = Vitamin D, red = Nitric Oxide, teal = Serotonin)
- Home screen shows "Today: 25 min · 5,600 IU"
- History records your session with full metadata

---

## Core Features in 30 Seconds

### Home Screen
- **Progress rings**: Show today's nutrient progress (gold/red/teal)
- **Next window**: When to get your next sun exposure
- **Conditions**: Current weather, UV Index, your settings
- **Action buttons**: "Begin Session" or "Log Past Session"

### During a Session
- **Live timer**: Elapsed time (MM:SS)
- **Nutrient counters**: Real-time IU, μmol, % earned
- **Live stats bar**: UV Index, IU/min rate, burn time
- **Mid-session adjustments**: Change clothing/activity (earnings preserved!)

### History
- View all past sessions grouped by date
- Filter by Today / Week / Month / All Time
- Tap a session to see full details (conditions, time, nutrients)

### Profile
- Edit your information (name, age, skin type, goal)
- Set daily targets (customize how many IU/NO/% you aim for)
- Choose theme (Dark Luxury, Light & Clean, Auto)

### Schedule
- See your three daily light windows (morning, midday, evening)
- Enable/disable notifications
- View next window countdown

---

## Tips for Best Results

### Vitamin D
- ✅ **Midday is best** (11 AM–1 PM): UVB angle is highest
- ✅ **Less clothing = faster**: Swimwear earns 2.4× faster than t-shirt
- ✅ **Eat fat first**: Fatty meal before sun boosts absorption by 35%
- ✅ **Avoid SPF**: Sunscreen blocks 93%+ of UVB (needed for VD)
- ❌ Avoid: Overcast days (75% less), heavy clothing

### Nitric Oxide
- ✅ **Any time**: UVA is present all day (less angle-dependent)
- ✅ **Movement helps**: Active boosts rate 10%
- ✅ **Summer > Winter**: UVA increases seasonally
- ⚠️ SPF still blocks some UVA (but less than UVB)

### Serotonin
- ✅ **Morning light is key** (6–8 AM): Synchronizes circadian rhythm
- ✅ **Activity boosts it** (moving/active +10%)
- ✅ **Eyes matter**: Even clothed, light enters eyes and affects mood
- ✅ **Evening counts too** (4–7 PM): Prepares melatonin for sleep

### Circadian Rhythm (Sleep)
- ✅ Get **morning light (6:30–7:30 AM)** every day for best sleep
- ✅ Avoid screens **1–2 hours before bed**
- ✅ **Evening light (6:30–7:30 PM)** also helps sleep timing
- ⚠️ Midday sun is great for VD but doesn't reset sleep as well

---

## Troubleshooting

### "Location not detected"
- Ensure Safari has location permission: **Settings → Safari → Location → Allow**
- If still not working, manually enter your city in the Conditions panel

### "UV Index says —"
- Restart the app or refresh
- Check internet connection (needs OpenMeteo API access)
- Fallback: Enter city name manually to re-fetch

### "Progress rings not updating"
- Make sure you ended the session (tapped ✕)
- Check that the session duration was >12 seconds
- Refresh the page if needed

### "History is empty"
- You just started! Your first few sessions will appear here
- Check that you ended sessions properly (tapped ✕ button)

### "Data disappeared"
- Did you clear Safari cache/cookies? This deletes localStorage
- Use **Settings → Safari → Clear History and Website Data** carefully

---

## Keyboard Shortcuts (Desktop/PWA)

| Key | Action |
|-----|--------|
| `Space` | Start/Pause session |
| `Esc` | Close modal |
| `←` / `→` | Navigate between screens |

---

## What's NOT in KYN Lux (Yet)

- ❌ Cloud sync (planned for v5 via Supabase)
- ❌ Apple Health integration (planned)
- ❌ Batch upload of past sessions (planned)
- ❌ Photo attachments (planned)
- ❌ Notes on sessions (planned)

---

## Need Help?

- **Read FEATURES.md** for detailed documentation of every feature
- **Check CHANGELOG.md** to see what's new in each version
- **Open GitHub Issues** with bugs or feature requests
- **Review README.md** for science sources and disclaimers

---

## Privacy & Data

✅ **All data stays on your device** — localStorage only, no cloud upload
✅ **No tracking** — No analytics, ads, or third-party SDKs
✅ **Weather data only**: OpenMeteo API fetches cloud cover and UV Index (no personal data sent)
✅ **Delete anytime**: Tap "Clear History" in Profile to remove all sessions

---

## Next Steps

1. ✅ Complete your profile (you just did!)
2. 🌞 Take a 15–30 minute sun session
3. 📊 Check your progress rings fill up
4. 📅 Enable Schedule reminders for your light windows
5. 📱 Customize daily targets in Profile based on your goals

**Enjoy optimizing your sun exposure!** ☀️

---

Last updated: April 2026
