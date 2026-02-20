# ⚙️ Ansible Automation Learning & Practice

This repository serves as a structured collection of my **Ansible** learning journey, from core fundamentals to real-world automation scenarios. It contains playbooks, inventory configurations, and practical examples demonstrating Infrastructure as Code (IaC) principles.

The primary goal of this repository is to build a robust foundation in configuration management and server automation, specifically tailored for DevOps and Cloud Engineering roles.

---

## 📖 What is Ansible?

Ansible is a powerful, open-source IT automation tool. It is unique because it is **agentless**, meaning you do not need to install special software on the servers you want to manage. It connects via standard SSH.

It is widely used in the industry for:
* **Configuration Management:** Ensuring servers are set up exactly the same way every time.
* **Application Deployment:** Automating the release of complex, multi-tier applications.
* **Server Provisioning:** Setting up raw servers with necessary dependencies.
* **Task Automation:** Replacing manual, repetitive bash scripts with declarative YAML.

---

## 📂 Repository Structure & Topics Covered

This repository is broken down into easily digestible playbooks, each focusing on a core concept of Ansible:

* **`01-playbook-structure`**: Understanding the basic YAML layout (`hosts`, `tasks`, `name`).
* **`02-variables`**: Declaring, scoping, and accessing data using Jinja2 templating (`vars`, `{{ }}`).
* **`03-modules`**: Practical examples of common modules (`command` vs `shell`, `package`, `service`, `file`).
* **`04-loops`**: Executing tasks iteratively using simple lists and dictionaries (`loop`, `item`).
* **`05-conditions`**: Controlling task execution flow based on dynamic data (`when`).
* **`06-error-handling`**: Managing failures gracefully without crashing the playbook (`ignore_errors`, `register`).
* **`07-filters`**: Transforming data formats on the fly (e.g., String to List, Dict to JSON).
* **`08-idempotency`**: Demonstrating Ansible's golden rule: achieving the desired state (`state: present/absent`) safely.

---

## 🚀 How to Run the Playbooks

Ensure you have Ansible installed on your control node. Most of these playbooks are configured to run locally for testing purposes (`hosts: localhost`, `connection: local`).

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/chellojuramu/ansible.git](https://github.com/chellojuramu/ansible.git)
    cd ansible
    ```

2.  **Execute a specific playbook:**
    ```bash
    ansible-playbook <playbook-name>.yml
    ```
    *Example:* `ansible-playbook 16-idempotency.yml`

---

## 🔜 Next Steps: The RoboShop Project

The concepts demonstrated in these basic playbooks are currently being utilized to transition a legacy, shell-script-based microservices architecture (**RoboShop**) into fully automated, declarative Ansible playbooks.

*Developed and maintained as part of an ongoing DevOps learning initiative.*
