# Azure_Windows_VM creation
Creating an Azure Windows VM using the Azure Portal and connecting to the VM with RDP
## Microsoft Azure
Microsoft Azure, commonly referred to as Azure, is a cloud computing platform and service offered by Microsoft. It provides a wide range of cloud-based services, including infrastructure as a service (IaaS), platform as a service (PaaS), and software as a service (SaaS) that can be used for various purposes such as hosting web applications, running virtual machines, storing data, and more. Microsoft Azure is widely used by organizations of all sizes for its scalability, reliability, and extensive set of services. It allows businesses to leverage cloud technology to innovate, reduce costs, and scale their applications and infrastructure as needed.
# Resource Group
Resource group is a logical container used to organize and manage Azure resources
## Create a Resource Group (RG)
1. Log in to Azure Portal (portal.azure.com). Sign in with your Azure username and password.
2. Azure dashboard is displayed. Search for Resource Group either using the search button, navigation (if RG has been previously accessed) or the left-hand menu ico 
3. click the + sign at the top to create the Resource group
4. We have 3 sub-tab icons:
   
   "BASICS" tab which consist of
       1. Project Details:
          a. Subscription: Select the Azure subscription to associate with this resource group.
          b. Name the Resource group: Enter a unique name for your resource group. This name should be descriptive and help you identify its purpose.
      
       2. Resource Details: Collection of resources that share the same lifecycle, permission and policies
          a.Region: Choose the Azure region where you want to create the resource group. 

    "TAGS" tab: for unique identification. Tags are key-value pairs that you can use to categorize and filter resources.It consists of name and Value
   
     "REVIEW + CREATE" tab: Review the information you entered for accuracy. Once you're satisfied with the settings, click the "Review + create" button at the bottom of the page.

  Validation will be completed once there are no conflicts or issues. You can download a template for automation

Create the Resource Group: After validation passes, click the "Create" button to create the resource group.
A notification that the resource group has bee created will be shown. Once the resource group is created, it would show on the Azure dashboard

Click on the name of the Resource Group created. The following menu will appear at the left side of the worksheet:
1. Overview
2. Activity log
3. Access Control
4. Tags
5. Resource Visualizer
6. Events

SETTINGS which include:
1. Deployments
2. Security
3. Deployment Sacks
4. Policies
5. Properties
6. Locks

Cost Management, Monitoring and Automation can also be seen.

RESOURCE GROUPS can also be created via the Cloud Shell route
1. Lunch the Cloud Shell
2. You will see both Bash and PowerShell
3. Click on Bash
4. You will be promted to create a storage
5. Once you create the storage, a successful notification will be seen
6. create the Resource group by typing the command (az group -- create RG)

# VIRTUAL MACHINES
Virtual machines are a fundamental resource that allows users to run and manage virtualized OS and applications
## Creating a VM
1. Search for Virtual machines
2. Click on Create Virtual Machines
3. To create a new VM, click the "+ Add" button at the top of the Virtual machines page.
   VMs can either run on Linux or Windows. We have the following Sub Tabs
### Basics Configuration:
    -- Project Details: 
    a. Select your Azure subscription.
    b. Resource Group: Choose an existing resource group or create a new one.
    
    -- Instance Details:
      a. Virtual Machine Name: Enter a unique name for your VM.
      b. Region: Choose the Azure region where you want to deploy your VM.
      c. Availability options
      d. Availability zone
      e. Security type
      f. Image: Select an operating system image. For RDP access, you can choose a Windows Server image.
      g. Size: Choose the VM size based on your requirements.

   -- Administrator Account:The user will be prompted to input 
      a. Username
      b. Enter a username and password. These credentials will be used for RDP access to the VM.

    --Inbound Port Rules:
       a. Public inbound ports
       b. Select Inbound ports --- RDP 3389

### Disks:
   - Configure the OS disk and any additional data disks as needed. You can specify the disk type and size.
### Networking:
   - Configure the virtual network settings, including subnet, public IP address and Network Security Group rules.
### Management:
   - Configure options like Boot diagnostics, Guest OS diagnostics, and Auto-shutdown according to your preferences.
### Advanced:
    - Configure additional settings like extensions, custom scripts, and tags if necessary.
### Tags 
### Review + Create:
    Review the configuration settings you've provided. Ensure everything is accurate.
Once the user is done with all these, the next step is 
4. Create the Virtual Machine: Click the "Review + create" button, and then click "Create" to start deploying your VM.
5. Deployment Progress: Azure will begin creating your Virtual Machine. You can monitor the deployment progress on the Azure Portal dashboard.
6. Access VM via RDP: Once the deployment is complete, you can access the VM via RDP. Open the Remote Desktop Client on your local machine, enter the VM's public IP address, and use the username and password you set up earlier to log in.

