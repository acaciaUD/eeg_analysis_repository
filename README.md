# EEG Analysis Repository

This repository contains the implementation and supporting files for analyzing EEG data. The project focuses on extracting Task-Related Power (TRP) in the alpha band from two EEG sessions, specifically targeting two channels of interest.

## Repository Structure

```
├── eeglab_current/                   # Supporting folder for EEGLAB processing
├── comparacion                       # MATLAB script for comparing sessions
├── comparacion2                      # Alternate comparison script
├── comparacionCanales                # MATLAB script for channel comparisons
├── EEGLAB1_16_etiquetas              # MATLAB script for channel labeling
├── eeglab2_16electrodes_puntos       # MATLAB script for point extraction
├── Sesión 1.txt                      # Text file containing Session 1 data
├── Sesión 2.txt                      # Text file containing Session 2 data
├── Topographical_map_S1x1cifra_etiquetas.pdf   # Topographic map of Session 1 with labels
├── Topographical_map_S1x1cifra_puntos.pdf      # Topographic map of Session 1 with points
├── Topographical_map_S2x2cifras_etiqueta.pdf  # Topographic map of Session 2 with labels
├── Topographical_map_S2x2cifras_puntos.pdf    # Topographic map of Session 2 with points
```

## Program Overview

### Main Script
The main script for this repository is structured as follows:

1. **Loading and Preprocessing EEG Data:**
    - Data from two sessions is loaded and cleaned.
    - Signals are filtered to reduce noise (0.5-40 Hz).

2. **Alpha Band Analysis:**
    - Extracts alpha band power using Short-Time Fourier Transform (STFT).

3. **TRP Calculation:**
    - Computes Task-Related Power (TRP) in the alpha band.
    - Results are stored for comparison between sessions.

4. **Visualization:**
    - Graphs comparing TRP values over time for the specified channels.

### Key Parameters
- **Frequency Sampling (fs):** 125 Hz
- **Analysis Duration:** First 10 seconds (3 * fs)
- **Alpha Band Range:** 8-13 Hz
- **Channels of Interest:** T4 and O1

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/acaciaUD/eeg_analysis_repository.git
   ```
2. Add the necessary EEG data files (`Sesión 1.txt` and `Sesión 2.txt`) to the root directory.
3. Run the MATLAB scripts to analyze and visualize the EEG data.

## Dependencies
- MATLAB R2021a or newer
- EEGLAB toolbox (for additional processing)

## Results
The analysis outputs topographical maps and TRP time series comparisons for each session, allowing detailed exploration of EEG dynamics in the alpha band.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

Feel free to contribute to this repository by opening issues or submitting pull requests. Happy analyzing!
