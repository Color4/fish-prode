---
title: "FISH-ProDe Database"
---

# How to extract/generate a database

To run, `FISH-ProDe` requires at least one database to be located in the `db/` folder. Each database should consists of a folder with one txt file per chromosome, containing an ordered list of oligonucleotide start sites. The length of the oligonucleotides should be encoded in the database folder name (e.g., `kmerXX_...`).

Currently, each database should have one file per chromosome, including chr1-chr22, chrX, and chrY. In the future we will make the script able to recognize which chromosomes are available.

The `extract_database.py` allow to generate a compatible txt-like database folder from a sqlite3 database. The sqlite3 database must contain a table with the following columns:

* `START` and `CHR` if the database is of genomic oligonucleotides (default).
* `GSTART` and `CHR` if the database id of transcriptomic nucleotides (`--rna` flag).

Use `extract_database.py -h` for more details on how to run the script.

Ready to download databases will be made available in the near future.