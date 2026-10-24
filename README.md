# Hisaab Saathi

A free guide that helps small businesses in India understand digital tax filing: which GST, income tax and TDS filings apply, what is due next, and which papers to keep ready.

It is a plain static site in a single file. The HTML, CSS and JavaScript are all inside `index.html`, so it looks right wherever you open it. There is no build step, no server and no database.

## Files

- `index.html` the whole site: the page (HTML), the design (the `<style>` block) and the GST calculator, filing finder, due-date list and checklist (the `<script>` block)
- `render.yaml` tells Render how to host it

## Run it on your computer

Double-click `index.html`, or run `python3 -m http.server 8000` in this folder and open http://localhost:8000.

## Host it publicly on Render (free)

1. Create a free account at https://github.com and make a new **public** repository called `hisaab-saathi`.
2. Upload these files to it. On the repository page choose **Add file > Upload files**, drag in `index.html`, `render.yaml` and `README.md`, then **Commit changes**.
3. Create a free account at https://render.com and sign in with GitHub.
4. Click **New > Static Site** and choose your `hisaab-saathi` repository.
5. Fill in the form:
   - Name: `hisaab-saathi`
   - Branch: `main`
   - Build Command: leave empty
   - Publish Directory: `.` (a single dot)
6. Click **Create Static Site**. After about a minute Render shows your public address, which looks like `https://hisaab-saathi.onrender.com`. If the name is taken, Render adds letters to it. That is the link to submit.

Every time you change a file on GitHub, Render redeploys on its own.

## Backup hosting

If Render gives trouble, GitHub Pages works too: repository **Settings > Pages**, pick the `main` branch and the root folder, and your site appears at `https://<your-username>.github.io/hisaab-saathi/`.

## Before you submit

Tax limits and due dates change. Open gst.gov.in and incometax.gov.in and check the figures in the `<script>` block of `index.html` against the latest notices. The thresholds are in the `buildFilings` function and the due dates are in the `RULES` list.
