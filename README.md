# CompSpoof Dataset

The **CompSpoof dataset** is designed for studying **component-level anti-spoofing**, where either the **speech** or the **environmental sound component** (or both) may be spoofed.

***

## 📂 Dataset Overview

*   **Total samples:** 2,500
*   **Classes:** 5 (500 samples per class)
*   **Duration:** 5–21 seconds
*   **Sampling rate:** 16 kHz
*   **Partitioning:** 70% train, 10% dev, 20% eval (stratified to preserve class balance)

| ID | Mixed | Speech    | Environment | Class Label        | Description                                                                  |
| :- | :---- | :-------- | :---------- | :----------------- | :--------------------------------------------------------------------------- |
| 0  | ❌     | Bona fide | Bona fide   | original           | Original bona fide speech and corresponding environment audio without mixing |
| 1  | ✅     | Bona fide | Bona fide   | bonafide\_bonafide | Bona fide speech mixed with another bona fide environmental audio            |
| 2  | ✅     | Spoofed   | Bona fide   | spoof\_bonafide    | Spoof speech mixed with bona fide environmental audio                        |
| 3  | ✅     | Bona fide | Spoofed     | bonafide\_spoof    | Bona fide speech mixed with spoof environmental audio                        |
| 4  | ✅     | Spoofed   | Spoofed     | spoof\_spoof       | Spoof speech mixed with spoof environmental audio                            |

***

## 🎧 Data Sources

*   **Bona fide speech:** ASVspoof5, CommonVoice
*   **Spoofed speech:** ASVspoof5, SSTC
*   **Bona fide environmental sounds:** VGGSound
*   **Spoofed environmental sounds:** VCapAV
*   **Original mixed audio:** VGGSound (speech + environment simultaneously captured)

Environmental sounds cover **indoor, street, and natural settings**, ensuring acoustic diversity.

During processing:

*   All files are **resampled to 16 kHz**.
*   The **shorter signal** determines the final duration, with longer ones truncated.
*   Environmental sound is scaled to a **predefined SNR** relative to the speech.

***


## 🎧 Audio Examples

Below are audio samples from the **CompSpoof** dataset.  
For each class, we provide the **mixed audio** (if applicable), along with the **speech** and **environment** sources.  

---

### Class 0 — Original
**Label:** `original`  
**Description:** Original bona fide speech and corresponding environment audio without mixing  

- **Original Speech (bona fide)**
 
  <audio controls>
    <source src="audio_demo/class0/bonafide_0_259.mp3" type="audio/wav">
  </audio>
---

### Class 1 — Bona fide + Bona fide
**Label:** `bonafide_bonafide`  
**Description:** Bona fide speech mixed with another bona fide environmental audio  

- **Mixed**

  <audio controls>
    <source src="audio_demo/class1/bonafide_bonafide_0203.wav" type="audio/wav">
  </audio>
  
- **Speech (bona fide)**

  <audio controls>
    <source src="audio_demo/class1/T_0000155380.flac" type="audio/wav">
  </audio>
  
- **Environment (bona fide)**

  <audio controls>
    <source src="audio_demo/class1/-8S9TKWIOSc_30.mp3" type="audio/wav">
  </audio>

---

### Class 2 — Spoofed Speech + Bona fide Environment
**Label:** `spoof_bonafide`  
**Description:** Spoof speech mixed with bona fide environmental audio  

- **Mixed**
  
- <audio controls>
    <source src="audio_demo/class2/spoof_bonafide_0296.wav" type="audio/wav">
  </audio>
  
- **Speech (spoofed)**
  
  <audio controls>
    <source src="audio_demo/class2/T_0000087396.flac" type="audio/wav">
  </audio>
  
- **Environment (bona fide)**
  
  <audio controls>
    <source src="audio_demo/class2/-UjHThfWx_o_30.mp3" type="audio/wav">
  </audio>

---

### Class 3 — Bona fide Speech + Spoofed Environment
**Label:** `bonafide_spoof`  
**Description:** Bona fide speech mixed with spoof environmental audio  

- **Mixed**

  <audio controls>
    <source src="audio_demo/class3/bonafide_spoof_0096.wav" type="audio/wav">
  </audio>

- **Speech (bona fide)**

  <audio controls>
    <source src="audio_demo/class3/T_0000156775.flac" type="audio/wav">
  </audio>
  
- **Environment (spoofed)**
 
  <audio controls>
    <source src="audio_demo/class3/IvUXQLAqHz4_000971.wav" type="audio/wav">
  </audio>

---

### Class 4 — Spoofed Speech + Spoofed Environment
**Label:** `spoof_spoof`  
**Description:** Spoof speech mixed with spoof environmental audio  

- **Mixed**
 
  <audio controls>
    <source src="audio_demo/class4/spoof_spoof_0060.wav" type="audio/wav">
  </audio>
  
- **Speech (spoofed)**
  
  <audio controls>
    <source src="audio_demo/class4/T_0000142036.flac" type="audio/wav">
  </audio>
  
- **Environment (spoofed)**

  <audio controls>
    <source src="audio_demo/class4/nUs5SJyQPnM_000350.wav" type="audio/wav">
  </audio>

## 📥 Download

You can download the dataset here:\
👉 [CompSpoof Download Link](https://huggingface.co/datasets/XuepingZhang/CompSpoof)

***

## 🔖 Citation

If you use this dataset in your research, please cite:

```
```

