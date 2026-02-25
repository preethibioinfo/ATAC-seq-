# ATAC-seq Chromatin Accessibility Analysis

This repository contains a reproducible ATAC-seq workflow for chromatin accessibility analysis and transcription factor motif discovery in human cancer datasets.

---

## 📊 Dataset Information

**Source:** NCBI GEO  
**Organism:** Homo sapiens  
**Data Type:** Bulk ATAC-seq  
**Genome Build:** GRCh38 (hg38)  
**Annotation:** GENCODE v38  

Raw sequencing data can be downloaded using the SRA Toolkit.  
Peak files and signal tracks are processed for downstream chromatin accessibility analysis.

---

## 📁 Repository Structure

ATAC-seq/  
├── README.md  
├── data/  
│   ├── sample_metadata.csv  
│   ├── GSE230793_ATAC_peaks.bed  
│   ├── GSE230798_ATAC_peaks.bed  
│   ├── bigwig/  
│   │   ├── sample1.bw  
│   │   ├── sample2.bw  
│  
├── scripts/  
│   ├── 01_merge_peaks.sh  
│   ├── 02_peak_annotation.sh  
│   ├── 03_motif_analysis.sh  
│   ├── 04_signal_matrix.sh  
│   ├── 05_heatmap_profile.sh  
│   ├── 06_generate_counts.sh  
│  
└── sessionInfo.txt  

---

## 🧪 Experimental Design

The study compares chromatin accessibility differences between biological conditions (e.g., tumor vs control).

Metadata includes:

• Sample ID  
• Patient ID  
• Condition  
• Replicate  

See `data/sample_metadata.csv`.

---

## 📌 Statistical & Analysis Parameters

• Peak merging using BEDTools  
• Genome annotation using HOMER (hg38)  
• Motif enrichment: HOMER (known + de novo motifs)  
• Signal visualization: deepTools  
• Accessibility window: ±2kb from peak center  
• Differential-ready counts exported for DESeq2  

---

## 🔬 Analysis Workflow

1. Download raw data (SRA Toolkit)
2. Peak merging (BEDTools)
3. Peak annotation (HOMER)
4. Motif enrichment analysis
5. Signal matrix computation (deepTools)
6. Heatmap and profile visualization
7. Peak count extraction (multiBigwigSummary)
8. Genome browser visualization (IGV/UCSC)

---

## 📈 Outputs Generated

✔ Merged peak set  
✔ Annotated peak file  
✔ Transcription factor motif enrichment results  
✔ Accessibility heatmap  
✔ Average accessibility profile plot  
✔ Peak count matrix for differential accessibility  
✔ Genome browser–compatible BigWig tracks  

---

## 🔄 Reproducibility

• Analysis performed using Conda-managed environment  
• Tools: HOMER, deepTools, BEDTools  
• Script-based modular workflow  
• All outputs generated programmatically  

---

## 📖 How to Run

1. Activate Conda environment
2. Run scripts sequentially from `scripts/`
3. Outputs will be saved in `results/` and `figures/`

---

## 👩‍🔬 Author

D. Preethi  
M.Sc. Biochemistry  
Stem Cell Biology Laboratory  
Cancer & Epigenetics Research  
