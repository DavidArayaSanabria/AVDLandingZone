# Azure Virtual Desktop or AVD

Azure Virtual Desktop is a desktop and app virtualization service that runs on the cloud.

Here's what you can do when you run Azure Virtual Desktop on Azure:

Set up a multi-session Windows 10 and 11 deployment that delivers a full Windows 10 and 11 with scalability
Virtualize Microsoft 365 Apps for enterprise and optimize it to run in multi-user virtual scenarios
Provide Windows 7 virtual desktops with free Extended Security Updates
Bring your existing Remote Desktop Services (RDS) and Windows Server desktops and apps to any computer
Virtualize both desktops and apps
Manage Windows 10 and 11, Windows Server, and Windows 7 desktops and apps with a unified management experience

# Azure Virtual Desktop Landing Zone

Azure landing zones are the output of a multisubscription Azure environment that accounts for scale, security governance, networking, and identity. Azure landing zones enable application migration, modernization, and innovation at enterprise-scale in Azure. These zones consider all platform resources that are required to support the customer's application portfolio and don't differentiate between infrastructure as a service or platform as a service.

## Target audience

- Infrastructure Architect
- Application Developer
-	IT Professional
-	Cloud Solution Architect

# Azure Virtual Desktop Architure 

The [Template.json](Template.json) Azure Resource Manager template will help you automatically deploy the diagram below, which includes:

- A Hub Azure Virtual Network with two subnets, one for an Azure Network Gateway and one for DMZ.
- A Virutal Network Gateway and a Public IP address.
- A Spoke Azure Virtual Network for allocation Azure Virtual Desktop Hostpools.
- A Network Security Group with the necessary outbound rules for Azure Virtual Desktop Hostpools to properly activate and work.

![alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/dad885cfb0c6fca8913d68e4daa8dd9e6ee41c92/AVD%20Landing%20Zone%20Diagram.png?raw=true)


[Template.json](Template.json) can be modified to match your current infrastructure needs.

## Deploying an ARM Template using the Azure portal

- Visit https://portal.azure.com

Using the search bar on top type Templates

![alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/0c27bbe224b6c1e408883e4fd22b992d503549fd/Search.png?raw=true)

- Create a new template 

![alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/8bd3fb167da7f7c76eb01954d73f1ce6948a9a41/create.png?raw=true)

- Give a name and a description to the template

![alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/8bd3fb167da7f7c76eb01954d73f1ce6948a9a41/Name%20and%20Description.png?raw=true)

- Add for modified [Template.json](Template.json) and save it

![alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/8bd3fb167da7f7c76eb01954d73f1ce6948a9a41/add%20code.png?raw=true)

- Select the newly added template and click deploy

![alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/8bd3fb167da7f7c76eb01954d73f1ce6948a9a41/Select%20and%20deploy%20template.png?raw=true)

- Fill out the blanks with your details and click purchase

[alt image](https://github.com/DavidArayaSanabria/AVDLandingZone/blob/8bd3fb167da7f7c76eb01954d73f1ce6948a9a41/Fill%20out%20the%20details%20and%20purchase.png?raw=true)

- Allow 30 minutes for the deployment to complete
- Peer your Hub and Spoke Virtual Networks as needed

## Azure services and related products

- Azure Virtual Desktop
- Azure Networking
- Security

## Related references
- https://docs.microsoft.com/en-us/azure/virtual-desktop/overview
- https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/
- https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-connect-virtual-networks-portal#peer-virtual-networks
- https://docs.microsoft.com/en-us/azure/virtual-desktop/safe-url-list#virtual-machines
