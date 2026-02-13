---
title: "3D Print Warping: Causes and Fixes That Work"
date: 2026-02-13
description: "Fix 3D print warping with proven methods including bed temp, brims, enclosures, and surface upgrades that stop lifting"
keywords: ["3D print warping", "fix warping 3D printer", "print lifting from bed", "warping solutions"]
categories: ["troubleshooting"]
tags: ["warping", "bed adhesion", "troubleshooting"]
series: ["troubleshooting-guides"]
draft: false
---

**Affiliate Disclosure:** Some links in this article are affiliate links. We may earn a small commission if you purchase through them, at no extra cost to you.

# 3D Print Warping: Causes and Fixes That Work

3D print warping happens when the corners or edges of your print curl up from the bed. It's one of the most common and frustrating problems in 3D printing. The fix depends on your material, your environment, and your bed setup. In most cases, you can stop warping completely with the right combination of bed temperature, adhesion helpers, and environmental control.

## What Causes Warping?

Plastic shrinks when it cools. That's the root cause of all warping. When a layer cools and contracts, it pulls on the layers around it. The bottom layers are locked to the bed while upper layers are free to contract. This mismatch creates stress that eventually pulls the corners up.

Three factors make warping worse:

**Uneven cooling.** Drafts from open windows, AC vents, or even the printer's own part cooling fan can cool one side of the print faster than the other. That uneven contraction causes warping.

**Bad bed adhesion.** If the first layer isn't stuck firmly to the bed, the contraction forces will pull it loose. The corners go first because they have the most surface area exposed to cooling air.

**High shrinkage materials.** Some plastics shrink more than others. The higher the shrinkage, the more warping force.

## Which Materials Warp the Most?

Here's the ranking from worst to best:

1. **ABS** warps the most. It has high shrinkage and needs an enclosure for anything larger than a few centimeters.
2. **Nylon** warps badly and also absorbs moisture, making it doubly difficult.
3. **ASA** warps less than ABS but still needs careful temperature management. See our [ASA vs ABS comparison](/blog/asa-vs-abs/) for the full breakdown.
4. **PETG** warps occasionally, usually on large flat parts. It's much more forgiving than ABS.
5. **PLA** rarely warps. If PLA is warping, something is very wrong with your setup.

For a full material comparison, read our guide on [PLA vs PETG vs ABS](/blog/pla-vs-petg-vs-abs/).

## How to Fix 3D Print Warping

### Fix 1: Use a Brim

A brim is extra material printed around the base of your model. It increases the surface area touching the bed, which means more holding force against warping stress. Set your brim to 5-10mm wide for best results.

A brim works better than a raft in most cases. It uses less material, prints faster, and is easier to remove.

### Fix 2: Raise Your Bed Temperature

A warmer bed keeps the bottom layers from cooling too fast. This reduces the temperature difference between layers and cuts down on contraction stress.

Typical bed temperatures for warp-prone materials:
- ABS: 100-110C
- ASA: 95-105C
- PETG: 75-85C
- Nylon: 70-80C
- PLA: 55-65C (warping is rare)

If you're at the low end of the range for your material, try bumping up 5C.

### Fix 3: Use an Enclosure

An [enclosure](/blog/3d-printer-enclosure-guide/) is the single best upgrade for preventing warping. It blocks drafts, traps heat, and keeps the ambient temperature stable around your print. For ABS and nylon, an enclosure isn't optional. It's required.

Even a simple cardboard box or plastic bin over your printer makes a difference. You don't need a fancy setup to see results.

### Fix 4: Eliminate Drafts

If you don't have an enclosure, at least control your environment. Close windows near the printer. Turn off fans and AC vents aimed at the print area. Don't open the door to the room while printing ABS.

Even PLA can warp if you have a strong draft blowing across the bed.

### Fix 5: Upgrade Your Build Surface

The right build surface makes a huge difference. A [PEI sheet](/blog/pei-vs-glass-vs-magnetic-build-plate/) gives excellent adhesion for most materials without any glue or tape. Textured PEI is especially good for PETG.

For ABS on glass, use a thin layer of ABS juice (ABS dissolved in acetone). For PLA on glass, a glue stick works fine.

### Fix 6: Adjust First Layer Settings

A squished first layer sticks better. Make sure your Z offset is close enough. The first layer should be slightly squished flat, not round.

Set your first layer height to 0.28-0.3mm for a 0.4mm nozzle. Use a wider first layer line width, around 120-150% of your nozzle diameter. Slow your first layer speed to 20-25mm/s.

For detailed first layer settings in Cura, check our [best Cura settings for PLA](/blog/best-cura-settings-pla/) guide. Those principles apply to other materials too.

### Fix 7: Design Considerations

Some designs are more warp-prone than others. Large flat surfaces with sharp corners are the worst. If you can, add fillets (rounded corners) to the base of your model. Mouse ears (small discs at corners) also help.

Orienting the part so the largest flat surface isn't on the bed can also reduce warping, though this sometimes creates other challenges with supports.

## When Warping Won't Stop

If you've tried everything above and still get warping, check these less obvious causes:

- **Bed not actually flat.** A warped bed surface means some areas aren't getting good contact. Try a different spot on the bed or use mesh bed leveling.
- **Bed losing heat mid-print.** Check your bed temperature during printing. If it fluctuates, run a PID autotune on the heated bed.
- **Part cooling fan too aggressive.** For ABS and ASA, turn the part cooling fan off completely. For PETG, keep it under 50%.

For more print quality fixes, check our [3D print troubleshooting master guide](/blog/3d-print-troubleshooting/).

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Why do my PLA prints warp even though PLA isn't supposed to warp?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "PLA warping usually means there's a draft hitting the print, the bed temperature is too low (under 55C), or the bed isn't level. PLA has low shrinkage so it rarely warps under normal conditions. Check for air currents and make sure your bed is properly leveled."
      }
    },
    {
      "@type": "Question",
      "name": "Is a brim or a raft better for preventing warping?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "A brim is better in most cases. It uses less filament, prints faster, and leaves a cleaner bottom surface. Rafts are only needed when the bed surface is very uneven or when printing tiny parts that don't have enough surface area to stick on their own."
      }
    },
    {
      "@type": "Question",
      "name": "Do I need an enclosure to print ABS without warping?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "For anything beyond very small ABS prints, yes. An enclosure keeps the ambient temperature stable and blocks drafts. Without one, ABS will warp on most parts larger than a few centimeters. Even a simple cardboard box over the printer helps significantly."
      }
    }
  ]
}
</script>

### Why do my PLA prints warp even though PLA isn't supposed to warp?

PLA warping usually means there's a draft hitting the print, the bed temperature is too low (under 55C), or the bed isn't level. PLA has low shrinkage so it rarely warps under normal conditions. Check for air currents and make sure your bed is properly leveled.

### Is a brim or a raft better for preventing warping?

A brim is better in most cases. It uses less filament, prints faster, and leaves a cleaner bottom surface. Rafts are only needed when the bed surface is very uneven or when printing tiny parts that don't have enough surface area to stick on their own.

### Do I need an enclosure to print ABS without warping?

For anything beyond very small ABS prints, yes. An enclosure keeps the ambient temperature stable and blocks drafts. Without one, ABS will warp on most parts larger than a few centimeters. Even a simple cardboard box over the printer helps significantly.
