# phosphor-green-stylus
CRT-inspired color schemes for reduced eye strain during extended screen time
# Phosphor Green Stylus

CRT-inspired color schemes designed to reduce eye strain during extended screen time on LCD displays.

## Problem
White backgrounds cause significant eye strain during overnight shifts and extended training sessions. Modern LCD displays emit predominantly blue-spectrum backlight that increases cognitive load and disrupts circadian rhythm.

## Solution
Two phosphor-inspired themes optimized for different use cases:

### Phthalo Green (Sustained Work)
- Deep, organic earth tones (`#3a7a4d`)
- Cyan underglow compensates for LCD blue backlight bleed
- Designed for 8+ hour sessions
- Reduces head temperature and cognitive strain
- Accidentally matches Whole Foods brand aesthetic

### Electric Green (High Alert)
- Bright phosphor aesthetic (`#00ff00`)
- Maximum contrast for short-burst focus
- Classic CRT terminal appearance
- Cyan underglow for optical depth

## Technical Details
- **Dual-layer text-shadow** creates authentic phosphor glow effect
- **Rounded edges** mimic light diffusion on curved CRT glass
- **Color values** selected to optically mix with blue LCD backlighting
- **Universal selector with exemptions** preserves video/image functionality
- **Cyan underglow** (`rgba(31, 77, 77, ...)`) compensates for LCD blue backlight bleed

## Installation
1. Install [Stylus extension](https://add0n.com/stylus.html) for your browser
2. Click "Create new style" in Stylus
3. Copy contents of desired CSS file from this repository
4. Paste into Stylus editor
5. Save and enable

## Real-World Testing
Developed and tested during overnight retail training shifts at Whole Foods Market. Phthalo variant reduced physiological stress indicators (measurable head temperature decrease) during extended screen exposure on standard LCD monitors.

## Use Cases
- **Phthalo Green**: Long training sessions, overnight work, sustained reading
- **Electric Green**: Quick reference tasks, terminal work, high-alert situations

## Files
- `phthalo-green.css` - Sustained work variant (earth tones)
- `electric-green.css` - High-alert variant (bright phosphor)

## Design Philosophy
Colors designed for actual hardware constraints: LCD backlight bleed is blue-spectrum, so cyan undertones create optical mixing that maintains green perception while reducing harsh saturation.

## License
MIT License - Use freely, modify as needed

---

*Built to solve a real problem: making 8-hour overnight training shifts sustainable without eye strain.*
