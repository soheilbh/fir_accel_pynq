# FIR Filter Acceleration on PYNQ-Z2 (Zynq-7020)

This project demonstrates how to accelerate a Finite Impulse Response (FIR) filter using hardware on the **PYNQ-Z2** board.  
It compares the performance of a software-based FIR filter with a custom hardware implementation using DMA and a custom driver.

## 📚 Based On

This notebook is based on the tutorial:  
[*How to accelerate a function with PYNQ*](https://www.youtube.com/watch?v=PwG037LuNvA) by **Jeff Johnson** of **FPGA Developer**.

## ✨ Updates in This Version

- Migrated from deprecated `Xlnk` to modern `allocate()` for buffer allocation.
- Added `.hwh` support instead of `.tcl`, required for newer PYNQ versions.
- Cleaned and commented code using **ChatGPT-4**, organized into logical steps.
- Custom driver class (`Filter`) using `DefaultHierarchy` for clean abstraction.

## 🔧 Requirements

- PYNQ-Z2 board (Zynq-7020)
- PYNQ image 2.7 or later
- Vivado project to generate:
  - `fir_accel.bit`
  - `fir_accel.hwh`

## 📁 Files

- `FIR_accel.ipynb`: Main Jupyter notebook (run on the PYNQ board).
- `fir_accel.bit`: Bitstream file for FIR overlay.
- `fir_accel.hwh`: Hardware metadata file for overlay.

## 🚀 How to Use

1. Copy all files to your PYNQ board (e.g., using Jupyter file browser or `scp`).
2. Open `FIR_accel.ipynb` in the Jupyter interface.
3. Follow each section step by step.

Make sure the `.bit` and `.hwh` files are in the same folder as the notebook and have the same base name.

## 🤝 Credits

Tutorial by Jeff Johnson — [FPGA Developer](https://www.youtube.com/c/FPGAdeveloper)  
Code structure and cleanup supported by **ChatGPT-4**