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

## 📥 Download

You can download the dataset here:\
👉 [CompSpoof Download Link](https://huggingface.co/datasets/XuepingZhang/CompSpoof)

***

## 🔖 Citation

If you use this dataset in your research, please cite:

```
```

