---
title: "Best Cura Settings for PLA: A Complete Profile Guide"
date: 2026-02-13
description: "Get the best Cura settings for PLA with our tested profile guide. Exact temps, speeds, and retraction values for great prints"
keywords: ["best Cura settings for PLA", "Cura PLA profile", "Cura print settings"]
categories: ["slicer-settings"]
tags: ["cura", "pla", "slicer-settings", "print-profiles"]
series: ["slicer-guides"]
draft: false
---

*This post may contain affiliate links. If you buy through these links, we may earn a small commission at no extra cost to you. [Full disclosure here](/disclosure/).*

# Best Cura Settings for PLA: A Complete Profile Guide

The best Cura settings for PLA are 200-210C nozzle temperature, 60C bed temperature, 50 mm/s print speed, and 0.2mm layer height. These work as a reliable starting point for most printers. But the details matter, and small tweaks make the difference between an okay print and a great one.

Here's a complete breakdown of every setting that matters.

## Recommended Cura Settings for PLA

This table gives you a solid starting profile. Use these values, then fine-tune based on your results.

| Setting | Recommended Value | Notes |
|---|---|---|
| **Layer Height** | 0.2mm (standard) | 0.12mm for detail, 0.28mm for speed |
| **Line Width** | 0.4mm | Match your nozzle diameter |
| **Wall Count** | 3 | 4 for stronger parts |
| **Top/Bottom Layers** | 4 | Prevents pillowing on top surfaces |
| **Infill Density** | 20% | 15% for decorative, 40%+ for functional |
| **Infill Pattern** | Cubic | Good balance of strength and speed |
| **Print Speed** | 50 mm/s | 30 mm/s for detailed prints |
| **Travel Speed** | 150 mm/s | Faster travel reduces stringing |
| **Nozzle Temp** | 200-210C | Start at 205C and adjust |
| **Bed Temp** | 60C | 50C works for PEI surfaces |
| **Cooling Fan** | 100% after layer 3 | First layers need less cooling |
| **Retraction Distance** | 5mm (Bowden) / 1mm (direct drive) | Critical for reducing stringing |
| **Retraction Speed** | 45 mm/s | 25 mm/s for direct drive |
| **Initial Layer Speed** | 20 mm/s | Slow first layer = better adhesion |
| **Initial Layer Height** | 0.28mm | Slightly thicker helps adhesion |

## Temperature Settings

Temperature is the most important setting to get right. Too hot and you'll see stringing, oozing, and poor overhangs. Too cold and you'll get weak layer adhesion and under-extrusion.

**Nozzle temperature:** Start at 205C. If you see stringing, drop by 5 degrees. If layers aren't bonding well or you hear clicking from the extruder, bump it up by 5 degrees.

Different [PLA brands](/blog/best-pla-filament/) have different sweet spots. Hatchbox PLA tends to print well at 200C. Polymaker and Overture often prefer 210C. Always check the range printed on your spool.

**Bed temperature:** 60C works for almost all PLA. If you're using a [PEI build plate](/blog/pei-vs-glass-vs-magnetic-build-plate/), you can often drop to 50C and still get excellent adhesion.

## Speed Settings

For most printers, 50 mm/s gives you good quality without painfully long print times. Here's how to think about speed.

**Outer walls:** Drop to 30-40 mm/s. This is what you actually see, so it's worth slowing down.

**Inner walls:** 50 mm/s is fine. Nobody sees these.

**Infill:** You can push this to 60-80 mm/s. Infill quality doesn't matter much visually.

**First layer:** Always print at 20 mm/s. A slow first layer gives the filament time to bond to the bed. Rushing this leads to failed prints.

If you want to push speeds higher, check out our guide on [print speed vs quality tradeoffs](/blog/print-speed-vs-quality/).

## Retraction Settings

Bad retraction settings are the number one cause of [stringing](/blog/reduce-stringing-slicer-settings/). Get these right and your prints will look much cleaner.

**Bowden extruders** (like stock Ender 3) need longer retraction. Use 5-6mm distance at 45 mm/s speed. The long PTFE tube means more filament to pull back.

**Direct drive extruders** need much less. Use 0.5-1.5mm distance at 25 mm/s speed. Too much retraction on direct drive will cause jams.

Don't know which type you have? Check our [direct drive vs Bowden comparison](/blog/direct-drive-vs-bowden/).

