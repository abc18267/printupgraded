---
title: "Support Settings Guide: When and How to Use Supports"
date: 2026-02-13
description: "Master 3D print support settings with this guide. Learn when to use supports, which type to pick, and how to remove them cleanly"
keywords: ["3D print support settings", "tree supports 3D printing", "when to use supports"]
categories: ["slicer-settings"]
tags: ["supports", "slicer-settings", "print-quality", "overhangs"]
series: ["slicer-guides"]
draft: false
---

*This post may contain affiliate links. If you buy through these links, we may earn a small commission at no extra cost to you. [Full disclosure here](/disclosure/).*

# Support Settings Guide: When and How to Use Supports

Getting your 3D print support settings right is the difference between clean prints and damaged ones. You need supports when your model has overhangs greater than 45 degrees from vertical. The best approach for most prints is tree or organic supports with 2-3 interface layers at 15% density. This gives you strong support that still removes cleanly.

Here's everything you need to know about supports.

## When Do You Need Supports?

The basic rule is the 45-degree rule. If any part of your model extends outward at more than 45 degrees from vertical without anything underneath it, that section needs support.

**You need supports for:**
- Overhangs greater than 45 degrees
- Bridges longer than about 50mm (shorter bridges often print fine without support)
- Floating sections with nothing below them
- Arms, antlers, or other features that stick out horizontally

**You don't need supports for:**
- Overhangs under 45 degrees
- Short bridges (under 30-40mm)
- Chamfers and fillets
- Vertical or near-vertical surfaces

Most slicers can show you exactly where supports will be placed in the preview. Always check before printing. Sometimes rotating your model 90 degrees eliminates the need for supports entirely.

## Support Types: Normal vs Tree vs Organic

There are three main support styles. Each works differently.

### Normal (Linear) Supports

These are the traditional supports. Straight columns of material built up from the build plate or from the model surface. They create a grid-like structure under overhangs.

**Pros:** Fast to generate and print. Predictable. Work well for simple overhangs.

**Cons:** Use more material. Can be hard to remove. Often leave marks on the surface. Can fuse to the model if settings aren't right.

### Tree Supports

Tree supports grow trunk-like structures from the build plate that branch out to reach overhangs. They only touch the model where needed.

**Pros:** Use less material. Easier to remove. Leave fewer marks on the print. Can reach overhangs without touching the model's sides.

**Cons:** Take longer to slice (the slicer needs to calculate the branching paths). Can be less stable for very heavy overhangs.

### Organic Supports

Organic supports are the newest option, available in OrcaSlicer and PrusaSlicer. They're similar to tree supports but with smoother, more natural-looking branches.

**Pros:** Best surface finish where supports meet the model. Very easy to remove. Efficient material usage.

**Cons:** Longest slicing time. May not be available in older slicer versions. Less predictable for extreme overhangs.

For most prints, tree or organic supports are the best choice. They save material, remove more easily, and leave better surfaces. Our [slicer comparison guide](/blog/cura-vs-orcaslicer-vs-prusaslicer/) covers how each slicer handles these support types.

## Key Support Settings

These settings control how your supports behave. Getting them right prevents two common problems: supports that won't come off, and supports that don't support well enough.

### Support Density

This controls how solid the support structure is. Think of it like [infill percentage](/blog/infill-patterns-explained/).

- **10-15%:** Good for most PLA prints. Light, easy to remove.
- **20-25%:** Better for larger overhangs or heavier sections.
- **30%+:** Rarely needed. Uses lots of material and is harder to remove.

Start at 15% and increase only if the supported area sags or fails.

### Support Z Distance (Top and Bottom)

This is the gap between the top of the support and the bottom of your model's overhang. It's the most important setting for clean removal.

**Top Z distance:** Set this to 1-2 layer heights (0.2-0.4mm at 0.2mm layer height). Too small and the support fuses to your print. Too large and the overhang sags before it reaches the support.

**Bottom Z distance:** This is the gap at the bottom where support meets the model (for supports that start on the model surface). Same range, 1-2 layer heights.

### Support Interface Layers

Interface layers are dense, flat layers printed between the support structure and your model. They create a smooth platform for your overhang to print on.

