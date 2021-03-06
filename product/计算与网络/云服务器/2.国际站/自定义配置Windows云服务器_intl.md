This document introduces the custom configuration of Windows CVM.
Different from quick configuration, custom configuration provides full options, and you can choose the appropriate configuration based on your needs.

<div id="page1"></div>
## Prerequisites

 1. Before getting started with custom configuration, you need to complete Step 1 in ["Quick Start for Windows CVM"](/doc/product/213/2764#.E6.AD.A5.E9.AA.A4.E4.B8.80.EF.BC.9A.E5.87.86.E5.A4.87.E4.B8.8E.E9.80.89.E5.9E.8B) document.
 2. Go to the Tencent Cloud official website, select **Cloud Products** -> **Computing and Website** -> **CVM**, then click **Buy Now** button to enter the [CVM purchase page](https://buy.cloud.tencent.com/buy/cvm).
 3. Click **Custom Configuration** to go to the custom configuration interface.

<div id="page2"></div>
## Selecting Region and Model
![](//mc.qcloudimg.com/static/img/3ed8bab8cce3dde578a6e3fb14267ea5/image.png)
 1. Select a billing method: Prepaid or Postpaid (users who cannot purchase postpaid CVMs need to complete [Identity Verification](https://console.cloud.tencent.com/developer/infomation) first). For more information, please see [Billing Methods](https://cloud.tencent.com/document/product/213/2180).

 2. Select a region and an availability zone. When you need more than one CVMs, it is recommended that you choose different availability zones to implement disaster recovery.

 3. Select a model and configuration.
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Based on different underlying hardware, Tencent Cloud offers two series of instances: **Series 1** and **Series 2** (also referred to as **last-generation instance** and **current-generation instance**). They respectively provide the following instance types:

- Last-generation instance types: Standard S1, High IO I1, MEM Optimized M1
- Current-generation instance types: [Standard S2](/doc/product/213/7154), [High IO I2](/doc/product/213/7155), [MEM Optimized M2](/doc/product/213/7156), [Computing C2](/doc/product/213/7157), [GPU-based G2](/doc/product/560), [FPGA-based FX2](/doc/product/565) 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;It is recommended that you create an instance using a current-generation instance type to achieve optimal performance. For more information, please see [Instance Types](/doc/product/213/7153).

>Note:
>Series and models vary with different areas and availability zones.

Click **Next Step: Select Image** button to enter the image selection page.

<div id="page3"></div>
## Selecting an Image
![](//mc.qcloudimg.com/static/img/56c4ecbdb12dd0a366ecf701153fce1d/image.png)
 1. Select an image provider.
Tencent Cloud supports public images, custom images, shared images and service marketplace images. Select one by referring to [Image Types](/doc/product/213/4941) document.
We recommend that users who have just started using Tencent Cloud select public images, which contain legitimate Windows operating system. You need to build subsequent operating environment on your own.

 2. Select an operating system: Windows Server.
 
 3. Select a system version.
-  The system contains legitimate activation key at no extra charge (except for the North America region). 
-  Suitable for running programs developed under Windows, such as .NET. 
-  Support SQL Server and other more databases (you need to install it yourself). 

Click **Next Step: Select Storage and Network** button to enter the storage and network selection page.

<div id="page4"></div>
## Selecting Storage and Network
![](//mc.qcloudimg.com/static/img/e95a5bf7bf47c60f43dd0ee62946b67a/image.png)
 1. Select the type of disk and the size of data disk.
Tencent Cloud provides cloud disk and local disk. (System disk size is optional. Default is 50 GB.)
- Cloud disk: Deliver high data reliability with the distributed three-copy mechanism.
- Local disk: A storage located on the physical machine where the CVM resides in, which allows low latency but may cause single point of failure risk. For the comparison, please see [Product Category](/doc/product/362/2353#.E5.90.84.E7.A7.8D.E5.9D.97.E5.AD.98.E5.82.A8.E8.AE.BE.E5.A4.87.E7.9A.84.E5.AF.B9.E6.AF.94).

 2. Select a network type.
Tencent Cloud provides two network types: basic network and VPC.
- Basic network: Suitable for new users. CVMs of the same user are interconnected via private network.
- VPC: Suitable for advanced users. Different VPCs are logically isolated from each other.

	>**Note:**
	> Windows CVM cannot be used as [Public Network Gateway](/doc/product/215/%E7%BD%91%E5%85%B3#1.-公网网关). Users who need public network gateway can refer to [Quick Start for Linux CVM](/doc/product/213/2936).

 3. Select public network bandwidth.
Tencent Cloud provides two options: Bill-by-bandwidth or Bill-by-traffic.
- Bill-by-bandwidth: Select a fixed bandwidth. Packet loss occurs if this bandwidth is exceeded. This is suitable for scenarios with minor network fluctuation.
- Bill-by-traffic: The service is charged based on actual traffic usage. You can set a limit for peak bandwidth. Packet loss occurs when the instantaneous bandwidth exceeds this limit This is suitable for scenarios with large network fluctuations.

 4. Select quantity.

 5. Select usage period and renewal method (only for Prepaid CVMs).

Click **Next Step: Set Information** button to enter the information setting page.

<div id="page5"></div>
## Setting Information
![](//mc.qcloudimg.com/static/img/fbc4230b5e6a19ef6ec60ffebfc62aaa/image.png)
 1. Set CVM name: You can choose "Name It after Creation" or "Name It Now".

 2. Set login information: You can set a password or use a system-generated password. The password you set can be modified after creation of CVM, the system-generated password is sent to you via internal message.

 3. Select security group (**Make sure that the login port 3389 is enabled**. For more information, please see [Security Group](/doc/product/213/%E5%AE%89%E5%85%A8%E7%BB%84)).

Click **Buy Now** button to complete the payment before you can log in to the [console](https://console.cloud.tencent.com/cvm) to check your CVM.

After the CVM is created, you will receive an internal message containing instance name, public IP address, private IP address, login name, initial login password, and other information. You can use these information to log in to and manage your instance. To ensure the security of your CVM, change your Windows login password as soon as possible.

Click [here](/doc/product/213/2764#.E6.AD.A5.E9.AA.A4.E4.B8.89.EF.BC.9A.E7.99.BB.E5.BD.95-windows-.E4.BA.91.E6.9C.8D.E5.8A.A1.E5.99.A8) to complete subsequent configurations, including logging in to Windows CVM, formatting and partitioning data disk.

