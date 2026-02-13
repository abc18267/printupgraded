---
title: "Layer Adhesion Problems: Why Your Prints Are Weak"
date: 2026-02-13
description: "Fix 3D print layer adhesion problems that cause weak, brittle prints with these proven temperature and speed adjustments"
keywords: ["3D print layer adhesion", "weak 3D prints", "layer bonding problems", "delamination"]
categories: ["troubleshooting"]
tags: ["layer adhesion", "print strength", "troubleshooting"]
series: ["troubleshooting-guides"]
draft: false
---

**Affiliate Disclosure:** Some links in this article are affiliate links. We may earn a small commission if you purchase through them, at no extra cost to you.

# Layer Adhesion Problems: Why Your Prints Are Weak

If your 3D prints snap apart along the layer lines, you have a layer adhesion problem. Good 3D print layer adhesion means each layer fuses properly to the one below it. When it works, your parts are strong. When it doesn't, they're brittle and fragile. The most common cause is printing too cold. Raise your temperature 5-10C and you'll probably fix it.

But temperature isn't the only factor. Let's dig into all the causes and fixes.

## What Causes Poor Layer Adhesion?

Every layer needs to partially melt the previous layer to bond with it. If the new layer doesn't get hot enough, or the previous layer has cooled too much, the bond is weak. Think of it like welding. Both surfaces need heat to fuse together.

Here are the main culprits:

### Temperature Too Low

This is the number one cause. When your hotend temperature is too low, the filament isn't fluid enough to bond with the previous layer. Each material has a range where adhesion is best:

- PLA: 200-215C (bump up from the typical 200C starting point)
- PETG: 230-245C
- ABS: 235-250C
- Nylon: 250-270C
- TPU: 220-235C

If you're at the bottom of the range and getting weak layers, go up 5-10C.

### Printing Too Fast

Speed affects adhesion in two ways. First, faster printing means less time for each layer to bond. Second, faster speeds require higher temperatures to keep the filament properly melted. If you've increased your speed without raising your temperature, that's probably your problem.

For parts that need strength, slow down to 40-50mm/s. Our guide on [print speed vs quality](/blog/print-speed-vs-quality/) explains the tradeoffs in detail.

### Too Much Cooling

Part cooling fans help with overhangs and fine details. But too much cooling can freeze each layer before the next one arrives. This kills adhesion.

For PLA, 100% fan is usually fine after the first few layers. For PETG, keep the fan at 30-50%. For ABS and ASA, turn the fan off completely. Nylon prints best with no fan as well.

### Wet Filament

Moisture in filament causes tiny steam explosions at the nozzle. These create micro-voids in each layer that weaken the bond. You might hear popping or crackling sounds while printing. If so, your filament needs drying.

Nylon, PETG, and TPU absorb moisture the fastest. Even PLA can absorb enough moisture to cause problems if left out for weeks. Our [filament drying guide](/blog/filament-drying-guide/) covers the right temperatures and times for every material.

### Under-Extrusion

If your printer isn't pushing out enough filament, each layer is thinner than it should be. Thin layers don't make good contact with the layer below. This creates weak bonds. Under-extrusion has many causes, from clogged nozzles to worn extruder gears.

### Layer Height Too Tall

If your layer height is too close to your nozzle diameter, the layers sit on top of each other without enough squish. A good rule of thumb: keep your layer height at or below 75% of your nozzle diameter. For a 0.4mm nozzle, that's a maximum of 0.3mm layer height.

## How to Test Layer Adhesion

You can test adhesion with a simple method. Print a thin-walled box (1-2 walls, no infill). Try to break it along the layer lines with your hands. Good adhesion means you'll struggle to split the layers. Bad adhesion means it snaps apart easily.

For a more scientific approach, print a small hook or bracket and hang weights from it. Compare results at different temperatures and speeds to find the strongest combination.

## Fixes for Better Layer Adhesion

Here's your action plan, in order of what to try first:

1. **Raise hotend temperature by 5-10C.** This is the fix most of the time.
2. **Slow down your print speed.** Try 40mm/s for structural parts.
3. **Reduce part cooling fan.** Drop to 50% or lower for everything except PLA.
4. **Dry your filament.** Especially if it's been sitting out for more than a week.
5. **Check your extrusion.** Calibrate e-steps and make sure the nozzle isn't partially clogged.
6. **Use a wider extrusion width.** Setting your extrusion width to 110-120% of nozzle diameter pushes filament down harder onto the previous layer.
7. **Use an enclosure.** For ABS, ASA, and nylon, an enclosure keeps the ambient temperature warm enough to prevent rapid cooling between layers.

## When Hardware Is the Problem

Sometimes settings won't fix layer adhesion because the hardware is the issue.

**Inconsistent hotend temperature.** If your hotend temperature swings up and down, some layers get proper heat and others don't. Run a PID autotune (M303 in Marlin) to stabilize your temperature. An [all-metal hotend upgrade](/blog/all-metal-hotend-upgrade/) often provides more consistent heating than stock hotends because of better thermal design.

**Drafty environment.** Cold air hitting the print causes rapid, uneven cooling. An [enclosure](/blog/3d-printer-enclosure-guide/) solves this completely. Even for PLA, an enclosure can improve layer adhesion on large prints.

**Worn nozzle.** A worn nozzle has an inconsistent opening that leads to uneven extrusion. Brass nozzles wear out over time, especially if you print abrasive filaments. Replace the nozzle and see if adhesion improves.

For more print quality issues and fixes, see our [3D print troubleshooting master guide](/blog/3d-print-troubleshooting/).

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What temperature should I print at for the strongest layer adhesion?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Print at the higher end of the recommended range for your filament. For PLA, try 210-215C. For PETG, try 240-245C. Higher temperatures give better layer bonding, but going too high can cause stringing and other issues. Find the balance that gives you both strength and quality."
      }
    },
    {
      "@type": "Question",
      "name": "Does layer height affect print strength?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Thinner layers generally give better adhesion because each layer squishes more firmly onto the previous one. A 0.16mm layer height will produce a stronger part than 0.28mm in the Z direction. But thinner layers also mean longer print times, so balance strength against time."
      }
    },
    {
      "@type": "Question",
      "name": "Can infill pattern affect layer adhesion?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Infill pattern affects overall part strength but not layer-to-layer adhesion directly. However, some patterns provide better internal support. Grid and cubic patterns work well for general strength. For parts that need maximum resistance to splitting along layers, increasing wall count matters more than infill pattern."
      }
    }
  ]
}
</script>

### What temperature should I print at for the strongest layer adhesion?

Print at the higher end of the recommended range for your filament. For PLA, try 210-215C. For PETG, try 240-245C. Higher temperatures give better layer bonding, but going too high can cause stringing and other issues. Find the balance that gives you both strength and quality.

### Does layer height affect print strength?

Yes. Thinner layers generally give better adhesion because each layer squishes more firmly onto the previous one. A 0.16mm layer height will produce a stronger part than 0.28mm in the Z direction. But thinner layers also mean longer print times, so balance strength against time.

### Can infill pattern affect layer adhesion?

Infill pattern affects overall part strength but not layer-to-layer adhesion directly. However, some patterns provide better internal support. Grid and cubic patterns work well for general strength. For parts that need maximum resistance to splitting along layers, increasing wall count matters more than [infill pattern](/blog/infill-patterns-explained/).
