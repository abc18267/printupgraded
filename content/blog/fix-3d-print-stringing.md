---
title: "How to Fix 3D Print Stringing Once and For All"
date: 2026-02-13
description: "Fix 3D print stringing with the right retraction, temperature, and speed settings plus a step-by-step tuning process"
keywords: ["3D print stringing", "fix stringing 3D printer", "retraction settings", "stringing test"]
categories: ["troubleshooting"]
tags: ["stringing", "retraction", "troubleshooting"]
series: ["troubleshooting-guides"]
draft: false
---

**Affiliate Disclosure:** Some links in this article are affiliate links. We may earn a small commission if you purchase through them, at no extra cost to you.

# How to Fix 3D Print Stringing Once and For All

3D print stringing is those thin, wispy threads of filament that stretch between parts of your model. They look like spider webs. They're annoying. And they're one of the most common print quality issues you'll run into. The good news is that stringing is almost always fixable with the right combination of temperature, retraction, and travel settings.

If you're dealing with strings on every print, this guide will walk you through a step-by-step process to eliminate them.

## What Causes 3D Print Stringing?

Stringing happens when filament oozes out of the nozzle while the print head moves between two points. The nozzle travels across an open gap, and melted filament leaks out along the way. That leaked filament creates the strings.

Four things cause this:

**Temperature too high.** The hotter the filament, the more runny it gets. Runny filament oozes more during travel moves. This is the number one cause of stringing.

**Retraction too low.** Retraction pulls filament back into the nozzle before a travel move. If it doesn't pull back far enough or fast enough, filament keeps oozing. On Bowden setups, you typically need 4-7mm of retraction. Direct drive systems need only 0.5-2mm.

**Wet filament.** Moisture in the filament turns to steam at printing temperatures. This creates pressure that pushes filament out of the nozzle during travel moves. If you hear popping or crackling sounds while printing, your filament is wet. Check our [filament drying guide](/blog/filament-drying-guide/) for how to fix this.

**Travel speed too slow.** The longer the nozzle takes to cross a gap, the more time filament has to ooze. Faster travel means less stringing.

## Which Materials String the Most?

Not all filaments string equally. Here's the ranking from worst to best:

1. **PETG** is the worst. It's naturally stringy and gooey. Even with perfect settings, you might still see some stringing. Our [PETG printing guide](/blog/how-to-print-petg/) has specific tips for taming it.
2. **TPU** strings badly because you can't use retraction with most Bowden setups.
3. **Nylon** strings moderately due to its high print temperature.
4. **ABS** strings a moderate amount.
5. **PLA** is the easiest to get string-free prints with.

## Step-by-Step: How to Fix Stringing

Follow these steps in order. Each one builds on the last.

### Step 1: Lower Your Print Temperature

Start by dropping your hotend temperature 5C below your current setting. Print a test. If stringing improves, drop another 5C. Keep going until you see under-extrusion or poor layer adhesion. Then go back up 5C. That's your sweet spot.

For PLA, the typical sweet spot is 195-205C. For PETG, try 225-235C. For ABS, aim for 230-240C.

### Step 2: Tune Your Retraction Distance

Print a retraction tower test. Most slicers have one built in. OrcaSlicer has a great built-in calibration for this.

For Bowden tube printers, start at 5mm and test in 1mm increments from 3-8mm. For direct drive printers, start at 1mm and test in 0.5mm increments from 0.5-3mm.

More retraction isn't always better. Too much retraction can cause clogs, especially in all-metal hotends.

### Step 3: Increase Retraction Speed

Try 25-45mm/s for most printers. If you're below 25mm/s, that's probably too slow. Most printers do well around 35-40mm/s.

### Step 4: Increase Travel Speed

Set your travel speed to at least 150mm/s. Most modern printers handle 200mm/s travel speed fine. Faster travel means less time for oozing.

### Step 5: Enable Combing or Avoid Crossing Perimeters

This slicer setting tells the nozzle to travel within the walls of your print instead of crossing open gaps. It doesn't fix stringing. It hides it. Any strings end up inside the model where you can't see them.

In Cura, it's called "Combing Mode." In PrusaSlicer and OrcaSlicer, it's "Avoid crossing perimeters." For more slicer-specific settings, see our guide on [reducing stringing with slicer settings](/blog/reduce-stringing-slicer-settings/).

### Step 6: Try Wiping and Coasting

Wiping makes the nozzle move along the perimeter at the end of a line to clean off excess filament. Coasting stops extruding slightly before the end of a line to relieve pressure. Both help reduce oozing.

Start with wipe distance at 2mm and coasting volume at 0.064mm3 in Cura. Adjust from there.

## The Retraction Tower Test

A retraction tower is the fastest way to find your perfect retraction settings. It prints a tower with different retraction distances at each level. You look at the results and pick the level with the least stringing.

Here's how to run one:

1. Download or generate a stringing test model. The classic one has two towers with a gap between them.
2. In OrcaSlicer, go to Calibration and select Retraction Test. It automates the whole process.
3. In Cura, you'll need to use the Post Processing plugin to change retraction at each layer height.
4. Print the tower and compare each section.

Pick the retraction distance that gives you the cleanest travel between the two towers. That's your setting.

## When Nothing Works

If you've tried everything and still have stringing, check these:

- **Your filament is wet.** This is the hidden cause most people overlook. Even "new" filament from a poorly sealed bag can have moisture. [Dry it](/blog/filament-drying-guide/) and try again.
- **Your PTFE tube has a gap.** A gap between the PTFE tube and the nozzle creates a pocket where filament pools and oozes. Re-seat the tube or upgrade to an [all-metal hotend](/blog/all-metal-hotend-upgrade/).
- **Your nozzle is worn.** A worn nozzle has a wider opening, which means more oozing. Replace it.

For a broader look at print quality issues, check our [3D print troubleshooting master guide](/blog/3d-print-troubleshooting/).

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What retraction distance should I use to fix stringing?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "For Bowden tube printers, use 4-7mm of retraction. For direct drive printers, use 0.5-2mm. Run a retraction tower test to find the exact best value for your printer."
      }
    },
    {
      "@type": "Question",
      "name": "Why does PETG string so much?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "PETG is naturally more viscous and sticky than PLA. It requires higher temperatures, which makes it more prone to oozing. Even with optimized settings, some minor stringing is normal with PETG. Lowering the temperature to the low end of the range and increasing retraction helps."
      }
    },
    {
      "@type": "Question",
      "name": "Can I just remove strings after printing instead of fixing settings?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "You can remove light stringing with a heat gun on low or a quick pass with a lighter. But this only works for thin wisps. Heavy stringing indicates a real problem that will also affect other aspects of print quality. It's better to fix the root cause."
      }
    }
  ]
}
</script>

### What retraction distance should I use to fix stringing?

For Bowden tube printers, use 4-7mm of retraction. For direct drive printers, use 0.5-2mm. Run a retraction tower test to find the exact best value for your printer.

### Why does PETG string so much?

PETG is naturally more viscous and sticky than PLA. It requires higher temperatures, which makes it more prone to oozing. Even with optimized settings, some minor stringing is normal with PETG. Lowering the temperature to the low end of the range and increasing retraction helps.

### Can I just remove strings after printing instead of fixing settings?

You can remove light stringing with a heat gun on low or a quick pass with a lighter. But this only works for thin wisps. Heavy stringing indicates a real problem that will also affect other aspects of print quality. It's better to fix the root cause.
