# User Guide

Welcome to the SelfCoE User Guide! This guide will help you get started with using the Self-Service Center of Excellence platform.

## Table of Contents

- [Getting Started](#getting-started)
- [Service Catalog](#service-catalog)
- [Software Templates](#software-templates)
- [Documentation](#documentation)
- [Search and Discovery](#search-and-discovery)
- [User Management](#user-management)
- [Troubleshooting](#troubleshooting)

## Getting Started

### Accessing SelfCoE

1. Navigate to your SelfCoE instance URL
2. Sign in using your organization's authentication method
3. You'll be taken to the main dashboard

### First Steps

After signing in, you'll see:

- **Service Catalog**: Browse all services and components
- **Create**: Use templates to scaffold new projects
- **Docs**: Access technical documentation
- **Search**: Find resources across the platform

## Service Catalog

The Service Catalog is the heart of SelfCoE, providing a unified view of all your organization's services, APIs, and components.

### Browsing the Catalog

1. Click on **"Catalog"** in the main navigation
2. Use filters to narrow down results:
   - **Kind**: Component, System, API, etc.
   - **Type**: Service, Website, Library, etc.
   - **Lifecycle**: Experimental, Production, Deprecated
   - **Owner**: Team or individual responsible

### Understanding Entity Types

#### Components
Services, websites, libraries, and other software components.

#### Systems
Collections of entities that work together to provide business value.

#### APIs
Interfaces that components provide to each other.

#### Resources
Infrastructure that components depend on (databases, queues, etc.).

### Entity Details

Click on any entity to view:

- **Overview**: Description, ownership, and key information
- **Dependencies**: What this entity depends on and what depends on it
- **API**: API specifications and documentation
- **Docs**: Associated technical documentation
- **Monitoring**: Health and performance metrics

## Software Templates

Templates help you create new projects with consistent structure and best practices.

### Using Templates

1. Click **"Create"** in the main navigation
2. Browse available templates
3. Select a template that fits your needs
4. Fill out the required parameters:
   - Project name
   - Description
   - Owner team
   - Repository details
5. Click **"Create"** to scaffold your project

### Template Categories

#### Backend Services
- **Node.js API**: RESTful API with Express.js
- **Python Service**: Flask/FastAPI service
- **Java Spring Boot**: Enterprise Java service

#### Frontend Applications
- **React App**: Modern React application
- **Angular App**: Angular single-page application
- **Vue.js App**: Vue.js frontend

#### Documentation Sites
- **TechDocs**: Backstage documentation site
- **MkDocs**: Python-based documentation
- **Docusaurus**: React-based documentation

#### Libraries and Packages
- **NPM Package**: JavaScript/TypeScript library
- **Python Package**: Python library with setuptools
- **Maven Library**: Java library

### Template Outputs

After creation, templates typically provide:

- Git repository with initial code
- CI/CD pipeline configuration
- Documentation structure
- Catalog registration

## Documentation

SelfCoE integrates with TechDocs to provide unified documentation.

### Finding Documentation

1. Navigate to an entity in the catalog
2. Click the **"Docs"** tab
3. Browse the documentation structure

### Documentation Features

- **Search**: Full-text search across all documentation
- **Navigation**: Hierarchical documentation structure
- **Versioning**: Multiple documentation versions
- **Cross-references**: Links between related documentation

### Writing Documentation

Documentation is typically written in Markdown and stored alongside your code:

```
docs/
├── index.md          # Main documentation page
├── getting-started.md
├── api-reference.md
└── troubleshooting.md
```

## Search and Discovery

### Global Search

Use the search bar in the top navigation to find:

- Services and components
- Documentation pages
- API endpoints
- Team information

### Advanced Search

Use search filters:

- **Entity type**: `kind:component`
- **Owner**: `owner:team-platform`
- **Technology**: `spec.type:service`
- **Tags**: `metadata.tags:frontend`

### Search Tips

- Use quotes for exact phrases: `"user authentication"`
- Combine filters: `kind:component owner:team-api`
- Use wildcards: `user-*` to find entities starting with "user-"

## User Management

### User Profiles

View and edit your profile:

1. Click your avatar in the top-right corner
2. Select **"Settings"**
3. Update your information and preferences

### Team Management

If you're a team lead or admin:

1. Navigate to **"Catalog"** → **"Groups"**
2. Find your team
3. Manage team members and permissions

### Permissions

SelfCoE uses role-based access control:

- **Read**: View catalog entities and documentation
- **Write**: Create and modify entities you own
- **Admin**: Manage users, teams, and system configuration

## Troubleshooting

### Common Issues

#### "Entity not found" error
- Check if the entity exists in the catalog
- Verify you have permission to view the entity
- Ensure the entity is properly registered

#### Template creation fails
- Check template parameters are correct
- Verify you have permission to create in the target location
- Review template logs for specific errors

#### Documentation not loading
- Ensure documentation is properly configured
- Check if the documentation source is accessible
- Verify TechDocs integration is working

#### Search returns no results
- Try different search terms
- Check if entities are properly indexed
- Verify search service is running

### Getting Help

If you need assistance:

1. **Documentation**: Check this user guide and API documentation
2. **Search**: Use the platform search to find answers
3. **Support**: Contact your platform team
4. **Issues**: Report bugs through your organization's issue tracking

### Keyboard Shortcuts

- `Ctrl/Cmd + K`: Open global search
- `Ctrl/Cmd + /`: Show keyboard shortcuts
- `Esc`: Close modals and overlays

### Browser Support

SelfCoE supports modern web browsers:

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### Mobile Access

While SelfCoE is primarily designed for desktop use, basic functionality is available on mobile devices through responsive design.

## Best Practices

### Catalog Management

- **Consistent naming**: Use clear, descriptive entity names
- **Proper ownership**: Assign clear owners to all entities
- **Regular updates**: Keep entity information current
- **Good descriptions**: Write helpful descriptions for all entities

### Documentation

- **Keep it current**: Update documentation with code changes
- **Clear structure**: Organize documentation logically
- **Search-friendly**: Use descriptive headings and keywords
- **Examples**: Include code examples and tutorials

### Team Collaboration

- **Share knowledge**: Document decisions and processes
- **Use templates**: Leverage templates for consistency
- **Regular reviews**: Periodically review and update entities
- **Communication**: Use entity annotations for important information

---

Need more help? Check out our [API Documentation](../api/index.md) or contact your platform team.