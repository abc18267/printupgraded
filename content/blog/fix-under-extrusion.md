---
title: "Under-Extrusion: Causes, Diagnosis, and Fixes"
date: 2026-02-13
description: "Fix 3D printer under-extrusion causing gaps, thin walls, and weak prints with this complete diagnosis and repair guide"
keywords: ["3D printer under-extrusion", "fix under-extrusion", "not enough filament", "gaps in 3D print"]
categories: ["troubleshooting"]
tags: ["under-extrusion", "extrusion problems", "troubleshooting"]
series: ["troubleshooting-guides"]
draft: false
---

**Affiliate Disclosure:** Some links in this article are affiliate links. We may earn a small commission if you purchase through them, at no extra cost to you.

# Under-Extrusion: Causes, Diagnosis, and Fixes

3D printer under-extrusion means your printer isn't pushing out enough filament. You'll see gaps between lines, thin or missing layers, and weak infill. Your prints look incomplete and feel fragile. The most common causes are a clogged nozzle, wrong temperature, or an extruder that's slipping. Here's how to diagnose and fix it.

## What Under-Extrusion Looks Like

Under-extrusion has several telltale signs:

- **Gaps between perimeter lines.** You can see through the walls of your print.
- **Missing layers.** Some layers look like they barely printed.
- **Thin, stringy infill.** The infill pattern looks skeletal instead of solid.
- **Rough top surfaces.** The top layers don't fill in completely.
- **Clicking from the extruder.** The motor is trying to push filament but something is blocking it.

If you see these symptoms, one of the causes below is responsible.

## Common Causes of Under-Extrusion

### 1. Clogged or Partially Clogged Nozzle

This is the most common cause. A partial clog restricts filament flow but doesn't stop it completely. You get inconsistent extrusion that comes and goes.

**How to fix it:**
1. Try a cold pull. Heat the nozzle to printing temp. Push filament through. Cool to 90C (PLA) or 160C (PETG/ABS). Pull the filament out firmly. The tip should show the inside shape of the nozzle. Repeat until clean.
2. Use an acupuncture needle to clear the nozzle while hot.
3. If cold pulls don't work, replace the nozzle. Brass nozzles are cheap. Keep spares.

### 2. Printing Temperature Too Low

If the filament isn't hot enough, it won't flow easily through the nozzle. This is especially true at higher print speeds, where the filament spends less time in the melt zone.

**How to fix it:** Raise your temperature by 5-10C. If you recently increased your print speed, you probably need higher temps too.

### 3. Extruder Gear Slipping

The extruder gear grips the filament and pushes it forward. If the gear is worn, the tension is too low, or filament dust has built up on the teeth, the gear will slip. You'll see shavings of filament near the extruder and hear clicking.

**How to fix it:**
- Clean the gear teeth with a small brush.
- Increase the extruder tension (the spring or thumbscrew).
- Check if the gear is worn and replace it if the teeth are flat.
- If you have a stock plastic extruder, upgrade to a metal one. The plastic arm on Creality extruders is known to crack.

### 4. Bowden Tube Gap

On Bowden setups, the PTFE tube needs to sit flush against the back of the nozzle inside the hotend. If there's a gap, filament pools in that space. It creates back pressure, inconsistent flow, and eventually clogs.

**How to fix it:**
- Remove the nozzle and PTFE tube. Clean out any accumulated filament.
- Cut the end of the PTFE tube flat with a tube cutter (not scissors).
- Reassemble by pushing the tube all the way down, then tightening the nozzle against it.
- Consider upgrading to an [all-metal hotend](/blog/all-metal-hotend-upgrade/). All-metal hotends eliminate the PTFE tube in the heat zone entirely, which means no more bowden gap issues.

### 5. Filament Tangle

A tangled spool prevents filament from feeding smoothly. The extruder fights the tangle and either skips or under-extrudes. Tangles usually happen when the filament end slips under another wrap on the spool.

**How to fix it:** Always keep the filament end secured in the spool holder holes when not in use. If you find a tangle, unspool enough to free it. Check that the filament path from spool to extruder is smooth and not rubbing against anything.

### 6. Worn PTFE Tube

