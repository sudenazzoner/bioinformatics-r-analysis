# 🧬 Bioinformatics Data Analysis in R

A collection of R scripts and data files for computational genomics and
bioinformatics analysis, covering dinucleotide frequency analysis,
viral genome processing, and multi-format data parsing.

---

## 📁 Repository Contents

```
bioinformatics-r-analysis/
├── homework_part_1.R              # Dinucleotide frequency analysis (multiple sequences)
├── data/
│   ├── Chikungunya_virus.csv      # Chikungunya viral genome dataset
│   ├── Saccharomyces_cerevisiae.txt  # Yeast reference genome sequence
│   ├── comparison.ccap            # Sequence comparison output
│   └── roster_data.json           # JSON-format course roster data
└── README.md
```

---

## 🔬 Analysis 1: Dinucleotide Frequency Mapping

**File:** `homework_part_1.R`

Scans DNA sequences and maps positional occurrences of all **16 possible dinucleotide pairs** (AT, AA, AG, AC, GG, GC, GA, GT, CC, CT, CG, CA, TT, TA, TC, TG).

Applied to 4 different sequences including:
- Chikungunya virus genome fragments
- *Saccharomyces cerevisiae* (baker's yeast) reference sequence
- Custom query sequences

```r
source("homework_part_1.R")

sequence <- "TTAGGATTAT..."  # Any DNA string
result <- find_differential_duos(sequence)

# Returns named list: each dinucleotide → vector of positions
# e.g. $CG → [3, 47, 112, ...]
print(result)
```

**Why dinucleotide context matters in Precision Medicine:**
- **CpG sites** are major epigenetic methylation targets — altered in cancer
- **Mutational signatures** depend on trinucleotide/dinucleotide context
- **SNP calling** considers local sequence context for accuracy

---

## 🦠 Analysis 2: Chikungunya Virus Genome Data

**File:** `data/Chikungunya_virus.csv`

Chikungunya virus (CHIKV) is a re-emerging RNA arbovirus with significant
public health impact. This dataset is used for:
- Sequence feature extraction
- Comparative genomics with reference strains
- Mutation pattern analysis

**Precision Medicine relevance:** Viral genomics informs vaccine design and
antiviral target identification — core applications of personalized infectious disease management.

---

## 🍺 Analysis 3: *Saccharomyces cerevisiae* Reference Genome

**File:** `data/Saccharomyces_cerevisiae.txt`

~5000 bp segment of the *S. cerevisiae* genome used as a reference sequence
for alignment and dinucleotide analysis. Yeast is a key model organism for:
- Gene function studies
- Drug target validation
- Evolutionary genomics

---

## 📊 Analysis 4: JSON Data Parsing

**File:** `data/roster_data.json`

Demonstrates parsing of structured **JSON data** in a bioinformatics context —
the same pattern used to consume genomic API responses (e.g. Ensembl REST API,
NCBI Entrez).

---

## 🧠 Key Skills Demonstrated

| Skill | Description |
|---|---|
| Sliding window analysis | Dinucleotide position mapping across full sequences |
| Multi-format I/O | CSV, TXT, JSON data handling in R |
| Genomic data processing | Real viral and model organism sequences |
| Functional R programming | Modular, reusable functions with clear I/O |

---

## 🛠️ Requirements

Base R only — no additional packages required.

```r
# Tested on R 4.x
source("homework_part_1.R")
```

---

## 👤 Author
[Your Name] — Molecular Biology Graduate  
Applying to M.Sc. Precision Medicine, University of Vienna
