# NeuroAI Lab Website

The official website for the NeuroAI Lab at EPFL, built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com).

## Features

- **Home** - Lab introduction, research directions, and recent publications
- **People** - Team members organized by role (Faculty, Scientists, PhD Students, etc.)
- **Publications** - Filterable list of publications by type (Conference, Journal, Workshop, Preprint)
- **Research** - Detailed research directions and teaching information
- **Join Us** - Information for prospective PhD students, postdocs, and interns
- **Contact** - Contact information and lab locations

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm

### Installation

```bash
# Clone the repository
git clone https://github.com/epfl-neuroai-lab/neuroai-lab-website.git
cd neuroai-lab-website

# Install dependencies
npm install
```

### Development

```bash
# Start the development server
npm run dev
```

The site will be available at `http://localhost:4321`.

### Building

```bash
# Build for production
npm run build

# Preview the production build
npm run preview
```

## Project Structure

```
/
├── public/
│   └── logo.png              # Lab logo
├── src/
│   ├── components/
│   │   ├── Header.astro      # Navigation header
│   │   └── Footer.astro      # Site footer
│   ├── data/
│   │   ├── people.json       # Team member data
│   │   └── publications.json # Publications data
│   ├── layouts/
│   │   └── Layout.astro      # Main layout template
│   ├── pages/
│   │   ├── index.astro       # Home page
│   │   ├── people/           # People page
│   │   ├── publications/     # Publications page
│   │   ├── research/         # Research page
│   │   ├── join/             # Join Us page
│   │   └── contact/          # Contact page
│   └── styles/
│       └── global.css        # Global styles and Tailwind config
├── astro.config.mjs          # Astro configuration
└── package.json
```

## Updating Content

### Adding Team Members

Edit `src/data/people.json` to add or modify team members. Each person should include:

```json
{
  "name": "Full Name",
  "role": "Role Title",
  "email": "email@epfl.ch",
  "image": "filename.jpg",
  "website": "https://optional-website.com"
}
```

### Adding Publications

Edit `src/data/publications.json` to add publications:

```json
{
  "title": "Publication Title",
  "authors": ["Author 1", "Author 2"],
  "venue": "Conference/Journal Name",
  "year": 2025,
  "type": "conference|journal|workshop|preprint",
  "highlight": "Optional: Oral, Spotlight, etc.",
  "links": {
    "paper": "https://paper-link.com",
    "code": "https://github.com/...",
    "project": "https://project-page.com"
  }
}
```

## Deployment

The site is automatically deployed to GitHub Pages when pushing to the `main` branch. The deployment is handled by the GitHub Actions workflow in `.github/workflows/deploy.yml`.

### Manual Deployment

1. Build the site: `npm run build`
2. The output will be in the `dist/` directory
3. Deploy the `dist/` directory to any static hosting service

## Customization

### Colors

The color scheme can be modified in `src/styles/global.css`. The main colors are:

- Primary Green: `#00a86b`
- Primary Blue: `#0088cc`

### Configuration

Update `astro.config.mjs` to change:

- `site`: Your production URL
- `base`: The base path if deploying to a subdirectory

## License

MIT License - see LICENSE file for details.

## Contact

For questions about the website, please contact the NeuroAI Lab team.
