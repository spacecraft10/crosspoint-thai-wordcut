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

### Option 1: Web Flashing (Browser):
1. Open a Web Serial compatible browser (Google Chrome, Microsoft Edge).
2. Connect your Xteink device to your computer using a USB-C data cable.
3. Go to [CrossPoint Web Flash Tools](https://crosspointreader.com/#flash-tools).
4. Click **Connect** and select the Serial/COM port corresponding to your device.
5. Select your device model (X3, X4, or X4 Pro), then choose the **Custom .bin** option.
6. Select the downloaded firmware binary file (`.bin`) from your computer (e.g., `crosspoint-thai-wordcut-v1.6.0-x4.bin`).
7. Click **Flash** / **Install** and wait until the progress reaches 100%, then disconnect and restart the device.

### Option 2: MicroSD Card Setup:
1. Download the firmware binary matching your hardware model from [Releases](https://github.com/spacecraft10/crosspoint-thai-wordcut/releases) (e.g., `crosspoint-thai-wordcut-v1.6.0-x4.bin`).
2. Format a microSD card as **FAT32**.
3. **Rename the downloaded file to `firmware.bin`** and copy it directly to the root directory of the microSD card.
4. Power off the Xteink device and insert the microSD card.
5. Connect the device to power via USB-C while holding the **Power + Up** button combination until the bootloader detects `firmware.bin` and flashes the firmware.

---

### การติดตั้ง

ขั้นตอนการติดตั้งเหมือนกับการอัปเดตเฟิร์มแวร์ CrossPoint มาตรฐาน สำหรับคู่มืออย่างเป็นทางการและการแฟลชผ่านเว็บ สามารถดูเพิ่มเติมได้ที่:
- [CrossPoint Official Documentation](https://crosspointreader.com/)
- [CrossPoint Web Flash Tools](https://crosspointreader.com/#flash-tools)

#### วิธีที่ 1: ติดตั้งผ่านหน้าเว็บ (Web Flashing):
1. เปิดเบราว์เซอร์ที่รองรับ Web Serial (เช่น Google Chrome, Microsoft Edge)
2. เชื่อมต่ออุปกรณ์ Xteink เข้ากับคอมพิวเตอร์ด้วยสาย USB-C (ต้องใช้สายส่งข้อมูล / Data Cable)
3. เข้าไปที่หน้า [CrossPoint Web Flash Tools](https://crosspointreader.com/#flash-tools)
4. กด **Connect** แล้วเลือกพอร์ต Serial/COM ของอุปกรณ์ที่เชื่อมต่อ
5. เลือกรุ่นเครื่องของคุณ (X3, X4 หรือ X4 Pro) จากนั้นเลือกตัวเลือก **Custom .bin**
6. เลือกไฟล์เฟิร์มแวร์ `.bin` ที่ดาวน์โหลดมาจาก [Releases](https://github.com/spacecraft10/crosspoint-thai-wordcut/releases) ในเครื่องของคุณ (เช่น `crosspoint-thai-wordcut-v1.6.0-x4.bin`)
7. กด **Flash** หรือ **Install** แล้วรอจนกระบวนการแฟลชเสร็จสมบูรณ์ (100%) จากนั้นถอดสายออกและรีสตาร์ทเครื่อง

#### วิธีที่ 2: ติดตั้งผ่าน MicroSD Card:
1. ดาวน์โหลดไฟล์เฟิร์มแวร์รุ่นที่ตรงกับเครื่องของคุณจาก [Releases](https://github.com/spacecraft10/crosspoint-thai-wordcut/releases) (เช่น `crosspoint-thai-wordcut-v1.6.0-x4.bin`)
2. ฟอร์แมต MicroSD card เป็นระบบ **FAT32**
3. **เปลี่ยนชื่อไฟล์ที่ดาวน์โหลดมาเป็น `firmware.bin`** แล้วคัดลอกไว้ที่ Root Directory (โฟลเดอร์นอกสุด) ของ MicroSD card
4. ปิดเครื่อง Xteink แล้วใส่ MicroSD card เข้าไปในเครื่อง
5. เสียบสาย USB-C เพื่อจ่ายไฟ พร้อมกดปุ่ม **Power + ปุ่มขึ้น (Up)** ค้างไว้ จนกว่า Bootloader จะตรวจพบไฟล์ `firmware.bin` และเริ่มติดตั้งเฟิร์มแวร์

---

## Dictionary & Vocabulary

The embedded dictionary data (`ThaiDictData.h`) is compiled directly from [wordcut-engine](https://codeberg.org/mekong-lang/wordcut-engine) and expanded with contemporary transliterations, colloquial phrases, and loanwords to ensure accurate segmentation of modern Thai texts and translated literature.

---

## Credits

- [CrossPoint](https://github.com/crosspoint-reader/crosspoint-reader) — Open-source e-reader firmware for ESP32 and E-Paper devices.
- [wordcut-engine](https://codeberg.org/mekong-lang/wordcut-engine) — Thai word segmentation library by mekong-lang.
