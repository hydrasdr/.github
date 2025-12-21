# HydraSDR

Welcome to the official HydraSDR GitHub organization — a high-performance, open-source Software Defined Radio (SDR) platform.

The first product in the lineup is the **HydraSDR RFOne**, a powerful SDR receiver offering 10 MHz instantaneous bandwidth and wide frequency coverage from 24 MHz to 1.8 GHz.

- **Website**: [https://hydrasdr.com](https://hydrasdr.com)
- **RFOne Specs**: [https://hydrasdr.com/hydrasdr-rfone](https://hydrasdr.com/hydrasdr-rfone)
- **Purchase on DigiKey**: [HydraSDR RFOne - Under $190](https://www.digikey.com/en/products/detail/benjamin-vernoux/hydrasdr-rfone/26256067)
- **Support & Discussion**: Use GitHub Issues across repositories
- **Creator**: Benjamin VERNOUX

---

## Overview

HydraSDR RFOne is a professional-grade SDR receiver, designed in France and manufactured in the USA. It features a completely open-source stack, including firmware, host tools, and application integrations.

### Key Features

| Feature | Description |
|--------|-------------|
| Frequency Range | 24 MHz to 1.8 GHz continuous |
| Bandwidth | 10 MHz instantaneous (9 MHz alias/image-free) |
| ADC | 12-bit @ 20 MSPS |
| Dynamic Range | Up to 80 dB (64 dB SNR, 10.4 ENOB) |
| Tuner | Rafael Micro R828D |
| Microcontroller | NXP LPC4370 (Cortex-M4F + 2× M0, 204 MHz) |
| Interface | USB-C (USB 2.0) |
| Antenna | SMA female connector |
| Enclosure | 7075 aluminum, black anodized |
| Noise Figure | ~3.5 dB (42–1002 MHz typical) |
| IIP3 | Up to +35 dBm |
| Expansion | 2× U.FL (reserved), 18-pin GPIO header |
| Clock Outputs | 2× configurable up to 160 MHz |
| Multi-Unit Sync | Supports up to 3 boards in single enclosure |

---

## Architecture

- Open-source firmware and tools
- Cross-platform host tools, shared libraries, and DLLs for Windows,GNU Linux,macOS integration
- High-quality RF front-end and low-noise design
- Compact, robust, modular hardware
- USB-powered with filtering via included ferrite choke cable

---

## Software Support

HydraSDR RFOne is compatible with major open-source SDR applications.

### Primary Applications

- **[SDR++ fork](https://github.com/hydrasdr/SDRPlusPlus)** – HydraSDR fork of the popular cross-platform SDR++ application, featuring native RFOne supportd.
  - Official SDR++ now support HydraSDR RFOne in nightly (Since 5 Sept 2025) see https://github.com/AlexandreRouma/SDRPlusPlus/releases/tag/nightly
- **[RFAnalyzer](https://github.com/demantz/RFAnalyzer)** – RF Analyzer is an Android app for real-time spectrum analysis using SDR hardware. It displays live FFT and waterfall plots of the radio frequency (RF) spectrum and supports demodulation, recording, and more, support HydraSDR RFOne (Since 6 Oct 2025)
- **[GNU Radio gr-osmosdr fork](https://github.com/hydrasdr/gr-osmosdr)** – Native HydraSDR RFOne support via the gr-osmosdr source block, enabling integration with GNU Radio Companion (GRC) for creating advanced DSP flowgraphs, prototyping demodulators, and conducting RF experiments in a visual programming environment.
   - **[GNURadio companion graph files](https://github.com/wb2ifs/HydraSDR-graphs)** - GNURadio companion graph files for the HydraSDR RFOne receiver. They are based on the demonstration FM receiver in this tutorial.
- **[SoapyHydraSDR](https://github.com/hydrasdr/SoapyHydraSDR)** – SoapySDR hardware support module for RFOne, enabling integration with GQRX, CubicSDR, and any Soapy-compatible SDR application across Windows, Linux, and macOS

- **[rfone_host](https://github.com/hydrasdr/rfone_host)** – HydraSDR RFOne host tools, shared libraries, and DLLs for Windows/Linux/macOS integration, with comprehensive build instructions for Visual Studio 2019, CMake, and cross-platform development
- **[rfone_fw](https://github.com/hydrasdr/rfone_fw)** - HydraSDR RFOne Open-source firmware

### Specialized Tools

- **[kalibrate-hydrasdr](https://github.com/hydrasdr/kalibrate-hydrasdr)** - Kalibrate-HydraSDR - GSM-based frequency calibration tool for HydraSDR RFOne. Scans GSM base stations to measure and correct the internal TCXO frequency offset with precision PPM/PPB measurements.
- **[SatDump fork](https://github.com/hydrasdr/SatDump)** – Satellite decoding (nightly builds supported)
- **[URH fork](https://github.com/hydrasdr/urh)** – Universal Radio Hacker with HydraSDR RFOne support
- **[LuaRadio fork](https://github.com/hydrasdr/luaradio)** – LuaRadio framework fork with HydraSDR RFOne support
- **[nfc-laboratory](https://github.com/josevcm/nfc-laboratory)** - NFC signal sniffer and protocol decoder using SDR receiver for demodulation and decoding NFC-A, NFC-B, NFC-F and NFC-V signals in real-time up to 424 Kbps. ([nfc-laboratory v3.3.0](https://github.com/josevcm/nfc-laboratory/releases/tag/3.3.0) or more supports HydraSDR RFOne)
- **[ka9q-radio](https://github.com/ka9q/ka9q-radio)** - Multichannel SDR based on fast convolution and IP multicasting with HydraSDR RFOne support
- **[AIS-catcher fork](https://github.com/hydrasdr/AIS-catcher)** - AIS-catcher: A multi-platform AIS Receiver fork with native HydraSDR RFOne support
- **[GNSS-SDRLIB-PVT](https://github.com/AgileEngineeringLLC/GNSS-SDRLIB-PVT_WBS_121625)** - This is a significantly-modifed version of GNSS-SDRLIB. Instead of requiring a TCP link to RTKLIB for positioning, it has its own least squares solver built-in with native HydraSDR RFOne support
- **[SDRTrunk fork](https://github.com/hydrasdr/sdrtrunk)** - A cross-platform java application for decoding, monitoring, recording and streaming trunked mobile and related radio protocols using Software Defined Radios (SDR) native HydraSDR RFOne SDR support
- **[SatNOGS](https://satnogs.org)** - SatNOGS Client 2.1 docker container updated with gr-satellites 5.8 and HydraSDR RFOne SDR support
- **[GNSS-SDR](https://github.com/gnss-sdr/gnss-sdr)** - Open-source GNSS receiver for GPS/Galileo/GLONASS

### Docker Multi-Platform RF Toolbox / SDR
- **[PentHertz RF-Swift](https://github.com/PentHertz/RF-Swift)** - A comprehensive Docker-based RF toolbox that enables rapid deployment of specialized radio frequency tools across multiple platforms and architectures. Supports Linux, Windows, and macOS on x86_64, ARM64 (Raspberry Pi, Apple Silicon), and RISC-V systems. Features containerized deployment that installs in seconds without modifying your host operating system.
  - **Variants**: `sdr_light` and `sdr_full` configurations available
  - **Hardware Support**: Compatible with HydraSDR RFOne
  - **Documentation**: Complete setup guide at [rfswift.io/docs/getting-started](https://rfswift.io/docs/getting-started)

### GNU/Linux SDR Distribution
- **[DragonOS](https://sourceforge.net/projects/dragonos-focal/files/)** - A ready-to-use Lubuntu-based Linux distribution specifically designed for software-defined radio enthusiasts and professionals. Provides an out-of-the-box SDR environment with pre-configured tools and drivers for immediate use.
  - **Available Version with HydraSDR RFOne support**: DragonOS Noble (24.04 LTS)
  - **Architecture**: x86_64 support
  - **Hardware Support**: HydraSDR RFOne compatibility (DragonOS Noble R5 and later)
  - **Latest Release**: DragonOS Noble R5 (July 3, 2025)

---
## Quick Start

### Requirements

* **Operating System:**
  * Windows 8.1 or later
  * GNU/Linux (Ubuntu 20.04+, Debian 11+)
  * macOS 10.14+
  * Android 9+ with OpenGL 2.1+
* **USB Port:** USB 2.0 or higher
* **Antenna:** SMA-compatible **male** connector

---

### Setup for Windows, GNU/Linux, macOS and Android

1. **Connect the device**
   Connect the HydraSDR RFOne to your computer using the **USB-C to USB-A cable included with the HydraSDR RFOne**.

   > For Android, connect via an **OTG adapter** that supports **USB 2.0 High Speed** and provides **power**.

2. **Attach the antenna**
   Connect your antenna to the **ANT** port.

   > The port uses an SMA female connector; your antenna must have an SMA male connector.

3. **Install SDR++**
   
   Download the [HydraSDR SDR++ fork](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly) for your operating system and install it.

4. **Launch and configure**
   
   Open SDR++, select **HydraSDR RFOne** as the device, then set your desired sample rate and gain

   > **Tip:** A gain setting of **Linear 12** is a good starting point.
---

## Real-World Reviews

### 🎥 Video Reviews

- **[Radio Bunker YouTube 26 Oct, 2025](https://www.youtube.com/watch?v=5HKlgXaHoF8)** -  HydraSDR RFOne: THE NEW HIGH-PERFORMANCE SDR RECEIVER
  - In this review, we take an in-depth look at one of the most advanced SDR receivers available today.
  - Precision, sensitivity, and a design designed for radio amateurs who demand maximum reception performance.
  - We analyze its signal quality, processing power, and all the features that make it a true technological gem.
  - From its interface to its field performance, the HydraSDR RFOne demonstrates why it's generating so much buzz in the SDR community.
- **[Penthertz YouTube Aug 14, 2025](https://www.youtube.com/watch?v=y5QCNphhGP4)** - HydraSDR RFOne: Setup & Testing using RF Swift (SDR++, URH, GNU Radio, OsmoSDR, LuaRadio)
- **[Ham Radio DX YouTube Aug 4, 2025](https://www.youtube.com/watch?v=8GZ7tcCjORQ)** - HydraSDR RFOne – Is This the Future of SDR's? With a Software Defined Radio (SDR), you can see the entire radio spectrum — and the HydraSDR RFone takes that to the next level. This brand-new SDR stands out with fully open-source firmware, applications, and host tools,  offering a level of flexibility that most proprietary radios can’t match.
- **[Tech Minds YouTube July 23, 2025](https://www.youtube.com/watch?v=UvMIeRP8L4s)** - HydraSDR RFOne - A New High Performance Software Defined Radio - Made in the USA! Comprehensive hands-on review covering specifications, unboxing, enclosure disassembly, PCB examination, firmware updating, and real-world testing with SDR++ software.
- **[Geerling Engineering YouTube June 28, 2025](https://www.youtube.com/watch?v=tXIPQK28aJY)** - SDR is an incredible tool for understanding radio (featuring HydraSDR RFOne) - Comprehensive 21-minute exploration of Software Defined Radio technology, featuring hands-on demonstrations with multiple SDR devices (RTL-SDR v3/v4, HackRF One, HydraSDR RFOne) Covers FM band analysis, signal spurs, antenna impact, digital carrier decoding, gain optimization, 900 MHz Meshtastic signals, and practical SDR selection guidance for RF engineers and enthusiasts.

### 📝 Articles

- **[Zero Retries 0209 Article July 4, 2025](https://www.zeroretries.org/p/zero-retries-0209?open=true#%C2%A7hydrasdr-rfone-new-software-defined-receiver)**
This July 2025 article discusses the HydraSDR RFOne in the context of amateur radio, praising its 24-1800 MHz coverage (ideal for VHF/UHF bands including 10m at 28 MHz without transverters), 10 MHz sampling, metal enclosure (fits up to three boards for phase-coherent radar/scanning), and included USB-C cable with toroid filters for noise reduction. It's open-source with support for SDR++, SatDump, GNU Radio, GQRX, URH, and LuaRadio via GitHub. Priced at $190, it's positioned as affordable for its class.
Positive/Enthusiastic Quotes and Feedback:"Another reasonable cost, reasonable performance software-defined receiver option manufactured in the US."
"Ultra-extensible... capable of containing up to three boards for unique ultra-compact phase-coherent receivers."
"Qualified for use with the open-source, cross-platform SDR++ application, enhancing its usability."

- **[RTL-SDR Blog - Comprehensive Review July 2, 2025](https://www.rtl-sdr.com/rtl-sdr-blog-review-of-the-hydrasdr)** - Comparison review between HydraSDR and Airspy R2, covering design similarities, performance testing, shielding analysis, software compatibility, and practical usage scenarios. Independent testing found excellent RF shielding and cleaner spectrum with lower internal spurs compared to the Airspy R2.

---

## 📁 Repository Structure

This organization consists of several repositories:

| Repository | Description |
|-----------|-------------|
| [rfone_host](https://github.com/hydrasdr/rfone_host) | Host tools, shared libraries, drivers |
| [rfone_fw](https://github.com/hydrasdr/rfone_fw) | Open-source firmware |
| [SDRPlusPlus fork](https://github.com/hydrasdr/SDRPlusPlus) | SDR++ fork with RFOne support |
| [SoapyHydraSDR](https://github.com/hydrasdr/SoapyHydraSDR) | SoapySDR plugin |
| [gr-osmosdr fork](https://github.com/hydrasdr/gr-osmosdr) | GNU Radio block |
| [SatDump fork](https://github.com/hydrasdr/SatDump) | Satellite decoding |
| [urh fork](https://github.com/hydrasdr/urh) | Universal Radio Hacker fork |
| [luaradio fork](https://github.com/hydrasdr/luaradio) | LuaRadio fork for embedded DSP |

---

## 🛠️ Contributing & Development

HydraSDR is an open platform. We welcome contributions, patches, documentation improvements, and feedback.

- Use GitHub Issues for bug reports, questions, and feature requests
- See each repo for contribution guidelines
- Code is cross-platform and CMake-friendly
- Firmware built with GCC-based toolchains

---

## 📦 Availability

- **In Stock**: [HydraSDR RFOne DigiKey Product Page](https://www.digikey.com/en/products/detail/benjamin-vernoux/hydrasdr-rfone/26256067)
- **Price**: Under $190 USD
- **Shipping**: Global

---

## 📚 Resources

- 📄 Datasheet: Comprehensive specs and details for HydraSDR RFOne [https://hydrasdr.com/hydrasdr-rfone](https://hydrasdr.com/hydrasdr-rfone)
- 🧰 SDK & Tools: Software development kits, utilities, and official tools [https://github.com/hydrasdr](https://github.com/hydrasdr)
- 🧠 Community & Support: 
  - General discussions: [hydrasdr/discussions](https://github.com/orgs/hydrasdr/discussions)
  - Report issues or feature requests in specific repositories:
    - [rfone_host issues](https://github.com/hydrasdr/rfone_host/issues)
    - [rfone_fw issues](https://github.com/hydrasdr/rfone_fw/issues)
    - [SDRPlusPlus fork issues](https://github.com/hydrasdr/SDRPlusPlus/issues)
    - …and more on the HydraSDR GitHub

---

HydraSDR — Open-source radio done right.
