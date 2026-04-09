# KYN Lux — Features & Usage Guide

Complete documentation of all KYN Lux features and how to use them.

## Table of Contents
1. [Home Screen](#home-screen)
2. [Session Tracking](#session-tracking)
3. [Backlog Feature](#backlog-feature)
4. [History & Analytics](#history--analytics)
5. [Profile & Settings](#profile--settings)
6. [Circadian Schedule](#circadian-schedule)
7. [Science Engine](#science-engine)

---

## Home Screen

### Progress Rings
The home screen displays three progress rings showing your daily progress toward nutrient targets:

- **Vitamin D (Gold)** — Top ring, measures IU earned
- **Nitric Oxide (Red)** — Right ring, measures μmol earned
- **Serotonin (Teal)** — Left ring, measures % serotonin lift

Each ring fills from 0% to 100% as you approach your daily target. Rings are **color-coded**:
- 🟡 **Gold** (0–49%): You're on track
- 🟠 **Amber** (50–74%): Getting close
- 🟡 **Full** (75–100%): Target achieved

### Daily Summary
Below the rings, you'll see:
- **Total minutes** of sun exposure today
- **Next light window** (e.g., "Peak Vitamin D in 4h 32m")
- **Current conditions** (location, sky, UV Index)

### Current Conditions Panel
Shows real-time weather and environment:
- **Location** with GPS icon and manual override option
- **Sky condition** (clear ☀️, partly ⛅, mostly 🌥, overcast ☁️)
- **Cloud cover %** updated from OpenMeteo API
- **UV Index** (0–11+ scale with burn risk indicator)
- **Effective UV** bar showing how much UV reaches your skin given all modifiers

#### Clothing Coverage
Five buttons showing your current clothing level:
- 🧥 **Face & Arms** (18% exposure)
- 👕 **T-shirt & Shorts** (35% exposure) ← default
- 🩱 **Tank & Shorts** (55% exposure)
- 🩲 **Swimwear** (85% exposure)

Each affects how much skin is exposed to UV radiation.

#### Sunscreen (SPF)
- **Off** (0% UVB block) ← default
- **SPF 15** (93.3% UVB block)
- **SPF 30** (96.7% UVB block)
- **SPF 50+** (98% UVB block)

SPF blocks UVB (needed for VD) more effectively than UVA.

#### Pre-session Meal
- 💧 **None** (1.0× VD boost)
- 🥗 **Light Meal** (1.15× VD boost)
- 🥑 **Fatty Meal** (1.35× VD boost) ← best for absorption

Fat-soluble vitamin D absorbs better with dietary fat before sun exposure.

### Effective Rate Bar
Shows your estimated IU/minute earning rate based on:
- Current UV Index
- Sky conditions
- Clothing coverage
- Sunscreen protection
- Activity level (upcoming feature)

**Example**: Clear sky + swimwear + no SPF = ~300 IU/min. Overcast + t-shirt + SPF 50 = ~40 IU/min.

### Action Buttons

#### Begin Sun Session
Taps into the session tracking screen where you'll set conditions and start the timer.

#### Log Past Session
Opens the backlog modal to log a session you forgot to track in real-time.

---

## Session Tracking

### Starting a Session

1. Tap **"Begin Sun Session"** button
2. You're taken to the **Session Screen** with a live timer
3. Conditions are pre-populated from your home screen settings (you can adjust them)
4. Tap **"Start"** to begin the timer

### Live Session Display

#### Session Timer
Large, prominent display showing elapsed time in MM:SS format (00:00 to 59:59+).

#### Live Nutrient Counters
Real-time display of nutrients earned:
- **Vitamin D**: Shown in IU (e.g., "2,400 IU")
- **Nitric Oxide**: Shown in μmol (e.g., "18.5 μmol")
- **Serotonin**: Shown as % (e.g., "45%", capped at 100% daily)

#### Dial Ring
Animated progress ring that fills as you sit in the sun:
- One full rotation = 60 minutes
- Shows visual progress toward burn time and daily serotonin cap

#### Live Stats Bar
Sticky header showing three critical metrics:

**UV Index** (e.g., "8" with color coding)
- 🟢 Low (0–2)
- 🟡 Moderate (3–5)
- 🟠 High (6–7)
- 🔴 Very High (8–10)
- 🔴 Extreme (11+)

**IU/min rate** (e.g., "220 IU/min")
- Updates every 10 seconds
- Changes if you adjust clothing or activity

**Burn time countdown** (e.g., "23 min until burn")
- Based on your Fitzpatrick skin type
- Color-coded:
  - 🟢 Green (>30 min): Safe
  - 🟡 Yellow (15–30 min): Caution
  - 🔴 Red (<15 min): Reduce time

### Mid-Session Controls

#### Pause/Resume Button
Press to pause the timer without losing nutrients already earned. Paused time doesn't count toward nutrient earnings.

#### Clothing Adjuster
Accordion dropdown menu showing five coverage levels. Tap to change:
- ✓ **Already-earned nutrients are preserved**
- Only the **forward rate changes**
- Example: 10 minutes at 35% coverage earning 200 IU/min = 2,000 IU earned. Change to 85% coverage, earn 300 IU/min going forward.

#### Activity Adjuster
Three options affecting NO and Serotonin:
- 🧘 **Still** (0.9× multiplier) — Sitting, resting
- 🚶 **Moving** (1.0× multiplier) — Walking slowly
- 🏃 **Active** (1.1× multiplier) — Exercise, sports

#### SPF Adjustment
Change sunscreen level mid-session (e.g., applied SPF after 10 minutes).

### Ending a Session

Tap the **close button (✕)** to end the session. If you've been in the sun for **>12 seconds**:
- Session is saved to history
- Nutrients added to today's progress
- Progress rings update
- Toast notification shows summary: "☀️ 25 min · 5,600 IU earned"

If **<12 seconds**, session is discarded (likely accidental tap).

---

## Backlog Feature

### Why Log Past Sessions?
Sometimes you sit in the sun but forget to open the app. The backlog feature lets you retroactively log those sessions with full accuracy.

### How It Works

1. **Tap "Log Past Session"** on home screen
2. **Modal opens** with these fields (pre-populated with current settings):

#### Date & Time
- Date picker (YYYY-MM-DD format)
- Time picker (HH:MM format)
- Used to determine if session counts toward today's progress

#### Duration (minutes)
- Number input (1–240 minutes)
- Required field

#### Location
- **Displays current location** from your app settings (e.g., "Phoenix, Arizona")
- Tap **"Change"** button to edit if you were elsewhere
- Optional location override with city name or lat,lng format

#### Sky Conditions
- Four buttons: ☀️ Clear, ⛅ Partly, 🌥 Mostly, ☁️ Overcast
- Defaults to "Clear"
- Affects VD and NO calculations

#### Clothing Coverage
- Five buttons representing exposure % (18%, 35%, 55%, 85%, or nude)
- Defaults to "T-shirt & Shorts" (35%)

#### Activity Level
- Three buttons: 🧘 Still, 🚶 Moving, 🏃 Active
- Defaults to "Still"
- Affects NO and Serotonin rates

#### Pre-session Meal
- Three buttons: 💧 None, 🥗 Light, 🥑 Fatty
- Defaults to "Light"
- Only affects Vitamin D boost

#### Sunscreen (SPF)
- Four buttons: None, SPF 15, SPF 30, SPF 50+
- Defaults to "None"
- Affects UVB/UVA blocking

### Real-Time Earnings Estimate
As you adjust parameters, the modal shows a live preview:
```
Estimated Earnings:
Vitamin D: 4,800 IU
Nitric Oxide: 12.5 μmol
Serotonin: 42%
```

This helps you verify the session makes sense before logging.

### Logging & Updates
Tap **"Log Session"** to:
1. Validate all required fields (date, time, duration)
2. Calculate earnings using the full science engine
3. Add session to your history
4. **If session is for today**, update daily progress rings immediately
5. **If session is for past day**, store it in history (doesn't affect today)

Toast notification confirms: "✓ 30 min · 6,000 IU logged"

---

## History & Analytics

### History Screen
Tap the **History** icon in bottom navigation (📊) to view past sessions.

### Period Filters
Choose how far back to view:
- **Today** — All sessions since midnight
- **Week** — Last 7 days
- **Month** — Last 30 days
- **All Time** — Every session ever logged

### Daily Grouping
Sessions are grouped by date:
```
Tuesday, March 25
⏰ 9:15 AM  |  30 min  |  5,600 IU  |  ☀️ Clear
⏰ 5:30 PM  |  15 min  |  1,800 IU  |  ⛅ Partly

Daily total: 45 min | 7,400 IU | 68% VD target
```

Each day shows:
- **Total minutes** of sun exposure
- **Total Vitamin D** earned (IU)
- **% of daily VD target** completed
- **All sessions** with time, duration, nutrient gains, and sky condition

### Session Details
Tap a session to see full metadata:
- Exact timestamp (date + time)
- Duration
- VD, NO, and Serotonin earned
- Full conditions:
  - Sky (clear/partly/mostly/overcast)
  - Clothing coverage level
  - Activity level
  - Pre-meal (none/light/fatty)
  - Sunscreen (SPF level)
  - Location
  - Whether it was real-time tracked or backlogged

### Charts
History displays a **bar chart** showing daily totals:
- X-axis: Date
- Y-axis: IU earned
- Color-coded by nutrient mix
- Tapping a bar shows that day's sessions

---

## Profile & Settings

### Profile Screen
Tap the **Profile** icon in bottom navigation (👤).

### User Information

#### Name
First name only. Used in welcome messages and notifications.

#### Age
Numeric age (18–100). Used for:
- Vitamin D deficiency risk assessment
- Circadian rhythm recommendations

#### Biological Sex
- Male
- Female

Used for hormone-related serotonin response estimation.

#### Skin Type (Fitzpatrick Scale)
Six options (Type I–VI). Determines UV sensitivity and burn time:
- **Type I** — Always burns, never tans (pale/fair)
- **Type II** — Burns easily, tans minimally (fair)
- **Type III** — Burns moderately, tans gradually (light brown)
- **Type IV** — Burns minimally, tans easily (brown)
- **Type V** — Rarely burns, tans deeply (dark brown)
- **Type VI** — Never burns, deeply pigmented (very dark)

Higher types require longer sun exposure for equivalent VD and tolerate UV better.

### Health Goal
Choose your primary focus:
- **Vitamin D Optimization** — Maximize IU/min rate
- **Mood & Mental Wellbeing** — Prioritize serotonin (morning + evening windows)
- **Cardiovascular Health** — Emphasize nitric oxide production
- **Immune Support** — Balanced VD and NO
- **General Wellness** — Balanced all three

This affects your daily targets and window recommendations.

### Daily Targets
Customize your daily nutrient goals:
- **Vitamin D target** (default 2,000–4,000 IU, varies by goal)
- **Nitric Oxide target** (default 20–30 μmol)
- **Serotonin target** (default 50–100%)

Progress rings fill to 100% when you hit these targets.

### Appearance

#### Theme
- **Dark Luxury** (default) — Deep blacks, warm gold/amber accents
- **Light & Clean** — Bright whites, muted browns
- **Auto** — Follows your iPhone's system theme (dark/light mode)

Theme changes apply instantly to all screens.

### Data Management

#### Clear Session History
⚠️ **Destructive action** — Permanently deletes all logged sessions. A confirmation dialog appears before deletion.

---

## Circadian Schedule

### Schedule Screen
Tap the **Schedule** icon in bottom navigation (📅).

### Three Light Windows
The app recommends sun exposure at three optimal times:

#### 1. Cortisol Reset (6:30–7:30 AM)
**Purpose**: Morning light synchronizes circadian rhythm and boosts morning cortisol.

**Why**: Early sunlight resets your 24-hour cycle, improving sleep at night and alertness during day.

**Nutrients**: Serotonin boost (alertness), some Vitamin D.

**Recommendation**: 10–20 minutes of direct sunlight, minimal clothing.

---

#### 2. Peak Vitamin D (12:00–1:00 PM)
**Purpose**: Midday sun has the highest UVB angle, maximizing vitamin D synthesis.

**Why**: UVB index peaks when sun is highest in sky; skin produces D3 most efficiently.

**Nutrients**: Maximum Vitamin D, good Nitric Oxide.

**Recommendation**: 20–40 minutes depending on skin type and season.

---

#### 3. DLMO Wind-down (6:30–7:30 PM)
**Purpose**: Evening light prepares melatonin (sleep hormone) for bedtime.

**Why**: Afternoon/evening sunlight suppresses melatonin, promoting later sleep onset and deeper night sleep.

**Nutrients**: Serotonin (mood), Nitric Oxide (vascular health).

**Recommendation**: 10–30 minutes, moderate clothing (outdoor activity is ideal).

---

### Window Indicators
For each window, you see:
- **Status** (e.g., "In 4h 32m" or "Active now" or "Passed")
- **Countdown timer** to next window
- **Duration** (e.g., "1 hour window")
- **Toggle** to enable/disable reminders

### Notifications
When enabled, you'll receive an iPhone notification **at the start of each window**:
```
🌅 Cortisol Reset
Time for morning light! 10–20 min recommended.
```

Tap to open the app and start a session.

---

## Science Engine

### Vitamin D Calculation

```
Rate = Base Rate × Sky Mod × Exposure % × SPF Mod × Meal Boost
Earned = Rate × Duration
```

**Base Rate**: 200 IU/min (peak midday conditions, clear sky, 85% exposure, no SPF)

**Sky Modifier**:
- Clear: 1.0×
- Partly Cloudy: 0.75×
- Mostly Cloudy: 0.5×
- Overcast: 0.25×

**Exposure %** (clothing):
- Nude: 100% (not recommended)
- Swimwear: 85%
- Tank & Shorts: 55%
- T-shirt & Shorts: 35%
- Face & Arms: 18%

**SPF Modifier** (UVB blocking):
- None: 1.0× (0% block)
- SPF 15: 0.067× (93.3% block)
- SPF 30: 0.033× (96.7% block)
- SPF 50+: 0.02× (98% block)

**Meal Boost** (fat-soluble absorption):
- None: 1.0×
- Light Meal: 1.15×
- Fatty Meal: 1.35×

**Example**:
```
Conditions: Clear sky, swimwear, no SPF, fatty meal, 30 min
Rate = 200 × 1.0 × 0.85 × 1.0 × 1.35 = 230 IU/min
Earned = 230 × 30 = 6,900 IU
```

---

### Nitric Oxide Calculation

```
Rate = Base Rate × Sky Mod × Exposure % × SPF Mod × Activity Mod
Earned = Rate × Duration
```

**Base Rate**: 0.8 μmol/min (UVA-dependent, peak conditions)

**Sky Modifier**: Same as Vitamin D

**Exposure %**: Same as Vitamin D

**SPF Modifier** (UVA blocking, less effective):
- None: 1.0×
- SPF 15: 0.85×
- SPF 30: 0.75×
- SPF 50+: 0.65×

**Activity Modifier**:
- Still: 0.9×
- Moving: 1.0×
- Active: 1.1×

**Example**:
```
Conditions: Partly cloudy, t-shirt, SPF 30, moving, 20 min
Rate = 0.8 × 0.75 × 0.35 × 0.75 × 1.0 = 0.157 μmol/min
Earned = 0.157 × 20 = 3.14 μmol
```

---

### Serotonin Calculation

```
Rate = Base Rate × Activity Mod × Exposure %
Earned = min(Rate × Duration, 100%)
```

**Base Rate**: 0.5%/min (retinal light exposure, mood lift)

**Activity Modifier**: Same as Nitric Oxide

**Exposure %**: How much skin + eyes are exposed

**Daily Cap**: Serotonin cannot exceed 100% in a single day (diminishing returns)

**Example**:
```
Conditions: Moving, tank top, 25 min
Rate = 0.5 × 1.0 × 0.55 = 0.275%/min
Earned = 0.275 × 25 = 6.875%, capped at 100% if already high
```

---

### Burn Time Calculation

Based on **Minimal Erythemal Dose (MED)** per skin type (WHO guidelines):

```
Burn Time (min) = (MED × SPF) / Current UV Index
```

**MED by Skin Type**:
- Type I: 15–20 minutes
- Type II: 20–30 minutes
- Type III: 30–40 minutes
- Type IV: 40–50 minutes
- Type V: 50–60 minutes
- Type VI: 60+ minutes

**Example**:
```
Skin Type III (MED 35 min), SPF 0, UV Index 8
Burn Time = (35 × 1.0) / 8 = 4.375 minutes

Same conditions with SPF 50 (blocks 98%):
Burn Time = (35 × 50) / 8 = 218.75 minutes (~3.6 hours)
```

---

## Research Sources

**Vitamin D Synthesis:**
- Holick, M.F. (2007) "Vitamin D deficiency." NEJM 357:266–281
- Holick, M.F. (2015) "The vitamin D deficiency pandemic." Molecules 20(12):21961–21976

**Nitric Oxide (Sunlight):**
- Weller, R.B., Wang, Y., He, J., et al. (2014) "Does oral ingestion of nitrite increase plasma nitrite in fasted subjects?" Br J Clin Pharmacol 77(2):357–366

**Serotonin & Light:**
- Lambert, G.W., Reid, C., Kaye, D.M., et al. (2002) "Effect of sunlight and season on serotonin turnover in the brain." Lancet 360(9348):1840–1842

**Circadian Rhythm:**
- Czeisler, C.A. & Gooley, J.K. (2007) "Sleep and circadian rhythms in humans." Cold Spring Harb Symp Quant Biol 72:579–597

**Sunburn Risk (Fitzpatrick):**
- Fitzpatrick, T.B. (1988) "The validity and practicality of sun-reactive skin types I through VI." Arch Dermatol 124(6):869–871

---

**Last Updated**: April 2026
