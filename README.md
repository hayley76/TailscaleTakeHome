# Tailscale Take Home Assignemtn
# Tailscale Infrastructure

This repository contains infrastructure-as-code for deploying a Tailscale personal Tailnet, a subnet router, and a device with SSH enabled. In this example, the deployment is set up on an Azure Linux Virtual Machine (VM)

## Prerequisites

- A Tailscale account
     - You can create an account by visiting Tailscale's website at [Tailscale]https://tailscale.com/ and clicking the 'Get Started' button. Follow the instructions to create a personal account.
- Azure VM
     - You can follow the instructions listed here [Azure]https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu for creating a VM and deploying Linux Ubuntu onto it.
- Terraform
    - Run the following command in your VM console:
      - ```bash
        sudo apt update && sudo apt install terraform
- Git
      - You can install onto your VM by running the following commands:
           ```bash
            sudo apt update
            sudo apt install git
            git --version

## Technologies Used

This project is built using the following technologies:

- [Tailscale](https://tailscale.com/) - A simple, secure mesh VPN.
- [Azure](https://azure.microsoft.com/) - Cloud platform for hosting the VM and subnet router.
- [Terraform](https://terraform.io/) - Infrastructure-as-code tool to automate the deployment.

## Setup Instructions

### 1. Clone the Repository

In your VM console run the following to be able to clone your respository.
```bash
git clone https://github.com/your-username/tailscale-infrastructure.git
cd tailscale-infrastructure

## Accessing Deployed Resources

Once the deployment is complete:

1. Log in to the Tailscale admin console [here](https://login.tailscale.com/).
2. Find the Tailscale IP address of your deployed Azure VM.
     - You can do this by running the following on your VM console "ip addr show tailscale0" or you can find the IP address on your Tailscale Admin Console under the Addresses column.
3. Use the following command to SSH into the VM:
   ```bash
   ssh username@<tailscale-ip>
Example:
     ```bash
     ssh  hayley76@100.99.207.24
