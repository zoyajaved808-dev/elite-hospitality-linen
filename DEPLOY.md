# Deployment Guide: GitHub & Vercel

This guide explains how to deploy your newly created **Elite Hospitality Linen Website** to **GitHub** and **Vercel**.

---

## 1. Push to GitHub

Since Git is not globally initialized on your system yet, follow these steps:

### Option A: Using VS Code (Recommended & Simplest)
1. Open the project folder `D:\website\laudary web` in **VS Code**.
2. Click on the **Source Control** icon on the left sidebar (shortcut: `Ctrl+Shift+G`).
3. Click the **Publish to GitHub** button.
4. Choose whether to publish it as a **Public** or **Private** repository.
5. VS Code will automatically initialize Git, stage files, commit them, and push them to your GitHub account.

### Option B: Using GitHub Desktop
1. Download and open [GitHub Desktop](https://desktop.github.com/).
2. Go to `File` -> `Add Local Repository...`.
3. Select your project folder: `D:\website\laudary web`.
4. Click **Create a Repository here** (since it doesn't have Git initialized).
5. Fill in the repository details and click **Create Repository**.
6. Click **Publish Repository** to upload it to your GitHub account.

---

## 2. Deploy to Vercel

Once your code is pushed to GitHub, deploying to Vercel is free and takes under 2 minutes:

### Option A: Import via Vercel Web Dashboard (Recommended)
1. Go to [Vercel](https://vercel.com/) and sign in using your GitHub account.
2. Click the **Add New...** button and select **Project**.
3. Under "Import Git Repository", find your repository (e.g., `laudary-web`) and click **Import**.
4. Vercel will automatically detect **Vite** as the framework:
   - **Framework Preset**: `Vite`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
5. Click **Deploy**.
6. Once completed, Vercel will give you a public production URL (e.g., `https://laudary-web.vercel.app`).

### Option B: Deploy using Vercel CLI
If you prefer the command line:
1. Open terminal/PowerShell and install Vercel CLI globally:
   ```bash
   npm install -g vercel
   ```
2. Navigate to your project directory (if not already there):
   ```bash
   cd "D:\website\laudary web"
   ```
3. Run the login command:
   ```bash
   vercel login
   ```
4. Deploy by typing:
   ```bash
   vercel
   ```
5. Follow the command prompts (use defaults). Once the preview build looks good, deploy to production:
   ```bash
   vercel --prod
   ```
