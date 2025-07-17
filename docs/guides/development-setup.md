# Development Environment Setup Guide

This guide will help you set up your development environment for working with Tiation projects.

## 📋 Table of Contents

- [Prerequisites](#prerequisites)
- [Operating System Setup](#operating-system-setup)
  - [Ubuntu/Linux](#ubuntulinux)
  - [Windows](#windows)
  - [macOS](#macos)
- [Core Tools Installation](#core-tools-installation)
- [Repository Setup](#repository-setup)
- [IDE Configuration](#ide-configuration)
- [Verification](#verification)
- [Troubleshooting](#troubleshooting)

## 🔧 Prerequisites

Before starting, ensure you have:
- Administrative access to your machine
- Stable internet connection
- At least 20GB free disk space
- Basic command line knowledge

## 💻 Operating System Setup

### Ubuntu/Linux

For detailed Ubuntu setup, see our [Ubuntu Dev Setup Repository](https://github.com/tiation/ubuntu-dev-setup).

Quick start:
```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install essential tools
sudo apt install -y git curl wget build-essential

# Clone setup repository
git clone https://github.com/tiation/ubuntu-dev-setup.git
cd ubuntu-dev-setup
./setup.sh
```

### Windows

For detailed Windows setup, see our [Windows Dev Setup Repository](https://github.com/tiation/windows-dev-setup).

Quick start:
1. Install [Windows Subsystem for Linux (WSL2)](https://docs.microsoft.com/en-us/windows/wsl/install)
2. Install [Windows Terminal](https://aka.ms/terminal)
3. Run PowerShell as Administrator:
```powershell
# Clone setup repository
git clone https://github.com/tiation/windows-dev-setup.git
cd windows-dev-setup
.\setup.ps1
```

### macOS

```bash
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install essential tools
brew install git node python go rust

# Install development tools
brew install --cask visual-studio-code docker
```

## 🛠️ Core Tools Installation

### Git Configuration
```bash
# Set up Git identity
git config --global user.name "Your Name"
git config --global user.email "tiatheone@protonmail.com"

# Configure Git preferences
git config --global init.defaultBranch main
git config --global pull.rebase false
```

### Node.js & npm
```bash
# Install Node Version Manager (nvm)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# Install latest LTS Node.js
nvm install --lts
nvm use --lts

# Verify installation
node --version
npm --version
```

### Python
```bash
# Install Python 3.10+
# Ubuntu/Debian
sudo apt install python3 python3-pip python3-venv

# macOS
brew install python@3.10

# Create virtual environment
python3 -m venv ~/.venvs/tiation
source ~/.venvs/tiation/bin/activate
```

### Docker
```bash
# Install Docker
# Ubuntu
sudo apt install docker.io docker-compose
sudo usermod -aG docker $USER

# macOS/Windows
# Download and install Docker Desktop from https://www.docker.com/products/docker-desktop
```

### Go (for infrastructure projects)
```bash
# Install Go
# Ubuntu
sudo snap install go --classic

# macOS
brew install go

# Set up Go workspace
echo 'export GOPATH=$HOME/go' >> ~/.bashrc
echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.bashrc
source ~/.bashrc
```

## 📦 Repository Setup

### 1. Create Workspace Directory
```bash
mkdir -p ~/tiation-workspace
cd ~/tiation-workspace
```

### 2. Clone Core Repositories
```bash
# Clone main repositories
git clone https://github.com/tiation/19-trillion-solution.git
git clone https://github.com/tiation/company-intranet.git
git clone https://github.com/tiation/workflows.git
git clone https://github.com/tiation/tiation-docs.git

# For mobile development
git clone https://github.com/tiation/RiggerConnect-RiggerJobs-Workspace-PB.git
```

### 3. Install Dependencies
```bash
# Navigate to each project and install dependencies
cd 19-trillion-solution
npm install  # or yarn install

cd ../company-intranet
pip install -r requirements.txt

# Continue for other projects...
```

## 💡 IDE Configuration

### Visual Studio Code

1. Install recommended extensions:
```bash
code --install-extension dbaeumer.vscode-eslint
code --install-extension esbenp.prettier-vscode
code --install-extension ms-python.python
code --install-extension golang.go
code --install-extension eamodio.gitlens
```

2. Configure workspace settings:
```json
{
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "go.useLanguageServer": true
}
```

### JetBrains IDEs

1. Install appropriate IDE (IntelliJ IDEA, PyCharm, WebStorm)
2. Import project settings from `.idea` folder if available
3. Configure code style settings to match project standards

## ✅ Verification

Run these commands to verify your setup:

```bash
# Check tool versions
git --version
node --version
npm --version
python3 --version
docker --version
go version

# Test repository access
cd ~/tiation-workspace/19-trillion-solution
npm test

# Verify Docker
docker run hello-world
```

## 🔍 Troubleshooting

### Common Issues

#### Permission Denied (Git)
```bash
# Fix SSH key permissions
chmod 600 ~/.ssh/id_rsa
chmod 644 ~/.ssh/id_rsa.pub

# Add SSH key to agent
ssh-add ~/.ssh/id_rsa
```

#### Node Version Conflicts
```bash
# Switch Node versions
nvm use 16  # or required version
nvm alias default 16
```

#### Docker Permission Issues (Linux)
```bash
# Add user to docker group
sudo usermod -aG docker $USER
# Log out and back in for changes to take effect
```

#### Python Virtual Environment Not Activating
```bash
# Manually activate
source ~/.venvs/tiation/bin/activate

# Add to shell profile
echo 'source ~/.venvs/tiation/bin/activate' >> ~/.bashrc
```

## 📚 Next Steps

1. Read the [Contributing Guide](../../CONTRIBUTING.md)
2. Review [Repository Index](../REPOSITORY_INDEX.md)
3. Check project-specific README files
4. Join our developer community

## 🆘 Getting Help

- **Documentation**: [tiation-docs](https://github.com/tiation/tiation-docs)
- **Issues**: Create an issue in the relevant repository
- **Discord**: Join our developer Discord server
- **Email**: dev-support@tiation.com

---

*Last updated: July 2025*
