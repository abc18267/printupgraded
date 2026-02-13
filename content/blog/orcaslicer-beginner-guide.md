---
title: "OrcaSlicer Beginner Guide: Setup and First Print"
date: 2026-02-13
description: "OrcaSlicer beginner guide covering download, setup, printer profiles, and your first print. Get started in under 15 minutes"
keywords: ["OrcaSlicer beginner guide", "OrcaSlicer setup", "how to use OrcaSlicer"]
categories: ["slicer-settings"]
tags: ["orcaslicer", "slicer-setup", "beginner-guide"]
series: ["slicer-guides"]
draft: false
---

*This post may contain affiliate links. If you buy through these links, we may earn a small commission at no extra cost to you. [Full disclosure here](/disclosure/).*

# OrcaSlicer Beginner Guide: Setup and First Print

OrcaSlicer is a free, open-source slicer that started as a fork of BambuStudio (which itself forked from PrusaSlicer). It's become one of the most popular slicers in the 3D printing community thanks to its built-in calibration tools, fast slicing, and excellent multi-color support. This OrcaSlicer beginner guide will walk you through downloading, setting up, and making your first print.

You can go from download to your first sliced file in about 15 minutes.

## What Makes OrcaSlicer Different?

You might wonder why you'd pick OrcaSlicer over Cura or PrusaSlicer. Check out our full [Cura vs OrcaSlicer vs PrusaSlicer comparison](/blog/cura-vs-orcaslicer-vs-prusaslicer/) for a detailed breakdown. But here's the quick version.

OrcaSlicer's biggest strengths are its built-in calibration tools and its Bambu Lab integration. You can run flow rate tests, pressure advance tuning, and temperature towers directly from the slicer. No extra downloads. No G-code editing.

It also handles multi-color printing better than any other free slicer. If you own a Bambu Lab printer with an AMS, OrcaSlicer is the best tool for the job.

## How to Download and Install OrcaSlicer

OrcaSlicer is available for Windows, macOS, and Linux. Here's how to get it.

