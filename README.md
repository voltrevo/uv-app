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
