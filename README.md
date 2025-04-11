

```markdown
# 🗂️ version-controlled-devops-project

This is a sample DevOps project demonstrating proper **Git-based version control workflow** using a Flask app.  
It follows best practices including feature branching, commits, pull requests, `.gitignore`, and markdown documentation ✅  
🛠️ **We also resolved merge conflicts** to simulate real-world collaborative workflows.

---

## ⚙️ Tools & Technologies Used

- 🐍 Python 3.12
- ⚙️ Flask 2.2.5
- 🌐 Git & GitHub
- 📝 Markdown (for project documentation)

---

## 🌱 Git Workflow Lifecycle (Real DevOps Practice)

```mermaid
graph TD
A[Stage 1: Start in dev branch] --> B[Stage 2: Build base app (app.py, index.html)]
B --> C[Stage 3: Push dev to GitHub]
C --> D[Stage 4: Merge dev → main for production]
D --> E[Stage 5: Client requests feature]
E --> F[Stage 6: Create feature/about-page from dev]
F --> G[Stage 7: Push → PR → Resolve conflicts → Merge to dev after testing]
G --> H[Stage 8: Final review → Merge dev → main → Tag release]
```

---

## 📦 Stages & Commands

### 🔹 Stage 1: Initialize Repo & Dev Branch
```bash
git init
git checkout -b dev
```

### 🔹 Stage 2: Create Initial App Code
- `app.py`
- `templates/index.html`
- `requirements.txt`

```bash
git add .
git commit -m "Initial dev version of Theme Farm app"
```

### 🔹 Stage 3: Push dev Branch to GitHub
```bash
git push -u origin dev
```

### 🔹 Stage 4: Merge dev → main (First Production Merge)
```bash
git checkout main
git merge dev
git push origin main
```

### 🔹 Stage 5: Feature Request by Client
(e.g. Add About Page)

---

### 🔹 Stage 6: Create Feature Branch from Dev
```bash
git checkout dev
git pull
git checkout -b feature/about-page
```

### 🔹 Stage 7: Develop Feature & Push
Make changes in `app.py`, add `about.html`

```bash
git add .
git commit -m "Add About page feature"
git push -u origin feature/about-page
```

🛠️ If there are merge conflicts while merging PR → resolve them locally:
```bash
# After pulling conflicting dev branch:
git merge dev
# Edit files, resolve conflicts
git add .
git commit -m "Resolve merge conflict"
```

---

### 🔹 Stage 8: Final Review → Merge dev → main & Tag
```bash
git checkout main
git merge dev
git tag -a v1.0 -m "Production-ready release"
git push origin main
git push origin v1.0
```

---

## 📁 Project Structure

```
version-controlled-devops-project/
├── app.py
├── requirements.txt
├── .gitignore
├── templates/
│   ├── index.html
│   └── about.html
└── README.md
```

---

## 🛡️ .gitignore Implementation

We created `.gitignore` to exclude unnecessary or sensitive files:

```
.env
*.log
__pycache__/
.venv/
```

Files like `.env` and `error.log` were created locally for demo but successfully excluded from Git.

---

## 🧪 How to Run Locally

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

🧭 Navigate to:
- Home: `http://localhost:5000/`
- About: `http://localhost:5000/about`

---

## ✅ All Tasks Completed

- 📌 Git initialized, `dev` branch created
- 🧪 Initial app pushed to `dev`
- 🔁 Merged into `main` for first release
- 🧩 New feature added via `feature/about-page`
- 🔀 Pull Request & Merge Conflict resolved
- 🏁 Final merge → `main`
- 🏷️ Tag `v1.0` created
- 🛡️ `.gitignore` used to ignore `.env` and `*.log`
- 📝 Markdown used for clear documentation

---

## 🧠 Key Concepts Practiced

- Dev → Main merge flow
- Feature branching (`feature/*`)
- Merge conflict resolution
- Tagging and release
- Clean repo management with `.gitignore`
- Markdown for professional documentation

---

## ✍️ Author

👤 **Prasad0108-ux**  
🔗 [GitHub Profile](https://github.com/prasad0108-ux)
