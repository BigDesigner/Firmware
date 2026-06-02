# Legacy Network Hardware & BIOS Firmware Archive

This repository is a production-oriented, verified firmware and BIOS archive dedicated to legacy networking equipment (Modems, Firewalls, Access Points, Switches, and System BIOS). 

It aims to bypass broken vendor upstream links, resolve controller synchronization loops (e.g., ezMaster "Downloading..." bugs), and preserve critical deployment binaries for out-of-support (EoL) hardware.

---

## 💾 Direct Download Manifest

Clicking on any file name below will trigger an immediate direct download of the respective firmware/BIOS binary via your browser:

| Vendor | Device / Model | Type | Version | Direct Download Link (Click to Download) | Status / Notes |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **EnGenius** | EWS310AP | AP FW | v3.5.1.9_c1.9.04 | [ews310ap-all-v3.5.1.9_c1.9.04.bin](https://github.com/BigDesigner/Firmware/raw/refs/heads/main/EnGenius/ews310ap-all-v3.5.1.9_c1.9.04.bin) | Full original production binary |
| **EnGenius** | EWS310AP | AP FW | v3.5.1 (Short) | [EWS310AP-v3.5.1.bin](https://github.com/BigDesigner/Firmware/raw/refs/heads/main/EnGenius/EWS310AP-v3.5.1.bin) | Alias binary for ezMaster bulk upload |

> 💡 *As new files are added to the repository, new rows will be appended to this table following the Vendor, Type, and Direct Download Link structure.*

> ⚠️ **Security Note:** Depending on your browser's security policies, downloading .bin files might trigger an "Insecure download blocked" warning. You can safely bypass this by selecting "Keep" from your browser's download panel.

---

## 📂 Repository Structure

The directory architecture layout is designed to scale as new vendors and hardware categories are introduced:

~~~text
├── EnGenius/             # EnGenius Systems Infrastructure (APs, Switches)
│   ├── EWS310AP-v3.5.1.bin
│   ├── ews310ap-all-v3.5.1.9_c1.9.04.bin
│   └── readme.md         # Specific hardware deployment nuances
│
├── [Vendor_Name]/        # Future Expansion (Modem, Firewall, BIOS categories)
│   └── [Device_Model]/
└── README.md             # Repository Global Overview & Download Table (This file)
~~~

---

## 🛡️ Deployment & Integrity Verification

To eliminate the risk of bricking legacy devices during manual or automated bulk upgrades, always verify the binary integrity before flashing:

~~~bash
# Navigate to the specific vendor directory
cd EnGenius/

# Verify checksums (Ensure SHA256SUMS exists in the target directory)
sha256sum -c SHA256SUMS
~~~

---

## 🤝 Contribution & Maintenance
To contribute missing firmware, internal documentation, or dumped BIOS images for legacy hardware:
1. Create a new directory under the corresponding Vendor folder using the exact device model name.
2. Commit the verified binary files.
3. Update the **Direct Download Manifest** table in this root README.md by appending the new raw GitHub URL link.
