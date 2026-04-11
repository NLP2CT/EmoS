# EmoS: A High-Fidelity Multimodal Benchmark for Fine-grained Streaming Emotional Understanding

This repository is the open-source release package for the EmoS benchmark.

EmoS is a bilingual multimodal benchmark built for fine-grained emotion understanding in both static clips and streaming monologues. This release focuses on data organization, annotation artifacts, and release-ready files for reproducible academic use.

## Abstract

In the context of today's high-pressure, aging society, the demand for large-scale emotional models capable of providing empathetic support is more critical than ever. However, existing benchmarks fail to simultaneously achieve ecological validity, signal clarity, and reliable fine-grained labeling. We introduce EmoS, a high-fidelity bilingual benchmark designed to resolve the limitations of ecological validity and noise in existing datasets by combining strictly filtered static slices with a dynamic Streaming Monologue subset. Supported by a rigorous dual-layer human annotation pipeline, EmoS provides trusted ground truth that captures continuous emotional evolution. Empirical results show that fine-tuning MLLMs (multimodal large language models) on EmoS yields significant gains over zero-shot baselines, laying the foundation for the training and evaluation of future emotion recognition models and empathy models. The dataset and code are released with this publication package.

## Repository Structure

Only the main structure and representative file names are listed below.

```text
.
├── README.md
├── .gitignore
├── manifest.csv
├── file_counts.json
├── paper/
│   └── Association_for_Computational_Linguistics__ACL__conference-3.pdf
└── datasets/
    ├── data-final/
    │   ├── annotator_radar_filled.csv
    │   ├── annotator_radar_template.csv
    │   ├── annotator_radar_types.csv
    │   ├── Chinese/
    │   │   ├── basic7/
    │   │   │   ├── basic7_ds_high_confidence.xlsx
    │   │   │   └── basic7_ds_low_confidence.xlsx
    │   │   ├── goemotion/
    │   │   │   ├── front2500_training_data.xlsx
    │   │   │   ├── after2500_training_data.xlsx
    │   │   │   └── training_data_merged.xlsx
    │   │   └── Raw/
    │   ├── English/
    │   │   ├── basic7/
    │   │   │   ├── 3000_basic7_high_confidence_ge0.5.xlsx
    │   │   │   ├── 3000_basic7_low_confidence_lt0.5.xlsx
    │   │   │   ├── last2000_basic7_high_confidence_ge0.5.xlsx
    │   │   │   └── last2000_basic7_low_confidence_lt0.5.xlsx
    │   │   ├── goemotion/
    │   │   │   ├── goemotion_soft_labels_first3000.xlsx
    │   │   │   └── goemotion_soft_labels_last2000.xlsx
    │   │   └── train_splits/
    │   └── datasets/
    │       ├── ch-simsv2s/
    │       │   ├── meta.csv
    │       │   ├── First-2500/
    │       │   │   ├── a1.xlsx
    │       │   │   ├── a2.xlsx
    │       │   │   ├── a3.xlsx
    │       │   │   ├── combined_first2499.xlsx
    │       │   │   ├── combined_first2500.xlsx
    │       │   │   ├── confusion_a1.xlsx
    │       │   │   ├── confusion_a2.xlsx
    │       │   │   ├── confusion_a3.xlsx
    │       │   │   ├── analysis_outputs/
    │       │   │   └── Revisit/
    │       │   └── Last-2500/
    │       │       ├── chenpengyu.xlsx
    │       │       ├── liangjingxi.xlsx
    │       │       ├── wangqifeng.xlsx
    │       │       ├── combined_after2500.xlsx
    │       │       └── analysis_outputs_after2500/
    │       └── newdataset-MELD/
    │           ├── Annotations-3000/
    │           │   ├── 陈思琪train_sent_emo.xlsx
    │           │   ├── 任芳菲train_sent_emo.xlsx
    │           │   ├── train_sent_emo刘彦秀.xlsx
    │           │   └── analysis_outputs/
    │           └── Annotations-last-2000/
    │               ├── a10.xlsx
    │               ├── a11.xlsx
    │               ├── a12.xlsx
    │               └── analysis_outputs/
    └── streaming-finalsplit/
        ├── 中文_带句子.json
        ├── 英文_带句子.json
        ├── A Few Good Men/
        ├── Accepted/
        ├── Good Will Hunting/
        ├── The Newsroom/
        ├── Black Ice/
        ├── The Equation of Love and Death/
        ├── The Truman Show/
        └── ...
```

## Data Organization Notes

- `datasets/data-final/Chinese/` and `datasets/data-final/English/` are the simplified, release-oriented data folders.
- `datasets/data-final/datasets/` is the more complete package. It keeps annotation workbooks, intermediate organization, processing-side artifacts, analysis outputs, and additional result files.
- Directory names in this GitHub release have been normalized to English for easier international use.
- Some file names still remain in their original language to preserve one-to-one correspondence with source materials and annotation artifacts.

## Original Source Files and Reproducibility

- Due to copyright restrictions, we do not redistribute the original copyrighted source files from MELD and CH-SIMS v2 in this repository.
- All released annotations and derived tables are aligned with the corresponding original files from those datasets.
- In practice, you can obtain the original source files directly from the official MELD and CH-SIMS v2 dataset providers, match them by filename, and use them together with the annotations released here.
- The released annotation files are intended to be directly mappable to the original dataset items.

## Streaming Video Release

- The streaming portion is distributed separately via Google Drive rather than bundled as a tracked GitHub payload.
- If a Google Drive link is available, please use the author-provided release link.
- If the Google Drive link is missing or expired, please remind the authors to refresh it.
- The repository still keeps the folder structure and metadata so the streaming split remains understandable even without the source videos.

## Copyright and Usage

- Copyright of the EmoS annotations, derived tables, and repository-specific release files belongs to the EmoS authors unless otherwise noted.
- Copyright of the original source media and original base datasets remains with their respective copyright holders and dataset authors.
- For commercial use, please contact the authors first.
- For academic and non-commercial use, please follow the open-source license of this repository and also comply with the original terms, licenses, and citation requirements of MELD and CH-SIMS v2.
- By using this repository, you agree not to redistribute copyrighted source media in ways that violate the terms of the original data owners.

## Included Metadata Files

- `manifest.csv`: file-level release manifest
- `file_counts.json`: file counts and package sizes
- `paper/Association_for_Computational_Linguistics__ACL__conference-3.pdf`: published paper file used for this release

## Citation

If you use EmoS in academic work, please cite:

```bibtex
@inproceedings{guo-etal-2026-emos,
    title = "{E}mo{S}: A High-Fidelity Multimodal Benchmark for Fine-grained Streaming Emotional Understanding",
    author = "Guo, Pengze  and
      Liang, Jingxi  and
      Xie, Zhiwen  and
      Wang, Qifeng  and
      Wong, Derek F.",
    booktitle = "Proceedings of the 64th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2026",
    address = "San Diego, California",
    publisher = "Association for Computational Linguistics",
}
```
