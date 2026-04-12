# Dr Nicky Garland - Professional Website

This is the source code for my professional website built with [Quarto](https://quarto.org).

## About

This website showcases my work at the intersection of archaeology, data science, and research training. It includes:

- Professional background and experience
- Research projects and publications
- Teaching and training portfolio
- Technical skills and expertise
- Blog posts and tutorials

## Building the Site

### Prerequisites

- [R](https://cran.r-project.org/) (version 4.0+)
- [RStudio](https://posit.co/downloads/) (recommended)
- [Quarto](https://quarto.org/docs/get-started/) (version 1.3+)

### Required R Packages

Install the following R packages:

```r
install.packages(c(
  "tidyverse",
  "sf",
  "ggplot2",
  "knitr",
  "rmarkdown"
))
```

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/nickyjgarland/nickyjgarland.github.io.git
cd nickyjgarland.github.io
```

2. Preview the site locally:
```bash
quarto preview
```

3. Build the site:
```bash
quarto render
```

The rendered site will be in the `docs/` folder.

## Deployment

### GitHub Pages

This site is configured to deploy to GitHub Pages:

1. Push changes to the main branch
2. GitHub Actions will automatically build and deploy
3. Site will be available at `https://nickyjgarland.github.io`

### Manual Deployment

Alternatively, deploy manually:

```bash
quarto publish gh-pages
```

## Project Structure

```
.
├── _quarto.yml           # Site configuration
├── index.qmd             # Home page
├── about.qmd             # About page
├── experience.qmd        # Experience/CV page
├── research.qmd          # Research projects
├── teaching.qmd          # Teaching portfolio
├── skills.qmd            # Skills and tools
├── publications.qmd      # Publications list
├── blog.qmd              # Blog landing page
├── posts/                # Blog posts
│   └── getting-started-r/
│       └── index.qmd
├── images/               # Image assets
├── styles.css            # Custom CSS
├── custom.scss           # Custom SCSS theme
└── README.md             # This file
```

## Customization

### Colors and Theme

Edit `custom.scss` to change the color scheme:

```scss
$primary: #2C7FB8;        // Main brand color
$secondary: #7FCDBB;      // Accent color
```

### Navigation

Edit `_quarto.yml` to modify navigation:

```yaml
website:
  navbar:
    left:
      - text: "Home"
        href: index.qmd
      # Add more items here
```

### Adding Content

#### New Page

Create a new `.qmd` file:

```yaml
---
title: "New Page"
---

Content goes here...
```

Add to `_quarto.yml` navigation.

#### New Blog Post

Create a new folder in `posts/`:

```
posts/
└── my-new-post/
    └── index.qmd
```

Include front matter:

```yaml
---
title: "My New Post"
author: "Nicky Garland"
date: "2026-03-15"
categories: [R, tutorial]
---
```

## Adding Images

1. Create an `images/` folder if it doesn't exist
2. Add images (profile photo, project screenshots, etc.)
3. Reference in `.qmd` files:

```markdown
![Caption](images/photo.jpg)
```

## Dependencies

### R Packages Used

- `tidyverse` - Data manipulation and visualization
- `sf` - Spatial data handling
- `ggplot2` - Graphics and plots
- `knitr` - Dynamic document generation
- `rmarkdown` - R Markdown support

### Additional Tools

- Quarto academicons extension for ORCID, Google Scholar icons
- Font Awesome icons for social media

## License

Content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  
Code: MIT License

## Contact

- Email: nickyjgarland@gmail.com
- GitHub: [@nickyjgarland](https://github.com/nickyjgarland)
- ORCID: [0000-0002-6789-0779](https://orcid.org/0000-0002-6789-0779)

## Acknowledgments

Built with:
- [Quarto](https://quarto.org)
- [R](https://www.r-project.org/)
- [RStudio](https://posit.co/)
- Inspired by the Quarto gallery and community examples
