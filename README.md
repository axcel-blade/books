# 📚 Computer Science Books

This repository is a curated collection of essential and recommended books for learning and mastering various areas of Computer Science. Whether you're a beginner starting your journey or an experienced developer looking to deepen your knowledge, this list includes resources across a wide range of topics including:

* **Algorithms and Data Structures**
* **Programming Languages**
* **Computer Architecture**
* **Operating Systems**
* **Databases**
* **Software Engineering**
* **Artificial Intelligence & Machine Learning**
* **Cybersecurity**
* **Networking**
* **Theory of Computation**
* **And more...**

The goal is to help students, self-learners, and professionals find the right materials to support their learning paths.

Feel free to contribute by suggesting new titles, correcting errors, or organizing the list better!

---

## Library layout

PDFs are grouped by publisher, then by imprint or series. Use plain ASCII in file names (regular hyphens, not special dash characters), and put editions in parentheses, for example `Title (3rd Edition).pdf`.

| Location | Contents |
| --- | --- |
| `For Dummies/` | For Dummies titles |
| `OReilly/Cookbooks/` | O'Reilly cookbook-style titles |
| `OReilly/Head First/` | Head First series |
| `OReilly/Learning/` | Learning … series |
| `OReilly/In a Nutshell/` | … in a Nutshell series |
| `OReilly/General/` | Other O'Reilly titles that are not part of the series folders above |

---

## How to Contribute (book uploads)

Use the **`upload-books`** branch so additions are reviewed together before they land on `main`.

1. Fork the repository and clone your fork.
2. Add this repository as `upstream` (optional but helpful) and fetch **`upload-books`**:
   ```bash
   git remote add upstream https://github.com/<owner>/books.git
   git fetch upstream upload-books
   git checkout -b my-new-books upstream/upload-books
   ```
   If your fork does not have `upload-books` yet, create it from `upstream/upload-books` in the GitHub UI, or run `git push origin upload-books` once you have that branch locally (see branch note below).
3. Add PDFs under **`For Dummies/`** or **`OReilly/<series>/`**, using the naming style in [Library layout](#library-layout).
4. Commit, push to your fork, and open a **pull request into `upload-books`** (base = `upload-books`, compare = your branch). A GitHub Action checks that only allowed PDF paths changed and that each file is under 95 MiB.
5. After review, a maintainer merges your PR into `upload-books`, then merges **`upload-books` → `main`** when the batch is ready.

**Repository maintainers:** ensure branch **`upload-books`** exists on GitHub (same tip as `main` is fine). If it is missing, create it from the current default branch and push: `git checkout -b upload-books main && git push -u origin upload-books`.

Other changes (README, workflows, renames) should use a normal pull request **into `main`**, not the upload-only flow.