1. Go to the [OrcaSlicer GitHub releases page](https://github.com/SoftFever/OrcaSlicer/releases).
2. Download the latest stable release for your operating system. Look for the file ending in .exe (Windows), .dmg (macOS), or .AppImage (Linux).
3. Run the installer and follow the prompts.

On Windows, you might see a SmartScreen warning since OrcaSlicer isn't signed by Microsoft. Click "More info" and then "Run anyway." It's safe.

The install takes about 2 minutes. OrcaSlicer updates frequently, so check for new releases every few weeks.

## Setting Up Your First Printer Profile

When you launch OrcaSlicer for the first time, it asks you to select your printer.

**Bambu Lab printers:** Select your exact model (X1C, P1S, P1P, A1, A1 Mini). OrcaSlicer will load tested profiles automatically. If your printer is on the same network, you can connect directly and send prints without using an SD card or USB drive.

**Other printers:** OrcaSlicer now supports most popular brands. Look for your printer in the list. Creality Ender 3 series, Anycubic Kobra, Voron, and many others have community-tested profiles.

**Custom printer:** If your printer isn't listed, you can create a custom profile. You'll need to know your bed size, nozzle diameter, max print speed, and firmware type (Marlin or Klipper).

After selecting your printer, choose a filament profile. Start with Generic PLA. This gives you safe default settings that work on most printers.

## Navigating the Interface

OrcaSlicer organizes everything into tabs across the top.

**Prepare tab:** This is your main workspace. Import models, arrange them on the build plate, and access slicing options. You'll spend most of your time here.

**Filament tab:** Adjust temperature, cooling, and retraction settings for your selected filament. Each filament type like [PLA, PETG, or ABS](/blog/pla-vs-petg-vs-abs/) needs different settings here.

**Process tab:** Control layer height, speed, infill, support, and other print parameters. This is where you fine-tune quality vs speed.

**Printer tab:** Hardware settings like bed size, nozzle diameter, and start/end G-code. You usually set this once and forget it.

The 3D viewport in the center shows your model on the virtual build plate. Use the mouse to rotate, zoom, and pan. Controls feel similar to most 3D software.

## Slicing Your First Model

Let's walk through your first print step by step.

1. **Import a model.** Click the "+" button or drag a .STL or .3MF file onto the build plate. A good first test is a calibration cube (20mm cube) or a benchy.

2. **Check positioning.** Make sure the model sits flat on the build plate. If it's floating, right-click and select "Lay on face." OrcaSlicer auto-orients most models, but double-check.

3. **Select your settings.** Choose your printer, filament, and process profile from the dropdowns. For a first print, stick with the defaults. 0.2mm layer height and Generic PLA are good choices.

4. **Click "Slice."** The button is in the bottom right. OrcaSlicer processes the model and shows you a preview with estimated print time and filament usage.

5. **Preview the result.** Use the layer slider on the right to scrub through the print layer by layer. Check that the first layer looks solid and that there aren't any obvious problems.

6. **Export or send.** Click "Export G-code" to save to an SD card or USB drive. If you have a Bambu Lab printer on your network, click "Print" to send it directly.

That's it. Your first print is ready.

## Key Features Worth Exploring

Once you're comfortable with the basics, try these features.

### Built-In Calibration Tools

Go to the Calibration menu at the top. You'll find tools for:

- **Temperature tower.** Prints a tower at different temperatures so you can pick the best one for your filament.
- **Flow rate test.** Dials in your extrusion multiplier for cleaner prints.
- **Pressure advance.** Tunes how your printer handles speed changes. This reduces bulging at corners.
- **Retraction test.** Helps you find the right retraction settings to [eliminate stringing](/blog/reduce-stringing-slicer-settings/).

Run the flow rate test first. It makes the biggest difference for most people.

### Multi-Color Painting

If you have a multi-color setup, OrcaSlicer has a paint tool that lets you assign colors to different parts of a model. Click on the model, select the paint tool, and paint directly on the surface.

### Custom Plate Management

You can set up multiple build plates in one session. This is handy for batch printing. Add models to different plates, slice them all, and print them one after another.

## Common First-Time Issues

**Model is too big for the build plate.** Right-click the model and use Scale to resize it. OrcaSlicer shows a red warning if anything extends past the build area.

**Slicer doesn't connect to my printer.** Make sure your printer and computer are on the same network. For Bambu Lab printers, you'll need your printer's access code from the display menu.

**Default settings aren't great.** The generic profiles are starting points. After your first test print, you'll want to tune temperature and retraction for your specific filament. Our [Cura settings guide for PLA](/blog/best-cura-settings-pla/) covers the general approach. The same principles apply in OrcaSlicer.

## Frequently Asked Questions

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Is OrcaSlicer free?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. OrcaSlicer is completely free and open source. You can download it from GitHub. There are no paid features or premium tiers."
      }
    },
    {
      "@type": "Question",
      "name": "Can I use OrcaSlicer with a non-Bambu Lab printer?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. OrcaSlicer supports most popular 3D printers including Creality, Anycubic, Voron, and many others. It started as a Bambu Lab tool but has expanded to support a wide range of printers."
      }
    },
    {
      "@type": "Question",
      "name": "Is OrcaSlicer better than BambuStudio?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "For most users, yes. OrcaSlicer has all the features of BambuStudio plus calibration tools, more printer support, and more frequent updates. It's a fork of BambuStudio with additional features added by the community."
      }
    }
  ]
}
</script>

### Is OrcaSlicer free?

Yes. OrcaSlicer is completely free and open source. You can download it from GitHub. There are no paid features or premium tiers.

### Can I use OrcaSlicer with a non-Bambu Lab printer?

Yes. OrcaSlicer supports most popular 3D printers including Creality, Anycubic, Voron, and many others. It started as a Bambu Lab tool but has expanded to support a wide range of printers.

### Is OrcaSlicer better than BambuStudio?

For most users, yes. OrcaSlicer has all the features of BambuStudio plus calibration tools, more printer support, and more frequent updates. It's a fork of BambuStudio with additional features added by the community.
