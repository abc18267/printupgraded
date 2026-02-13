---
title: "Elephant's Foot and Other First Layer Issues Explained"
date: 2026-02-13
description: "Fix elephant's foot 3D printing defects and other first layer problems with Z offset, temperature, and slicer fixes"
keywords: ["elephant's foot 3D printing", "first layer problems", "first layer too wide", "bottom layer bulge"]
categories: ["troubleshooting"]
tags: ["elephant's foot", "first layer", "troubleshooting"]
series: ["troubleshooting-guides"]
draft: false
---

**Affiliate Disclosure:** Some links in this article are affiliate links. We may earn a small commission if you purchase through them, at no extra cost to you.

# Elephant's Foot and Other First Layer Issues Explained

Elephant's foot in 3D printing is when the first layer or two of your print bulge outward. The bottom of the part ends up wider than the rest. It's named after what it looks like: a flat, flared base, similar to an elephant's foot. The main causes are a Z offset that's too close, a bed temperature that's too high, or too much weight pressing down on a hot first layer. Here's how to fix it and other first layer problems.

## What Causes Elephant's Foot?

Three things work together to create elephant's foot:

**Z offset too close.** When the nozzle is too close to the bed, the first layer gets squished wider than it should be. You get great adhesion, but the bottom of your print flares out.

**Bed temperature too high.** A hot bed keeps the bottom layers soft. The weight of the print above presses down on these soft layers and squishes them outward. This is more noticeable on tall, heavy prints.

**Initial layer settings too aggressive.** If your first layer flow rate is set too high, or your first layer line width is too wide, the extra material has to go somewhere. It spreads outward.

## How to Fix Elephant's Foot

### Lower Your Z Offset Slightly

If your first layer is perfectly flat and shiny, your nozzle is probably a tiny bit too close. Raise the Z offset by 0.02-0.04mm. The first layer should still have visible lines that are slightly flattened, not completely smooth.

This is a balancing act. Too far and you lose adhesion. Too close and you get elephant's foot. Make small adjustments and test.

### Reduce Bed Temperature After the First Layer

Keep the bed at full temperature for the first layer to ensure adhesion. Then drop it 5-10C for the remaining layers. Most slicers let you set different bed temperatures for the first layer versus the rest.

For PLA, try 60C for the first layer and 55C after that. For PETG, try 80C first layer and 70C after. This small reduction lets the bottom layers firm up before the weight of the print stacks up.

### Use Elephant's Foot Compensation

Many slicers have a built-in setting for this. In Cura, it's called "Initial Layer Horizontal Expansion" (set it to a negative value like -0.2mm). In PrusaSlicer and OrcaSlicer, it's called "Elephant foot compensation."

This setting slightly shrinks the first layer inward to compensate for the expected spread. Start with 0.1-0.2mm and adjust from there. It's a quick fix that works well for most cases.

### Reduce First Layer Flow

If your first layer flow is above 100%, try bringing it back to 100% or even 95%. Extra flow means extra material, which contributes to the flare.

### Add a Chamfer to Your Model

If you're designing the part yourself, add a small 45-degree chamfer to the bottom edge. This accounts for the slight spread of the first layer and makes the final result look clean. A 0.5mm chamfer is usually enough.

## Other Common First Layer Problems

Elephant's foot isn't the only first layer issue you'll encounter. Here are the others.

### First Layer Too Thin

If your first layer looks like a whisper, barely visible lines that you can see through, it's too thin. This causes poor adhesion and weak parts.

**Causes:**
- Z offset too high (nozzle too far from bed)
- First layer flow too low
- Bed not level (too far in some spots)

**Fix:** Lower the Z offset by 0.02mm increments until the first layer looks solid. Each line should be visible but slightly flattened, with no gaps between them.

### First Layer Too Thick

The opposite problem. The first layer is blobby, rough, and the nozzle might even drag through it. You might hear scraping sounds.

**Causes:**
- Z offset too close
- First layer flow too high
- First layer height set too tall in the slicer

**Fix:** Raise the Z offset slightly. Check that your first layer height in the slicer isn't set higher than 0.3mm for a 0.4mm nozzle. Reduce first layer flow to 100%.

### Inconsistent First Layer

