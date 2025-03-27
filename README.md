# Arkyt
A Scaffolding CLI tool:  Generates project boilerplates for different tech stacks.
# Arkyt CLI

## Overview
**Arkyt** is a command-line tool for scaffolding  projects efficiently. It automates project setup, applies custom templates, and provides a structured approach to  development. This version is designed with a modular architecture, allowing for future expansion to support other frameworks such as Go or Express.

## Folder Structure

```
arkyt/
├── cmd/                  # CLI command definitions
│   ├── root.go           # Main CLI entry point (`arkyt` command)
│   ├── create.go         # Handles project creation (`arkyt create`)
│   ├── flutter.go        # Handles Flutter-specific project creation (`arkyt create flutter-app`)
│   ├── list.go           # Lists available templates or configurations (`arkyt list`) [Future]
│   ├── customize.go      # Allows customization of templates (`arkyt customize`) [Future]
├── internal/             # Core business logic (separate from CLI handling)
│   ├── scaffold/         # Handles project scaffolding
│   │   ├── flutter/      # Contains Flutter-specific scaffolding logic
│   │   │   ├── template/ # Stores Flutter project templates
│   │   │   ├── modify.go # Modifies project structure or files as needed
│   │   │   ├── setup.go  # Handles project setup (dependencies, config files, etc.)
│   ├── utils.go          # General utility functions (e.g., logging, error handling)
├── pkg/                  # Reusable components and utilities
│   ├── executor/         # Runs commands like `flutter create`
│   ├── files/            # Handles file operations (copy, modify, delete)
│   ├── config/           # Loads and manages configuration settings
│   ├── logger/           # Logging utility for structured logging
├── templates/            # Customizable project templates
│   ├── flutter/          # Contains base template modifications for Flutter projects
├── go.mod                # Go module file
├── main.go               # CLI entry point, initializes commands
├── README.md             # Documentation for the project
```

## Features
- **Project Scaffolding**: Easily create new Flutter projects with custom templates.
- **Custom Modifications**: Modify generated projects with predefined settings.
- **Extendable**: Built to support additional frameworks in the future.

## Installation
1. Install Go if you haven't already.
2. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/arkyt.git
   cd arkyt
   ```
3. Install dependencies:
   ```sh
   go mod tidy
   ```
4. Build the CLI:
   ```sh
   go build -o arkyt
   ```
5. Run the CLI:
   ```sh
   ./arkyt
   ```

## Usage
### Create a Flutter Project
```sh
arkyt create flutter-app my_project
```

### List Available Templates (Future Feature)
```sh
arkyt list
```

### Customize a Project (Future Feature)
```sh
arkyt customize --template=custom_template
```

## Contributing
- Fork the repository and create a new branch for your feature.
- Ensure your code follows best practices and is well-documented.
- Submit a pull request for review.

## License
MIT License. See `LICENSE` for more details.