The PTFE tube inside a Bowden system degrades over time, especially if you print at temperatures above 240C. The inner surface becomes rough, creating friction that restricts filament movement.

**How to fix it:** Replace the PTFE tube. Use Capricorn brand tubing for better heat resistance and a tighter inner diameter. Or upgrade to a [direct drive system](/blog/direct-drive-vs-bowden/), which is less prone to these issues because the filament path is much shorter.

### 7. Wrong E-Steps

If your extruder steps per millimeter (e-steps) aren't calibrated, the printer might think it's pushing 100mm of filament when it's only pushing 95mm. That 5% shortfall shows up as under-extrusion.

**How to fix it:**
1. Mark your filament 120mm above the extruder inlet.
2. Send G1 E100 F100 to extrude 100mm.
3. Measure the remaining distance from the mark to the extruder.
4. Calculate: New e-steps = (current e-steps x 100) / actual mm extruded.
5. Save with M92 E[new value] and M500.

### 8. Filament Diameter Variation

Cheap filament can vary in diameter. If a section is thinner than 1.75mm, the extruder pushes less material than expected. Quality filament stays within +/- 0.02mm.

**How to fix it:** Measure your filament at several points with calipers. If it varies more than 0.05mm, that's a problem. Buy better filament.

## Bowden vs Direct Drive: Which Has More Under-Extrusion Issues?

Bowden tube setups are more prone to under-extrusion. The long tube creates friction, introduces potential gap issues, and makes retraction harder to tune. Direct drive systems have a short, direct filament path with fewer failure points.

If under-extrusion is a constant battle with your Bowden printer, a [direct drive conversion](/blog/direct-drive-vs-bowden/) might solve the problem permanently. It's one of the [best upgrades](/blog/best-3d-printer-upgrades/) you can make for extrusion reliability.

That said, plenty of Bowden printers work great when properly maintained. Don't assume you need to convert. Fix the basics first.

## Dry Your Filament

Wet filament can mimic under-extrusion. Moisture creates steam bubbles that interrupt the flow of filament. If you hear popping sounds while printing and see inconsistent extrusion, moisture is likely the culprit.

Our [filament drying guide](/blog/filament-drying-guide/) covers drying temperatures and times for every material type.

## FAQ

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How do I know if my 3D printer is under-extruding?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Look for gaps between perimeter lines, missing or thin layers, skeletal infill patterns, and rough top surfaces. Print a single-wall cube and measure the wall thickness. If it's significantly thinner than your slicer's line width setting, you're under-extruding."
      }
    },
    {
      "@type": "Question",
      "name": "Can under-extrusion cause weak prints?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Under-extrusion creates gaps between lines and layers, which reduces the bonding area. This makes prints significantly weaker, especially along the layer lines. Fixing under-extrusion improves both appearance and structural strength."
      }
    },
    {
      "@type": "Question",
      "name": "What's the difference between under-extrusion and a clogged nozzle?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "A clogged nozzle is one cause of under-extrusion, but under-extrusion can also be caused by wrong temperature, extruder gear problems, filament tangles, or incorrect e-steps. A full clog stops all extrusion. A partial clog causes inconsistent under-extrusion that varies throughout the print."
      }
    }
  ]
}
</script>

### How do I know if my 3D printer is under-extruding?

Look for gaps between perimeter lines, missing or thin layers, skeletal infill patterns, and rough top surfaces. Print a single-wall cube and measure the wall thickness. If it's significantly thinner than your slicer's line width setting, you're under-extruding.

### Can under-extrusion cause weak prints?

Yes. Under-extrusion creates gaps between lines and layers, which reduces the bonding area. This makes prints significantly weaker, especially along the layer lines. Fixing under-extrusion improves both appearance and structural strength.

### What's the difference between under-extrusion and a clogged nozzle?

A clogged nozzle is one cause of under-extrusion, but under-extrusion can also be caused by wrong temperature, extruder gear problems, filament tangles, or incorrect e-steps. A full clog stops all extrusion. A partial clog causes inconsistent under-extrusion that varies throughout the print.

For a complete overview of print problems and fixes, see our [3D print troubleshooting master guide](/blog/3d-print-troubleshooting/).
