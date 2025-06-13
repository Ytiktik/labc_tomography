# labc_tomography

This repository contains the software used for the analysis presented in the paper:
***Quantum Tricks with Classical Tools: Tomography and Bell Tests Made Simple Using Classical Optics***
by *Noa Gabbay, Yoav Tiktin, and Sara Gandelman*.

The software was used to process video recordings from an optical experiment simulating quantum state tomography and Bell tests using classical optics. It identifies and counts "positive incidence" events—frames where detector intensity crosses a defined threshold—based on pixel brightness.

This project was developed as part of the **Lab C course at Tel Aviv University**.

---

## Project Overview

* Implemented in Jupyter Notebooks for ease of visualization and interaction.
* Structured into **three parts (A, B, and C)**:

  * **Part A and B**: Each uses **4 video files** - calculated densitz matrix.
  * **Part C**: Uses **16 video files** - for the full CHSH/Bell parameter analysis.
 
  The matlab file attached for this project is for visualization of part A and B.
  It uses the array of the results of the python notebook to produce a 3D visuallization

---

## Core Class: `Detector`

All parts rely on a shared `Detector` class, which processes video data and identifies "positive" frames based on total frame luminosity.

### Key Features:

* `threshold`: A required argument specifying the luminosity cutoff for detecting a "positive" event.
* **"Cool frames"**: A nickname for frames above the threshold—considered **detection events**.
* Implements logic to **avoid counting consecutive high-intensity frames** as multiple events (i.e., temporal deduplication).

### Main Methods:

* `plot_current_sum()`: Visualizes the summed pixel intensity of each frame.
* `show_cool_frames()`: Displays frames exceeding the defined threshold.

---

## File Structure

* `qtm_notebook.ipynb` – analyses used for the paper made of 3 parts. 
* `Final3DPlotterSaraGarry.m` – 3D visuallization for part A
* `notebook_partC.ipynb` – analyzes Bell correlations and calculates CHSH $S$ value

---

## Input Requirements

* **Part A and B**: 4 videos (HH, HV, VH, VV channels)
* **Part C**: 16 videos (for all angle combinations in Bell test)

---

## License and Credits

This code is part of a final lab project at Tel Aviv University.
For questions or reuse, please contact the authors.






