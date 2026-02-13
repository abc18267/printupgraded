---
title: "Infill Patterns Explained: Which One Should You Use?"
date: 2026-02-13
description: "Infill patterns in 3D printing explained. Compare grid, gyroid, cubic, lightning, and more to find the right pattern for your prints"
keywords: ["infill patterns 3D printing", "best infill pattern", "gyroid vs grid infill"]
categories: ["slicer-settings"]
tags: ["infill", "slicer-settings", "print-strength", "3d-printing-basics"]
series: ["slicer-guides"]
draft: false
---

*This post may contain affiliate links. If you buy through these links, we may earn a small commission at no extra cost to you. [Full disclosure here](/disclosure/).*

# Infill Patterns Explained: Which One Should You Use?

Infill patterns in 3D printing determine the internal structure of your prints. The right pattern depends on what you're printing. Grid and lines work great for quick prints that don't need strength. Gyroid is the best all-around choice for functional parts. Lightning saves the most material when you just need to support top layers.

Here's what each pattern does and when to use it.

## What Is Infill and Why Does It Matter?

Most 3D prints aren't solid. They have solid outer walls and a partially filled interior. That interior structure is your infill.

Infill affects three things: strength, weight, and print time. More infill means stronger and heavier prints that take longer. Less infill means lighter, faster prints that are weaker.

But the pattern of that infill matters just as much as the percentage. A 20% gyroid infill is significantly stronger than 20% lines infill, even though they use about the same amount of material.

## Infill Patterns Compared

| Pattern | Strength | Print Speed | Material Use | Best For |
|---|---|---|---|---|
| **Lines/Rectilinear** | Low | Very fast | Low | Quick prints, prototypes |
| **Grid** | Medium | Fast | Medium | General purpose |
| **Triangles** | Medium-High | Medium | Medium | Parts loaded from the top |
| **Cubic** | High | Medium | Medium | Functional parts, all-direction strength |
| **Gyroid** | High | Slower | Medium | Best all-around strength |
| **Lightning** | Very Low | Fastest | Very Low | Decorative prints, vases |
| **Honeycomb** | High | Slow | High | Maximum strength |

## Lines and Rectilinear

Lines is the simplest infill pattern. It prints parallel lines in one direction, alternating by 90 degrees each layer. Rectilinear is similar but slightly denser at the connection points.

**Pros:** Fastest print time. Uses the least material of the traditional patterns. Minimal retraction means less chance of [stringing](/blog/reduce-stringing-slicer-settings/).

**Cons:** Weak in the direction perpendicular to the lines. Not great for functional parts. Top layers can sag between the lines if the infill percentage is low.

**Use when:** You're prototyping, printing decorative items, or need something fast. Bump the density to 25% if you notice the top layer pillowing.

## Grid

Grid prints lines in two perpendicular directions on every layer, creating a crosshatch pattern. It's one of the most commonly used patterns.

**Pros:** Stronger than lines in all horizontal directions. Still fairly fast to print. Good default choice.

**Cons:** Not as strong as cubic or gyroid for the same material usage. Can create pressure buildup in enclosed spaces, causing surface defects on some prints.

**Use when:** You need a simple, reliable infill for everyday prints. 20% grid works for most things.

## Triangles

Triangle infill creates a pattern of triangles on each layer. It's strong when forces push down from the top, which makes it good for structural parts.

**Pros:** Strong against vertical loads. More rigid than grid. Good for shelf brackets, mounts, and similar parts.

**Cons:** Uses more material than grid at the same percentage. Slower to print because of the extra travel moves.

**Use when:** Your part needs to support weight from above. Think mounting brackets, tool holders, or structural supports.

## Cubic

Cubic creates a 3D pattern of tilted cubes. Unlike grid or triangles, cubic provides strength in all three directions, not just the horizontal plane.

**Pros:** Strong in every direction. Good balance of strength, speed, and material usage. Doesn't trap air pockets that cause surface issues.

**Cons:** Slightly slower than grid. A bit harder to preview in the slicer.

**Use when:** You're printing functional parts that experience forces from multiple directions. Cubic is an excellent default for anything that needs to be strong.

## Gyroid

Gyroid is a wavy, 3D pattern that curves through the model interior. It's become the go-to recommendation for strength-focused prints in the 3D printing community.

