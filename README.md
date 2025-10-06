# GridLoc

**Tactical MGRS Mapping System for Military Operations Planning**

GridLoc is a web-based Progressive Web App (PWA) that provides Military Grid Reference System (MGRS) coordinate mapping and scaled PDF generation for operational planning and navigation.

![GridLoc Interface](https://img.shields.io/badge/Status-Production-00d9ff?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-00d9ff?style=flat-square)
![PWA](https://img.shields.io/badge/PWA-Ready-00d9ff?style=flat-square)

## Features

### Core Functionality
- **MGRS Grid Overlay**: Display 1km × 1km MGRS grid lines on maps
- **Multiple Map Types**: Switch between satellite imagery and terrain maps
- **Flexible Search**: Search by city name, MGRS coordinates, or lat/long
- **Scaled PDF Export**: Generate print-ready maps at 1:25k, 1:50k, or 1:100k scales
- **Grid Labels**: Automatic 2-digit coordinate labels on all map edges
- **Multiple Paper Sizes**: Letter (8.5"×11"), Tabloid (11"×17"), Arch-D (24"×36")

### Technical Features
- Progressive Web App (installable on mobile and desktop)
- Responsive mobile interface with hamburger menu
- Touch-optimized controls for mobile devices
- Real-time MGRS coordinate conversion
- WGS84 datum with magnetic declination calculations
- Geocoding via OpenStreetMap Nominatim

## Installation

### As a Web App
1. Navigate to the hosted URL (HTTPS required)
2. **Mobile**: Tap Share → "Add to Home Screen"
3. **Desktop**: Click install icon in address bar
4. Launch GridLoc from your home screen or applications

### Self-Hosting
1. Download `index.html`
2. Host on any HTTPS-enabled web server
3. No build process or dependencies required

## Usage

### Basic Workflow
1. **Search Location**: Enter city name, MGRS coordinates, or lat/long
2. **Adjust View**: Pan and zoom to desired area
3. **Select Scale**: Choose 1:25k (detailed), 1:50k (standard), or 1:100k (overview)
4. **Configure Output**: Set paper size and orientation
5. **Generate PDF**: Click "Create Map" to export

### Search Formats

**Place Names:**
```
Babadag, Romania
Caracas, Venezuela
Mount Rainier
```

**MGRS Coordinates:**
```
18SUJ 23 06
18S UJ 15999 08500
```

**Latitude/Longitude:**
```
38.9072, -77.0369
40.7128, -74.0060
```

### Map Scales

- **1:25,000** - 1km = 4cm on paper (hiking/detailed operations)
- **1:50,000** - 1km = 2cm on paper (general planning)
- **1:100,000** - 1km = 1cm on paper (area overview)

## PDF Output

Generated PDFs include:
- Map at geometrically accurate scale
- 1km MGRS grid overlay
- 2-digit grid coordinate labels on all edges
- Header with MGRS center coordinate
- Footer with scale, datum, date, and magnetic declination
- Grid north indicator
- Map source attribution
- Terrain legend (for topographic maps)

## System Requirements

- Modern web browser (Chrome, Safari, Edge, Firefox)
- Internet connection (for map tiles and geocoding)
- HTTPS connection (for PWA installation)

**Supported Platforms:**
- iOS 11.3+
- Android 5.0+
- Windows 10+
- macOS 10.13+
- Linux (any modern distribution)

## Security

- Input validation and length limits (200 character max)
- Subresource Integrity (SRI) hashes on CDN resources
- No localStorage/sessionStorage usage
- Client-side only processing (no data transmitted to servers except map tiles)
- HTTPS required for production deployment

## Technology Stack

- **Mapping**: Leaflet.js
- **Tile Sources**: Esri World Imagery, OpenTopoMap
- **PDF Generation**: jsPDF
- **Screenshot**: dom-to-image
- **Geocoding**: OpenStreetMap Nominatim
- **No backend required** - fully client-side application

## Browser Compatibility

| Browser | Desktop | Mobile | PWA Support |
|---------|---------|--------|-------------|
| Chrome  | ✓       | ✓      | ✓           |
| Safari  | ✓       | ✓      | ✓           |
| Edge    | ✓       | ✓      | ✓           |
| Firefox | ✓       | ✓      | ✓           |

## Known Limitations

- Requires internet connection for map tiles and geocoding
- PDF generation may be slow on low-end mobile devices
- Map tile availability depends on third-party services
- MGRS calculations valid for UTM zones only (not polar regions)
- No offline functionality

## Contributing

Contributions are welcome! This tool is designed to support military operations planning and training worldwide.

**Areas for improvement:**
- Offline map tile caching
- Additional coordinate systems (UTM, USNG)
- Route planning features
- Elevation profiles
- Custom map symbols/annotations

## License

MIT License - See LICENSE file for details

## Acknowledgments

- Map tiles: Esri World Imagery, OpenTopoMap
- Geocoding: OpenStreetMap Nominatim
- MGRS coordinate system: NATO standardized grid reference

## Support

For issues, questions, or feature requests, please open an issue on the GitHub repository.

## Disclaimer

This software is provided "as is" without warranty of any kind. Users are responsible for verifying the accuracy of coordinates and maps for operational use. Always cross-reference with official military maps and GPS systems for mission-critical navigation.

---

**GridLoc** - Precision mapping for tactical operations
