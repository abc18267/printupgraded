---
title: "First Layer Not Sticking? Here's How to Fix Bed Adhesion"
date: 2026-02-13
description: "Fix 3D print bed adhesion problems with this step-by-step guide to leveling, Z offset, bed temp, and surface prep"
keywords: ["3D print bed adhesion", "first layer not sticking", "bed leveling", "Z offset"]
categories: ["troubleshooting"]
tags: ["bed adhesion", "first layer", "troubleshooting"]
series: ["troubleshooting-guides"]
draft: false
---

**Affiliate Disclosure:** Some links in this article are affiliate links. We may earn a small commission if you purchase through them, at no extra cost to you.

# First Layer Not Sticking? Here's How to Fix Bed Adhesion

If your first layer won't stick, nothing else matters. The whole print will fail. 3D print bed adhesion problems are the most common issue beginners face. In most cases, the fix is simple: your bed isn't level, your Z offset is wrong, or your build surface is dirty. Let's walk through every cause and fix.

## Why Your First Layer Won't Stick

The first layer needs three things to stick properly:

1. **The right distance between nozzle and bed.** Too far and the filament doesn't press down onto the surface. Too close and the nozzle scrapes the filament away.
2. **Enough heat.** The bed needs to be warm enough to keep the filament soft while it bonds to the surface.
3. **A clean, appropriate surface.** Oils from your fingers, dust, and residue all prevent adhesion.

Let's fix each one.

## Step-by-Step Diagnostic

### Step 1: Level Your Bed

An unlevel bed means some areas are too close and others are too far. Most printers use manual leveling with four corner knobs.

Here's the process:
1. Home all axes.
2. Disable steppers so you can move the head by hand.
3. Move the nozzle to each corner.
4. Slide a piece of paper between the nozzle and bed. You should feel slight resistance when pulling it. The paper should slide but not freely.
5. Adjust the corner knob until you get that feel.
6. Repeat all four corners twice. Adjusting one corner affects the others.

If your printer has automatic bed leveling (ABL), run the probe calibration. ABL compensates for an uneven bed but it doesn't replace setting the correct Z offset.

### Step 2: Set Your Z Offset

Even with a level bed, the Z offset might be wrong. The Z offset tells the printer exactly how far the nozzle is from the bed when it's at "zero."

Print a single-layer square (about 50x50mm). Look at the result:
- **Lines not touching each other:** Z offset is too high. Lower it (make the number more negative).
- **Lines squished into a smooth sheet:** Z offset is too low. Raise it slightly.
- **Lines touching but slightly flat:** Perfect. That's what you want.

Adjust in 0.02mm increments. Small changes make a big difference. Our [best Cura settings for PLA](/blog/best-cura-settings-pla/) guide covers first layer settings in detail.

### Step 3: Check Your Bed Temperature

Every material needs a specific bed temperature:
- PLA: 55-65C
- PETG: 75-85C
- ABS: 100-110C
- TPU: 45-60C
- Nylon: 70-80C

If you're below these ranges, bump up the temperature. Give the bed 5 minutes to fully heat soak before printing. The surface temperature lags behind the thermistor reading.

### Step 4: Clean Your Build Surface

This is the fix people overlook. Fingerprints leave oils that create a invisible barrier between filament and bed. Even touching the build surface once can cause adhesion issues in that spot.

Clean your bed with isopropyl alcohol (IPA) at 90% concentration or higher. Wipe it down before every print. For glass beds, dish soap and warm water works even better.

For PEI surfaces, clean with IPA regularly. If adhesion drops even after cleaning, lightly sand the surface with 1000-grit sandpaper. This refreshes the texture.

### Step 5: Match Your Surface to Your Material

Not every build surface works with every material. Here's what works best:

- **PEI (smooth):** Great for PLA and ABS. PETG sticks too well and can damage the surface.
- **PEI (textured):** Great for PETG, good for PLA. The texture prevents PETG from bonding permanently.
- **Glass:** Works for PLA with glue stick. Good for ABS with ABS juice.
- **Magnetic flex plates:** Convenient but vary in quality. Look for PEI-coated versions.

For a full comparison, read our guide on [PEI vs glass vs magnetic build plates](/blog/pei-vs-glass-vs-magnetic-build-plate/).

## Adhesion Aids: When to Use Them

Sometimes a clean, level bed with the right temperature still isn't enough. That's when adhesion aids help.

**Glue stick.** The classic choice. Apply a thin, even layer. Works great for PLA on glass and PETG on smooth PEI (also acts as a release agent so PETG doesn't bond permanently).

**Hairspray.** Use unscented, extra-hold hairspray. Apply a light coat. Works for PLA and ABS. Can build up over time and needs cleaning.

**Painter's tape.** Blue painter's tape works well for PLA without a heated bed. Clean the tape with IPA first.

**Specialty adhesives.** Products like Magigoo and Vision Miner Nano Polymer work well but cost more. They're worth it if you print a lot of tricky materials.

The goal is to not need adhesion aids. If your setup requires glue on every print, the underlying issue (leveling, temperature, or surface type) probably isn't solved yet.

## First Layer Speed and Settings

Your first layer should print differently from the rest:

- **Speed:** 20-25mm/s. Slow and steady.
- **Layer height:** 0.28-0.3mm for a 0.4mm nozzle. A thicker first layer is more forgiving.
- **Line width:** 120-150% of nozzle diameter. A wider first layer squishes more material onto the bed.
- **Flow:** 100-105%. A slight bump in flow for the first layer helps.
- **Fan:** Off for the first 1-3 layers. Cooling the first layer hurts adhesion.

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Why does my first layer stick in some spots but not others?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "This almost always means your bed isn't level or the bed surface is warped. Re-level all four corners carefully. If the bed itself is warped (common on cheaper printers), use mesh bed leveling in firmware to compensate. A glass sheet placed on top of a warped aluminum bed can also help."
      }
    },
    {
      "@type": "Question",
      "name": "Should I use a brim or a raft for better bed adhesion?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "A brim adds extra first-layer material around the outside of your print. It's the best option for most adhesion problems. A raft is a full platform printed under your model. Use a raft only when the bed surface is very uneven or when the model has tiny contact points with the bed."
      }
    },
    {
      "@type": "Question",
      "name": "How often should I clean my 3D printer bed?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Clean with isopropyl alcohol before every print for best results. A quick wipe takes 10 seconds and prevents most adhesion failures. Deep clean with soap and water once a week if you print daily. Avoid touching the print surface with bare hands after cleaning."
      }
    }
  ]
}
</script>

### Why does my first layer stick in some spots but not others?

This almost always means your bed isn't level or the bed surface is warped. Re-level all four corners carefully. If the bed itself is warped (common on cheaper printers), use mesh bed leveling in firmware to compensate. A glass sheet placed on top of a warped aluminum bed can also help.

### Should I use a brim or a raft for better bed adhesion?

A brim adds extra first-layer material around the outside of your print. It's the best option for most adhesion problems. A raft is a full platform printed under your model. Use a raft only when the bed surface is very uneven or when the model has tiny contact points with the bed.

### How often should I clean my 3D printer bed?

Clean with isopropyl alcohol before every print for best results. A quick wipe takes 10 seconds and prevents most adhesion failures. Deep clean with soap and water once a week if you print daily. Avoid touching the print surface with bare hands after cleaning.

For more troubleshooting help, visit our [3D print troubleshooting master guide](/blog/3d-print-troubleshooting/).
