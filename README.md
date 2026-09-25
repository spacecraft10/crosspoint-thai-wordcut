# CrossPoint (Thai Wordcut Edition) 🇹🇭

A custom build of **CrossPoint for Xteink e-Paper Readers** integrated with a native Thai word-segmentation engine into the EPUB / text rendering pipeline to resolve improper Thai word wrapping and accidental line breaks mid-word.

- **Thai Word Segmentation**: Powered by [wordcut-engine](https://codeberg.org/mekong-lang/wordcut-engine) with character cluster boundary protection.
- **Embedded Thai Typography**: Built-in **Sarabun** reader fonts (12–18 pt, Regular/Bold/Italic/BoldItalic) and Thai UI glyphs.
- **OPDS Batch Download**: "Download All" catalog feeds directly to the SD card with per-server subfolder routing.
- **Tested & Verified Devices**:
  - **Xteink X3**
  - **Xteink X4**
  - **Xteink X4 Pro**

---

## Download

Download the latest pre-compiled release package from:  
[GitHub Releases](https://github.com/spacecraft10/crosspoint-thai-wordcut/releases)

---

## Installation

The installation procedure is identical to standard CrossPoint firmware updates. For comprehensive instructions and web-based flashing, please refer to:  
- [CrossPoint Official Documentation](https://crosspointreader.com/)
- [CrossPoint Web Flash Tools](https://crosspointreader.com/#flash-tools)

### Quick Setup (MicroSD Card):
1. Download the firmware binary matching your hardware model from [Releases](https://github.com/spacecraft10/crosspoint-thai-wordcut/releases) (e.g., `crosspoint-thai-wordcut-v1.6.0-x4.bin`).
2. Format a microSD card as **FAT32**.
3. **Rename the downloaded file to `firmware.bin`** and copy it directly to the root directory of the microSD card.
4. Power off the Xteink device and insert the microSD card.
5. Connect the device to power via USB-C while holding the **Power + Up** button combination until the bootloader detects `firmware.bin` and flashes the firmware.

---

## Dictionary & Vocabulary

The embedded dictionary data (`ThaiDictData.h`) is compiled directly from [wordcut-engine](https://codeberg.org/mekong-lang/wordcut-engine) and expanded with contemporary transliterations, colloquial phrases, and loanwords to ensure accurate segmentation of modern Thai texts and translated literature.

---

## Credits

- [CrossPoint](https://github.com/crosspoint-reader/crosspoint-reader) — Open-source e-reader firmware for ESP32 and E-Paper devices.
- [wordcut-engine](https://codeberg.org/mekong-lang/wordcut-engine) — Thai word segmentation library by mekong-lang.
