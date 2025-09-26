# AI Voice Bias: The Erosion of Vocal Diversity

A research website examining the socioindexical influence of standardized AI voices on human communication and identity.

## Overview

This website presents critical research on how the proliferation of biased AI voices threatens to entrench harmful stereotypes, diminish vocal diversity, and fundamentally alter human communication patterns.

## Key Features

- **Three Critical Takeaways**: Comprehensive analysis of AI voice bias impacts
- **Audio Examples**: Problematic AI voice implementations from ElevenLabs
- **Research Documents**: Supporting academic and journalistic sources
- **Methodology**: Framework for detecting and addressing AI voice bias

## Structure

```
├── index.html              # Main website file
├── styles.css              # CSS styling
├── elevenlabs_flirty/      # Audio examples directory
├── PDFs/                   # Research documents directory
└── README.md               # This file
```

## Deployment to GitHub Pages

### Option 1: Direct Repository Deployment

1. Push this repository to GitHub
2. Go to repository Settings → Pages
3. Select "Deploy from a branch" as source
4. Choose "main" branch and "/ (root)" folder
5. Click Save

### Option 2: GitHub Actions Deployment

Create `.github/workflows/pages.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v4
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: '.'
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

## Adding New Content

### Audio Examples
1. Add new audio files to the `elevenlabs_flirty/` directory
2. Update the audio showcase section in `index.html`
3. Follow the existing pattern for audio items

### Research Documents
1. Add PDF files to the `PDFs/` directory
2. Update the document list section in `index.html`
3. Ensure proper URL encoding for filenames with spaces

### Placeholder Content
I've put  sections for future audio examples and case studies. Replace the placeholder content with actual materials as they become available.