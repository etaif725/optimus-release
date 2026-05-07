<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://optimusoc.vercel.app/logo.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://optimusoc.vercel.app/logo.svg">
  <img alt="Optimus" src="https://optimusoc.vercel.app/logo.svg" width="420">
</picture>

AI-powered PC optimization assistant for overclocking, undervolting, and performance tuning. No guesswork, no risk — just intelligent recommendations tailored to your exact hardware.

---

## Overview

Optimus is a desktop application that bridges the gap between complex PC optimization and everyday users. By combining real-time hardware detection, live sensor monitoring, and AI-powered analysis, Optimus delivers personalized overclocking and undervolting recommendations that are safe, effective, and tailored to your specific system.

**No more forum-diving. No more trial and error. Just smart optimization.**

---

## Vision

PC optimization has always been gatekept by complexity. Overclocking guides assume you already know what you're doing. Undervolting tutorials vary wildly based on silicon lottery. And one wrong setting can crash your system — or worse.

Optimus changes that. We believe everyone deserves to get the most out of their hardware, whether you're a first-time builder or a seasoned enthusiast. Our AI agent understands your exact CPU, GPU, cooling solution, and current thermals, then generates recommendations that actually make sense for *your* system.

---

## Key Features

| Feature | Description |
|---------|-------------|
| **Hardware Detection** | Automatic detection of CPU, GPU, RAM, storage, and cooling configuration |
| **Real-Time Monitoring** | Push-based live sensor data with persistent daemon — instant readings, no polling delays |
| **AI Analysis** | Claude-powered recommendations with tiered prompts for optimal cost and speed |
| **Platform Integrations** | Direct SDK access: Ryzen Master (AMD), XTU/MSR (Intel), NVAPI (NVIDIA), ADL/ADLX (Radeon) |
| **OC Verification** | Stock vs effective fingerprinting — know if your settings are actually applied |
| **Benchmark Comparison** | Compare against Geekbench/GPU Ark databases with your personal result tracking |
| **OC Tools** | Benchmark launcher, results import, and performance tracking |
| **Scan Local** | Auto-detect Cinebench, HWiNFO, 3DMark, and other benchmark results |
| **Overclock Profiles** | Create, edit, delete, and manage profiles with inline value editing |
| **PDF Reports** | Generate professional downloadable reports of your optimization settings |
| **OC Agent Chat** | Interactive AI with Eco/Concise/Detailed modes and beautiful JSON rendering |
| **Glossary** | Comprehensive reference guide for overclocking terminology |
| **SMUI Theme** | Terminal-aesthetic UI with beautified markdown, styled lists, and gradient accents |

---

## How It Works

### 1. Hardware Detection

On first launch, Optimus scans your system to identify:

- **Processor** — Model, architecture, core count, base/boost clocks
- **Graphics Card** — Model, VRAM, driver version
- **Memory** — Capacity, speed, configuration (dual-channel, etc.)
- **Storage** — Drives and their types (NVMe, SSD, HDD)
- **Cooling** — Your cooler type and class (air, AIO, custom loop)

This information forms the foundation for all AI recommendations.

### 2. System Monitoring

The **Monitor** dashboard displays real-time sensor data powered by a persistent sensor daemon:

- CPU temperature, per-core clocks, and utilization
- GPU temperature, hotspot, memory temps, and power draw
- AMD-specific: PPT, TDC, EDC limits and current values
- Intel-specific: PL1, PL2, per-core ratios
- Memory usage and configuration (channels, XMP/EXPO state)

Data streams in real-time via push events — instant readings with no polling delays.

### 3. AI-Powered Analysis

Click **Analyze** to run a comprehensive optimization analysis. The AI agent receives:

- Your complete hardware configuration
- Current sensor readings at time of analysis
- Your cooling solution capabilities
- System context (desktop vs laptop, use case)

Within seconds, you receive:

