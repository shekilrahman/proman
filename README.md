
# 🚀 ProMan

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Shell Script](https://img.shields.io/badge/Shell_Script-121011?style=flat\&logo=gnu-bash\&logoColor=white)

> A powerful and intuitive **Bash CLI tool** to manage and launch your development projects in separate GNOME Terminal tabs — all with clean UI and automated workflows.

---

## 📚 Table of Contents

* [✨ Features](#-features)
* [🖼️ Screenshots](#-screenshots)
* [⚙️ Installation](#️-installation)
* [🧩 Dependencies](#-dependencies)
* [🚦 Usage](#-usage)

  * [🔹 Command-line Mode](#-command-line-mode)
  * [🔸 Interactive Mode](#-interactive-mode)
* [🛠️ Configuration](#-configuration)
* [🪵 Logging](#-logging)
* [🐞 Troubleshooting](#-troubleshooting)
* [🤝 Contributing](#-contributing)
* [📄 License](#-license)

---

## ✨ Features

### 🔧 Project Management

* Add, list, show, and delete projects effortlessly
* Assign multiple startup commands per project
* Navigate automatically to project directories

### 🧠 Smart Launching

* Launch all project commands in **separate GNOME Terminal tabs**
* Automatically set tab titles and working directories
* Minimal, colored output for clean UX

### 📊 Project Overview

* List all projects in a neat format
* View detailed project metadata
* Manage project configuration with ease

### 🪵 Logging & Debugging

* Auto-generated logs of all operations
* Helpful error messages
* Config stored in easy-to-edit **JSON** format

---

## 🖼️ Screenshots

> *(Coming soon: Add your terminal screenshots here!)*

---

## ⚙️ Installation

```bash
git clone https://github.com/shekilrahman/proman.git
cd project-launcher
chmod +x proman.sh
sudo ln -s "$(pwd)/proman.sh" /usr/local/bin/pro
```

---

## 🧩 Dependencies

* **GNOME Terminal**
* **Bash** (v4+ recommended)
* `jq` (for parsing JSON)

Install dependencies (Ubuntu/Debian):

```bash
sudo apt update
sudo apt install gnome-terminal jq
```

---

## 🚦 Usage

```bash
proman [command] [project_name]
```

### 🔹 Command-line Mode

| Command   | Description                        |
| --------- | ---------------------------------- |
| `launch`  | Launch a project (default command) |
| `add`     | Add a new project interactively    |
| `list`    | List all available projects        |
| `show`    | Show details of a project          |
| `delete`  | Delete a project                   |
| `help`    | Display help message               |
| `version` | Show version information           |

---

### 🔸 Examples

```bash
proman launch my-web-app      # Launch 'my-web-app' in tabs
proman add                    # Add a new project interactively
proman list                   # List all configured projects
proman delete old-project     # Remove 'old-project'
```

---

## 🛠️ Configuration

All project data is stored in:

```bash
~/.config/project-launcher/config.json
```

Edit manually using any text editor or manage via CLI.

---

## 🪵 Logging

Logs are saved automatically in:

```bash
~/.config/project-launcher/logs/
```

Each session is timestamped for easy debugging.

---

## 🐞 Troubleshooting

* **Issue**: Tabs close immediately
  ✅ *Solution*: Make sure each command/script ends with `; exec bash` or use `bash -c` with quoted commands.

* **Issue**: `jq` not found
  ✅ *Solution*: Install via `sudo apt install jq`

* **Issue**: GNOME Terminal not available
  ✅ *Solution*: This tool currently supports only **GNOME Terminal**.

---

## 🤝 Contributing

Feel free to fork this project, submit issues, or open PRs. Contributions are welcome!

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).


