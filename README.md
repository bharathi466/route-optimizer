# Multi-Stop Route Optimizer → Google Maps

A simple, free web tool that takes a starting location and a list of addresses, figures out the fastest or shortest order to visit every stop, and gives you a **Google Maps link** you can open directly on your phone.

No app store download, no logins, and no paid subscriptions required.

---

## What It Does (In Plain English)

When you have multiple deliveries or errands to run, typing stops into Google Maps one by one and guessing the best order takes forever. This tool does the heavy lifting for you:

1. **You pick where you are starting from** (for example, *Target Arlington* or *Target Wheeling*).
2. **You give it your stops**—either by uploading screenshots from your phone or pasting/typing the addresses.
3. **It calculates the smartest order** so you spend less time driving and avoid zig-zagging across town.
4. **You tap "Open in Google Maps ↗"** and your phone launches Google Maps with every stop already loaded in order.

---

## How to Use It (Step by Step)

### Step 1: Choose Your Starting Location
- Pick a preset store from the **Starting Location (Source)** dropdown.
- Want to save another store on your phone? Tap **+ Add Store**, type a label and full address, and tap **Save Store**. *(Note: Stores added this way are saved only on that specific phone/browser.)*
- Need a one-time starting spot? Pick **Custom Starting Address...** from the dropdown.

### Step 2: Add Your Destination Stops (2 Easy Ways)
- **Option A — Upload Screenshots (Easiest on a Phone):**
  1. Tap **📷 Upload Screenshots**.
  2. Select one or multiple screenshots from your photo library at the same time.
  3. Wait a few seconds while it reads the images—it works on both Light Mode and Dark Mode screenshots and automatically pulls the street addresses into the text box.
  - *Tip:* Leave **"Replace existing text box contents"** unchecked if you want to scan more screenshots and add them to your current list.
- **Option B — Type or Paste Addresses:**
  - Tap **Paste** (or type directly into the box).
  - Separate each address with a semicolon (`;`) or put each address on a new line.
  - Example:
    `2580 Forest Glen Trl, Riverwoods, IL 60015; 1260 Anthony Ln, Deerfield, IL 60015`

### Step 3: Pick Your Route Options
- **Optimize For:**
  - **Quickest Travel Time** *(default)* — Finds the fastest driving route.
  - **Shortest Distance** — Finds the route with the fewest total miles.
- **Trip Structure:**
  - **Start at Source → Best Final Stop** *(default)* — Best for one-way routes when you don't need to return to the store afterward.
  - **Round Trip (Return to Source)** — Loops you back to your starting store at the end.
  - **Start at Source → End at Last Box Stop** — Keeps your first stop and the very last address in your box fixed, and optimizes everything in between.
- **Google Maps Link Limit:**
  - **Up to 10 stops / link** *(default)* — Works best when opening the route in the Google Maps app.
  - **Up to 5 stops / link** — Use this if you open links in a phone web browser instead of the Google Maps app.
  - *If you have more stops than the limit, the tool automatically splits your trip into **Leg 1**, **Leg 2**, etc., so nothing gets cut off.*

### Step 4: Optimize & Drive
1. Tap **Optimize Route**.
2. Review your total estimated drive time, mileage, and stop order.
3. Tap **Open in Google Maps ↗** to start navigation.

---

## Save It Like an App on Your Phone

You can add this tool to your phone's Home Screen so it opens with one tap:

- **iPhone (Safari):** Open the page → tap the **Share** button (square with an arrow) → tap **Add to Home Screen**.
- **Android (Chrome):** Open the page → tap the **⋮ menu** (top right) → tap **Add to Home screen** (or **Install app**).

---

## Privacy & Cost

- **100% Free:** Uses free, open mapping data (OpenStreetMap & OSRM) to figure out the stop order, then hands the route off to your Google Maps app for live-traffic navigation.
- **Private on Your Device:** When you upload screenshots, the text reading happens directly inside your phone's browser. Your screenshots are **not** uploaded or saved to any external server.

---

## Quick Troubleshooting

- **"Could not locate address"**
  Make sure the address includes the **City, State, or ZIP code**. If a screenshot cropped out the city/ZIP, just type it in at the end of that address in the box.
- **A screenshot missed an address or read a word strangely**
  Tap **View raw scanned text from screenshots** right below the upload bar. You can see everything the scanner read and copy/fix any line manually.
- **Too many stops for one Google Maps link**
  Google Maps limits how many stops fit in a single link. If you have 12 stops, you'll get **Leg 1** and **Leg 2** buttons—just finish Leg 1, then come back and tap Leg 2.

---

## Updating Constant Stores for Everyone (For the Site Owner)

Stores saved with **+ Add Store** only stay on that single device. To add a permanent store that appears on **all** phones and computers:
1. Open `index.html` in GitHub and click the **Edit (pencil)** icon.
2. Find `DEFAULT_SOURCES` near the middle of the file and add a new entry:
   ```js
   {
     id: "target_palatine",
     name: "Target Palatine",
     address: "679 E Dundee Rd, Palatine, IL 60074"
   }
