# IML — Introduction to Machine Learning

Public learning repo for my Introduction to Machine Learning coursework. Notes, notebooks, and resource pages I'm collecting as I work through the material.

## Structure

- `modules/` — lab notebooks organized by module (`M0X/M0X-L01`, `M0X-L02`), each with its instructions
- `readings/` — lecture materials and curated resource pages (HTML + PDF)
- `notes/` — personal notes
- `summary/` — per-lab study summaries (local only)
- `datasets/` — oversized datasets, gitignored and kept locally (see `datasets/README.md`)
- `learning/` — scratch notebooks (start with `learning/hello_world.ipynb`)

## Resource pages

Standalone HTML guides in `readings/`:

- **Module 8 Lecture Materials** — Introduction to ML concepts
- **Python Libraries for Cybersecurity** — foundational → AI integration toolkit
- **Recommended Cybersecurity Datasets** — CICIDS, UNSW-NB15, NSL-KDD, etc.
- **Project Documentation Worksheet** — fillable CRISP-DM capstone template

## Running the notebooks

```bash
pip install jupyter numpy pandas scikit-learn
jupyter notebook
```

Then open anything under `modules/`.

## Disclaimer

This is a personal learning repo. Code and notes here are works in progress and not intended for production use.
