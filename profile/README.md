# HydraSDR

Welcome to HydraSDR organization main repository - an advanced open-source Software Defined Radio platform.

The first product in the HydraSDR lineup is the **HydraSDR RFOne** receiver with 10MHz instantaneous bandwidth sampling capability across 24MHz to 1800MHz.

**Official Documentation**: [HydraSDR Website](https://hydrasdr.com) | **HydraSDR RFOne specification URL**: https://hydrasdr.com/hydrasdr-rfone  
**Purchase Information**: In stock at DigiKey - price under 190USD https://www.digikey.com/en/products/detail/benjamin-vernoux/hydrasdr-rfone/26256067  
**Community**: GitHub Issues for support and development discussions  
**Creator**: Benjamin VERNOUX

## Project Overview

The HydraSDR RFOne is a professional-grade Software Defined Radio receiver designed and engineered in France, manufactured in the USA.
It features **open-source Firmware, Applications, Host Tools with shared libraries(DLL)** as a key differentiator from proprietary alternatives.

**Key Features:**
- **Frequency Range**: 24 MHz to 1.8 GHz continuous coverage
- **Bandwidth**: 10 MHz instantaneous sampling capability (9MHz alias/image free)
- **Dynamic Range**: 12-bit ADC @ 20 MSPS providing 80 dB dynamic range (64 dB SNR, 10.4 ENOB)
- **Microcontroller**: NXP LPC4370 (Cortex-M4F + 2× Cortex-M0, up to 204 MHz)
- **Tuner**: Rafael Micro R828D
- **Connectivity**: USB-C (USB 2.0), SMA antenna connector
- **Enclosure**: 7075 aerospace aluminum, black anodized
- **Extensible**: Expandable with extension modules for additional frequency coverage

## Reviews / Analysis
### Video Reviews
- **[Ham Radio DX YouTube Aug 4, 2025](https://www.youtube.com/watch?v=8GZ7tcCjORQ)** - HydraSDR RFone – Is This the Future of SDR's? With a Software Defined Radio (SDR), you can see the entire radio spectrum — and the HydraSDR RFone takes that to the next level. This brand-new SDR stands out with fully open-source firmware, applications, and host tools,  offering a level of flexibility that most proprietary radios can’t match.
- **[Tech Minds YouTube July 23, 2025](https://www.youtube.com/watch?v=UvMIeRP8L4s)** - HydraSDR RFOne - A New High Performance Software Defined Radio - Made in the USA! Comprehensive hands-on review covering specifications, unboxing, enclosure disassembly, PCB examination, firmware updating, and real-world testing with SDR++ software.
- **[Geerling Engineering YouTube June 28, 2025](https://www.youtube.com/watch?v=tXIPQK28aJY)** - SDR is an incredible tool for understanding radio (featuring HydraSDR RFOne) - Comprehensive 21-minute exploration of Software Defined Radio technology, featuring hands-on demonstrations with multiple SDR devices (RTL-SDR v3/v4, HackRF One, HydraSDR RFOne) Covers FM band analysis, signal spurs, antenna impact, digital carrier decoding, gain optimization, 900 MHz Meshtastic signals, and practical SDR selection guidance for RF engineers and enthusiasts.

### Written Reviews & Technical Analysis

- **[Zero Retries 0209 Article July 4, 2025](https://www.zeroretries.org/p/zero-retries-0209?open=true#%C2%A7hydrasdr-rfone-new-software-defined-receiver)**
This July 2025 article discusses the HydraSDR RFOne in the context of amateur radio, praising its 24-1800 MHz coverage (ideal for VHF/UHF bands including 10m at 28 MHz without transverters), 10 MHz sampling, metal enclosure (fits up to three boards for phase-coherent radar/scanning), and included USB-C cable with toroid filters for noise reduction. It's open-source with support for SDR++, SatDump, GNU Radio, GQRX, URH, and LuaRadio via GitHub. Priced at $190, it's positioned as affordable for its class.
Positive/Enthusiastic Quotes and Feedback:"Another reasonable cost, reasonable performance software-defined receiver option manufactured in the US."
"Ultra-extensible... capable of containing up to three boards for unique ultra-compact phase-coherent receivers."
"Qualified for use with the open-source, cross-platform SDR++ application, enhancing its usability."

- **[RTL-SDR Blog - Comprehensive Review July 2, 2025](https://www.rtl-sdr.com/rtl-sdr-blog-review-of-the-hydrasdr)** - Comparison review between HydraSDR and Airspy R2, covering design similarities, performance testing, shielding analysis, software compatibility, and practical usage scenarios. Independent testing found excellent RF shielding and cleaner spectrum with lower internal spurs compared to the Airspy R2.


## Supported Software

The HydraSDR RFOne works with a comprehensive ecosystem of SDR applications:

### Primary Software
- **[SDR++ fork](https://github.com/hydrasdr/SDRPlusPlus)** - SDR++ fork for HydraSDR RFOne (recommended)
- **[GNU Radio](https://github.com/hydrasdr/gr-osmosdr)** - gr-osmosdr for HydraSDR RFOne for GNU Radio
- **[SoapyHydraSDR](https://github.com/hydrasdr/SoapyHydraSDR)** - Soapy for HydraSDR RFOne supporting GQRX and other applications

### Docker Multi-Platform RF Toolbox / SDR
- **[PentHertz RF-Swift](https://github.com/PentHertz/RF-Swift)** - A comprehensive Docker-based RF toolbox that enables rapid deployment of specialized radio frequency tools across multiple platforms and architectures. Supports Linux, Windows, and macOS on x86_64, ARM64 (Raspberry Pi, Apple Silicon), and RISC-V systems. Features containerized deployment that installs in seconds without modifying your host operating system.
  - **Variants**: `sdr_light` and `sdr_full` configurations available
  - **Hardware Support**: Compatible with HydraSDR RFOne
  - **Documentation**: Complete setup guide at [rfswift.io/docs/getting-started](https://rfswift.io/docs/getting-started)

### GNU/Linux SDR Distribution
- **[DragonOS](https://sourceforge.net/projects/dragonos-focal/files/)** - A ready-to-use Lubuntu-based Linux distribution specifically designed for software-defined radio enthusiasts and professionals. Provides an out-of-the-box SDR environment with pre-configured tools and drivers for immediate use.
  - **Available Versions**: 
    - DragonOS Noble (24.04 LTS)
    - DragonOS FocalX (22.04 LTS) 
    - DragonOS Focal (20.04 LTS)
  - **Architecture**: x86_64 support
  - **Hardware Support**: HydraSDR RFOne compatibility (DragonOS Noble R5 and later)
  - **Latest Release**: DragonOS Noble R5 (July 3, 2025)

### Specialized Applications  
- **[SatDump](https://github.com/SatDump/SatDump/releases/tag/nightly)** - Satellite signal decoding and processing (nightly build supports HydraSDR RFOne)
- **[URH (Universal Radio Hacker)](https://github.com/hydrasdr/urh)** - Repository contains the Universal Radio Hacker fork with HydraSDR RFOne support for protocol analysis and signal intelligence applications.
- **[luaradio](https://github.com/hydrasdr/luaradio)** - Repository contains the LuaRadio framework fork with HydraSDR RFOne providing lightweight signal processing capabilities for embedded and resource-constrained applications.
- **[nfc-laboratory](https://github.com/josevcm/nfc-laboratory)** - NFC signal sniffer and protocol decoder using SDR receiver for demodulation and decoding NFC-A, NFC-B, NFC-F and NFC-V signals in real-time up to 424 Kbps. ([nfc-laboratory v3.3.0](https://github.com/josevcm/nfc-laboratory/releases/tag/3.3.0) or more supports HydraSDR RFOne)
- **[GNSS-SDR](https://github.com/gnss-sdr/gnss-sdr)** - Open-source GNSS receiver for GPS/Galileo/GLONASS

All software supports **Windows, Linux, and macOS** platforms.

## Repository Structure

The HydraSDR project consists of 8 specialized repositories supporting the HydraSDR RFOne and future HydraSDR products:

[**rfone_host**](https://github.com/hydrasdr/rfone_host) repository contains HydraSDR RFOne Host Tools, shared libraries, and DLLs for Windows/Linux/macOS integration with comprehensive build instructions for Visual Studio 2019, CMake, and cross-platform development.

[**rfone_fw**](https://github.com/hydrasdr/rfone_fw) repository contains the open-source firmware for HydraSDR RFOne, built with Python-based components and standard GCC toolchains.

[**SDRPlusPlus**](https://github.com/hydrasdr/SDRPlusPlus) repository contains the SDR++ fork with native HydraSDR RFOne support and optimized performance configurations.

[**SoapyHydraSDR**](https://github.com/hydrasdr/SoapyHydraSDR) repository contains the SoapyHydraSDR plugin enabling HydraSDR RFOne compatibility with GQRX, CubicSDR, and other SoapyHydraSDR-based applications.

[**gr-osmosdr**](https://github.com/hydrasdr/gr-osmosdr) repository contains the GNU Radio OsmoSDR source block with HydraSDR RFOne support for integration with GNU Radio Companion and custom flowgraphs.

[**SatDump**](https://github.com/hydrasdr/SatDump) repository contains the forked SatDump software with native HydraSDR RFOne support for satellite signal decoding and weather satellite image processing.

[**urh**](https://github.com/hydrasdr/urh) repository contains the Universal Radio Hacker fork with HydraSDR RFOne support for protocol analysis and signal intelligence applications.

[**luaradio**](https://github.com/hydrasdr/luaradio) repository contains the LuaRadio framework fork providing lightweight signal processing capabilities for embedded and resource-constrained applications.

## Quick Start Guide

### System Requirements
- **Operating System**: Windows 8.1+, Linux (Ubuntu 20.04+), or macOS 10.14+
- **USB Port**: USB 2.0 or higher
- **Antenna**: SMA connector compatible

### Installation

**Windows Setup:**
1. Connect your HydraSDR RFOne using a USB-C cable for power and data (it is recommended to use the USB-C / USB-A cable provided with the HydraSDR RFOne).
2. Download pre-built SDR++ fork with HydraSDR RFOne support from [nightly releases](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly)

**Linux Setup:**
1. Connect your HydraSDR RFOne using a USB-C cable for power and data (it is recommended to use the USB-C / USB-A cable provided with the HydraSDR RFOne).
2. Download and Install the HydraSDR RFOne package from [GitHub releases](https://github.com/hydrasdr/rfone_host/releases)
3. Download pre-built SDR++ fork (for your GNU/Linux distribution) with HydraSDR RFOne support from [nightly releases](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly)

**macOS Setup:**
1. Connect your HydraSDR RFOne using a USB-C cable for power and data (it is recommended to use the USB-C / USB-A cable provided with the HydraSDR RFOne).
2. Download the HydraSDR RFOne macOS package from [GitHub releases](https://github.com/hydrasdr/rfone_host/releases)
3. Download pre-built SDR++ fork (for macOS) with HydraSDR RFOne support from [nightly releases](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly)

### First Use
1. Connect HydraSDR RFOne via USB-C / USB-A cable
3. Connect your antenna to the ANT port.
   * The antenna must have an SMA male connector to mate with the device’s SMA female port.   
4. Launch SDR++ fork or your preferred SDR application
5. Select HydraSDR RFOne as input device
6. Configure the sample rate (up to 10 MSPS), frequency, and gain settings (Linear 12 is recommended as a starting point), then start RX streaming.

### Software Installation
- **SDR++**: Download HydraSDR RFOne-optimized fork from [nightly releases](https://github.com/hydrasdr/SDRPlusPlus/releases/tag/nightly)
- **GNU Radio**: Install dedicated gr-osmosdr with native HydraSDR RFOne support from [releases](https://github.com/hydrasdr/gr-osmosdr/releases)
- **SoapyHydraSDR Applications**: Install SoapyHydraSDR plugin, then use with GQRX or other compatible software

## Technical Specifications

**RF Performance:**
- Frequency Range: 24 MHz to 1.8 GHz (continuous)
- Instantaneous Bandwidth: 10 MHz (9MHz alias/image free)
- ADC Resolution: 12-bit
- Sample Rate: Up to 10 MSPS output
- Dynamic Range: Up to 80 dB
- Noise Figure: Optimized for low-noise performance

**Hardware Architecture:**
- MCU: NXP LPC4370 (1× Cortex-M4F + 2× Cortex-M0 @ up to 204 MHz)
- Tuner: Rafael Micro R828D
- Interface: USB-C (USB 2.0 compatible)
- Enclosure: 7075 aerospace aluminum with black anodized finish
- Expansion: Two unused uFL connectors for advanced applications
- Multi-unit: Oversized enclosure supports up to 3 boards

**Key Features:**
- Open-source firmware and API host tools enabling community development
- High Quality PCB layout with superior RF front-end design
- State of the art filtering and thermal management
- Robust USB-C connector for modern connectivity
- Made in USA manufacturing with European design expertise

## HydraSDR RFOne Availability

The HydraSDR RFOne is available on DigiKey.
**Pricing**: Under 190USD  
**Availability**: In stock at [DigiKey](https://www.digikey.com/en/products/detail/benjamin-vernoux/hydrasdr-rfone/26256067) with worldwide shipping  
**Documentation**: Full specifications at https://hydrasdr.com/hydrasdr-rfone

## Development and Contributions

The HydraSDR project welcomes community contributions across all repositories.
Each repository contains specific contribution guidelines and coding standards.
For technical support, feature requests, or bug reports, please use the GitHub Issues system in the relevant repository.

**Development Tools:**
- Open-source firmware built with standard GCC toolchains
- Cross-platform host software supporting Windows / GNU Linux(major distribution) / macOS (arm/intel)
- Comprehensive build systems with CMake integration

**Community Resources:**
- GitHub Issues for technical support and feature requests
- Active development with regular updates and improvements
- Integration with existing SDR software ecosystem
- Educational resources and documentation for developers

The HydraSDR project provides enhanced capabilities through open-source development and community collaboration, starting with the RFOne and expanding to future HydraSDR products.
