## Exercise 1
In this exercise, we will deploy the OneAgent to a Linux instance and let the OneAgent discover what is running in that instance.

### 1. Download the OneAgent

Select Deploy Dynatrace from the navigation menu.

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/101-DeployDynatrace.jpg)

Click the Start installation button and select Linux.

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/102-StartInstallation.jpg)

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/103-Linux.jpg)


Choose the installer type from the drop-down list. Use the Linux shell script installer on any Linux system that's supported by Dynatrace, regardless of the packaging system your distribution depends on.

**Copy** the command provided in the "Use this command on the target host" text field. **Paste** the command into your terminal window and execute it.

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/104-Download.jpg)

### 2. Execute the installation script

(Optional) Once the download is complete, you can verify the signature by copying the command from the "Verify signature" text field, then pasting the command into your terminal window and executing it. Make sure your system is up to date, especially SSL and related certificate libraries.

**Copy** the command that's provided in the text box "And run the installer with root rights" text field.

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/105-Install.jpg)

**Paste** the command into your terminal window and execute it. You’ll need to make the script executable before you can run it.

**Note that you’ll need root access.**  You can use su or sudo to run the installation script. To do this, type one of the following commands into the directory where you downloaded the installation script.

```bash
su -c '/bin/sh Dynatrace-Agent-Linux-1.0.0.sh'
```

### 3. Validate the installation in Deployment status

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/106-Status.jpg)

Reference: https://www.dynatrace.com/support/help/technology-support/operating-systems/linux/

### 4. Start Easy Travel application

Use PuTTy (Windows) or Terminal (Mac), ssh into the instance (IP address provided to you, please check your email)

```bash
login: perform
password: perform
```

Execute the command

```bash
$ ./starteasytravel.sh
...
--> Deploying template "easytravel/easytravel-with-loadgen" for "easytravel-with-loadgen.yml" to project easytravel

     easytravel-with-loadgen
     ---------
     The Dynatrace easyTravel sample application (with UEM loadgen).

--> Creating resources ...
    deploymentconfig.apps.openshift.io "mongodb" created
    deploymentconfig.apps.openshift.io "backend" created
    deploymentconfig.apps.openshift.io "frontend" created
    deploymentconfig.apps.openshift.io "www" created
    deploymentconfig.apps.openshift.io "loadgen" created
    service "mongodb" created
    service "backend" created
    service "frontend" created
    service "www" created
    route.route.openshift.io "www" created
--> Success
    Access your application via route 'www-easytravel.<your public ip>.nip.io'
    Run 'oc status' to view your app.

```

Wait about 5 mins to access the Easy Travel, copy the URL shown to you:

**PICTURE Goes here!**

If you need the URL again, execute the command

```bash
$ ./showurl.sh
Easytravel URL: www-easytravel.<your public ip>.nip.io
```

### 5. Explore the Smartscape

While waiting for Easy Travel to start, you can explore Dynatrace and using the Smartscape, Dynatrace will automatically discover the processes and dependencies that comprises the Easy Travel application! 

[4 things](https://www.dynatrace.com/support/help/get-started/4-things-youll-absolutely-love-about-dynatrace/) that you will love about Dynatrace!

![Smartscape](https://dt-cdn.net/images/smartscape-horizontal-topology-2-860-6bdf46eb74.png)

---

:arrow_forward: [Next exercise: Exercise 2](/ex2)

:arrow_up_small: [Back to overview](https://github.com/performgohot19/DEM)
