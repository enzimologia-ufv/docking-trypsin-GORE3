🧬 Molecular Docking Pipeline: Trypsin-like × Peptide
📌 Overview

This repository contains a complete pipeline for molecular docking between a trypsin-like protein and a peptide ligand.

🔬 Steps

Receptor modeling using Swiss-Model

Ligand prediction using PepFold4

Preparation using AutoDock Tools

Docking using AutoDock Vina

Analysis and visualization

⚙️ Requirements

AutoDock Vina

AutoDock Tools

Discovery Studio

Linux / WSL recommended

🚀 Running Docking
vina --receptor prepared/receptor.pdbqt \
     --ligand prepared/ligand.pdbqt \
     --center_x X --center_y Y --center_z Z \
     --size_x 30 --size_y 30 --size_z 30 \
     --exhaustiveness 24 \
     --num_modes 12 \
     --out docking/out.pdbqt \
     --log docking/log.txt
✂️ Splitting Results
vina_split --input docking/out.pdbqt
📊 Results

Binding affinity (kcal/mol)

Binding poses

Interaction analysis

📷 Visualization

Performed using Discovery Studio.

📁 Project Structure

(see folders above)

👨‍🔬 Author

Your Name

📌 Notes

Grid box must be centered on active site

Lower binding energy indicates stronger interaction
