# EVOLUTION.md — Phosphor Text Style Changer

The decisions, pivots, and deeper lessons from building a CSS color system grounded in display physics.

---

## Origin: Thinking at the Hardware Level

Most people who want dark mode install a dark mode extension. The instinct is "make it dark." That's a cosmetic solution to a physical problem.

This project started from a different question: **why does this screen hurt?**

The answer isn't "it's too bright." The answer is that LCD backlights emit predominantly blue-spectrum light, and white backgrounds maximize that emission directly into the viewer's eyes. The problem is spectral, not just luminance.

Once you see it that way, the solution isn't "make it dark" — it's "shift the spectral output to something the human eye handles better during extended exposure."

Green sits in the middle of the visible spectrum where the eye is most sensitive and least strained. But not any green — the right green, compensated for the hardware it's displayed on.

This is the difference between surface-level problem-solving and systems thinking. The extension works because it addresses the actual physics, not just the symptom.

---

## The Iteration Pattern: Debug by Feeling

Fifteen CSS versions in one session. Each one tested on a live workstation during an actual shift. No test suite, no automated checks — just eyes on screen, feeling the difference.

This sounds chaotic but it's actually a valid methodology for perceptual design. Color correction can't be fully evaluated in a code editor. It has to be felt on the target hardware, in the target environment, under the target lighting conditions.

**What this taught:**

1. **The universal selector is a conversation with the entire DOM.** `*` doesn't just mean "everything" — it means "every element's specificity battle, every inherited property, every layout assumption." Understanding what breaks when you use it teaches more about CSS architecture than any tutorial.

2. **Text-shadow is density-dependent.** The same glow that looks beautiful on a heading becomes unreadable noise on a paragraph. Real CRT phosphors weren't uniform either — the glow varied with electron beam focus. The CSS needed to reflect actual phosphor physics, not idealized uniformity.

3. **Hover states reveal reachability.** When hover worked but default states didn't, it proved the CSS rules could reach those elements. The specificity was the issue, not the targeting. That diagnostic pattern — testing interaction states to verify selector reach — transfers to any CSS debugging context.

---

## Two Greens, Two Cognitive States

The dual variant system wasn't planned. It emerged from understanding that "green" isn't one thing:

**Electric Green (`#00ff00`):** Pure digital phosphor. High contrast against black. Activating. Good for short bursts of focused attention. This is the green that says "pay attention now."

**Phthalo Green (`#3a7a4d`):** Organic, desaturated, earth-toned. Low visual aggression. Sustainable for 8+ hours. This is the green that says "you can stay here."

**The insight:** color affects cognitive state, and cognitive state should match the task. A theme system isn't just aesthetics — it's ergonomic tooling for the brain.

This connects to broader work on understanding how nutrition, environment, and sensory input affect cognitive performance. The extension is one data point in a larger pattern of optimizing the input layer to get better output from the processor.

---

## The Accidental Brand Alignment

Phthalo green's palette landed close to Whole Foods' brand colors. This was unintentional but instructive: organic, earth-toned greens are used by brands that want to signal "natural" and "trustworthy" because those associations are baked into human color perception.

The same perceptual properties that make Phthalo green easy on the eyes during long sessions are why brands use similar palettes to feel approachable.

Color psychology and display ergonomics share the same root: how the human visual system responds to spectral input.

---

## Scope Discipline: Why This Stayed Separate

This extension was originally considered as a feature addition to the Claude Wide Chat Extender. The decision to keep it separate came from the same principle established during that build: **one tool, one problem.**

Width extension solves readability geometry. Color theming solves spectral eye strain. They operate on different layers of the user experience. Combining them would create a Swiss Army knife when the user needs a scalpel.

The separation also created a better portfolio signal: two published extensions show breadth and consistency, not just one extension with feature creep.

---

## What This Project Reveals About the Developer

Most first-time CSS projects are "make it look different." This one started from:

- Understanding LCD backlight physics
- Designing for real hardware constraints (non-OLED company monitors)
- Iterating through failure states (15 versions) without abandoning the approach
- Recognizing that color perception is contextual (ambient light, display technology, session duration)
- Splitting the solution into task-appropriate variants based on cognitive state theory

That's not a CSS project. That's a systems engineering approach applied to a visual design problem. The CSS is just the implementation layer.

---

## Connected Projects

- [Claude Wide Chat](https://github.com/Peterc3-dev/claude-wide-chat) — The companion extension. Width + color = complete Claude.ai ergonomic optimization.
- [Learning Forge](https://github.com/Peterc3-dev/learning-forge) — Chrome extension architecture patterns documented in `/web-dev/chrome-extensions/`

---

*This document captures the evolution of thinking. For the build dialogue, see [CONVERSATION.md](CONVERSATION.md). For installation and technical details, see [README.md](../README.md).*