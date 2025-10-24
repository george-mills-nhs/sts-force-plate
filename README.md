# Interactive Force Analysis Tool

This R script provides an interactive workflow for analysing force–time data from the five-repetition sit-to-stand assessment collected using a force plate.  
It allows the user to visually define baseline and repetition windows, applies signal smoothing and baseline correction, and automatically calculates rate of force development (RFD) and impulse metrics for each repetition.

---

## 🧠 Overview

The script:
1. Loads a `.txt` force plate data file exported from acquisition software.
2. Smooths the raw signal using a Butterworth low-pass filter.
3. Allows interactive selection of the baseline window.
4. Corrects the force trace to remove baseline offset.
5. Prompts the user to define start and end times for each repetition.
6. Automatically computes:
   - Time zero (onset of force rise)
   - RFD at 50, 100, and 200 ms
   - Peak RFD, peak force, time to peak
   - Impulse over multiple time intervals
7. Optionally visualises each repetition.
8. Exports results to an Excel file.

---

## ⚙️ Dependencies

The following R packages are required:
```r
plotly, readr, dplyr, signal, writexl, pracma, zoo
