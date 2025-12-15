# Quickstart: Docusaurus Textbook Structure

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn package manager
- Python 3.11+ with `uv` package manager
- Git for version control

## Setup Instructions

### 1. Clone and Initialize the Repository

```bash
git clone <repository-url>
cd <repository-name>
```

### 2. Set up Python Environment

```bash
# Initialize Python project with uv
uv init
# Or if working in existing project:
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install Docusaurus

```bash
# Create Docusaurus project in website directory
npx create-docusaurus@latest website classic

# Navigate to the website directory
cd website
```

### 4. Configure Docusaurus

1. Update `docusaurus.config.js` with:
   - Site title: "Physical AI & Humanoid Robotics"
   - Organization name: Your GitHub organization
   - Project name: Repository name
   - Deployment branch: `gh-pages`

2. Create the required directory structure in `website/docs/`:
   ```
   docs/
   ├── 01-introduction/
   ├── 02-module-1-ros2/
   ├── 03-module-2-simulation/
   ├── 04-module-3-isaac/
   └── 05-module-4-vla/
   ```

### 5. Set up Navigation

Create or update `sidebars.js` to auto-generate navigation from the folder structure:

```javascript
module.exports = {
  docs: [
    {
      type: 'category',
      label: 'Introduction',
      items: ['01-introduction/01-overview', '01-introduction/02-hardware-lab'],
    },
    {
      type: 'category',
      label: 'Module 1: The Robotic Nervous System',
      items: ['02-module-1-ros2/01-nervous-system'],
    },
    {
      type: 'category',
      label: 'Module 2: The Digital Twin',
      items: ['03-module-2-simulation/01-digital-twin'],
    },
    {
      type: 'category',
      label: 'Module 3: The AI-Robot Brain',
      items: ['04-module-3-isaac/index'],
    },
    {
      type: 'category',
      label: 'Module 4: Vision-Language-Action',
      items: ['05-module-4-vla/index'],
    },
  ],
};
```

### 6. Content Creation Guidelines

1. **File Naming**: Use kebab-case with numeric prefixes (e.g., `01-overview.md`)
2. **Frontmatter**: Include required metadata:
   ```markdown
   ---
   module: "Introduction"
   learning-objectives: ["Objective 1", "Objective 2"]
   hardware-requirements: ["RTX 4070 Ti+", "Jetson Orin Nano"]
   ---
   ```
3. **Admonitions**: Use for hardware constraints and safety:
   ```markdown
   :::note
   This section requires a high-performance workstation with NVIDIA RTX 4070 Ti+.
   :::

   :::warning
   Always follow safety protocols when working with physical robots.
   :::
   ```
4. **Code Blocks**: Specify language and include file titles when needed:
   ```python title="example.py"
   print("Hello, Physical AI!")
   ```

## Local Development

```bash
cd website
npm start
```

This command starts a local development server and opens the website in your browser. Most changes are reflected live without restarting the server.

## Build for Production

```bash
cd website
npm run build
```

This command generates static content in the `build` directory and can be served using any static hosting service.

## Deployment

The site is configured for GitHub Pages deployment. The GitHub Actions workflow in `.github/workflows/deploy.yml` will automatically build and deploy the site when changes are pushed to the main branch.

## Adding New Content

1. Create a new Markdown file in the appropriate module directory
2. Use kebab-case naming with numeric prefix
3. Include required frontmatter
4. Add the new file to `sidebars.js` to make it appear in navigation
5. Use admonitions for hardware requirements and safety information