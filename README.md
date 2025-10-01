# ☁️ Colab Setup Instructions

If you are working on this project in **Google Colab**, follow these steps to clone, configure, and push changes to GitHub.

---

## 1. Clone the repository into Colab
```bash
cd /content
git clone https://github.com/ameya1252/nlp-usc-project.git
cd nlp-usc-project
```

---

## 2. Configure your Git identity
Each teammate must set their GitHub username and email (so commits are attributed correctly):

```bash
git config user.name "<your-github-username>"
git config user.email "<your-github-email>"
```

---

## 3. Authenticate with GitHub
Since Colab sessions are temporary, authentication resets each time. Use a **Personal Access Token (PAT)**.

1. Create a PAT:  
   - Go to GitHub → Settings → Developer settings → **Personal Access Tokens** → Fine-grained tokens.  
   - Give it `repo` access at minimum.  

2. Set the remote URL with your token (replace `<TOKEN>` and `<USERNAME>`):
```bash
git remote set-url origin https://<TOKEN>@github.com/<USERNAME>/nlp-usc-project.git
```

✅ Now `git push` and `git pull` will work without asking for username/password.

---

## 4. Typical workflow in Colab
Whenever you make changes in the notebook:

```bash
# Get the latest updates
git pull origin main

# Stage your changes
git add CSCI544_ARC_AGI_Starter.ipynb

# Commit with a message
git commit -m "Update notebook with <your changes>"

# Push to GitHub
git push origin main
```

⚠️ Remember: each **new Colab runtime** means you’ll need to re-run the setup (clone + config + remote with PAT).
