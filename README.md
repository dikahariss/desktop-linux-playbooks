# Desktop Linux Setup Playbooks

This repository contains Ansible playbooks for setting up comprehensive development environments on various Linux desktop distributions, including but not limited to Ubuntu, and Pop!_OS.

## Prerequisites

- A fresh installation of a Debian-based Linux distribution (e.g., Ubuntu, Pop!_OS)
- Internet connection
- Sudo privileges

## Getting Started

1. Update your system:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. Install Ansible and required collections:
   ```bash
   sudo apt install ansible
   ansible-galaxy collection install community.general
   ```

3. Clone this repository:
   ```bash
   git clone https://github.com/dikahariss/desktop-linux-playbooks.git
   cd desktop-linux-playbooks
   ```

4. Review and customize the playbooks in the `playbooks` directory as needed.

5. Run the main Ansible playbook:
   ```bash
   ansible-playbook playbooks/ubuntu24_desktop_setup.yml --ask-become-pass
   ```

6. Optionally, run additional playbooks:
   ```bash
   ansible-playbook playbooks/install_zsh_oh_my_zsh.yml --ask-become-pass
   ```

## Available Playbooks

- `ubuntu24_desktop_setup.yml`: Main playbook for setting up a development environment
- `install_zsh_oh_my_zsh.yml`: Installs Zsh and Oh My Zsh
- `pop!os_desktop_setup.yml`: Setup for Pop!_OS (if applicable)

## What's Included

- Essential development tools (Git, Curl, Wget, Vim, Tmux, etc.)
- Docker and Docker Compose
- Snap packages (VS Code, LibreOffice, Discord, etc.)
- IDEs and Text Editors
- Web Browsers
- Communication tools
- Productivity tools
- Development and security tools
- Multimedia applications

## Customization

Feel free to modify the playbook to suit your specific needs. You can add or remove tasks, change software versions, or include additional tools you frequently use.

## Post-Installation

After running the playbook:
1. Restart your system or log out and log back in to ensure all changes take effect.
2. Configure your Git global settings:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
3. For JetBrains IDEs, you may need to activate your license or start your trial.


---

Happy coding! 🚀