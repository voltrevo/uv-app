# UV Index App

A minimalist web app that shows the current UV index for your location and provides sun protection recommendations.

## Features

- **Auto-geolocation**: Automatically detects your location
- **Real-time UV data**: Fetches current UV index from Open-Meteo API
- **Color-coded safety levels**: 
  - 🟢 Low (0-3): No protection needed
  - 🟠 Moderate (3-6): Use sunscreen
  - 🔴 High (6-8): Use sunscreen
  - 🟣 Very High (8-11): Use sunscreen
  - 🔴 Extreme (11+): Use sunscreen
- **Clear recommendations**: Simple, actionable guidance for sun safety
- **Responsive design**: Works on mobile and desktop

## Usage

Visit: https://voltrevo.github.io/uv-app/

Or open `uv-simple.html` locally in any modern browser.

## How It Works

1. Requests your location using the browser's Geolocation API
2. Reverse geocodes coordinates to get city name (BigDataCloud API)
3. Fetches current UV index for your coordinates (Open-Meteo API)
4. Displays UV level with color-coded background and safety recommendation

## No Tracking

This app does not collect or store any personal data. All data fetching happens in your browser with no backend server.

## APIs Used

- **Geolocation API**: Browser native geolocation
- **BigDataCloud**: Reverse geocoding (city names from coordinates)
- **Open-Meteo**: Weather data including UV index

All APIs are free and require no authentication.

## Testing

The app includes comprehensive test files for verification:

### 1. **test-uv-levels.html** - UV Index Logic Tests
- Test all 5 UV index categories (Low, Moderate, High, Very High, Extreme)
- Verify background colors change correctly for each level
- Validate protection messages display properly
- Test boundary values between categories

**Access:** https://voltrevo.github.io/uv-app/test-uv-levels.html

### 2. **icon-verification.html** - Icon & PWA Tests
- Visual verification of app icons (192x192 and 512x512)
- Check manifest.json validity
- PWA installation instructions for iOS, Android, Windows, Mac
- Icon rendering verification checklist

**Access:** https://voltrevo.github.io/uv-app/icon-verification.html

### 3. **api-testing.html** - API Integration Tests
- Test geolocation permission flow
- Verify BigDataCloud reverse geocoding with multiple locations
- Test Open-Meteo UV index API
- Simulate error scenarios and timeout handling

**Access:** https://voltrevo.github.io/uv-app/api-testing.html

### Running Tests Locally

```bash
# Clone the repository
git clone https://github.com/voltrevo/uv-app.git
cd uv-app

# Open any test file in your browser
# Tests work on localhost without HTTPS (except geolocation)
open test-uv-levels.html
open icon-verification.html
open api-testing.html
```

## PWA Installation

The app can be installed as a progressive web app on mobile and desktop:

### iOS
1. Open https://voltrevo.github.io/uv-app/ in Safari
2. Tap Share button (middle icon at bottom)
3. Scroll down and tap "Add to Home Screen"
4. Name it "UV Index" and tap Add

### Android
1. Open https://voltrevo.github.io/uv-app/ in Chrome
2. Tap the menu button (⋮) at top right
3. Tap "Install app" or "Add to Home Screen"
4. Follow the prompts

### Desktop (Windows/Mac)
1. Open https://voltrevo.github.io/uv-app/
2. Click the install icon (⬇️) in the address bar, or
3. Right-click → Create shortcut → Check "Open as window"

## Browser Support

- Chrome/Edge: Full support
- Firefox: Full support (no PWA installation)
- Safari: Full support (PWA installation)
- iOS Safari: Full support
- Android Chrome: Full support

## Development

The app is a single HTML file (`index.html`) with embedded CSS and JavaScript. No build process or dependencies required.

### File Structure
```
uv-app/
├── index.html              # Main app
├── manifest.json           # PWA manifest
├── README.md               # This file
├── test-uv-levels.html     # UV level tests
├── icon-verification.html  # Icon & PWA tests
└── api-testing.html        # API integration tests
```

## Future Enhancements

- [ ] Hourly UV forecast
- [ ] Multi-location support
- [ ] Skin type recommendations
- [ ] Time to burn calculator
- [ ] Historical data graphs
- [ ] Offline support (service worker)
- [ ] Dark mode toggle
