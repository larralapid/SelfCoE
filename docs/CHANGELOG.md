# Changelog

All notable changes to the SelfCoE (Self-Service Center of Excellence) project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial Backstage application setup with version 1.41.0
- Basic configuration files (app-config.yaml, app-config.local.yaml, app-config.production.yaml)
- Core Backstage plugins enabled:
  - Software Catalog
  - Scaffolder (Template Engine)
  - TechDocs
  - Search
  - Authentication (Guest provider)
  - Permissions
  - Kubernetes integration
  - Proxy
- Example entities and templates in `/examples` directory
- Basic organizational structure with example entities
- SQLite in-memory database for development
- Playwright configuration for end-to-end testing
- TypeScript configuration and linting setup
- Yarn workspace configuration for monorepo structure

### Infrastructure
- GitHub repository created: https://github.com/larralapid/SelfCoE
- Development environment configured with Node.js 20.x and Yarn 4.4.1
- Frontend running on port 3000
- Backend API running on port 7007

## [0.1.0] - 2025-07-16

### Added
- Initial project setup following Backstage Getting Started guide
- Basic Backstage application structure
- Development environment configuration
- Core plugins initialization
- Example catalog entities and templates