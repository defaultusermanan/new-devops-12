# Architecture

## Overview

This repository is designed with modularity and automation in mind. It integrates a Java application with Maven for dependency management and build processes while leveraging DevOps practices such as CI/CD pipelines and code scanning.

### Structure

1. **Java Application**: 
    - Location: `java-hello-world-with-maven-master`.
    - Contains two primary source files:
        - `Greeter.java`: Defines greeting functionality.
        - `HelloWorld.java`: Implements the main entry point for the application.

2. **CI/CD Pipeline**:
    - The `Jenkinsfile` defines pipeline stages such as building, testing, and deploying the application.

3. **Code Scanning**:
    - File: `.github/workflows/codeql.yml`.
    - Automatically scans the codebase for vulnerabilities and maintains code quality using GitHub's CodeQL.

4. **Configuration and Metadata**:
    - `.gitignore`: Specifies files and directories to exclude from version control.
    - `.whitesource`: Used for dependency analytics or security scanning.

---

## Flow Diagram

```
           +-----------------------+
           | Java Source Code      |
           +-----------------------+
                     |
                Maven Build
                     |
           +-----------------------+
           | Jenkins Pipeline      |
           +-----------------------+
                     |
              Code Scanning via
               CodeQL Workflows
```

## Key Technologies

- **Java**: Core language for the application.
- **Maven**: Dependency and build management.
- **Jenkins**: Continuous Integration and Deployment.
- **CodeQL**: Security and quality code scanning.