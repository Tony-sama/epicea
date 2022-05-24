# epicea  
Dataset and data analysis of the article "EPICeA : A comprehensive radiobiologic assay using dynamic single cells phenotypic tracking under videomicroscopy"  
    
Notebooks:    
    - "radio-colab-transcription-extraction-txt-csv.ipynb": extraction of the dataset, organize txt transcription and encode them into csv files    
    - "radio-colab-radiation-based-profiling.ipynb": analysis of the dataset    
    - "pytoto-cell.ipynb": simple prototype of a python version of Toto-cell cell tree visualization    
    
Dataset architecture:    
    
glioblastoma_data    
├───extracted_data (data files extracted from raw_data/ folder)    
│   └───cell_behaviors    
│       ├───examples (examples of each type of data file)    
│       ├───videos_transcriptions_csv (csv conversion of the videos_transcriptions_txt/ folder files)    
│       └───videos_transcriptions_txt (manual transcription of cell behaviors event from videos as text files)    
└───raw_data    
    └───2021_lea_renaud_internship (Raw data from experiements on glioblastoma radiosensitivity of Lea-Isabelle Renaud's internship at CRCINA, university of Nantes, France)    
        ├───original (original dataset)    
        ├───reorganized ()    
    
Processed dataset is in folder "glioblastoma_data/extracted_data/cell_behaviors":    
    - "examples" contains examples of each type of data file of other foldes (txt and csv)    
    - "videos_transcriptions_txt" contains the selected original text transcriptions by Lea Renaud, organized by experiement type (normal/sox) and experiement group (n1/n2/n3). Some files were discard for lacking informations.    
    - "videos_transcriptions_csv" contains the csv encoding of those text trancription organized the same way with an additional subfolder grouping file per radiation level (0gy/2gy/4gy/8gy/10gy/15gy).    
    
Folder "glioblastoma_data/raw_data" contains all original text transcriptions by Lea Renaud as it was provided before processing. Not used in this repository notebooks. Contains additional files not used in the notebook analysis.    
    
Repository folder tree:    
.    
├── glioblastoma_data    
│   ├── extracted_data    
│   │   └── cell_behaviors    
│   │       ├── examples    
│   │       │   ├── example_videos_transcriptions_csv.csv    
│   │       │   └── example_videos_transcriptions_txt.txt    
│   │       ├── README.txt    
│   │       ├── videos_transcriptions_csv    
│   │       │   ├── normal    
│   │       │   │   ├── n1    
│   │       │   │   │   ├── 0gy    
│   │       │   │   │   ├── 10gy    
│   │       │   │   │   ├── 15gy    
│   │       │   │   │   ├── 2gy    
│   │       │   │   │   ├── 4gy    
│   │       │   │   │   └── 8gy    
│   │       │   │   ├── n2    
│   │       │   │   │   ├── 0gy    
│   │       │   │   │   ├── 10gy    
│   │       │   │   │   ├── 15gy    
│   │       │   │   │   ├── 2gy    
│   │       │   │   │   ├── 4gy    
│   │       │   │   │   └── 8gy    
│   │       │   │   └── n3    
│   │       │   │       ├── 0gy    
│   │       │   │       ├── 10gy    
│   │       │   │       ├── 15gy    
│   │       │   │       ├── 2gy    
│   │       │   │       ├── 4gy    
│   │       │   │       └── 8gy    
│   │       │   └── sox    
│   │       │       ├── n1    
│   │       │       │   ├── ct    
│   │       │       │   └── ko    
│   │       │       └── n2    
│   │       │           ├── ct    
│   │       │           └── ko    
│   │       └── videos_transcriptions_txt    
│   │           ├── normal    
│   │           │   ├── n1    
│   │           │   ├── n2    
│   │           │   └── n3    
│   │           └── sox    
│   │               ├── n1    
│   │               └── n2    
│   └── raw_data    
│       └── 2021_lea_renaud_internship    
│           ├── original    
│           │   ├── crisp    
│           │   │   ├── ct sox 2 0Gy n2    
│           │   │   ├── ct sox 2 4 Gy n2    
│           │   │   ├── mars-sox2    
│           │   │   ├── sox 2 crispr n2 0Gy    
│           │   │   └── sox 2 crispr n2 4Gy    
│           │   └── normal    
│           │       ├── 0 Gy    
│           │       ├── 10gy n2    
│           │       ├── 15Gy n2    
│           │       ├── 15gyN3    
│           │       ├── 2016    
│           │       ├── 2Gy    
│           │       ├── 4Gy    
│           │       └── 8Gy    
└── reorganized    
│               ├── normal    
│               │   ├── 0 Gy    
│               │   │   ├── 0Gy n2    
│               │   │   ├── 2020 11 04 n1    
│               │   │   ├── 2711    
│               │   │   └── n3 part 1 Ogy    
│               │   ├── 10 Gy    
│               │   │   ├── 10 Gy n1    
│               │   │   ├── 10gy n2    
│               │   │   └── 10 Gy n3    
│               │   ├── 15Gy    
│               │   │   ├── 15 Gy n1    
│               │   │   ├── 15Gy n2    
│               │   │   └── 15gyN3    
│               │   ├── 2Gy    
│               │   │   ├── 2020 n2 2Gy    
│               │   │   ├── 2021 n3 2gy    
│               │   │   └── 2Gy n1    
│               │   ├── 4Gy    
│               │   │   ├── 4Gy n1    
│               │   │   ├── 4Gy n2    
│               │   │   └── 4Gy n3    
│               │   └── 8Gy    
│               │       ├── 8Gy n1    
│               │       ├── 8Gy n2    
│               │       └── 8gy n3    
│               └── sox    
│                   ├── N1    
│                   │   ├── CT    
│                   │   └── KO    
│                   └── N2    
│                       ├── CRISPR    
│                       └── CT    
├── LICENSE    
├── pytoto-cell.ipynb    
├── radio-colab-radiation-based-profiling.ipynb    
├── radio-colab-transcription-extraction-txt-csv.ipynb    
└── README.md    
    
146 directories, 1920 files    
