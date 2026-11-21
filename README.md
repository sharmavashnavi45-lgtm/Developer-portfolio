# Developer-portfolio
# Hi there, I'm Vaishnavi Sharma 👋

Welcome to my official Developer Portfolio repository! This space serves as the central hub for my academic coursework, technical lab assignments, and development projects as part of my BCA (Honors with Research in AI & Data Science) degree at K.R. Mangalam University.

---

### 🚀 About Me
- **Degree:** BCA (Honors with Research in AI & Data Science) [2026–2029]
- **Institution:** K.R. Mangalam University, Gurugram
- **Location:** New Delhi, India
- **Core Interests:** Artificial Intelligence, Data Science, Python Programming, and Version Control Systems.

---

### 🛠️ Technical Skills & Tools
- **Programming Languages:** Python, Bash/Shell Scripting
- **Developer Tools & OS:** Git, GitHub, VS Code, Linux Terminal, Markdown
- **Core Concepts:** File Systems, Process Management, Version Control, Data Analytics

---

#!/usr/bin/env bash
set -e

REPO_DIR="${1:-Developer-portfolio}"
cd "$REPO_DIR"

mkdir -p src tests docs

cat <<'EOF' > README.md
# Vaishnavi Sharma — Developer Portfolio

**BCA (AI & Data Science)** | K.R. Mangalam University, Gurugram | Batch 2026–29

## Repository Index

| # | Repository | URL | Description | Tech Stack | Status |
| :---: | :--- | :--- | :--- | :--- | :--- |
| 1 | `cse103-lab-LAB3` | https://github.com/sharmavashnavi45-lgtm/cse103-lab-LAB3 | CSE103 lab — Git workflows, APIs, Shell scripting, and `src/`/`tests/`/`docs/` layout | Git, Python, Bash | Active |
| 2 | `Dscapstone` | https://github.com/sharmavashnavi45-lgtm/Dscapstone | Data Science Capstone Project — structured data analysis | Python, Data Analytics | Active |
| 3 | `Developer-portfolio` | https://github.com/sharmavashnavi45-lgtm/Developer-portfolio | Central portfolio index, learning roadmap, and coding platform progress tracker | Markdown, HTML/CSS | Active |

## Current Skills

- **Python:** 60%
- **Linux / Bash:** 50%
- **Git / GitHub:** 65%
- **SQL (SQLite):** 50%

## Documents & Trackers

- **Resume:** Vaishnavi Sharma Resume
- **Learning Roadmap:** [LEARNING_ROADMAP.md](./LEARNING_ROADMAP.md)
- **Progress Tracker:** [PROGRESS.md](./PROGRESS.md)
EOF

cat <<'EOF' > .gitignore
# Python & virtual environments
__pycache__/
*.py[cod]
*.egg-info/
.venv/
venv/
env/

# IDEs & OS files
.vscode/
.idea/
.DS_Store
Thumbs.db
EOF

git status -s
git add README.md .gitignore src tests docs
git commit -m "feat: add tabular repository index and update repo structure"
git push origin main

echo "Result: Repository index updated and pushed successfully."
