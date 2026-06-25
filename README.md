# Multi-Node Linux Automation & Configuration Management Lab

This production-ready repository serves as a practical showcase of enterprise infrastructure-as-code (IaC) and configuration management. Leveraging my foundational background as a Linux Infrastructure Engineer, this project demonstrates scalable automation pipelines using Ansible, Git Flow methodologies, and secure DevOps standards.

## 🛠️ Infrastructure & Environment Architecture
* **Control Node**: Rocky Linux 9.8 (Running Visual Studio Code workstation)
* **Target Nodes**: Multi-VM cluster running Enterprise Linux variants.
* **Network & Security**: Secure SSH Key Authentication (`ed25519`) with centralized task execution policies

## 📁 Repository Structure & Inventory Control
The project adheres strictly to standard Ansible directory structures to ensure clean role separation and modular playbook delivery:
* `ansible.cfg` - Customized for modern, human-readable YAML console formatting and automated timer diagnostics.
* `hosts` - Centrally managed inventory mapping target tiers (`[loadbalancer]`, `[webservers]`, `[db]`, `[control]`).
* `playbooks/` - Dedicated directory isolating active task scripts.
* `roles/` - Structured configuration bundles divided into functional infrastructure pillars:
  * `os_configuration` - Base operating system hardening, package updates, and system services.
  * `performance` - Kernel tuning, resource allocation optimization, and performance profiling.
  * `security` - SSH hardening (root access restrictions), firewall rules, and policy compliance.
  * `useradmin` - Centralized POSIX user creation, access control lists, and automated permission keys.

## 🚀 Applied Workflows & Git Methodologies
This lab utilizes strict **Git Flow** branching standards (`feature-` prefixes) to simulate cross-functional engineering workflows:
1. **Isolation**: Development occurs on isolated branches (e.g., `feature-security`) to ensure trunk stability.
2. **Verification**: Playbooks undergo syntax validation and dry-run simulation using Ansible Check Mode (`--check`).
3. **Integration**: Successful configurations are safely merged into the production `main` branch to guarantee predictable configuration state drift management.