Parts of the first layer look great while others are too thin or too thick. This one is frustrating because no single Z offset works.

**Causes:**
- Bed isn't level. Different corners are at different heights.
- Bed surface is warped. Common on aluminum beds, especially cheaper ones.
- Loose bed springs. The leveling drifts between prints.

**Fix:**
- Re-level the bed carefully. Check all four corners and the center.
- Use mesh bed leveling in firmware (Marlin or Klipper). This maps the bed surface and adjusts the Z height across the print.
- Replace loose springs with stiffer silicone spacers. They hold their position much better.
- For badly warped beds, a glass plate or a quality [PEI build plate](/blog/pei-vs-glass-vs-magnetic-build-plate/) can provide a flatter surface.

### First Layer Not Filling In

The perimeter of the first layer sticks fine, but the area inside has gaps. Lines don't overlap enough to create a solid surface.

**Causes:**
- First layer line width too narrow
- First layer flow too low
- Slightly too far from the bed

**Fix:** Increase your first layer line width to 120-150% of nozzle diameter. Bump first layer flow to 100-105%. Lower Z offset slightly. Check our [best Cura settings for PLA](/blog/best-cura-settings-pla/) for recommended first layer values.

## The Right First Layer Settings

Here's a starting point that works for most printers and materials:

| Setting | Recommended Value |
|---|---|
| First layer height | 0.28mm (for 0.4mm nozzle) |
| First layer line width | 120% of nozzle diameter |
| First layer speed | 20-25mm/s |
| First layer flow | 100% |
| First layer bed temp | Material-specific (see above) |
| Fan speed first layer | 0% |

These settings prioritize adhesion without creating elephant's foot. Adjust from here based on your results.

## When to Look at Hardware

If first layer problems persist despite tuning settings, the hardware might be the issue:

- **Warped bed:** A glass plate or quality [magnetic build plate](/blog/pei-vs-glass-vs-magnetic-build-plate/) gives you a flatter starting surface.
- **Loose gantry:** If the X gantry sags on one side, the nozzle height varies across the bed. Check that both sides of the gantry are at the same height.
- **Worn nozzle:** A worn nozzle has an uneven tip that creates inconsistent first layers. Replace it.

For a full overview of print problems, see our [3D print troubleshooting master guide](/blog/3d-print-troubleshooting/). If your first layer sticks but lifts later, check our guide on [fixing bed adhesion](/blog/fix-bed-adhesion/).

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is elephant's foot in 3D printing?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Elephant's foot is when the first few layers of a 3D print bulge outward, making the bottom wider than the rest of the model. It's caused by the nozzle being too close to the bed, bed temperature being too high, or the weight of the print squishing the soft bottom layers."
      }
    },
    {
      "@type": "Question",
      "name": "How do I fix elephant's foot without losing bed adhesion?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Use elephant's foot compensation in your slicer (a negative initial layer horizontal expansion of 0.1-0.2mm). This shrinks the first layer slightly to offset the spread. You can also reduce bed temperature by 5C after the first layer. Both fixes reduce elephant's foot without hurting adhesion."
      }
    },
    {
      "@type": "Question",
      "name": "Why is my first layer inconsistent across the bed?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "An inconsistent first layer usually means the bed isn't level or the bed surface is physically warped. Re-level the bed at all four corners and check the center. If the bed itself is warped, use mesh bed leveling in firmware or place a flat glass plate on top."
      }
    }
  ]
}
</script>

### What is elephant's foot in 3D printing?

Elephant's foot is when the first few layers of a 3D print bulge outward, making the bottom wider than the rest of the model. It's caused by the nozzle being too close to the bed, bed temperature being too high, or the weight of the print squishing the soft bottom layers.

### How do I fix elephant's foot without losing bed adhesion?

Use elephant's foot compensation in your slicer (a negative initial layer horizontal expansion of 0.1-0.2mm). This shrinks the first layer slightly to offset the spread. You can also reduce bed temperature by 5C after the first layer. Both fixes reduce elephant's foot without hurting adhesion.

### Why is my first layer inconsistent across the bed?

An inconsistent first layer usually means the bed isn't level or the bed surface is physically warped. Re-level the bed at all four corners and check the center. If the bed itself is warped, use mesh bed leveling in firmware or place a flat glass plate on top.
