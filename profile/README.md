# HydraSDR

**High-performance, open-source Software Defined Radio platform.**

The first product in the lineup is the **HydraSDR RFOne** — a professional-grade SDR receiver offering 10 MHz instantaneous bandwidth and continuous frequency coverage from 24 MHz to 1.8 GHz. Designed in France, manufactured in the USA.

[![Website](https://img.shields.io/badge/Website-hydrasdr.com-blue)](https://hydrasdr.com)
[![DigiKey](https://img.shields.io/badge/Buy-DigiKey_%3C%24190-green)](https://www.digikey.com/en/products/detail/benjamin-vernoux/hydrasdr-rfone/26256067)
[![Specs](https://img.shields.io/badge/Specs-RFOne-orange)](https://hydrasdr.com/hydrasdr-rfone)
[![Discussions](https://img.shields.io/badge/Community-Discussions-purple)](https://github.com/orgs/hydrasdr/discussions)

---

## Specifications

| Parameter | Value |
|:--|:--|
| **Frequency Range** | 24 MHz – 1.8 GHz continuous |
| **Bandwidth** | 10 MHz instantaneous (9 MHz alias/image-free) |
| **ADC** | 12-bit @ 20 MSPS |
| **Dynamic Range** | Up to 80 dB (64 dB SNR, 10.4 ENOB) |
| **Noise Figure** | ~3.5 dB (42–1002 MHz typical) |
| **IIP3** | Up to +35 dBm |
| **Tuner** | Rafael Micro R828D |
| **MCU** | NXP LPC4370 (Cortex-M4F + 2× M0, 204 MHz) |
| **Interface** | USB-C (USB 2.0) |
| **Antenna** | SMA female connector |
| **Enclosure** | 7075 aluminum, black anodized |
| **Expansion** | 2× U.FL (reserved), 18-pin GPIO header |
| **Clock Outputs** | 2× configurable up to 160 MHz |
| **Multi-Unit Sync** | Up to 3 boards in a single enclosure |

---

## Architecture

- Fully open-source firmware, host tools, shared libraries, and DLLs
- Cross-platform support: Windows, GNU/Linux, macOS, Android
- High-quality RF front-end with low-noise design
- Compact, robust, modular hardware in a CNC-machined aluminum enclosure
- USB-powered with filtering via included ferrite choke cable

---

## Core Repositories

| Repository | Description |
|:--|:--|
| **[hydrasdr-host](https://github.com/hydrasdr/hydrasdr-host)** | Host tools, shared libraries, and DLLs for Windows/Linux/macOS — includes build instructions for Visual Studio 2019, CMake, and cross-platform development |
| **[rfone_fw](https://github.com/hydrasdr/rfone_fw)** | Open-source firmware for HydraSDR RFOne |

---

## Software Ecosystem

### SDR Applications

| Application | Description |
|:--|:--|
| **[SDR++ fork](https://github.com/hydrasdr/SDRPlusPlus)** ([nightly](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly)) | HydraSDR fork of the popular cross-platform SDR++ application with native RFOne support. Also supported in [official SDR++ nightly](https://github.com/AlexandreRouma/SDRPlusPlus/releases/tag/nightly) since Sept 5, 2025 |
| **[RFAnalyzer](https://github.com/demantz/RFAnalyzer)** | Android app for real-time spectrum analysis — live FFT, waterfall, demodulation, and recording. HydraSDR RFOne support since Oct 6, 2025 |
| **[GNU Radio gr-osmosdr fork](https://github.com/hydrasdr/gr-osmosdr)** | Native RFOne support via the gr-osmosdr source block for GNU Radio Companion (GRC) flowgraphs. See also: [HydraSDR GRC graph files](https://github.com/wb2ifs/HydraSDR-graphs) |
| **[SoapyHydraSDR](https://github.com/hydrasdr/SoapyHydraSDR)** | SoapySDR module for RFOne — enables integration with GQRX, CubicSDR, and any Soapy-compatible application |

### Specialized Tools

| Tool | Description |
|:--|:--|
| **[hydrasdr_433](https://github.com/hydrasdr/hydrasdr_433)** ([nightly](https://github.com/hydrasdr/hydrasdr_433/releases/tag/nightly)) | Wideband ISM data receiver based on [rtl_433](https://github.com/merbanan/rtl_433/). Decodes 290+ protocols on 433.92/868/315/345/915 MHz ISM bands. Features native CF32 pipeline, polyphase filter bank channelizer, wideband scanning, runtime SIMD dispatch (SSE2/AVX2/AVX-512/NEON/SVE), and cross-channel deduplication |
| **[kalibrate-hydrasdr](https://github.com/hydrasdr/kalibrate-hydrasdr)** | GSM-based frequency calibration — scans GSM base stations to measure and correct TCXO frequency offset with PPM/PPB precision |
| **[SatDump fork](https://github.com/hydrasdr/SatDump)** | Satellite signal decoding with nightly build support |
| **[URH fork](https://github.com/hydrasdr/urh)** | Universal Radio Hacker — wireless protocol investigation with native RFOne support |
| **[LuaRadio fork](https://github.com/hydrasdr/luaradio)** | Lightweight, embeddable SDR framework with RFOne support |
| **[AIS-catcher fork](https://github.com/hydrasdr/AIS-catcher)** ([nightly](https://github.com/hydrasdr/AIS-catcher/releases/tag/Edge)) | Multi-platform AIS receiver with native RFOne support |
| **[SDRTrunk fork](https://github.com/hydrasdr/sdrtrunk)** ([nightly](https://github.com/hydrasdr/sdrtrunk/releases/tag/nightly)) | Cross-platform trunked radio decoder/monitor/recorder with native (JNI) HydraSDR support |
| **[ka9q-radio](https://github.com/ka9q/ka9q-radio)** | Multichannel SDR based on fast convolution and IP multicasting |
| **[nfc-laboratory](https://github.com/josevcm/nfc-laboratory)** | NFC signal sniffer and protocol decoder — NFC-A/B/F/V up to 424 Kbps in real-time (v3.3.0+) |
| **[GNSS-SDRLIB-PVT](https://github.com/AgileEngineeringLLC/GNSS-SDRLIB-PVT_WBS_121625)** | GNSS receiver with built-in least squares solver and native RFOne support |
| **[GNSS-SDR](https://github.com/gnss-sdr/gnss-sdr)** | Open-source GNSS receiver for GPS/Galileo/GLONASS |
| **[SatNOGS](https://satnogs.org)** | SatNOGS Client 2.1 docker container with gr-satellites 5.8 and RFOne support |

### Platforms & Distributions

| Platform | Description |
|:--|:--|
| **[PentHertz RF-Swift](https://github.com/PentHertz/RF-Swift)** | Docker-based RF toolbox — deploys containerized SDR tools in seconds across x86_64, ARM64, and RISC-V. Available in `sdr_light` and `sdr_full` configurations. [Documentation](https://rfswift.io/docs/getting-started) |
| **[DragonOS](https://sourceforge.net/projects/dragonos-focal/files/)** | Ready-to-use Lubuntu-based Linux distribution for SDR. HydraSDR RFOne supported in Noble R5+ (24.04 LTS) |

---

## Quick Start

### Requirements

| Platform | Minimum Version |
|:--|:--|
| Windows | 8.1 or later |
| GNU/Linux | Ubuntu 20.04+, Debian 11+ |
| macOS | 10.14+ |
| Android | 9+ with OpenGL 2.1+ |

You also need a USB 2.0+ port and an antenna with an **SMA male** connector.

### Setup

1. **Connect** the RFOne to your computer using the included USB-C to USB-A cable.
   > For Android, use an OTG adapter that supports USB 2.0 High Speed and provides power.

2. **Attach your antenna** to the **ANT** port (SMA female on device).

3. **Install SDR++** — download the [HydraSDR SDR++ fork](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly) for your OS.

4. **Launch and configure** — select **HydraSDR RFOne** as the device, set your sample rate and gain.
   > **Tip:** A gain setting of **Linear 12** is a good starting point.

---

## Reviews

### Video Reviews

| Review | Date |
|:--|:--|
| **[Radio Bunker](https://www.youtube.com/watch?v=5HKlgXaHoF8)** — "THE NEW HIGH-PERFORMANCE SDR RECEIVER" — in-depth signal quality, processing power, and field performance analysis | Oct 26, 2025 |
| **[Penthertz](https://www.youtube.com/watch?v=y5QCNphhGP4)** — Setup & testing using RF Swift (SDR++, URH, GNU Radio, OsmoSDR, LuaRadio) | Aug 14, 2025 |
| **[Ham Radio DX](https://www.youtube.com/watch?v=8GZ7tcCjORQ)** — "Is This the Future of SDR's?" — open-source flexibility and full spectrum visibility | Aug 4, 2025 |
| **[Tech Minds](https://www.youtube.com/watch?v=UvMIeRP8L4s)** — Hands-on review covering specs, unboxing, PCB examination, firmware updating, and real-world testing | July 23, 2025 |
| **[Geerling Engineering](https://www.youtube.com/watch?v=tXIPQK28aJY)** — 21-minute SDR exploration featuring RTL-SDR v3/v4, HackRF One, and HydraSDR RFOne comparisons | June 28, 2025 |

### Articles

| Article | Date |
|:--|:--|
| **[Zero Retries 0209](https://www.zeroretries.org/p/zero-retries-0209?open=true#%C2%A7hydrasdr-rfone-new-software-defined-receiver)** — Amateur radio perspective on 24–1800 MHz coverage, multi-board phase-coherent capability, and open-source ecosystem | July 4, 2025 |
| **[RTL-SDR Blog](https://www.rtl-sdr.com/rtl-sdr-blog-review-of-the-hydrasdr)** — Comparison with Airspy R2 covering RF shielding, internal spurs, and performance testing | July 2, 2025 |

---

## Contributing

HydraSDR is an open platform — contributions, patches, documentation improvements, and feedback are welcome.

- Use **GitHub Issues** for bug reports, questions, and feature requests
- Code is cross-platform and CMake-friendly
- Firmware built with GCC-based toolchains
- See each repository for specific contribution guidelines

---

## Availability

| | |
|:--|:--|
| **Status** | In Stock |
| **Price** | Under $190 USD |
| **Shipping** | Worldwide |
| **Order** | [DigiKey Product Page](https://www.digikey.com/en/products/detail/benjamin-vernoux/hydrasdr-rfone/26256067) |

---

## Resources

| Resource | Link |
|:--|:--|
| Datasheet & Specs | [hydrasdr.com/hydrasdr-rfone](https://hydrasdr.com/hydrasdr-rfone) |
| SDK & Tools | [github.com/hydrasdr](https://github.com/hydrasdr) |
| Community Discussions | [hydrasdr/discussions](https://github.com/orgs/hydrasdr/discussions) |
| Host Tools Issues | [hydrasdr-host/issues](https://github.com/hydrasdr/hydrasdr-host/issues) |
| Firmware Issues | [rfone_fw/issues](https://github.com/hydrasdr/rfone_fw/issues) |
| SDR++ Fork Issues | [SDRPlusPlus/issues](https://github.com/hydrasdr/SDRPlusPlus/issues) |

---

**HydraSDR — Open-source radio done right.**
