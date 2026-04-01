## BOM Scroller

A time-based BOM navigator built for live ERP data.


---

## Overview

BOM Scroller is a local web tool for exploring how a Bill of Materials (BOM) evolves over time.

It does **not** compare static version snapshots.  
Instead, it reconstructs BOMs from a **date-driven row model** and compares them visually.

The goal is simple:

> Understand *what changed, where,* and *when* — in a way that matches how BOMs actually behave in real systems.

---
## Example
<img width="1810" height="809" alt="image" src="https://github.com/user-attachments/assets/646dccd5-8bb9-4215-99a6-efa599fd9ab5" />

---


## Coloring logic

| Relation                  | Color   |
|--------------------------|--------|
| Change Left vs Center    | Blue   |
| Change Center vs Right   | Purple |

Changes include:
- different quantity
- different part number
- add new or remove part

---

## What this tool is

- A visual diff tool for BOM evolution  
- Based on date-effective data  
- Designed for human understanding  

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
## How it compares

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

#### BOM Scroller (this project)

BOM Scroller takes a different approach:

- No file upload  
- No “compare A vs B”  
- No static snapshots  

Instead:

→ Scroll through BOM versions over time, directly from ERP data

---
## Project status

This is a concept prototype.

The focus is on:

- data model correctness  
- visual clarity  
- realistic BOM behavior  

Not production readiness.