- **CPU Recommendations** — PBO settings, Curve Optimizer values, power limits
- **GPU Recommendations** — Undervolt curves, power targets, fan profiles
- **Memory Recommendations** — XMP/EXPO profiles, timing suggestions
- **Validation Steps** — How to test stability and verify your settings

### 4. Profile Management

Every analysis is automatically saved as an **Overclock Profile** with:

- Custom title (editable) and timestamp
- Complete hardware snapshot
- All AI recommendations with inline editing
- Applied/pending status with verification
- One-click PDF export

#### Profile Features
- **Create Manual Reports** — Build profiles from scratch with guided template
- **Inline Editing** — Modify CPU, GPU, and RAM values directly (no dialogs)
- **Platform-Aware Inputs** — Dropdowns show AMD or Intel-specific options
- **Dynamic Core Count** — Curve Optimizer shows correct inputs for your CPU
- **Verification** — See if your marked "Applied" settings match live hardware

Access saved profiles in **Settings > Overclocks** to review, edit, compare, or regenerate reports.

### 5. OC Tools & Benchmarking

The **OC Tools** page provides comprehensive benchmark management:

#### Benchmark Launcher
- Detects installed benchmark utilities (Cinebench, Prime95, FurMark, 3DMark, etc.)
- One-click launch for any detected benchmark
- **Custom Paths** — Manually select executable files for non-standard installations
- Download links for tools you don't have installed
- Filter by type: CPU, GPU, Memory, Storage, System

#### Import Results
- **Scan Local** — Automatically finds benchmark results in common Windows locations
- **Duplicate Detection** — Content-based fingerprinting prevents re-importing identical results
- Drag-and-drop file import for manual uploads
- Supported formats:
  - **Cinebench** — R23/2024 ranking files from cb_ranking folder
  - **HWiNFO** — CSV sensor logs
  - **3DMark** — XML result files
  - **AIDA64** — CSV benchmark exports
  - **Geekbench** — JSON exports
- Manual score entry for benchmarks without export support

#### Performance History
- Interactive timeline charts showing score trends over time
- Side-by-side benchmark comparisons
- HWiNFO sensor visualization with temperature and power graphs
- Export all benchmark data for backup or sharing

### 6. Interactive Chat

The **OC Agent** isn't just for analysis — it's a knowledgeable assistant. Ask questions like:

- "What is Curve Optimizer and how do I use it?"
- "Is my CPU temperature too high?"
- "Explain GPU voltage curves"
- "What's a safe undervolt for my RTX 4070?"

Load a saved profile into the chat context for follow-up questions about specific recommendations.

#### Response Modes
- **Concise** — Quick, focused answers (~5-15 sec)
- **Detailed** — Thorough explanations with examples (~30-60 sec)
- **Eco** — Ultra-efficient mode, ~90% cheaper for simple questions

#### Beautified Output
AI responses render with styled formatting:
- V/F curves and fan curves displayed as visual cards
- Memory timings and BIOS settings in formatted tables
- Clear section headers with visual dividers
- Numbered steps with gradient badges

---

## Application Pages

| Page | Purpose |
|------|---------|
| **Monitor** | Real-time hardware monitoring dashboard with live sensor data |
| **OC Agent** | AI chat interface for analysis and optimization questions |
| **OC Tools** | Benchmark launcher, results import, and performance history |
| **Glossary** | Searchable reference guide for PC optimization terminology |
| **Settings** | Hardware configuration, API setup, saved profiles, preferences |

---

## Settings Sections

| Section | Description |
|---------|-------------|
| **Hardware** | View and edit detected hardware configuration, re-run detection |
| **API Key** | Configure your Anthropic API key for AI features |
| **Overclocks** | Create, edit, delete profiles — inline value editing, custom titles, PDF export |
| **Catalogs** | Update hardware reference databases |
| **Preferences** | App behavior settings (units, response style, streaming, notifications) |
| **Data** | Export/import configuration, benchmark data, reset options |
| **About** | Version info and application details |

---

## Understanding AI Recommendations

Optimus's recommendations are categorized by component and risk level:

