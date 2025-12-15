# Data Model: Docusaurus Textbook Structure

## Entities

### Textbook Module
- **Name**: Unique identifier for the module (e.g., "introduction", "module-1-ros2")
- **Title**: Display title for the module (e.g., "Introduction", "The Robotic Nervous System")
- **Description**: Brief overview of the module content
- **Order**: Numeric prefix for proper sequencing (01, 02, 03, 04, 05)
- **Learning Objectives**: List of educational goals for the module
- **Hardware Requirements**: Specific hardware needed for practical exercises
- **Content Files**: Collection of Markdown/MDX files that make up the module

### Content File
- **Filename**: Kebab-case with numeric prefix (e.g., "01-overview.md", "02-hardware-lab.md")
- **Title**: Human-readable title for the content
- **Frontmatter**: Metadata including module, learning objectives, hardware requirements
- **Body**: Markdown content with proper syntax highlighting and admonitions
- **Navigation Path**: Relative path in the site structure
- **Prerequisites**: Other content that should be read before this file

### Navigation Structure
- **Sidebar ID**: Unique identifier for the sidebar configuration
- **Category**: Module category (e.g., "Introduction", "Module 1: ROS 2")
- **Items**: List of content files in the proper order
- **Collapsible**: Whether the category can be expanded/collapsed in navigation

## Relationships

- **Textbook Module** contains many **Content Files**
- **Content File** belongs to one **Textbook Module**
- **Navigation Structure** references multiple **Content Files** in specific order
- **Content File** may reference other **Content Files** as prerequisites

## Validation Rules

- Each **Textbook Module** must have a unique order value (01-05)
- Each **Content File** must follow kebab-case naming convention with numeric prefix
- Each **Content File** must include required frontmatter fields
- Each **Content File** must specify programming language for all code blocks
- Each **Content File** must use appropriate admonitions for hardware/safety information
- **Navigation Structure** must reflect the hierarchical directory structure

## State Transitions

- **Content File** moves from "Draft" to "Reviewed" to "Published" during the content lifecycle
- **Textbook Module** moves from "Planned" to "In Progress" to "Complete" as content is developed