# Tailscale Take Home Assignment
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
        ```
- Git
      - You can install onto your VM by running the following commands:
           ```bash
            sudo apt update
            sudo apt install git
            git --version
            ``
## Technologies Used

This project is built using the following technologies:

- [Tailscale](https://tailscale.com/) - A simple, secure mesh VPN.
- [Azure](https://azure.microsoft.com/) - Cloud platform for hosting the VM and subnet router.
- [Terraform](https://terraform.io/) - Infrastructure-as-code tool to automate the deployment.

## Setup Instructions

### 1. Clone the Repository
In your VM console run the following to be able to clone your repository.
```bash
git clone https://github.com/hayley76/tailscale-infrastructure.git
cd tailscale-infrastructure
```

### 2. Accessing Deployed Resources

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
     ```
### 6. **Documentation**

1. **Installing Tailscale**: Refer to the following instructions: https://tailscale.com/kb/1347/installation
2. **Enabling SSH**: Refer to the following instructions: https://tailscale.com/kb/1193/tailscale-ssh?q=ssh
3. **Subnet Routers**: Refer to the following instructions: https://tailscale.com/kb/1019/subnets?q=subnet
4. **Setting up a GitHub Repository**: Refer to the following instructions: https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories
5. **Terraform**: Refer to the following instructions: https://developer.hashicorp.com/terraform/tutorials
6. **Creating Azure VM:** Refer to the following instructions: https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu

### 6. **Troubleshooting**

1. **Unable to SSH into the VM**: Ensure that your SSH keys are properly configured and that the VM is accessible via its Tailscale IP. For instructions for please refer to the documentation above.
2. **Deployment Issues**: If Terraform reports errors, ensure you have the correct Azure credentials set up and that your account has the necessary permissions.
