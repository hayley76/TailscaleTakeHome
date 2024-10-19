# TailscaleTakeHome
# Tailscale Infrastructure

This repository contains infrastructure-as-code for deploying a Tailscale personal Tailnet, a subnet router, and a device with SSH enabled. In this example, the deployment is set up on an Azure Linux Virtual Machine (VM)

## Prerequisites

- A Tailscale account
    - Which you can create an account by going to https://tailscale.com/ and selecting the "Get Started" button. Follow the instructions for creating a personal account. 
- Azure VM. You can follow the instructions listed here https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu for creating a VM and deploying Linux Ubuntu onto it.
- Terraform 
- Git

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/tailscale-infrastructure.git
cd tailscale-infrastructure
