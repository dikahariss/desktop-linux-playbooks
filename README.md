# Ubuntu 24 Desktop Setup with Ansible

This repository contains an Ansible playbook for setting up a comprehensive development environment on Ubuntu 24.

## Prerequisites

- A fresh installation of Ubuntu 24 Desktop
- Internet connection
- Sudo privileges

## Getting Started

1. Update your system:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. Install Ansible and required collections:
   ```bash
   sudo apt install software-properties-common
   sudo add-apt-repository --yes --update ppa:ansible/ansible
   sudo apt install ansible
   ansible-galaxy collection install community.general
   ```

3. Clone this repository:
   ```bash
   git clone https://github.com/dikahariss/ubuntu24-desktop.git
   cd ubuntu24-desktop
   ```

4. Review and customize the playbook (`ubuntu24_desktop_setup.yml`) if needed.

5. Run the Ansible playbook:
   ```bash
   ansible-playbook playbooks/ubuntu24_desktop_setup.yml --ask-become-pass
   ```

## What's Included

- Essential development tools (Git, Curl, Wget, Vim, Tmux, etc.)
- Docker and Docker Compose
- Snap packages (VS Code, LibreOffice, Discord, etc.)
- IDEs and Text Editors:
  - Visual Studio Code
  - JetBrains IDEs (IntelliJ IDEA Ultimate, DataGrip, PhpStorm, WebStorm, PyCharm Professional)
- Browsers: Google Chrome, Firefox, Brave
- Communication tools: Discord, Telegram, Zoom
- Productivity tools: LibreOffice, Evince, Thunderbird
- Development tools: Postman, kubectl, OWASP ZAP
- Security tools: UFW (Uncomplicated Firewall), Nmap, OpenVPN3
- Other utilities: VLC, OBS Studio, Bitwarden, Pinta

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