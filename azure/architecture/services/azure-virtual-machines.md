
# Azure Virtual Machines

VMs provide IaaS, and can be used in many ways.

The user can:
- Have complete control over the OS
- The ability to run custom software
- Use custom hosting configs 

VMs provide virtualisation without having to maintain the physical hardware.

Several images are available allowing for rapid provision. You can also provide your own image.

# Scale VMs

Single VMs can be run for testing, development, or minor tasks.

VMs can be grouped together to provide availability, scalability, and redundancy.

Azure can manage this with:
- Scale sets
- Availability sets

## VM Scale Sets

> Allows you to create a group of identical, load-balanced VMs.

Creating VMs manually would take more time to configure and then monitor to determine if they are scaled
well.

Scale Sets automate the manual work. VMs scan be configured, updated, and scaled to demand very
quickly. Scale sets automatically deploy a load balancer to ensure efficiency.

## VM Availability Sets

> Allow you to create available environments through VMs with staggered updates, varied power, and
  different network connections.

These sets ensure the environment is highly available.

This is done through grouping into two methods:

1. Update Domain
    - Groups VMs that can be rebooted at same time.
    - Updates can be applied knowing that only one update domain grouping will be offline at the
      same time.
2. Fault Domain
    - Groups VMs by common power source and network switch. VMs, by default, are split between 3 fault
      domains.
    - Protects against physical or network failures.

# VM Usage Examples

- Testing and development
    - Easy way to create different OS and application configurations
    - When not needed, the VMs can easily be deleted
- Running applications in the cloud
    - Allows for scaling with demand
- Extending data-centre to the cloud
    - Adding additional VMs to the cloud could be cheaper than expanding an on-prem environment
- During disaster recovered
    - If a data centre fails, VMs running on Azure can take over running critical applications
    - Once the primary datacenter becomes operational again, the VMs can be deprovisioned

# Creating VMs

To create a VM,

```
az vm create \
  --resource-group learn-e5877dab-0505-4caf-9232-26850dabbd35 \
  --name my-vm \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
```

We then run this script hosted on github,

```bash
#!/bin/bash

# Update apt cache.
sudo apt-get update

# Install Nginx.
sudo apt-get install -y nginx

# Set the home page.
echo "<html><body><h2>Welcome to Azure! My name is $(hostname).</h2></body></html>" | sudo tee -a /var/www/html/index.html
```

We do this with,
```
az vm extension set \
  --resource-group learn-e5877dab-0505-4caf-9232-26850dabbd35 \
  --vm-name my-vm \
  --name customScript \
  --publisher Microsoft.Azure.Extensions \
  --version 2.1 \
  --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' \
  --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
```


