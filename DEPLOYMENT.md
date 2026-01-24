# Deployment Guide

This repository is configured to automatically deploy to GitHub Pages.

## Setup

To enable deployment:

1. Go to your GitHub repository settings
2. Navigate to **Settings > Pages**
3. Under "Build and deployment", select:
   - **Source**: GitHub Actions
4. Save the settings

## How it Works

The deployment is handled by a GitHub Actions workflow (`.github/workflows/deploy.yml`) that:

1. Triggers on every push to the `main` branch
2. Can also be manually triggered via workflow_dispatch
3. Uploads the repository contents as a GitHub Pages artifact
4. Deploys the artifact to GitHub Pages

## Manual Deployment

You can manually trigger a deployment by:

1. Going to the **Actions** tab in your repository
2. Selecting the "Deploy to GitHub Pages" workflow
3. Clicking "Run workflow"

## Accessing the Deployed Site

Once deployed, your site will be available at:
```
https://bitman.github.io/WorkHigher/
```

## Local Development

This is a static HTML website. To preview locally:

1. Open `index.html` directly in a web browser, or
2. Use a local web server:
   ```bash
   python -m http.server 8000
   ```
   Then visit `http://localhost:8000`
