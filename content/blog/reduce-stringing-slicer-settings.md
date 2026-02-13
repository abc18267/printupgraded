---
title: "How to Reduce Stringing in Your Slicer Settings"
date: 2026-02-13
description: "Learn how to reduce stringing in your slicer settings with retraction, temperature, and travel speed tweaks that actually work"
keywords: ["reduce stringing slicer settings", "3D print stringing fix", "retraction settings"]
categories: ["slicer-settings"]
tags: ["stringing", "retraction", "slicer-settings", "troubleshooting"]
series: ["slicer-guides"]
draft: false
---

*This post may contain affiliate links. If you buy through these links, we may earn a small commission at no extra cost to you. [Full disclosure here](/disclosure/).*

# How to Reduce Stringing in Your Slicer Settings

You can reduce stringing in your slicer settings by adjusting three things: retraction distance, retraction speed, and nozzle temperature. These three settings fix stringing in about 90% of cases. The remaining 10% usually comes from wet filament, which is a hardware problem, not a slicer problem.

Let's fix your stringing issue step by step.

## What Causes Stringing?

Stringing happens when melted filament oozes out of the nozzle while the print head moves between two points. Those thin threads of plastic stretch between parts of your model like cobwebs.

The root cause is simple. Filament stays liquid in the nozzle. When the print head travels across open space, some of that liquid leaks out. Your slicer settings control how much leaking happens.

Here are the main causes, ranked by how common they are:

1. **Retraction settings too low.** The slicer doesn't pull back enough filament during travel moves.
2. **Nozzle temperature too high.** Hotter filament flows more easily and oozes more.
3. **Wet filament.** Moisture in the filament creates steam that pushes plastic out of the nozzle.
4. **Travel speed too slow.** The nozzle spends too long hovering over open areas.

## Fix 1: Adjust Retraction Distance and Speed

Retraction is your main weapon against stringing. When the print head needs to move without printing, the extruder pulls filament back into the nozzle. This creates negative pressure that stops oozing.

Two values matter: distance and speed.

### Retraction Distance

This controls how far the filament gets pulled back.

**Bowden extruders** (stock Ender 3, CR-10, most budget printers): Start at 5mm. You can go up to 7mm if needed. Bowden setups need more retraction because of the long tube between the extruder and hotend.

**Direct drive extruders**: Start at 0.5-1mm. Don't go above 2mm. Direct drive has a short filament path, so less retraction is needed. Too much retraction on direct drive causes jams. Not sure which type you have? Check our [direct drive vs Bowden guide](/blog/direct-drive-vs-bowden/).

### Retraction Speed

This controls how fast the filament gets pulled back.

Start at 45 mm/s for Bowden setups and 25 mm/s for direct drive. If you still see stringing, try increasing by 5 mm/s increments.

Don't go above 70 mm/s. Very high retraction speeds can grind the filament and cause feeding problems.

## Fix 2: Lower Your Nozzle Temperature

If retraction alone doesn't solve it, your nozzle is probably too hot. Hotter filament is thinner and flows more freely. That means more oozing.

Drop your temperature by 5C at a time. For PLA, try going from 210C down to 200C. For [PETG](/blog/how-to-print-petg/), try 230C instead of 240C.

Don't go too low, though. If your temperature is too cold, you'll trade stringing for under-extrusion and weak layer adhesion. There's a sweet spot for every filament.

A temperature tower test helps you find that sweet spot. You print a tower with different temperature zones and pick the one that looks best. Both OrcaSlicer and Cura can generate these. Our [slicer comparison guide](/blog/cura-vs-orcaslicer-vs-prusaslicer/) explains which tools each slicer offers.

## Fix 3: Increase Travel Speed

Travel speed is how fast the print head moves when it's not printing. Faster travel means less time for filament to ooze.

Set your travel speed to 150-200 mm/s. Most printers handle this fine since the nozzle isn't extruding during travel moves.

This isn't a magic fix on its own, but it helps when combined with good retraction settings.

## Fix 4: Enable Wipe and Coasting

These two settings add extra stringing protection.

**Wipe** makes the nozzle move back along the printed path before lifting for a travel move. This wipes the nozzle tip clean and reduces the blob of filament that can string on the next move.

