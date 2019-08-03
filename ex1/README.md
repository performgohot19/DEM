## Exercise 1
In this exercise, we will deploy the OneAgent to a Linux EC2 instance and let the OneAgent discover what is running in the EC2 instnace.

### 1. Download the OneAgent

Select Deploy Dynatrace from the navigation menu.

Click the Start installation button and select Linux.

Choose the installer type from the drop-down list. Use the Linux shell script installer on any Linux system that's supported by Dynatrace, regardless of the packaging system your distribution depends on.

Copy the command provided in the Use this command on the target host text field. Paste the command into your terminal window and execute it.

### 2. Execute the installation script

Copy the command that's provided in the And run the installer with **root rights** text field.

Paste the command into your terminal window and execute it. You’ll need to make the script executable before you can run it.

**Note that you’ll need root access.**  You can use su or sudo to run the installation script. To do this, type one of the following commands into the directory where you downloaded the installation script.

```bash
su -c '/bin/sh Dynatrace-Agent-Linux-1.0.0.sh'
```

### 3. Validate the installation in Deployment status

Reference: https://www.dynatrace.com/support/help/technology-support/operating-systems/linux/

Go to [Exercise 2](/ex2)
Return to [main menu](/)
