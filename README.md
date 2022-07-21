# Connecting two VMs using a Virtual Network via the Azure Portal
![VirtualNetworkLogo](img/virtual-network-logo.png)


---------------------------------------------------------


## Requirements
- Microsoft Azure Account ( with funds or credits )
- Microsoft Azure Suscription
- A web browser
- Access to internet

---------------------------------------------------------

## Instructions
#### 1. Login to the [Azure Portal](https://portal.azure.com/).
#### 2. Once you're on the portal's home page, you will see something like this:
![PortalImage](img/portal-main.png)
#### 3. Inside the search bar (located at the top), look for *virtual machines* and click on it.
![Searchbar](img/searchbar.png)
#### 4. Click on *Create* and then *Azure virtual machine*.
![CreateVMButton](img/create-vm-button.png)
#### 5. First, you'll need to select or create a resource group. I will be creating one be by clicking *Create new*
![ResourceDetails](img/resource-group-create.png)
#### 6. Now, you have to configure the first virtual machine's details: name, region, operating system (image) and size are mandatory, the rest are optional.
![FirstVMConfig](img/vm1-config-instance.png)
#### 7. You will also need to configure the administrator account for this VM; just give it a name and a password.
![VM1AdminDetails](img/vm1-admin.png)
#### 8. If you chose Windows as your OS, confirm that you have the licensing to use it by checking the box at the bottom of the basics tab.
![LicensingVM1](img/vm1-licensing.png)
#### 9. Go to the *Networking* tab (ths menu  is available at the top side of the page).
![Tabs](img/tabs.png)
#### 10. Check that every option inside the network interface configuration is similar to the one below.
![NetworkInterface](img/vm1-network-interface.png)
#### 10. You can configure the rest of the VM's details if you want. When you're ready click *Review + create*.
![ReviewAndCreate](img/review-and-create.png)
#### 11. If validation passed, click *Create*.
![CreateButton](img/create.png)
#### 12. Deployment will begin. Please wait until it's over.
![ImplementationInProgress](img/deployment-progress.png)
#### 13. Once deployment has been completed, click on *Create another VM*.
![CreateAnotherVM](img/create-another-button.png)
#### 14. Now, configure the other VM's details.
![SecondVMConfig](img/vm2-details.png)
#### 15. Go to the *Networking* tab and make sure you have the same virtual network and disable the network security group. Then review and create it.
![VM2Networking](img/vm2-networking.png)
#### 16. Wait for deployment to complete.
![DeploymentProgress](img/deployment-progress.png)
#### 17. Once deployment has completed, go ot your resource group. 
![ResourceGroup](img/resource-group.png)
#### 18. Click inside one of your VMs and connect to it using your favorite RDP connection app (like [Windows Remote Desktop](https://www.microsoft.com/store/apps/9wzdncrfj3ps)).
![ConnectToVM1](img/vm1-connect.png)
![RDPDownload](img/rdp-download.png)
![ConnectingToVM](img/connecting-to-vm.png)
#### 19. If this appears inside your VM's desktop, click yes.
![AllowOtherDevices](img/discoverable.png)
#### 20. Inside your VM, open Powershell as administrator inside your VM by clicking on the windows icon on the bottom left of the VM's screen and typing *powershell* and then clicking *Run as administrator*.
![OpenCMD](img/powershell.png)
#### 21. Type *ipconfig* and press enter. This will give you your VM's IP.
![ipconfig](img/ipconfig.png)
#### 22. Go back the Azure Portal using your main PC, then, go back your resource group and click on your virtual network.
![VirtualNetwork](img/virtual-network.png)
#### 23. On the left side, click on *Connected devices*, you will see both of your VMs. Identify which one you did not connect to using the IP addresses.
![ConnectedDevices](img/connected-devices.png)
#### 24. Inside your VM, type *mstsc /v:(your other VM's ip)* to connect to it.
![mstsc](img/mstsc.png)
#### 25. Insert your other VM's credentials, then ok, then yes  .
![OtherVM'sCredentials](img/other-vm-credentials.png)
#### 26. You will now be using a remote VM inside a remote VM, congratulations!
![RemoteRemoteVM](img/remote-remote-vm.png)



---------------------------------------------------------


## Congratulations ! You've just connected two VMs inside a virtual network !
Don't forget to delete or pause all of your resources! If you don't, it will be very expensive.