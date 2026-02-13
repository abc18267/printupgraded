---
title: "Nylon Filament Printing Guide: Settings and Tips"
date: 2026-02-13
description: "Nylon filament printing requires the right temps, a dry spool, and an all-metal hotend. Here are the exact settings and tips you need"
keywords: ["nylon filament printing", "how to print nylon", "nylon 3D printing settings", "PA6 vs PA12"]
categories: ["filament"]
tags: ["nylon", "PA6", "PA12", "engineering filament"]
series: ["filament-guides"]
draft: false
---

*This article may contain affiliate links. We may earn a small commission if you buy something through them, at no extra cost to you. We only recommend products we'd actually use ourselves.*

# Nylon Filament Printing Guide: Settings and Tips

Nylon filament printing gives you parts that are tough, wear-resistant, and slightly flexible. It's one of the strongest materials you can print at home. But it's also one of the hardest to get right. Nylon absorbs moisture from the air like a sponge, needs high temperatures, and warps aggressively. If you know what to expect and set things up correctly, the results are worth the effort.

This guide covers the settings, hardware requirements, and practical tips you need to print nylon successfully.

## Why Print with Nylon?

Nylon isn't for everyone. But for certain applications, nothing else comes close.

**What makes nylon special:**

- Extremely tough. It bends before it breaks.
- Excellent wear resistance. Great for gears, bearings, and sliding parts.
- Good chemical resistance to oils, greases, and many solvents.
- Low friction surface. Parts slide against each other smoothly.
- Higher temperature resistance than PLA or PETG.

If you're printing functional parts that take abuse, nylon is a top choice. For display models or decorative prints, stick with [PLA or PETG](/blog/pla-vs-petg-vs-abs/). They're easier and cheaper.

## Types of Nylon Filament

Not all nylon is the same. The type you choose changes your settings and results.

**PA6 (Nylon 6):** The strongest and stiffest option. Also the hardest to print. Very high temps (260-280C), serious warping, and extremely moisture-sensitive. This is industrial-grade nylon.

**PA12 (Nylon 12):** The most beginner-friendly nylon. Lower printing temps (220-250C), less warping, and easier bed adhesion. Slightly less strong than PA6 but still much tougher than PETG. This is where most people should start.

**PA6/66 blends:** Some brands mix nylon types for a balance of strength and printability. Polymaker PA6-GF and PA6-CF fall in this category.

**Carbon fiber nylon (PA-CF):** Nylon reinforced with chopped carbon fiber. Stiffer and more dimensionally stable than plain nylon. Reduces warping significantly. But it's abrasive and will destroy a brass nozzle in hours. You need a hardened steel or ruby nozzle.

**Glass fiber nylon (PA-GF):** Similar idea to carbon fiber but with glass fiber reinforcement. Less stiff than CF but still more stable than plain nylon. Also abrasive.

## Nylon Printing Settings

Here are starting settings for the most common nylon types. Adjust from here based on your results.

| Setting | PA12 | PA6 | PA-CF/GF |
|---------|------|-----|----------|
| Nozzle temp | 230-250C | 260-280C | 260-280C |
| Bed temp | 70-90C | 90-110C | 90-100C |
| Print speed | 40-60mm/s | 30-50mm/s | 40-60mm/s |
| Fan speed | 0-30% | 0-20% | 0-30% |
| Retraction | 1-3mm (direct drive) | 1-3mm (direct drive) | 1-3mm (direct drive) |
| First layer speed | 20-30mm/s | 15-25mm/s | 20-30mm/s |
| Enclosure | Recommended | Required | Recommended |
| Nozzle type | Brass OK | Brass OK | Hardened steel required |

A few notes on these settings:

- **Keep fan speed low.** Nylon needs to stay warm for good layer adhesion. Too much cooling causes delamination.
- **Slow first layers are critical.** Nylon wants to warp. A slow, hot first layer bonds better.
- **Retraction values are for direct drive.** If you're running a Bowden setup, increase to 4-6mm. But honestly, direct drive is much better for nylon.

## Hardware Requirements

Nylon isn't a "just load it and print" material. Your printer needs specific hardware.

### All-Metal Hotend (Required)

PA12 prints at 230C minimum. PA6 needs 260C+. Stock PTFE-lined hotends max out at around 240C before the PTFE starts breaking down and releasing toxic fumes.

You need an [all-metal hotend](/blog/all-metal-hotend-upgrade/) for any serious nylon printing. A Micro Swiss, Slice Engineering Mosquito, or E3D V6 all-metal will handle nylon temps without issue.

