---
title: "How to Print TPU Flexible Filament: A Beginner's Guide"
date: 2026-02-13
description: "Learn how to print TPU flexible filament with the right settings, printer setup, and tips for clean, stretchy prints on any budget printer"
keywords: ["how to print TPU", "TPU filament settings", "flexible filament guide"]
categories: ["filament"]
tags: ["TPU", "flexible filament", "print settings", "beginner guide"]
series: ["filament-guides"]
draft: false
---

# How to Print TPU Flexible Filament: A Beginner's Guide

Printing TPU is easier than most people think. You just need the right settings and a little patience. If you know how to print TPU properly, you can make phone cases, drone bumpers, gaskets, shoe insoles, and anything else that needs to bend without breaking.

TPU (thermoplastic polyurethane) is a flexible, rubber-like filament. It's completely different from rigid materials like PLA, PETG, or ABS. If you're not sure how TPU compares to those options, check out our [filament comparison guide](/blog/pla-vs-petg-vs-abs/) for the full breakdown.

## What Makes TPU Different

TPU is soft and stretchy. That's what makes it useful, but it's also what makes it tricky to feed through a 3D printer.

Rigid filaments push smoothly through the extruder like a solid rod. TPU is flexible enough to buckle, bend, and jam in any gap between the drive gear and the nozzle. The softer the TPU, the harder it is to print.

TPU hardness is measured on the Shore A scale. Most printable TPU filament falls between 85A and 95A.

- **95A (like NinjaTek Cheetah, Overture TPU):** Slightly flexible. The easiest TPU to print. Good starting point.
- **85A (like NinjaTek NinjaFlex):** Very flexible. Harder to print. Requires a direct drive extruder.

Start with 95A TPU if this is your first time.

## Direct Drive vs Bowden: Does It Matter?

Yes. Your extruder type is the single biggest factor in whether TPU printing goes smoothly or becomes a frustrating mess.

**Direct drive extruders** mount the motor right on top of the hotend. The filament path is short, leaving almost no room for the TPU to buckle. This is the ideal setup for flexible filament.

**Bowden extruders** use a long PTFE tube between the motor and the hotend. Flexible filament can compress and jam inside this tube. You can still print 95A TPU with a Bowden setup, but you'll need to go much slower and may still have issues.

If you have a Bowden printer and want to print TPU regularly, consider a direct drive upgrade. For occasional TPU prints, you can make a Bowden setup work with patience and slow speeds.

Our [PETG printing guide](/blog/how-to-print-petg/) covers a material that's much easier on Bowden setups if you need something tougher than PLA without the extruder challenges.

## Recommended TPU Print Settings

| Setting | Direct Drive | Bowden |
|---|---|---|
| **Nozzle Temperature** | 220-235C | 220-235C |
| **Bed Temperature** | 50-60C | 50-60C |
| **Print Speed** | 20-30 mm/s | 15-20 mm/s |
| **Retraction Distance** | 0-2mm | 2-4mm (or disable) |
| **Retraction Speed** | 20-25 mm/s | 15-20 mm/s |
| **Cooling Fan** | 50-100% | 50-100% |
| **Layer Height** | 0.2mm | 0.2mm |
| **Infill** | 15-30% | 15-30% |
| **Flow Rate** | 100-105% | 100-110% |

### Key Settings Explained

**Speed is everything.** Print slow. Seriously. 25 mm/s is a good target for direct drive. 15-20 mm/s for Bowden. Going too fast causes the filament to buckle and jam. You can try increasing speed once you get successful prints, but start slow.

**Minimize retraction.** With direct drive, try 0.5-1.5mm retraction distance. With Bowden, some people disable retraction entirely to avoid jams. You'll get some stringing, but it's better than a clogged extruder.

**Temperature matters less than speed.** Most TPU prints fine at 225-230C. Unlike PETG, you don't need to worry much about dialing in the exact temperature.

**Use cooling.** Unlike PETG or ABS, TPU benefits from fan cooling. It helps maintain detail and prevents the soft material from deforming on overhangs.

## Tips for Successful TPU Prints

**Loosen your extruder tension.** If your extruder has an adjustable tensioner, back it off. Too much grip on flexible filament causes it to compress and buckle. You want just enough pressure to feed it through.

**Don't use a filament runout sensor.** Many runout sensors add friction and tight bends in the filament path. TPU can jam at these points. Bypass the sensor if possible.

**Remove any gaps in the filament path.** Check between the drive gear and the PTFE tube entrance. Any gap where TPU can escape will cause a jam. Some printers benefit from a small printed guide to close this gap.

**Print a test cube first.** Before starting a complex project, print a simple 20mm cube. This lets you verify your settings work without wasting time on a multi-hour print.

**Don't over-squish the first layer.** TPU is soft. If your nozzle is too close, it will compress the filament and create too much backpressure. Set your Z-offset slightly higher than you would for PLA.

**Store it dry.** TPU absorbs moisture. Wet TPU causes popping and poor surface quality. Keep it sealed with desiccant when you're not using it. Our [filament drying guide](/blog/filament-drying-guide/) covers the best storage and drying methods.

## Common TPU Problems and Fixes

**Filament jams in the extruder.** Slow down. Reduce retraction. Check for gaps in the filament path. Loosen extruder tension.

**Stringing everywhere.** This is normal with TPU, especially at low retraction values. You can clean up strings with a heat gun or lighter after printing. Increasing travel speed (not print speed) can also help.

**Print looks blobby.** Reduce flow rate by 2-5%. TPU is compressible, so the extruder can push more material than expected.

**First layer not sticking.** Clean your bed. Use a bed temperature of 50-60C. Blue painter's tape or a PEI sheet both work well with TPU. Glue stick helps on glass beds.

**Under-extrusion.** Increase flow rate to 105-110%. TPU compresses in the filament path, which means less material reaches the nozzle than the slicer expects.

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can I print TPU with a Bowden extruder?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, but it is more difficult. Use 95A hardness TPU, print at 15-20 mm/s, and minimize or disable retraction. A direct drive extruder gives much better results with flexible filaments."
      }
    },
    {
      "@type": "Question",
      "name": "What speed should I print TPU at?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Print TPU at 20-30 mm/s with a direct drive extruder, or 15-20 mm/s with a Bowden setup. Faster speeds cause the flexible filament to buckle and jam in the extruder."
      }
    },
    {
      "@type": "Question",
      "name": "Do I need a special nozzle for TPU?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. A standard brass nozzle works fine for TPU. The important factor is the extruder type and filament path, not the nozzle. A 0.4mm nozzle at standard printing temperatures handles TPU without issues."
      }
    }
  ]
}
</script>

### Can I print TPU with a Bowden extruder?

Yes, but it's harder. Use 95A hardness TPU, print at 15-20 mm/s, and minimize or disable retraction. A direct drive extruder gives much better results with flexible filaments.

### What speed should I print TPU at?

Print TPU at 20-30 mm/s with a direct drive extruder, or 15-20 mm/s with a Bowden setup. Faster speeds cause the flexible filament to buckle and jam in the extruder.

### Do I need a special nozzle for TPU?

No. A standard brass nozzle works fine for TPU. What matters is the extruder type and filament path, not the nozzle. A 0.4mm nozzle at standard printing temperatures handles TPU without issues.
