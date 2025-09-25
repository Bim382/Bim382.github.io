# GitHub Pages Deployment Setup

This repository contains a Quarto website that is configured for automatic deployment to GitHub Pages at `https://bim382.github.io`.

## Setup Instructions

To complete the deployment setup, you need to:

1. **Enable GitHub Pages in Repository Settings:**
   - Go to repository Settings → Pages
   - Under "Source", select "GitHub Actions"
   - Save the changes

2. **Trigger the Deployment:**
   - The workflow will automatically run when changes are pushed to the `main` branch
   - Or you can manually trigger it from Actions → "Publish Quarto Website" → "Run workflow"

## How it Works

- The GitHub Actions workflow (`.github/workflows/publish.yml`) automatically:
  - Sets up R, Python, and Quarto environments
  - Installs required dependencies
  - Renders the Quarto website to the `docs` folder
  - Deploys the site to GitHub Pages

## Configuration

- **Output Directory**: `docs` (configured in `_quarto.yml`)
- **Site URL**: `https://bim382.github.io` (configured in `_quarto.yml`)
- **Deployment Method**: GitHub Pages with GitHub Actions

## Files

- `_quarto.yml`: Main Quarto configuration
- `.github/workflows/publish.yml`: GitHub Actions workflow for deployment
- Various `.qmd` files: Website content and pages

The website should be accessible at `https://bim382.github.io` once the deployment completes successfully.