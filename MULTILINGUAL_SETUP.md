# Multilingual Website Setup (xample of french)

## Summary of Changes

### What changed:

#### 1. Directory Structure

```
RSAfrica26/
├── en/
│   ├── index.qmd                    (English home page)
│   ├── registration.qmd             (English registration)
│   ├── call_for_presentations.qmd   (English call for papers)
│   └── author_guidelines.qmd        (English author guidelines)
├── fr/
│   ├── index.qmd                    (French home page)
│   ├── registration.qmd             (French registration)
│   ├── call_for_presentations.qmd   (French call for papers)
│   └── author_guidelines.qmd        (French author guidelines)
├── _quarto.yml                      (Updated configuration)
├── _brand.yml                       (Branding unchanged)
└── custom.scss                      (Styling unchanged)
```

#### 2. Updated Configuration *(_quarto.yml)*

- Added both English and French render paths
- Enhanced navbar with language switcher
  - English section: Home, Call for presentations, Registration
  - French section: Accueil, Appel à Conférenciers, Inscription
- Updated footer reflecting both languages

#### 3. Content Files

All four key pages have been created in fr:
- Home/Index (Accueil)
- Registration (Inscription)
- Call for Presentations (Appel à Conférencier.es)
- Author Guidelines (Directives pour les Auteurs)


## How to Build & Deploy

### Prerequisites
Install Quarto if not already installed:
```bash
# On Ubuntu/Debian
apt-get update
apt-get install -y quarto

# Or via conda
conda install -c conda-forge quarto
```

### Build the Website
```bash
cd /workspaces/Research-Software-Africa
quarto render
```

This will generate:
- English version at: `_site/en/`
- French version at: `_site/fr/`

### View Locally
```bash
# Preview the website
quarto preview
```


## Navigation Structure

### English Path
- Home: `/en/index.html`
- Call for Presentations: `/en/call_for_presentations.html`
- Registration: `/en/registration.html`
- Author Guidelines: `/en/author_guidelines.html`

### French Path
- Accueil: `/fr/index.html`
- Appel à Conférencier.es: `/fr/call_for_presentations.html`
- Inscription: `/fr/registration.html`
- Directives pour les Auteurs: `/fr/author_guidelines.html`


## Adding More Content or Translations

To add more pages in the future:

1. Create English version in `en/your-page.qmd`
2. Create French version in `fr/your-page.qmd`
3. Update `_quarto.yml` to include new render paths:
   ```yaml
   render:
     - en/your-page.qmd
     - fr/your-page.qmd
   ```
4. Update navbar in `_quarto.yml` to add navigation links
