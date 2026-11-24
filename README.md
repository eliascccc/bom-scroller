## BOM scroller

A time-based BOM navigator built for ERP data.


---

## Overview

BOM scroller is a local web tool for exploring how a Bill of Materials (BOM) evolves over time. It does **not** compare static version snapshots. Instead, it reconstructs BOMs from a **data source** and compares them visually.

The goal is to understand *what changed, where,* and *when* — in a way that matches how BOMs actually behave in real systems.

---
## Example
<img width="1827" height="840" alt="image" src="https://github.com/user-attachments/assets/ebb80646-baac-45c4-9f1d-8d4422cca38a" />

---


## Coloring logic

Any changes from left to center are marked in: Blue

Any changes from Center to right are marked in: Purple

Change is defined by parts that are: added / removed / replaced / qty changed

Green indicates the current version

---

## Intended use case

- Fast navigation across many revisions  
- Rapid review of BOM changes  
- Clear visual overview of structural changes  
- For teams that currently export to Excel or manually compare versions  

Built for:
- date-effective ERP data  
- human understanding, not raw diff output  

For a detailed explanation of the underlying design and assumptions, see [BOM assumptions](bom-assumptions.md)

---


## Running locally

```bash
pip install flask
python app.py
```

Then open:

```
http://127.0.0.1:5000
```

---
## How this compares to other projects

#### File-based BOM diff tools

[bom-diff](https://github.com/ttran-tech/bom-diff)  
→ Upload and compare two BOM files (Excel/CSV)

[BOM Compare Tool (Sierra Circuits)](https://www.protoexpress.com/tools/bom-compare-tool/)  
→ Upload BOM files and highlight added/removed/changed parts

[Excel BOM Comparer](https://ddbim.com/excelbomcomparer/)  
→ Compare two revisions directly in Excel

---

#### ERP / PLM tools

eg. OpenBOM, NetSuite tools, ERPNext BOM compare

These allow comparing BOM revisions inside a system, typically:

- select BOM A  
- select BOM B  
- view differences  

---

#### BOM scroller (this project)

BOM scroller takes a different approach:

- No file upload  
- No “compare A vs B”  
- No static snapshots  

Instead:

→ Scroll through BOM versions over time, directly from ERP data

---

## Project status

This is a concept prototype with focus on visual clarity and realistic BOM behavior. Not production ready.
