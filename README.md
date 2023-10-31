# SNMP Up with Ansible

## Overview

SNMP Up is a project that simplifies the configuration and management of the Simple Network Management Protocol Daemon (`snmpd`) using Ansible. This README provides an overview of the project, its features, and instructions on how to get started.

In the first deployment we use it on PRTG service but in a new version it's developed on another services like `Influxdb` and `Grafana`.

## Table of Contents

1. [Introduction](#snmp-up-with-ansible)
2. [Overview](#overview)
3. [Features](#features)
4. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
   - [Usage](#usage)

## Features

SNMP Up offers the following features:

- **Simplified Configuration:** Easily configure and manage `snmpd` on your servers using Ansible playbooks.

- **Scalability:** Works with a single server or a large infrastructure. You can customize the configurations as needed.

- **Automation:** Reduce manual configuration tasks by automating SNMP setup and maintenance.

- **Security:** Ensure that your SNMP configuration adheres to security best practices.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following:

- [Ansible](https://www.ansible.com/) installed on your system.

### Installation

1. Clone the SNMP Up repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/snmp-up.git
   ```

2. Change to the project directory:

   ```bash
   cd snmp-up
   ```

3. Install ansible via `pip`:

    ```bash
    python -m venv venv
    source venv/bin/active
    pip install -U pip
    pip install -r requirements.txt
    ```

### Usage

1. Edit the `snmpd` configuration inventory to customize SNMP settings and hosts. You can find the inventory file at `inventory/inventory.ini`.

   ```bash
   cp inventory/inventory.ini.sample inventory/inventory.ini
   vim inventory/inventory.ini
   ```

2. Run the playbook to apply the configuration to your servers:

   ```bash
   ansible-playbook -i inventory/inventory.ini ansible/deploy.yml
   ```

Thank you for using SNMP Up! We hope it simplifies your SNMP configuration and management tasks.
