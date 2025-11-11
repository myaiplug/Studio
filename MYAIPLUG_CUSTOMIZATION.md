# MyAiPlug Studio Customization

This document describes the customizations made to openDAW to create MyAiPlug Studio with the MyAiPlug brand identity.

## Overview

MyAiPlug Studio is a customized version of [openDAW](https://github.com/andremichelle/opendaw) with the MyAiPlug brand colors, styling, and identity. The project maintains all the powerful features of openDAW while presenting a cohesive visual experience matching the MyAiPlug ecosystem.

## Color Scheme

The following MyAiPlug brand colors have been applied throughout the application:

### Primary Colors
- **Primary Purple**: `#7C4DFF` - Main brand color for buttons, accents, and interactive elements
- **Accent Cyan**: `#00C2FF` - Secondary accent for highlights and emphasis
- **Warm Orange**: `#FFB84D` - Warm accent for notifications and warnings
- **Deep Orange**: `#FF9900` - Additional warm accent for variety

### Background Colors
- **Dark Background**: `#0D0D0F` - Main application background
- **Panel Background**: `#111122` - Panel and container backgrounds
- **Panel Bright**: `#1a1a2a` - Brighter panel variant
- **Panel Dark**: `#0a0a10` - Darker panel variant

### Visual Features
- Animated gradient background smoothly transitioning between dark tones (22-second loop)
- Purple (#7C4DFF) loading spinner animations
- Glowing box shadows with purple tones for depth and emphasis

## Files Modified

### 1. `packages/app/studio/src/colors.sass`
- Replaced all color CSS variables with MyAiPlug brand colors
- Updated background colors to match myaiplug.com theme
- Mapped openDAW's color-green to purple (#7C4DFF)
- Mapped openDAW's color-blue to cyan (#00C2FF)

### 2. `packages/app/studio/index.html`
- Updated page title to "🎧 MyAiPlug Studio"
- Changed meta tags and OG tags to reference MyAiPlug branding
- Updated canonical URL to www.myaiplug.com
- Applied MyAiPlug gradient background to preloader
- Changed loading spinner colors to purple (#7C4DFF)

### 3. `README.md`
- Added MyAiPlug Studio branding and description
- Acknowledged openDAW as the foundation
- Documented the customization approach
- Listed the MyAiPlug color scheme

### 4. `.gitignore`
- Added `/cert/` to ignore temporary certificate directories

## Building and Running

### Prerequisites
- Node.js >= 23
- npm >= 10

### Installation
```bash
npm install
```

### Build
```bash
npm run build
```

### Development Server
```bash
# Generate SSL certificates (first time only)
npm run cert

# Start development server
npm run dev:studio

# Navigate to https://localhost:8080
```

## Design Philosophy

The customization follows these principles:

1. **Minimal Changes**: Only color scheme and branding elements were modified
2. **Functional Preservation**: All openDAW features remain fully functional
3. **Brand Consistency**: Colors match the myaiplug.com website aesthetic
4. **Professional Appearance**: Dark theme optimized for creative workflows
5. **Modern Design**: Animated gradients and subtle glow effects

## Color Mapping Reference

| openDAW Original | MyAiPlug Replacement | Usage |
|------------------|----------------------|-------|
| `--color-blue` (cyan) | `#00C2FF` | Accent highlights |
| `--color-green` (green) | `#7C4DFF` (purple) | Primary UI elements |
| `--color-yellow` | `#FFB84D` (orange) | Warnings, notifications |
| `--color-orange` | `#FF9900` | Additional accents |
| `--background` | `#0D0D0F` | Main background |
| `--panel-background` | `#111122` | Panel backgrounds |

## Screenshots

![MyAiPlug Studio Color Scheme](https://github.com/user-attachments/assets/c8cbe93e-589d-4451-b0c2-59f37a56681f)

The screenshot above demonstrates the MyAiPlug color palette applied to the interface, featuring:
- Purple primary color (#7C4DFF)
- Cyan accent (#00C2FF)
- Orange warm accents (#FFB84D, #FF9900)
- Animated dark gradient background
- Purple loading spinner

## License

This project maintains the same licensing as openDAW:
- **AGPL v3 (or later)** for open-source use
- **Commercial License** available for closed-source integration

See the main README.md for full licensing details.

## Credits

- **openDAW**: Original project by [André Michelle](https://github.com/andremichelle)
- **MyAiPlug Customization**: Applied MyAiPlug brand identity and color scheme
- **Color Scheme**: Based on myaiplug.com website design

## Support openDAW

Please consider supporting the original openDAW project:
- [Patreon](https://www.patreon.com/join/openDAW)
- [ko-fi](https://ko-fi.com/opendaw)