### Enclosure (Strongly Recommended)

Nylon warps. A lot. An [enclosure](/blog/3d-printer-enclosure-guide/) traps heat around the print and reduces drafts. This dramatically reduces warping, especially on larger parts.

For PA6, an enclosure is basically required. For PA12, you might get away without one on small parts, but you'll have a much better time with one.

Even a simple cardboard or foam board enclosure helps. You don't need a fancy heated chamber unless you're printing large PA6 parts.

### Dry Box or Filament Dryer (Required)

This is the biggest challenge with nylon. It's extremely hygroscopic, meaning it sucks moisture out of the air constantly. A spool left in the open for 24 hours can absorb enough moisture to ruin your prints.

Wet nylon causes:

- Popping, hissing, and bubbling during printing
- Rough, stringy surface finish
- Weak layer adhesion
- Stringing everywhere

You absolutely need a way to dry your nylon and keep it dry while printing. Check our [filament drying guide](/blog/filament-drying-guide/) for the full breakdown.

A filament dryer that feeds directly to your printer (like the Sunlu S2 or EIBOS Cyclopes) is the ideal setup. You print from the dryer so the filament never sits in open air. At minimum, dry your nylon at 70-80C for 6-12 hours before printing and store it with desiccant.

## Bed Adhesion Tips

Getting nylon to stick to the bed is half the battle. Here's what works.

**PEI sheet + glue stick** is the most reliable combo. The glue stick acts as both an adhesion promoter and a release agent. Without it, nylon might bond too well to PEI and tear off a chunk of the surface. With it, prints stick during printing and pop off cleanly when cool.

**Garolite (G10/FR4) sheets** are the gold standard for nylon adhesion. Nylon bonds to garolite extremely well at temperature and releases when cool. If you print a lot of nylon, a garolite build plate is worth the investment ($15-25).

**Blue painter's tape** works in a pinch but isn't as reliable for larger prints.

**Brims are your friend.** Always print nylon with at least a 5-10mm brim. The extra contact area fights warping on the edges. For large flat parts, consider 15mm or more.

## Common Problems and Fixes

**Stringing everywhere:** Your nylon is probably wet. Dry it. Also try increasing retraction by 0.5mm and dropping temp by 5C.

**Warping and lifting corners:** Add a brim. Use an enclosure. Increase bed temp by 5-10C. Try glue stick on PEI.

**Poor layer adhesion (layers peel apart):** Increase nozzle temp by 5-10C. Reduce fan speed to 0%. Make sure you're in an enclosure.

**Rough, bubbly surface:** Your filament is wet. Dry it at 70-80C for 8-12 hours. If it still pops, dry it longer.

**Nozzle clogging (CF/GF nylon):** You're probably using a brass nozzle. Switch to hardened steel. Carbon and glass fibers eat through brass in one or two prints.

## Is Nylon Worth the Hassle?

If you need strong functional parts, yes. Nothing in the consumer 3D printing world matches nylon for toughness and wear resistance. Gears, hinges, clips, bushings, tool handles. These are where nylon shines.

If you're printing shelf decorations or prototypes, stick with PLA or PETG. Nylon is overkill and more frustrating for those uses.

Start with PA12. It's the most forgiving nylon type and still gives you most of the strength benefits. Once you're comfortable with PA12, you can graduate to PA6 or carbon fiber nylon for maximum performance.

## FAQ

<details>
<summary>Can I print nylon on a stock Ender 3?</summary>

Not really. A stock Ender 3 has a PTFE-lined hotend that maxes out around 240C, no enclosure, and a Bowden tube that doesn't handle nylon's flexibility well. You'd need at minimum an all-metal hotend upgrade and ideally a direct drive conversion plus an enclosure. At that point you've spent $50-100 in upgrades, but the printer can handle PA12 nylon.
</details>

<details>
<summary>How long does nylon take to absorb moisture?</summary>

Nylon starts absorbing moisture immediately. In a humid environment, a spool can take on enough water to affect print quality within 12-24 hours. PA6 is worse than PA12. Once opened, always store nylon in an airtight container with fresh desiccant. For best results, print directly from a heated dryer.
</details>

<details>
<summary>Is carbon fiber nylon stronger than regular nylon?</summary>

Carbon fiber nylon is stiffer and more dimensionally stable, but not necessarily stronger in all directions. The fibers add rigidity and reduce warping. However, CF nylon can be more brittle than plain nylon, especially in the Z direction (between layers). Choose CF nylon when you need stiffness and dimensional accuracy. Choose plain nylon when you need flexibility and impact resistance.
</details>
