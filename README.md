# My Daily Journal

A robust, CLI-based journal application designed for efficiency, data integrity, and cross-platform compatibility.

## Table of Contents
- Overview
- Features
- Installation
  - From Source
  - Using .deb Package
  - Using Snap
- Usage Guide
  - Basic Commands
  - Undo and Backup System
- Development Setup
  - Building and Packaging
  - Building the .deb package
  - Building the Snap package
- Technical Architecture
- Roadmap & Future Enhancements
- License
- Contributing
- Final Thoughts

---

## Overview
**My Daily Journal** is a command-line-based journaling application that allows users to efficiently create, read, search, edit, and delete journal entries. The application ensures **data integrity** by implementing a **backup system** and **undo functionality**, making it ideal for users who prefer **terminal-based productivity tools**.

The project is designed with **cross-platform support**, meaning it runs seamlessly on **macOS** and **Ubuntu Linux**, including deployments via **.deb** and **Snap** packages.

---

## Features
- CLI-Based – Lightweight and easy to use in a terminal
- Multi-File Journal System – Create and manage multiple .txt journal files
- Backup & Undo – Automatic backup system before each modification
- Search Functionality – Find past entries efficiently
- Editing & Deleting – Modify past entries with a built-in editor
- Formatted Output – Well-structured display of journal entries with timestamps
- Cross-Platform – Runs on macOS, Ubuntu, and other Linux distributions
- Package Support – Distributed via .deb and Snap for easy installation

---

## Installation

### From Source
To manually install and run from source:

1. Clone the repository:
   ```
   git clone https://github.com/YOUR_GITHUB_USERNAME/my-daily-journal.git
   ```
2. Navigate to the project directory:
   ```
   cd my-daily-journal
   ```
3. Grant execute permissions:
   ```
   chmod +x my-daily-journal
   ```
4. Run the application:
   ```
   ./my-daily-journal
   ```

### Using .deb Package
For Debian-based distributions:

1. Install the package:
   ```
   sudo dpkg -i my-daily-journal_1.1_amd64.deb
   ```
2. Run the application:
   ```
   my-daily-journal
   ```

### Using Snap
For Ubuntu users who prefer Snaps:

1. Install the Snap package:
   ```
   sudo snap install my-daily-journal_1.1_amd64.snap --dangerous
   ```
2. Run the application:
   ```
   my-daily-journal
   ```

---

## Usage Guide

Once installed, launch the application:
```
my-daily-journal
```
You'll enter an interactive command-line interface where you can perform various journal operations.

### Basic Commands

| Command | Description |
|---------|------------|
| 1 | Add a new entry |
| 2 | Change the active journal file |
| 3 | List all entries (paginated) |
| 4 | Read a specific entry |
| 5 | Search for keywords in journal entries |
| 6 | Edit an existing entry |
| 7 | Delete an entry |
| 8 | Undo the last operation |
| 9 | Show help documentation |
| 10 | Configure preferences (timestamps, wrap width, colors) |
| 11 | Exit the application |

---

### Undo and Backup System
Each modification (new entry, edit, delete) automatically creates a `.bak` file that can be restored using the **Undo** option.

- Backup files are stored as `filename.txt.bak`
- Undo only restores the **last modification**

---

## Development Setup
To contribute or modify the project:

1. Clone the repository:
   ```
   git clone https://github.com/YOUR_GITHUB_USERNAME/my-daily-journal.git
   ```
2. Ensure Python 3.x is installed:
   ```
   python3 --version
   ```
3. Modify the source code as needed.

---

## Building and Packaging

### Building the .deb Package
To create a new `.deb` package:

1. Run the following command:
   ```
   dpkg-deb --build my-daily-journal
   ```
This generates a new `.deb` file in the directory.

### Building the Snap Package
Ensure **snapcraft** is installed:

1. Install snapcraft:
   ```
   sudo snap install snapcraft --classic
   ```
2. Navigate to the project directory and build:
   ```
   snapcraft
   ```
This will generate a `.snap` package for installation.

---

## Technical Architecture

The **My Daily Journal** application is structured as follows:

- **CLI Interface:** Handles user interaction via a menu-driven command-line system.
- **File Handling Module:** Manages reading, writing, and backups of journal files.
- **Backup & Undo System:** Implements a fail-safe mechanism before any modification.
- **Search & Filtering:** Implements keyword-based lookup in journal entries.
- **Packaging System:** Includes configurations for both `.deb` and **Snap** deployments.

### Key Dependencies:
- Python 3.x
- shutil (for backups)
- textwrap (for formatting)

---

## Roadmap & Future Enhancements
- Add encryption support for journal files
- Implement cloud synchronization for multi-device access
- Develop a web-based UI alongside CLI
- Extend to support Windows with an `.exe` package

---

## License
This project is licensed under the **MIT License**, meaning it is **free to use, modify, and distribute**.

---

## Contributing
**How to contribute:**
1. **Fork** the repository.
2. **Create a new branch** (`feature-branch-name`).
3. **Commit your changes**.
4. **Push your changes** and **create a pull request**.

For major contributions, please **open an issue** first to discuss.

---

## Final Thoughts
The **My Daily Journal** project is built for **speed, reliability, and security**. It provides an efficient way to track journal entries in a structured manner. Whether you use it daily for notes, tracking thoughts, or project logs, this tool ensures **data safety** with **backups and undo functionality**.

For any **issues or enhancements**, feel free to **open an issue on GitHub**.

🚀 **Happy journaling!** 🚀
