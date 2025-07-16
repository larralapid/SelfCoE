# Contributing to SelfCoE

Thank you for your interest in contributing to SelfCoE! This document provides guidelines and information for contributors.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Contributing Process](#contributing-process)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Issue Guidelines](#issue-guidelines)
- [Coding Standards](#coding-standards)
- [Testing](#testing)
- [Documentation](#documentation)
- [Release Process](#release-process)

## Code of Conduct

This project adheres to the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/). By participating, you are expected to uphold this code.

## Getting Started

### Prerequisites
- Node.js 20.x or 22.x
- Yarn 4.4.1
- Git
- Docker (for containerized development)

### Development Setup

1. **Fork the Repository**
   ```bash
   # Fork the repo on GitHub, then clone your fork
   git clone https://github.com/YOUR-USERNAME/SelfCoE.git
   cd SelfCoE
   ```

2. **Install Dependencies**
   ```bash
   yarn install
   ```

3. **Set Up Environment**
   ```bash
   # Copy the example config
   cp app-config.local.yaml.example app-config.local.yaml
   # Edit with your local settings
   ```

4. **Start Development Server**
   ```bash
   yarn start
   ```

5. **Verify Setup**
   - Frontend: http://localhost:3000
   - Backend: http://localhost:7007

## Contributing Process

### 1. Choose an Issue
- Check [existing issues](https://github.com/larralapid/SelfCoE/issues)
- Look for issues labeled `good first issue` or `help wanted`
- Comment on the issue to indicate you're working on it

### 2. Create a Branch
```bash
# Create and switch to a new branch
git checkout -b feature/your-feature-name
# or
git checkout -b fix/issue-number-description
```

### 3. Make Changes
- Follow the [coding standards](#coding-standards)
- Write tests for new functionality
- Update documentation as needed
- Ensure all tests pass

### 4. Commit Changes
```bash
# Stage your changes
git add .

# Commit with a clear message
git commit -m "feat: add user authentication to catalog"
```

#### Commit Message Format
We follow the [Conventional Commits](https://conventionalcommits.org/) specification:

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Test changes
- `chore`: Build process or auxiliary tool changes

**Examples:**
```
feat(catalog): add service discovery integration
fix(auth): resolve login redirect issue
docs(api): update authentication endpoints
```

### 5. Push and Create PR
```bash
# Push your branch
git push origin feature/your-feature-name

# Create a pull request on GitHub
```

## Pull Request Guidelines

### Before Submitting
- [ ] Code follows project style guidelines
- [ ] All tests pass locally
- [ ] Documentation is updated
- [ ] Self-review completed
- [ ] Related issues are linked

### PR Requirements
- **Title**: Clear and descriptive
- **Description**: Use the provided template
- **Tests**: Include tests for new functionality
- **Documentation**: Update relevant docs
- **Breaking Changes**: Clearly marked and explained

### Review Process
1. **Automated Checks**: CI/CD pipeline runs
2. **Code Review**: At least one maintainer reviews
3. **Testing**: Reviewer tests the changes
4. **Approval**: PR is approved and merged

## Issue Guidelines

### Reporting Bugs
Use the [bug report template](.github/ISSUE_TEMPLATE/bug_report.yml) and include:
- Clear description of the issue
- Steps to reproduce
- Expected vs actual behavior
- Environment details
- Logs and screenshots

### Feature Requests
Use the [feature request template](.github/ISSUE_TEMPLATE/feature_request.yml) and include:
- Problem statement
- Proposed solution
- Use cases
- Implementation considerations

### Plugin Requests
Use the [plugin request template](.github/ISSUE_TEMPLATE/plugin_request.yml) for:
- New Backstage plugins
- External service integrations
- Custom functionality

## Coding Standards

### General Guidelines
- **Language**: TypeScript for all new code
- **Style**: ESLint and Prettier configurations
- **Naming**: Use descriptive names for variables, functions, and classes
- **Comments**: Write clear, concise comments for complex logic

### Frontend (React)
- **Components**: Use functional components with hooks
- **State Management**: Use React Context or Redux (for complex state)
- **Styling**: Use Material-UI components and theme
- **Testing**: React Testing Library

### Backend (Node.js)
- **Architecture**: Follow existing patterns
- **API Design**: RESTful endpoints with proper HTTP methods
- **Database**: Use TypeORM for database operations
- **Error Handling**: Consistent error responses

### File Structure
```
packages/
├── app/                    # Frontend React app
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   └── plugins/        # Plugin integrations
└── backend/               # Backend Node.js API
    ├── src/
    │   ├── plugins/        # Backend plugins
    │   └── index.ts        # Main entry point
```

### Code Quality
- **Linting**: Run `yarn lint` before committing
- **Type Checking**: Run `yarn tsc` to check types
- **Formatting**: Use `yarn prettier` for consistent formatting

## Testing

### Test Types
- **Unit Tests**: Test individual functions/components
- **Integration Tests**: Test feature interactions
- **E2E Tests**: Test complete user workflows

### Running Tests
```bash
# Run all tests
yarn test

# Run tests with coverage
yarn test:coverage

# Run E2E tests
yarn test:e2e
```

### Test Guidelines
- Write tests for new functionality
- Maintain or improve test coverage
- Use descriptive test names
- Test both success and error cases

## Documentation

### Types of Documentation
- **Code Comments**: For complex logic
- **API Documentation**: For backend endpoints
- **User Documentation**: For end-user features
- **Developer Documentation**: For contributors

### Documentation Standards
- Use clear, concise language
- Include code examples
- Keep documentation up-to-date
- Use proper markdown formatting

### Updating Documentation
- Update README for significant changes
- Update API docs for endpoint changes
- Add to changelog for user-facing changes

## Release Process

### Versioning
We use [Semantic Versioning](https://semver.org/):
- **MAJOR**: Breaking changes
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes (backward compatible)

### Release Steps
1. Update version in `package.json`
2. Update `CHANGELOG.md`
3. Create release PR
4. Tag release after merge
5. Deploy to production

## Getting Help

### Communication Channels
- **GitHub Issues**: Bug reports and feature requests
- **GitHub Discussions**: Questions and general discussion
- **Discord**: Real-time chat with the community

### Development Questions
- Check existing documentation first
- Search closed issues and PRs
- Ask in GitHub Discussions
- Join the Backstage Discord

### Maintainer Contact
- Create an issue for bugs or features
- Use discussions for questions
- Mention @larralapid for urgent issues

## Recognition

Contributors are recognized in:
- `CONTRIBUTORS.md` file
- Release notes
- GitHub contributor graph
- Community acknowledgments

## License

By contributing, you agree that your contributions will be licensed under the same license as the project.

---

Thank you for contributing to SelfCoE! 🚀