# Probon — Software Requirements Specification (SRS) Package

This directory contains the finalized **Software Requirements Specification (SRS)** document for **Probon**, restructured to strictly follow the official 5-chapter course template for **UCS 503 (Software Engineering)** at Thapar Institute of Engineering and Technology, Patiala.

The document is written in a direct, natural third-year university style, preserving all 11 core functional modules, business rules, and technical requirements while eliminating enterprise boilerplate and redundant appendices.

---

## 📁 Directory Contents

| File / Folder | Description |
| :--- | :--- |
| **`srs.pdf`** | Compiled 17-page SRS document (`scrreprt` class) matching the course template's 5 main chapters, figures, and tables. |
| **`srs.tex`** | Master LaTeX SRS document formatted according to the 5-chapter course specification. |
| **`diagrams/`** | Editable PlantUML (`.puml`) source files and rendered PNGs for all 5 simplified diagrams. |
| **`images/`** | Diagram PNG assets referenced directly by `srs.tex`. |
| `*.png` | Diagram images duplicated in the root of `SRS/` to ensure zero compilation path errors regardless of how files are imported into Overleaf. |

---

## 🖼️ Simplified Course Diagrams

Following the template's structure, 5 simple and legible diagrams are integrated:

1. **Figure 1.1: Overall Workflow of the Probon Platform** (`workflow.png`, source: `diagrams/workflow.puml`)
   - Shows the student cycle (tasks, commits, evidence submission) and teacher cycle (class management, verification, XP attribution).
2. **Figure 2.1: Probon User Hierarchy and Operational Responsibilities** (`user_types.png`, source: `diagrams/user_types.puml`)
   - Inspired by Figure 2.1 of the course template: shows Teachers, Students (including designated Team Leaders), and host-level Infrastructure Administrators.
3. **Figure 2.2: Probon Data Overview and Core Entity Relationships** (`data_overview.png`, source: `diagrams/data_overview.puml`)
   - A clean horizontal overview showing key relational entities (Users, Classes, Teams, Projects, Tasks, Verifications, Contributions, Repositories, GitHub Activities) and their core fields.
4. **Figure 2.3: Probon Simplified 4-Tier System Architecture** (`system_architecture.png`, source: `diagrams/system_architecture.puml`)
   - Delineates Client Layer (React 19 SPA), API Gateway (Express REST + security middleware), Domain Service Layer (Services + Heuristic Evaluator), and Persistence Layer (SQLite WAL mode + GitHub REST API).
5. **Figure 2.4: Task Verification and Lifecycle Activity Flow** (`task_activity.png`, source: `diagrams/task_activity.puml`)
   - Illustrates the 4-stage task state machine (`Planned` $\rightarrow$ `In Progress` $\rightarrow$ `Verification Pending` $\rightarrow$ `Completed`) and teacher approval/rejection branches.

---

## 🚀 How to Use & Submit to Overleaf / GitHub

### Option A: Uploading to Overleaf
1. Open your project on [Overleaf](https://www.overleaf.com/).
2. Upload `srs.tex` and all image files from `images/` (or upload the `images` folder).
3. Set the compiler to **pdfLaTeX** or **XeLaTeX**.
4. Click **Recompile**. The 17-page specification compiles with zero errors.

### Option B: Local Compilation
Using the local Tectonic engine:
```bash
tectonic srs.tex --outdir .
```
Or with TeX Live:
```bash
pdflatex srs.tex
pdflatex srs.tex
```

---

## 👥 Project Metadata

- **Course:** UCS 503 -- Software Engineering
- **Project Title:** Probon: An Educational Collaborative Project Management and Contribution Verification Platform
- **Authors:**
  1. Vanshaj Sharma (Roll No: 1024160114)
  2. Aryan Thakkar (Roll No: 1024160100)
- **Group:** 3P14, BE Third Year, Computer Engineering
- **Faculty Guide / Reviewer:** Dr. Anushka, Assistant Professor, Computer Science and Engineering Department, Thapar Institute of Engineering and Technology, Patiala
- **Automated Backend Tests:** 52 / 52 Passed (100% test pass rate across 4 suites)
- **Frontend Production Bundle:** $412.44$ kB JS ($113.60$ kB gzip), $29.64$ kB CSS ($6.30$ kB gzip)
