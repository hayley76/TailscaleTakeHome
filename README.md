# TailscaleTakeHome
# Tailscale Infrastructure

This repository contains infrastructure-as-code for deploying a Tailscale personal Tailnet, a subnet router, and a device with SSH enabled. In this example, the deployment is set up on an Azure Linux Virtual Machine (VM)

## Prerequisites

- A Tailscale account
     - You can create an account by visiting Tailscale's website at https://tailscale.com/ and clicking the 'Get Started' button. Follow the instructions to create a personal account.
- Azure VM
     - You can follow the instructions listed here https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu for creating a VM and deploying Linux Ubuntu onto it.
- Terraform
    - Run the following command in your VM console:
      - sudo apt update && sudo apt install terraform
- Git
      - You can install onto your VM by running the following commands:
          - sudo apt update
          - sudo apt install git
          - git --version

## Setup Instructions

### 1. Clone the Repository

In your VM console run the following to be able to clone your respository.
```bash
git clone https://github.com/your-username/tailscale-infrastructure.git
cd tailscale-infrastructure