## Cooling Settings

PLA loves cooling. Unlike [PETG](/blog/how-to-print-petg/) or ABS, PLA prints best with the fan at full blast.

Set your fan to 0% for the first 2-3 layers. This helps bed adhesion. After that, crank it to 100% and leave it there.

If you're printing bridges or overhangs, good cooling makes a massive difference. Some printers benefit from a fan duct upgrade for better airflow direction.

## First Layer Settings

Your first layer is the foundation of every print. Mess it up and nothing else matters.

**Initial layer height:** Use 0.28mm even if your normal layer height is 0.2mm. The thicker first layer squishes into the bed better and improves adhesion.

**Initial layer speed:** 20 mm/s, no faster. Give the filament time to stick.

**Initial layer flow:** If your first layer looks thin or has gaps, bump the initial layer flow to 105-110%. This adds a little extra material to fill in any unevenness in your bed surface.

**Build plate adhesion:** For most PLA prints on PEI or textured surfaces, you don't need a brim or raft. If you're printing something with a small footprint, add a brim of 5-8 lines for extra grip.

## Infill Settings

For decorative prints, 15-20% infill is plenty. For functional parts that need strength, go to 40-60%.

The [infill pattern](/blog/infill-patterns-explained/) matters too. Cubic is a great default. It's strong in all directions without using too much material. Gyroid is another good option if you want even strength distribution.

Don't go above 60% infill unless you have a specific reason. Adding more walls (4-5 wall count) adds more strength than cranking infill to 80%.

## When to Change These Settings

These defaults work for most PLA prints. But here are situations where you should adjust.

**Miniatures and detailed models:** Drop layer height to 0.12mm. Slow print speed to 30 mm/s. These prints take longer but show much finer detail.

**Large flat prints:** Add a brim. Increase bed temp to 65C. Large PLA prints are prone to warping at the corners.

**Functional/strong parts:** Use 4 walls, 40% infill, and bump nozzle temp to 215C. Higher temps improve layer bonding. Learn more about material choices for functional parts in our [PLA vs PETG vs ABS guide](/blog/pla-vs-petg-vs-abs/).

**Speed prints:** If your printer supports it, you can push PLA to 100-150 mm/s with proper tuning. But you'll need to increase nozzle temperature to 215-220C to keep up with the higher flow rate. See our [slicer comparison guide](/blog/cura-vs-orcaslicer-vs-prusaslicer/) for tools that help with speed tuning.

If you want these settings pre-configured and ready to import, grab our [Slicer Starter Kit](/slicer-starter-kit/). It includes an optimized PLA profile for the Ender 3, plus profiles for PETG and TPU.

## Frequently Asked Questions

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What temperature should I print PLA at in Cura?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Start at 205C and adjust from there. Most PLA prints well between 200-210C. If you see stringing, lower the temperature by 5 degrees. If layers aren't bonding, raise it by 5 degrees."
      }
    },
    {
      "@type": "Question",
      "name": "What is the best print speed for PLA in Cura?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "50 mm/s is a reliable starting point for most printers. Slow down to 30 mm/s for detailed prints. You can push to 80-100 mm/s for fast prints if your printer can handle it, but you may need to increase nozzle temperature."
      }
    },
    {
      "@type": "Question",
      "name": "Should I use a brim or raft for PLA in Cura?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Most PLA prints don't need a brim or raft, especially on PEI or textured build surfaces. Add a brim of 5-8 lines if your print has a small base or you're seeing corners lift. Rafts waste material and are rarely needed for PLA."
      }
    }
  ]
}
</script>

### What temperature should I print PLA at in Cura?

Start at 205C and adjust from there. Most PLA prints well between 200-210C. If you see stringing, lower the temperature by 5 degrees. If layers aren't bonding, raise it by 5 degrees.

### What is the best print speed for PLA in Cura?

50 mm/s is a reliable starting point for most printers. Slow down to 30 mm/s for detailed prints. You can push to 80-100 mm/s for fast prints if your printer can handle it, but you may need to increase nozzle temperature.

### Should I use a brim or raft for PLA in Cura?

Most PLA prints don't need a brim or raft, especially on PEI or textured build surfaces. Add a brim of 5-8 lines if your print has a small base or you're seeing corners lift. Rafts waste material and are rarely needed for PLA.
