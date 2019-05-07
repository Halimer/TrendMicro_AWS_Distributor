# Deploy Deep Security Manager Agent with AWS System Manager Distributor

## Overview
AWS Systems Manager Distributor is a feature that you can use to securely store and distribute software packages, such as software agents, in your accounts. Distributor integrates with existing Systems Manager features to simplify and scale the package distribution, installation, and update process.

One common agent that is deployed is a security agent.  Trend Micro Deep Security is a host-based security product that provides Anti-Malware, Host Firewall, Intrusion Prevention, File Integrity Monitoring, Log Inspection, Web Application Firewalling, and Content Filtering modules in a single agent running in the guest operating system.  
### Creating and Distributing the Package

1. Go to [Systems Manager/Distributor - AWS Console](https://console.aws.amazon.com/systems-manager/distributor)

2. Click **Create Package**

![](https://github.com/Halimer/wiis_dallas/blob/master/images/distributor.png)

3. Under Name enter **WIISAgent**.

4. For S3 bucket URL enter **https://s3.amazonaws.com/wiis-dallas/**.

5. Leave everything else as the defaults.

6. Click **Create Package**
![](https://github.com/Halimer/wiis_dallas/blob/master/images/create_package.png)

7. It will take a couple of minutes to create the package.  Click the refresh button on your browser until the **Install One Time** button is visible at the top.  Once visible, click it to install.
![](https://github.com/Halimer/wiis_dallas/blob/master/images/install1.png)

8. Scroll down until you see **Target Instances**.  Select the check box next to the instance to select it.  The press **Run** at the bottom.

![](https://github.com/Halimer/wiis_dallas/blob/master/images/run.PNG)
![](https://github.com/Halimer/wiis_dallas/blob/master/images/run2.PNG)
![](https://github.com/Halimer/wiis_dallas/blob/master/images/run3.PNG)

9. Use the refresh button at the top and wait until you see the status change to 'Success'

![](https://github.com/Halimer/wiis_dallas/blob/master/images/run4.PNG)

10. Go back to your DSM console to see that the agent now shows Managed.

11. **Optional** - If you have time, proceed to the [Extra Credit Lab](https://github.com/Halimer/wiis/tree/master/Lab_Extra_Credit)

12. Proceed to the [Lab Cleanup](https://github.com/Halimer/wiis_dallas/tree/master/AWS_Lab_Cleanup).

