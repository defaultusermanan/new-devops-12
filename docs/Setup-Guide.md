# Setup Guide

Follow this guide to set up the `new-devops-12` project on your local machine or CI/CD environment.

---

## Prerequisites

1. **Java Development Kit (JDK)**:
   - Version: Java 8+
   - [Download here](https://www.oracle.com/java/technologies/javase-downloads.html).

2. **Apache Maven**:
   - Version: 3.6+
   - [Download here](https://maven.apache.org/download.cgi).

3. **Git**:
   - Installed and configured.
   - [Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

4. **Jenkins**:
   - CI/CD server.
   - [Jenkins Installation Guide](https://www.jenkins.io/doc/book/installing/).

5. **GitHub Access**:
   - Ensure you have access to the repository to integrate workflows.

---

## Local Setup

### Step 1: Clone the Repository
```bash
git clone https://github.com/your-org/new-devops-12.git
```

### Step 2: Navigate to the Project Directory
```bash
cd java-hello-world-with-maven-master
```

### Step 3: Verify Maven Dependencies
Ensure that all dependencies mentioned in `pom.xml` are resolved.
```bash
mvn install
```

### Step 4: Run the Application
Execute the Java application locally.
```bash
mvn exec:java -Dexec.mainClass="hello.HelloWorld"
```

---

## CI Setup

### Step 1: Configure Jenkins
1. Create a new pipeline job.
2. Link the repository to the pipeline.
3. Specify the `Jenkinsfile` for build definition.

### Step 2: Enable CodeQL Workflow
1. Navigate to `.github/workflows/codeql.yml`.
2. Ensure the workflows are triggered on `push` or `pull_request` events for code scanning.

### Step 3: Integrate Dependency Scanning
Ensure `.whitesource` configurations are active for analyzing dependencies.

---

## Common Issues

1. **Maven Build Errors**:
   - Verify `JAVA_HOME` and `MAVEN_HOME` are correctly set.

2. **Code Scanning Issues**:
   - Check if CodeQL is enabled in the repository.

3. **Jenkins Pipeline Failures**:
   - Confirm Jenkinsfile syntax and necessary agent configurations.

Ensure all prerequisites and setups are completed before proceeding!