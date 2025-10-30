# Mintlify Documentation Project - Context File

## Project Overview

This is a documentation website built using Mintlify, a modern platform for creating beautiful, developer-friendly documentation. The project uses MDX (Markdown with React components) for content creation and is configured through a `docs.json` file.

The project structure follows Mintlify's standard organization:
- Content is written in `.mdx` files using MDX syntax
- Navigation and site configuration are handled via `docs.json`
- API documentation can be auto-generated from OpenAPI specifications
- Custom components and styling are theme-based

## Project Type
Documentation website using Mintlify framework with MDX content format.

## Key Technologies & Tools
- **Mintlify CLI**: Used for local development and deployment
- **MDX**: Markdown with React components for rich content
- **OpenAPI 3.1**: For API documentation generation
- **React**: Component-based UI elements in MDX files

## Directory Structure
```
docs/
├── ai-tools/           # AI tool documentation pages
├── api-reference/      # API documentation with OpenAPI spec
├── essentials/         # Core documentation features guides
├── images/             # Image assets
├── logo/               # Light/dark mode logos
├── snippets/           # Reusable content snippets
├── docs.json          # Main configuration file
├── index.mdx          # Homepage content
├── quickstart.mdx     # Getting started guide
├── development.mdx    # Local development setup
└── README.md          # Project overview and quickstart
```

## Setup and Running

### Prerequisites
- Node.js version 19 or higher

### Installation
1. Install the Mintlify CLI globally:
   ```bash
   npm i -g mint
   ```

2. Navigate to the documentation directory (where `docs.json` is located)

3. Start the local development server:
   ```bash
   mint dev
   ```

4. View your documentation at `http://localhost:3000`

### Customization
- Site configuration is in `docs.json`
- Navigation structure is defined in the `navigation` property of `docs.json`
- Colors and theme settings are configured in `docs.json`
- Custom ports can be specified with: `mint dev --port 3333`

### Deployment
- Deployments happen automatically when pushing to the default branch (if GitHub app is installed)
- Install the Mintlify GitHub app from the dashboard for automatic deployments

## Content Creation

### Writing Content
- Use MDX format (.mdx files) which supports both Markdown and React components
- Frontmatter includes `title` and `description` fields
- Component library includes Cards, Steps, Accordion, Tabs, and more

### Navigation Structure
- Organized in tabs and groups within `docs.json`
- Each page is referenced by its file path relative to the docs directory
- Supports multiple navigation tabs with grouped content

### API Documentation
- Supports OpenAPI 3.1 specification files
- Auto-generates API documentation from JSON/YAML specs
- Includes interactive API playground functionality
- Authentication methods supported: Bearer, Basic, API Key

## Development Conventions

### File Naming
- Use kebab-case for file names (e.g., `getting-started.mdx`)
- Group related content in folders
- Navigation paths reference file paths without extensions

### Content Organization
- Index files define tab content in navigation
- Use consistent frontmatter across pages
- Organize content in logical groups within navigation

### Component Usage
- Leverage built-in Mintlify components for consistent UI
- Use Cards for linking to related content
- Apply proper accessibility attributes to images and interactive elements

## Key Configuration (`docs.json`)

The `docs.json` file contains:
- Site name and branding configuration
- Navigation structure with tabs and groups
- Color theme settings
- Logo and favicon paths
- API documentation setup
- Footer and navbar configurations

## Useful Commands
- `mint dev` - Start local development server
- `mint dev --port <number>` - Start on custom port
- `mint broken-links` - Validate internal links
- `mint update` - Update CLI to latest version

## Troubleshooting
- If sharp module errors occur on macOS ARM64, update Node.js to v19+ and reinstall CLI
- Clear `~/.mintlify` folder if encountering unknown errors
- Port conflicts will auto-resolve to next available port

## Special Features
- Dark/light mode toggle with customizable default
- Responsive design for all devices
- Built-in search functionality
- GitHub integration for collaborative editing
- Built-in analytics and feedback options
- Support for multiple documentation versions