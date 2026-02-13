---
title: "How to Print PETG: Settings, Tips, and Common Mistakes"
date: 2026-02-13
description: "Learn how to print PETG with the right temperature, speed, and retraction settings. Avoid stringing and get strong, clean prints every time"
keywords: ["how to print PETG", "PETG settings", "PETG print temperature"]
categories: ["filament"]
tags: ["PETG", "print settings", "filament guide"]
series: ["filament-guides"]
draft: false
---

# How to Print PETG: Settings, Tips, and Common Mistakes

PETG is one of the best filaments for functional prints. But if you try printing it with your PLA settings, you'll end up with a stringy mess. Here's how to print PETG properly, with the right temperatures, retraction settings, and tips to avoid the most common mistakes.

If you're still deciding whether PETG is right for your project, check out our [PLA vs PETG vs ABS comparison](/blog/pla-vs-petg-vs-abs/) first.

## Recommended PETG Print Settings

These settings work well as a starting point for most printers and PETG brands. You'll likely need to fine-tune based on your specific setup.

| Setting | Recommended Value |
|---|---|
| **Nozzle Temperature** | 230-245C |
| **Bed Temperature** | 75-85C |
| **Print Speed** | 40-60 mm/s |
| **Retraction Distance** | 3-5mm (Bowden) / 1-2mm (Direct Drive) |
| **Retraction Speed** | 25-35 mm/s |
| **Cooling Fan** | 30-50% (not full blast) |
| **Layer Height** | 0.2mm |
| **First Layer Speed** | 20-25 mm/s |

### Temperature Tips

Start at 235C for your nozzle and adjust from there. If you see stringing, drop 5 degrees. If you see poor layer adhesion or under-extrusion, bump it up 5 degrees.

For the bed, 80C works for most PETG brands. Going too hot can actually make adhesion worse because the first layer stays too soft and gets dragged around by the nozzle.

### Getting the First Layer Right

PETG is picky about the first layer. Unlike PLA, you don't want to squish the first layer down hard. If the nozzle is too close to the bed, PETG will stick to the nozzle and create blobs.

Set your Z-offset slightly higher than you would for PLA. You want the first layer to lay down flat but not get smashed. A little bit of light showing through is fine.

## How to Fix PETG Stringing

Stringing is the number one complaint with PETG. Those thin whispy threads between parts of your print are annoying, but fixable.

**Lower your nozzle temperature.** This is the single most effective fix. Drop 5C at a time until stringing decreases without hurting layer adhesion.

**Increase retraction distance.** Add 0.5mm at a time. Too much retraction causes clogs, so don't go crazy. For Bowden setups, 4-6mm is typical. For direct drive, 1.5-3mm.

**Slow down retraction speed.** PETG is more viscous than PLA. Pulling the filament back too fast can create bubbles and uneven extrusion. Try 25-30 mm/s.

**Reduce travel speed.** Slower travel moves give the filament more time to retract before the nozzle crosses open areas.

**Enable "wipe" and "combing" in your slicer.** Wipe makes the nozzle drag along the perimeter before retracting. Combing keeps the nozzle traveling within the printed area. Both help reduce visible stringing.

Don't expect zero stringing with PETG. Even with perfect settings, you may see a few thin hairs. They're easy to clean up with a heat gun or lighter.

## Common PETG Mistakes to Avoid

### Too Much Cooling

This is counterintuitive if you're coming from PLA. With PLA, you blast the cooling fan at 100%. With PETG, that much cooling causes poor layer adhesion and can make prints weak.

Keep the fan at 30-50%. Some people turn it off entirely for the first few layers. For bridges and overhangs, you might bump it up temporarily. But never full blast.

### Wrong Bed Surface

PETG sticks incredibly well to bare glass. Sometimes too well. It can actually rip chunks of glass off your bed when you try to remove the print.

Use a PEI spring steel sheet, textured build plate, or apply a thin layer of glue stick to glass beds. The glue stick acts as a release agent, not an adhesive. It makes removal much easier.

If your filament is absorbing moisture, you'll also get adhesion problems. Check our [filament drying guide](/blog/filament-drying-guide/) if you notice popping sounds or rough textures during printing.

### Printing Too Fast

PETG doesn't flow as easily as PLA. Pushing it too fast leads to under-extrusion, weak layers, and rough surface finish.

Keep your speed at 40-60 mm/s for best results. You can go faster with a volcano-style hotend, but standard hotends need time to melt PETG properly.

### Ignoring Moisture

PETG absorbs moisture from the air. Wet PETG produces bubbling, popping, stringing, and rough surfaces. If your spool has been sitting out for more than a week or two, dry it before printing.

A food dehydrator or dedicated filament dryer at 65C for 4-6 hours will fix most moisture issues. Store opened spools in sealed bags or containers with desiccant.

## Best Practices for Great PETG Prints

Here's a quick checklist for consistently good PETG results.

1. **Dry your filament** before printing, especially if it's been opened for a while.
2. **Level your bed carefully** and set Z-offset slightly higher than PLA.
3. **Start at 235C/80C** and adjust based on results.
4. **Keep cooling at 30-50%.** Only increase for bridges.
5. **Use a PEI or textured bed.** Avoid bare glass unless you use glue stick as a release agent.
6. **Print slow.** 40-60 mm/s for walls, 20-25 mm/s for the first layer.
7. **Tune retraction** to minimize stringing without causing clogs.

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What temperature should I print PETG at?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Most PETG prints well at 230-245C for the nozzle and 75-85C for the bed. Start at 235C and adjust in 5-degree increments. Lower temperatures reduce stringing but can hurt layer adhesion if you go too low."
      }
    },
    {
      "@type": "Question",
      "name": "Why does my PETG print have so many strings?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "PETG strings more than PLA because it is more viscous. Lower your nozzle temperature by 5C, increase retraction distance slightly, and enable wipe and combing in your slicer. Some minimal stringing is normal with PETG."
      }
    },
    {
      "@type": "Question",
      "name": "Do I need a heated bed for PETG?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. PETG requires a heated bed at 75-85C for proper adhesion. Without a heated bed, PETG will not stick reliably and will likely warp or pop off during printing."
      }
    },
    {
      "@type": "Question",
      "name": "Can I print PETG on a glass bed?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "You can, but be careful. PETG bonds extremely well to bare glass and can damage the surface when removed. Apply a thin layer of glue stick to act as a release agent. A PEI or textured build plate is a better long-term option."
      }
    }
  ]
}
</script>

### What temperature should I print PETG at?

Most PETG prints well at 230-245C for the nozzle and 75-85C for the bed. Start at 235C and adjust in 5-degree increments. Lower temps reduce stringing but can hurt layer adhesion if you go too low.

### Why does my PETG print have so many strings?

PETG strings more than PLA because it's more viscous. Lower your nozzle temperature by 5C, increase retraction distance slightly, and enable wipe and combing in your slicer. Some minimal stringing is normal with PETG.

### Do I need a heated bed for PETG?

Yes. PETG needs a heated bed at 75-85C for proper adhesion. Without one, PETG won't stick reliably and will likely warp or pop off during printing.

### Can I print PETG on a glass bed?

You can, but be careful. PETG bonds extremely well to bare glass and can damage the surface when you remove prints. Apply a thin layer of glue stick as a release agent. A PEI or textured build plate is a better long-term option.
