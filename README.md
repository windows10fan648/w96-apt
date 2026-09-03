# Windows 96 APT Repository

The Windows 96 APT repository provides packages for Windows 96 development tools and applications.

**Repository:** `https://w96apt.duckdns.org/`

**Architecture:** `amd64`

**Suite:** `stable`

---

## Installation

### 1. Add the W96 repository

Create an APT sources file:

```bash
echo "deb [trusted=yes] https://w96apt.duckdns.org stable main" | sudo tee /etc/apt/sources.list.d/w96.list
```

### 2. Update package lists

```bash
sudo apt update
```

APT will now retrieve the Windows 96 package information from the repository.

### 3. Install a W96 package

For example, to install the Windows 96 project generator:

```bash
sudo apt install w96-project-generator
```

### 4. Verify the installation

Check that `w96-new` is available:

```bash
w96-new --help
```

You can then create a Windows 96 project using one of the supported templates:

```bash
w96-new basic
w96-new gui
w96-new console
```

---

## Repository Configuration

The repository is configured as:

```text
deb https://w96apt.duckdns.org stable main
```

The repository currently provides packages for:

```text
amd64
```

---

## Repository Layout

```text
dists/
└── stable/
    ├── Release
    └── main/
        └── binary-amd64/
            └── Packages
```

---

## HTTPS

The repository is served over HTTPS:

`https://w96apt.duckdns.org/`

TLS is provided by Vercel.

---

## Updating W96 Packages

After adding the repository, update the package lists whenever you want to check for new versions:

```bash
sudo apt update
```

Then upgrade installed W96 packages normally:

```bash
sudo apt upgrade
```

---

## Removing the Repository

To remove the W96 repository:

```bash
sudo rm /etc/apt/sources.list.d/w96.list
```

Then refresh APT:

```bash
sudo apt update
```

---

## Current Packages

### `w96-project-generator`

Windows 96 project generator providing the `w96-new` command.

Supported project templates:

* `basic`
* `gui`
* `console`

---

## Windows 96

This repository is part of the Windows 96 development ecosystem and provides packages for developing and working with Windows 96 software.