**Pros:** Strongest infill pattern relative to material usage. Equal strength in all directions. Flexible rather than brittle. Allows liquid to flow through (useful for casting molds). Looks cool if you print a cross-section.

**Cons:** Slowest of the common patterns because of the curved movements. Can be harder on your printer's motors due to constant direction changes.

**Use when:** You're printing anything functional and want the best strength-to-weight ratio. Gyroid at 15-20% often matches grid at 30-40% in practical strength tests.

The material you print with affects how well infill works. Flexible materials like TPU work differently than rigid materials like PLA. Check our [PLA vs PETG vs ABS comparison](/blog/pla-vs-petg-vs-abs/) to understand how material choice and infill work together.

## Lightning

Lightning is a newer pattern available in Cura and OrcaSlicer. Instead of filling the entire interior, it only builds support structures where the top surface needs them. The result looks like lightning bolts branching upward.

**Pros:** Uses dramatically less material than any other pattern. Fastest print time. Still produces good top surfaces.

**Cons:** Almost zero internal strength. The part will be nearly hollow. Not suitable for any functional use.

**Use when:** You're printing decorative items, display models, or anything that won't experience force. Lightning at 15% can cut your print time and filament usage in half compared to grid at 15%.

## Honeycomb

Honeycomb creates a hexagonal pattern similar to a beehive. It's been around for a long time in 3D printing.

**Pros:** Very strong. Natural structure that distributes force well.

**Cons:** Slow to print because of the many short moves and direction changes. Uses more material than cubic or gyroid for similar strength. Lots of retraction can cause [stringing issues](/blog/reduce-stringing-slicer-settings/).

**Use when:** You need maximum strength and don't care about print time or material usage. For most people, gyroid or cubic is a better choice with similar strength and faster prints.

## What Infill Percentage Should You Use?

The pattern only tells half the story. The percentage matters too.

- **0-10%:** Display models, prototypes. Very fragile. Top layers may sag.
- **15-20%:** General purpose. Good enough for most non-functional prints.
- **30-40%:** Functional parts. Handles reasonable force and stress.
- **50-75%:** High-strength applications. Diminishing returns above 50%.
- **100%:** Solid. Rarely needed. Adding more walls is usually a better way to add strength.

Here's a tip most guides don't mention. Increasing wall count from 3 to 5 adds more strength than going from 20% to 40% infill. Walls are the structural backbone of your print. Infill mainly supports the top surface and adds some rigidity.

For the full picture on how to dial in these settings, see our [slicer comparison guide](/blog/cura-vs-orcaslicer-vs-prusaslicer/) which covers how each slicer handles infill options.

## Frequently Asked Questions

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is the strongest infill pattern for 3D printing?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Gyroid is the strongest infill pattern relative to the amount of material used. It provides equal strength in all directions and is more resilient than grid or cubic patterns. For absolute maximum strength regardless of material use, honeycomb is also very strong."
      }
    },
    {
      "@type": "Question",
      "name": "Does infill pattern affect print time?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, significantly. Lightning and lines are the fastest patterns. Gyroid and honeycomb are the slowest. At 20% infill, the difference between the fastest and slowest pattern can be 15-30 minutes on a typical print."
      }
    },
    {
      "@type": "Question",
      "name": "Is 100% infill ever worth using?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rarely. Going from 50% to 100% infill roughly doubles print time and material usage but only adds about 10-15% more strength. A better approach is using 40-50% infill with 5-6 walls. The extra walls add more structural strength than filling the interior solid."
      }
    }
  ]
}
</script>

### What is the strongest infill pattern for 3D printing?

Gyroid is the strongest infill pattern relative to the amount of material used. It provides equal strength in all directions and is more resilient than grid or cubic patterns. For absolute maximum strength regardless of material use, honeycomb is also very strong.

### Does infill pattern affect print time?

Yes, significantly. Lightning and lines are the fastest patterns. Gyroid and honeycomb are the slowest. At 20% infill, the difference between the fastest and slowest pattern can be 15-30 minutes on a typical print.

### Is 100% infill ever worth using?

Rarely. Going from 50% to 100% infill roughly doubles print time and material usage but only adds about 10-15% more strength. A better approach is using 40-50% infill with 5-6 walls. The extra walls add more structural strength than filling the interior solid.