Use 2-3 interface layers at 80-100% density. This gives you a smooth bottom surface on the overhang while still allowing the support to break away. Without interface layers, the loose support structure can leave a rough texture.

### Support X/Y Distance

This is the horizontal gap between support and the model's walls. Set it to 0.4-0.8mm (1-2 line widths). Too close and the support sticks to the walls. Too far and the edges of overhangs droop.

## Support Settings by Material

Different filament materials behave very differently with supports. Your material choice matters as much as your slicer settings here.

**PLA:** Easiest material for supports. It's rigid, so supports snap off cleanly. Use the default settings above and you'll be fine. PLA is also the easiest material to [get started with in your slicer](/blog/best-cura-settings-pla/).

**[PETG](/blog/how-to-print-petg/):** Trickier. PETG sticks to itself aggressively. Increase your Z distance to 0.3-0.4mm. If supports still fuse to your print, try dropping the support interface density to 60%. Some people have success printing PETG supports at a lower temperature than the main print.

**ABS:** Similar to PLA for support removal. The higher print temperature means you may need slightly more Z distance. If you're printing in an enclosure, supports can get a bit gooey from the heat. Check our [PLA vs PETG vs ABS guide](/blog/pla-vs-petg-vs-abs/) for more material-specific tips.

**TPU:** Flexible filament is tough to support well. The flex makes supports hard to remove without damaging the print. Avoid supports with TPU when possible by orienting your model carefully.

## Build Plate and Support Adhesion

Your [build plate surface](/blog/pei-vs-glass-vs-magnetic-build-plate/) affects how well supports stick, especially the first support layer.

PEI sheets give excellent adhesion for both the print and its supports. This is usually good, but it can make support bases harder to remove. If supports leave marks on your bed, try reducing the support base line width to 75% of your normal width.

Glass beds provide more moderate adhesion. Supports may pop off during printing if the density is too low. Bump to 20% if this happens.

## Tips for Removing Supports Cleanly

Even with perfect settings, support removal takes some care.

1. **Let the print cool completely.** Warm PLA and PETG deform when you pull supports off. Wait until the print reaches room temperature.

2. **Use needle-nose pliers.** Grab the support base and peel it off in sheets. Don't yank, pull steadily.

3. **Use a flush cutter for tight spots.** Snip supports where they meet the model rather than pulling them away.

4. **Sand the contact areas.** Even good supports leave some marks. A quick pass with 220-grit sandpaper smooths things out.

5. **Consider support orientation.** Before printing, think about which surfaces matter most. Orient the model so supports touch less visible areas.

## Frequently Asked Questions

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can I print a 60 degree overhang without supports?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "It depends on your printer and material. The standard rule is that anything over 45 degrees needs support. Some well-tuned printers with good cooling can handle 55-60 degree overhangs in PLA without support. Try it with a test print first."
      }
    },
    {
      "@type": "Question",
      "name": "Why are my supports impossible to remove?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Your Z distance is probably too small. Increase the top Z distance to 0.3-0.4mm. Also check that you're not printing too hot, as higher temperatures make supports fuse to the print. PETG is especially prone to this problem."
      }
    },
    {
      "@type": "Question",
      "name": "Are tree supports better than normal supports?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "For most prints, yes. Tree supports use less material, are easier to remove, and leave better surface finishes. Normal supports are faster to slice and can be better for very large flat overhangs. Try tree supports first and switch to normal only if you have issues."
      }
    }
  ]
}
</script>

### Can I print a 60-degree overhang without supports?

It depends on your printer and material. The standard rule is that anything over 45 degrees needs support. Some well-tuned printers with good cooling can handle 55-60 degree overhangs in PLA without support. Try it with a test print first.

### Why are my supports impossible to remove?

Your Z distance is probably too small. Increase the top Z distance to 0.3-0.4mm. Also check that you're not printing too hot, as higher temperatures make supports fuse to the print. PETG is especially prone to this problem.

### Are tree supports better than normal supports?

For most prints, yes. Tree supports use less material, are easier to remove, and leave better surface finishes. Normal supports are faster to slice and can be better for very large flat overhangs. Try tree supports first and switch to normal only if you have issues.
