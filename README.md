# Simple CICD Pipeline for MCUXpresso SDK v24.12 or newer

# mcuxpresso-cicd

A reference Continuous Integration / Continuous Deployment (CI/CD) setup for MCUXpresso SDK-based projects using GitHub Actions and Docker. This repository demonstrates how to automate the build and validation of embedded applications developed with the NXP MCUXpresso SDK and IDE.

## Overview

This project provides a working example of how to:

- Set up a CI/CD pipeline for MCUXpresso SDK projects.
- Use GitHub Actions to automate builds.
- Leverage Docker to ensure consistent build environments.
- Build a freestanding MCUXpresso SDK project (`my_app`) in a reproducible and scalable way.

## Repository Structure

```
mcuxpresso-cicd/
├── .github/workflows/     # GitHub Actions workflows for CI/CD
├── .vscode                # VS Code configuratin files for the project
├── my_app                 # Example MCUXpresso SDK project
├── dockerfile             # Dockerfile for creating docker image
└── README.md
```

## Prerequisites

- [Docker](https://www.docker.com/) installed and running.
- GitHub account with access to this repository.
- Basic understanding of GitHub Actions and Docker.

## CI/CD Workflow

The GitHub Actions workflow (`.github/workflows/build.yml`) performs the following steps:

1. **Checkout** the repository.
2. **Build** the Docker image with the MCUXpresso toolchain.
3. **Compile** the `my_app` project using the MCUXpresso SDK.

## Artifacts

After a successful build, the output binaries and logs are stored in the `my_app/build/` directory and uploaded as GitHub Actions artifacts.

## Future Enhancements

- Add unit testing support.
- Integrate static code analysis tools.
- Support for multiple boards and configurations.
- Deployment to hardware or emulators.