### CPU Optimization

| Setting | What It Does |
|---------|--------------|
| **PBO (Precision Boost Overdrive)** | AMD's automatic overclocking — safely pushes beyond stock limits |
| **Curve Optimizer** | Per-core voltage offsets — reduces heat while maintaining performance |
| **Power Limits (PPT/TDC/EDC)** | Maximum power and current delivery based on cooling capacity |

### GPU Optimization

| Setting | What It Does |
|---------|--------------|
| **Undervolt Curve** | Lower voltage at same frequency — dramatically reduces heat and power |
| **Power Limit** | Maximum GPU power draw — balance between performance and thermals |
| **Fan Curve** | Custom fan speeds at temperature thresholds |

### Memory Optimization

| Setting | What It Does |
|---------|--------------|
| **XMP/EXPO** | Enable manufacturer-rated memory speeds |
| **FCLK (Infinity Fabric)** | AMD memory controller clock — should match RAM speed |
| **Timing Adjustments** | Fine-tune memory latency for performance gains |

---

## Safety Philosophy

Optimus prioritizes safety above all else:

1. **Conservative Defaults** — Recommendations start safe and can be pushed further
2. **Cooling-Aware** — Settings scale based on your actual cooling capacity
3. **Validation Steps** — Every recommendation includes stability testing instructions
4. **Clear Warnings** — Potentially risky settings are flagged with explanations
5. **Reversible Changes** — All recommendations can be undone in BIOS/software

**Optimus never makes changes to your system automatically.** All recommendations are informational — you apply them manually through BIOS or manufacturer tools.

---

## Glossary Highlights

Optimus includes a comprehensive glossary covering:

| Category | Example Terms |
|----------|---------------|
| **CPU - AMD** | PBO, Curve Optimizer, PPT, TDC, EDC |
| **CPU - Intel** | LLC, Ring Ratio, Vcore |
| **Memory** | XMP/EXPO, FCLK, CAS Latency, Dual Rank |
| **GPU** | Voltage Curve, Power Limit, GDDR6X, Resizable BAR |
| **General** | Undervolting, Overclocking, TDP, Thermal Throttling |
| **Testing** | Stress Test, Stability Validation |

Each term includes:
- Clear definition
- Practical examples
- Safe operating ranges
- Warnings where applicable

---

## Roadmap

| Status | Feature |
|--------|---------|
| ✅ | Hardware detection and monitoring |
| ✅ | AI-powered optimization analysis |
| ✅ | Profile management and PDF export |
| ✅ | Interactive OC Agent chat |
| ✅ | Comprehensive glossary |
| ✅ | Benchmark integration with OC Tools |
| ✅ | Auto-scan local benchmark results |
| ✅ | Real-time push-based sensor daemon |
| ✅ | Platform SDK integrations (Ryzen Master, XTU, NVAPI, ADL) |
| ✅ | OC verification with stock vs effective fingerprinting |
| ✅ | Editable overclock profiles with inline editing |
| ✅ | Token-optimized AI with tiered prompts and caching |
| ✅ | Beautified chat UI with styled markdown rendering |
| 🔄 | Community profile sharing (planned) |
| 🔄 | Multi-language support (planned) |

---

## Support

For issues, feature requests, or questions:

- **GitHub Issues** — Bug reports and feature requests
- **Discussions** — Community Q&A and optimization tips

---

## License

This project is licensed under the MIT License — see the [LICENSE.txt](LICENSE.txt) file for details.

---

## Disclaimer

Optimus provides recommendations based on AI analysis of your hardware configuration. While we prioritize safety, overclocking and undervolting carry inherent risks including system instability, data loss, and potential hardware damage. Always:

- Back up important data before making changes
- Follow validation steps to test stability
- Monitor temperatures during stress testing
- Understand that silicon lottery affects results

**You are solely responsible for any changes made to your system based on Optimus's recommendations.**

---

<p align="center">
  <strong>Optimus</strong> — PC optimization, simplified.
</p>
