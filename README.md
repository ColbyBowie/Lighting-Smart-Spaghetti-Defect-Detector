# No More Midnight Filament Spaghetti 
About
A single-camera detector that spots 3D-printing “spaghetti” failures reliably across changing light. We trained YOLOv9-s on images from a Core-XY printer’s corner camera under three conditions: LED, shop light, and daylight. The goal is dependable 24/7 monitoring without per-site retuning.

## Key results (mAP@0.5)
Single-light models exceeded 70% in their home lighting but dropped to roughly 5–17% when lighting changed.

Dual-light training restored most cross-light performance, recovering about 80–85% of what was lost.

Tri-light training delivered steady performance around 65–70% across all lights.

Synthetic shadow augmentation added only a small gain compared to using real multi-light data.

## Quickstart
Dataset: download the open multi-lighting dataset on Roboflow Universe in YOLOv9 format: https://universe.roboflow.com/colbys-workplace/3d-printing-different-lighting-eh5fr/dataset/3 and extract and rename folder to 'frames'

Notebooks: use src/other/ seperate_files.ipynb and run cells in the same directory as 'frames' folder to seperate frames into correct folders. Then upload the 'Data_Frames.zip' to google drive

use src/main/ in Google Colab. Set your dataset path and run cells in order. Experiments were run on a T4 GPU.

Trained models and logs: see models/ for four experiment groups (Baseline_fixed_results, Baseline_best_results, Synthetic_shadow_fixed_results, Synthetic_shadow_best_results) and results/ for the corresponding CSVs.

Paper and poster: see documents/. 
3mf files used in the study are in data/3D_Print_Files/.
Utility notebooks are in src/other/.

## How to cite
C. Bowie and J. Satel, “No More Midnight Filament Spaghetti: A Lighting-Smart Detector for 3D Printers,” University of Lethbridge, 2025. [Online]. Available: https://github.com/ColbyBowie/Lighting-Smart-Spaghetti-Defect-Detector

## License
Code is released under the MIT License. See LICENSE for details.
Dataset is hosted on Roboflow Universe; please refer to the dataset page for its terms of use.
