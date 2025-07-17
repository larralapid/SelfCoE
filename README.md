# 🏗️ SelfCoE - Self-Service Center of Excellence

A comprehensive Self-Service Center of Excellence built on [Backstage](https://backstage.io). Empowering developers with unified service catalog, scaffolding templates, and organizational standards for modern software development.

[![GitHub Pages](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](https://larralapid.github.io/SelfCoE/)
[![GitHub Issues](https://img.shields.io/github/issues/larralapid/SelfCoE)](https://github.com/larralapid/SelfCoE/issues)
[![GitHub Stars](https://img.shields.io/github/stars/larralapid/SelfCoE)](https://github.com/larralapid/SelfCoE/stargazers)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](LICENSE)

## ✨ Features

- 🏗️ **Service Catalog** - Centralized view of all services, APIs, and components
- 🚀 **Software Templates** - Scaffolding tools for consistent project creation
- 📊 **Developer Analytics** - Usage metrics and insights
- 🔐 **Authentication & Authorization** - Secure access control
- 📚 **Documentation Hub** - Unified technical documentation
- 🔍 **Search & Discovery** - Find resources across your organization

## 🚀 Quick Start

### Prerequisites

- Node.js 20.x or 22.x
- Yarn 4.4.1
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/larralapid/SelfCoE.git
cd SelfCoE

# Install dependencies
yarn install

# Start the development server
yarn start
```

The application will be available at:
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:7007

## 📖 Documentation

Visit our [documentation site](https://larralapid.github.io/SelfCoE/) for:

- [Getting Started Guide](https://larralapid.github.io/SelfCoE/)
- [Changelog](https://larralapid.github.io/SelfCoE/CHANGELOG.html)
- [Contributing Guidelines](.github/CONTRIBUTING.md)
- [API Reference](docs/api/index.md)

## 🛠️ Development

### Available Scripts

```bash
# Start development server
yarn start

# Build for production
yarn build:all

# Run tests
yarn test

# Run linting
yarn lint

# Type checking
yarn tsc
```

### Project Structure

```
SelfCoE/
├── packages/
│   ├── app/           # Frontend React application
│   └── backend/       # Backend Node.js API
├── plugins/           # Custom Backstage plugins
├── docs/             # Documentation and GitHub Pages
├── examples/         # Example entities and templates
└── app-config.yaml   # Backstage configuration
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](.github/CONTRIBUTING.md) for details on:

- Code of Conduct
- Development process
- Submitting pull requests
- Reporting issues

## 📊 Project Status

Current development focus:

- [x] Initial Backstage setup and configuration
- [x] Basic service catalog and scaffolding
- [ ] Authentication provider configuration
- [ ] Production database setup
- [ ] Custom plugins and integrations
- [ ] Deployment pipeline

See our [GitHub Issues](https://github.com/larralapid/SelfCoE/issues) for detailed roadmap and progress.

## 🔧 Configuration

### Environment Variables

```bash
# Development
NODE_ENV=development
POSTGRES_HOST=localhost
POSTGRES_PORT=5432

# Production
NODE_ENV=production
POSTGRES_HOST=your-db-host
POSTGRES_PORT=5432
```

### Key Configuration Files

- `app-config.yaml` - Main Backstage configuration
- `app-config.local.yaml` - Local development overrides
- `app-config.production.yaml` - Production settings

## 🚀 Deployment

### Docker

```bash
# Build backend image
yarn build-image

# Run with Docker Compose
docker-compose up -d
```

### Kubernetes

```bash
# Apply manifests
kubectl apply -f k8s/
```

## 📝 License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

**Note**: This project is open source under the Apache License 2.0.

## 🙏 Acknowledgments

Built with:
- [Backstage](https://backstage.io/) - The platform for building developer portals
- [React](https://reactjs.org/) - Frontend framework
- [Node.js](https://nodejs.org/) - Backend runtime
- [TypeScript](https://www.typescriptlang.org/) - Type safety

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/larralapid/SelfCoE/issues)
- **Discussions**: [GitHub Discussions](https://github.com/larralapid/SelfCoE/discussions)
- **Documentation**: [Project Docs](https://larralapid.github.io/SelfCoE/)

---

Made with ❤️ for the developer community
