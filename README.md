# Rockcraft Rocks Template

This is a template repository for developing rocks with Canonical's [Rockcraft](https://documentation.ubuntu.com/rockcraft/en/latest).

This repository template provides a basic setup to help you get started quickly with developing your own rock(s).

## Table of Contents
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Directory Structure](#directory-structure)
- [Building the Rock](#building-the-rock)

## Prerequisites

Before you begin, ensure you have the required dependencies to build rocks using Rockcraft. For this, you'll need Rockcraft installed on your machine. Follow the official installation guide [here](https://documentation.ubuntu.com/rockcraft/en/latest/how-to/get-started/).

```bash
sudo snap install rockcraft --classic
```

## Setup Instructions

### 1. Start a new repository from this template

Check GitHub's documentation on [creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)

### 2. Customize the Template

This template comes with a basic setup to get you started. Here's what you need to customize:

- **`rockcraft.yaml`**: This is the main configuration file where you define your rock's properties like name, version, description, dependencies, etc.
- **`SECURITY.md`**: Set the security policy for the rocks inside this repository. 
- **`CODEOWNERS`**: Specify who are the owner(s) of this code.

## Directory Structure

Here's an overview of the directory structure of the repository:

```
rocks/				            # Directory containing all rocks and its versions
  └─ rock1/			            # Directory containing all versions of a single rock
     └─ v1			            # Directory containing the rock project file for a version
        └─ rockcraft.yaml	      # Rock project file
.gitignore
CODEOWNERS		   	            # Specify who are the authors. Useful for notifications
README.md			            # Top level document containing this specification
SECURITY.md			            # File explaining how to report a vulnerability
```

## Building the Rock

To build your rock, simply run the following command from the directory containing a `rockcraft.yaml` file

```bash
rockcraft pack
```