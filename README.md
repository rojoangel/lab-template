# Lab Template

This project serves as a template for creating labs and workshops to be executed in GitHub Codespaces. It provides a standardized structure and configuration for creating consistent learning environments.

## Project Structure

The template includes the following key components:

- `.devcontainer/` - Contains configuration for GitHub Codespaces development environment
  - `devcontainer.json` - Defines the development container configuration, including extensions and settings

- `.github/` - GitHub-specific configurations and workflows

- `.vscode/` - Visual Studio Code specific settings and configurations

- Configuration Files:
  - `.eslintrc.json` - ESLint configuration for JavaScript/TypeScript linting
  - `.gitignore` - Git ignore rules
  - `webpack-config.js` - Webpack configuration for bundling
  - `api.http` - HTTP request templates for API testing

- Documentation:
  - `CODE_OF_CONDUCT.md` - Community guidelines and code of conduct
  - `COPYRIGHT` - Copyright information
  - `LICENSE` - Project license details

## Getting Started

1. Use this template to create a new repository for your lab/workshop
2. Customize the `.devcontainer` configuration as needed for your specific requirements
3. Add your lab content and exercises
4. Share the repository with participants who can then open it in GitHub Codespaces

## Features

- Pre-configured development environment
- Standardized project structure
- Built-in code quality tools
- Ready-to-use GitHub Codespaces configuration

## Adobe I/O CLI Login Workaround

When using `aio login` in GitHub Codespaces, the authentication response is sent to `127.0.0.1:<EPHEMERAL_PORT>`. To make this work in Codespaces:

1. Run `aio login` and note the URL shown (it will start with `127.0.0.1:`)
2. Look for the automatically created port forwarding in your Codespace (usually shown in the "Ports" tab)
3. Replace the entire `127.0.0.1:<EPHEMERAL_PORT>` URL with the port forwarding URL provided by Codespaces
4. Open the modified URL in your browser to complete the authentication

This workaround is necessary because Codespaces creates its own port forwarding for localhost connections.