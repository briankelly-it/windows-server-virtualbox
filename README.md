<p align="center">
<img width="70%" align="center" src="https://i.imgur.com/63AvPgG.png" alt="windows 10 logo"/>
</p>

<h1>Windows Server Installation within VirtualBox</h1>
This tutorial outlines the steps to create a virtual machine running Windows Server inside of VirtualBox.<br />

<h2>Environments and Technologies Used</h2>

- Oracle VirtualBox

<h2>Operating Systems Used </h2>

- Windows Server 2016

<h2>List of Prerequisites</h2>

- Download and install VirtualBox - [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

<br />

<h1>Installation Steps</h1>

<h2>Step 1: Download Windows Server 2016</h2>

<p>To download Windows Server 2016 just visit the URL below and click "Download the ISO":</p>
<p>https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2016?filetype=ISO</p>

<p>
<img src="https://i.imgur.com/1JbQ8bN.png" width="80%" alt="Media Creation Tool download"/>
</p>

<p>Sign up for the Free Trial and click Download Now. This will give you 180 days to try Windows Server.</p>


<br />
<h2>Step 2: Create a VM in VirtualBox</h2>

<p>Once you have Windows Server downloaded, open up VirtualBox. From here, we need to create a new VM. You can do this by clicking the "New" button as shown below:</p>
<img src="https://i.imgur.com/Yk7s7BU.png" width="50%" alt="Media Creation Tool download"/>

<p>This will open the "Create Virtual Machine" dialog in Guided Mode. In the <a href="https://github.com/briankelly-it/windows-10-virtualbox">Windows 10 Tutorial</a> we used Guided Mode but this time we will use Expert Mode which allows use to create VMs a little quicker having all the settings on one screen. Click "Expert Mode" at the bottom.</p>
<img src="https://i.imgur.com/JiYI6BJ.png" width="70%" alt="Media Creation Tool download"/>

<p>Name your VM whatever you like, then move onto the "Hardware" and "Hard Disk" sections. For Hardware I recommend increasing the defaults to 4GB (4096) and 2 CPUs for a little more performance. Also I increase the hard disk size to 60GB but this isn't completely necessary if you don't have the extra sapce. Just know that the VM will use YOUR PC's resources so whatever the VM is using, the PC will not be able to use.</p>

<img src="https://i.imgur.com/vo6UiBy.png" width="49%" alt="Media Creation Tool download"/>
<img src="https://i.imgur.com/BQBXm4t.png" width="49%" alt="Media Creation Tool download"/>
<img src="https://i.imgur.com/9yeRl7t.png" width="49%" alt="Media Creation Tool download"/>

<p>Once you have made all of these selections you can click "Finish" to create the VM.</p>

<br /> 
<h2>Step 3: Install Windows Server on the VM</h2>

<p>In order to install Windows on the VM, we need to <b>mount</b> the ISO file. This is no different than inserting a USB or a CD-ROM with Windows into your computer. First, select the VM you just created on the left and click "Settings" as shown below:</p>
<img src="https://i.imgur.com/Xb0T0cR.png" width="50%" alt="Media Creation Tool download"/>

<p>Under the VM settings, click the Storage tab and click the disk icon under the "Storage Devices" section. In the image below, it has the word "Empty" next to it indicating that there is no optical disc (or disc image) selected. Then select the dropdown disc icon and click "Choose a disk file..."</p>
<img src="https://i.imgur.com/lUhHj3J.png" width="90%" alt="Media Creation Tool download"/>


<p>From here just navigate to the ISO you wish to mount to the VM. Once you selected the ISO click OK and save the settings. At this point we are ready to launch the VM.</p>

<p>To start a VM in VirtualBox you just need to right-click on the VM and select Start > Normal Start. (or just double-click the VM)</p>
<img src="https://i.imgur.com/67Bk04p.png" width="50%" alt="Media Creation Tool download"/>

<p>After the VM starts up, click next on the first Windows Setup screen to proceed, then "Install Now".</p>
<img src="https://i.imgur.com/C7M9r2h.png" width="70%" alt="Media Creation Tool download"/>

<p>On the next screen you will be asked to select the operating system you want to install. Here is an overview of the different versions you could install:</p>

- <b>Standard</b> - The standard version of Windows Server is designed for small businesses.
- <b>Datacenter</b> - This is designed for big business and large data center deployments.
- <b>Desktop Experience</b> - The desktop experience is the MOST commonly installed version of Windows Server.
- <b>Server Core</b> - This is a command-line version only. You install it by selecting anything other than "(Desktop Experience)".

<p>For this tutorial you will want to make sure you install the "Desktop Experience". It doesn't matter if you chose Standard or Data center. That is entirely up to you.</p>
<img src="https://i.imgur.com/k5Dgean.png" width="50%" alt="Media Creation Tool download"/>

<p>Click Next, and on the next screen accept the license terms and click Next again.</p>

<p>Click on the "Custom: Install Windows Only (advanced)" since this is a fresh installation of Windows. On the next screen select the drive you wish to install Windows Server on (there should only be one, the virtual drive created during the VM creation step) and click Next to begin the installation.</p>
<img src="https://i.imgur.com/Puut87l.png" width="50%" alt="Media Creation Tool download"/>
<img src="https://i.imgur.com/rNPbdyg.png" width="50%" alt="Media Creation Tool download"/>

<p>Congrats! You've successfully installed Windows Server 2016 on a VirtualBox VM.</p>

<br />
<h2>Next Steps...</h2>

<p>After the VM restarts, it will ask you for a password. Enter a password for your Administrator account that you will use to login with and click Finish.</p>
<img src="https://i.imgur.com/kGI2tmk.png" width="50%" alt="Media Creation Tool download"/>

<p>In order to login you might need to press Ctrl+Alt+Del, but this won't work because your PC will take the input instead of the VM. To get around this, VirtualBox has an "Input" menu allowing you to do actions such as this.</p>

<p>At the top of the VirtualBox window, click Input > Keyboard > Insert Ctrl+Alt+Del.</p>
<img src="https://i.imgur.com/MRfBcsd.png" width="80%" alt="Media Creation Tool download"/>

<p>Now you can login and enjoy Windows Server 2016!</p>

<h3>Related Tutorials</h3>

- [Installing Windows 10 within VirtualBox](https://github.com/briankelly-it/windows-10-virtualbox)
- [Installing and Configuring Active Directory](https://github.com/briankelly-it/configure-active-directory)