**Coasting** stops extrusion slightly before the end of each line. The remaining pressure in the nozzle finishes the line. This reduces the pressure that causes oozing during travel.

In Cura, enable both under the "Travel" section. In OrcaSlicer and PrusaSlicer, look for "Wipe while retracting" in the retraction settings.

Start with coasting at 0.064 mm3 in Cura. If your line ends look too thin, reduce it or turn it off.

## Fix 5: Dry Your Filament

If you've tuned all your slicer settings and still see stringing, the problem is probably wet filament.

Filament absorbs moisture from the air. When wet filament hits the hot nozzle, the moisture turns to steam. That steam pushes filament out of the nozzle, creating strings that no retraction setting can fix.

Signs of wet filament:

- Stringing that won't go away regardless of settings
- Popping or crackling sounds during printing
- Rough, pitted surface finish
- Small zits and blobs on the surface

Check our [filament drying guide](/blog/filament-drying-guide/) for step-by-step instructions on how to dry your spools.

[PETG](/blog/how-to-print-petg/) is especially prone to moisture-related stringing. If you're printing PETG and fighting strings, drying the filament should be your first step.

## How to Run a Retraction Tower Test

Instead of guessing at settings, print a retraction test. This prints a series of small towers with different retraction distances. You can see exactly which distance eliminates stringing.

**In OrcaSlicer:** Go to Calibration and select Retraction Test. Set your range (try 0.5mm to 6mm for Bowden, or 0.2mm to 2mm for direct drive). The slicer generates the model and inserts the setting changes automatically.

**In Cura:** Download a retraction tower STL from Thingiverse. Use the "Change at Z" post-processing script to set different retraction distances at different heights.

**In PrusaSlicer:** Similar to Cura. Download a test model and use custom G-code at layer changes.

After printing, examine each section. Pick the retraction distance where stringing disappears. Then use that value for all your future prints with that filament.

## Quick Reference: Anti-Stringing Settings

| Setting | Bowden Setup | Direct Drive Setup |
|---|---|---|
| Retraction Distance | 5-7mm | 0.5-1.5mm |
| Retraction Speed | 40-50 mm/s | 20-30 mm/s |
| Travel Speed | 150-200 mm/s | 150-200 mm/s |
| Nozzle Temp (PLA) | 195-205C | 195-205C |
| Nozzle Temp (PETG) | 225-235C | 225-235C |
| Wipe | Enabled | Enabled |
| Coasting | 0.064 mm3 | Optional |

## Frequently Asked Questions

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Why does my PETG string so much more than PLA?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "PETG is naturally more stringy than PLA for two reasons. It prints at higher temperatures (230-240C vs 200-210C), which makes it flow more easily. It also absorbs moisture faster, and wet PETG strings badly. Dry your PETG filament and lower your print temperature to reduce stringing."
      }
    },
    {
      "@type": "Question",
      "name": "Can too much retraction cause problems?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Excessive retraction can cause clogs, especially on direct drive extruders. It can also grind the filament, creating dust that clogs the extruder gears. Stick to the recommended ranges: 5-7mm for Bowden, 0.5-1.5mm for direct drive."
      }
    },
    {
      "@type": "Question",
      "name": "Should I use Z-hop to reduce stringing?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Z-hop lifts the nozzle during travel moves, which can help with some stringing issues. But it can also make stringing worse because the nozzle has more time to ooze while lifting and lowering. Try it with a small value (0.2mm) and see if it helps your specific situation."
      }
    }
  ]
}
</script>

### Why does my PETG string so much more than PLA?

PETG is naturally more stringy than PLA for two reasons. It prints at higher temperatures (230-240C vs 200-210C), which makes it flow more easily. It also absorbs moisture faster, and wet PETG strings badly. Dry your PETG filament and lower your print temperature to reduce stringing.

### Can too much retraction cause problems?

Yes. Too much retraction can cause clogs, especially on direct drive extruders. It can also grind the filament, creating dust that clogs the extruder gears. Stick to the recommended ranges: 5-7mm for Bowden, 0.5-1.5mm for direct drive.

### Should I use Z-hop to reduce stringing?

Z-hop lifts the nozzle during travel moves, which can help with some stringing issues. But it can also make stringing worse because the nozzle has more time to ooze while lifting and lowering. Try it with a small value (0.2mm) and see if it helps your specific situation.
