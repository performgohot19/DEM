## Exercise 2
In this exercise, we will cover the basics of configuring Real User Monitoring. These are some of the best practices that should be followed every time the Dynatrace JavaScript agent is deployed, be it an automated or manual injection. 

More information can be found here: [How to use Dynatrace > Real User Monitoring > Setup and configuration > Web applications](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/setup-and-configuration/web-applications/)

### 1. Defining an application

Reference: https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/setup-and-configuration/web-applications/initial-configuration/define-your-applications-via-the-my-web-application-placeholder

1. Select Applications from the navigation menu.
2. Click the My web application placeholder application.
3. Scroll down to find the Top 3 included domains panel. This panel includes the domains that contain the largest number of actions that have been automatically detected by OneAgent in your environment.
4. Click View full details.

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/201-Define.png)

5. Select a domain from the list appearing under Top domains and expand it by clicking the arrow under Transfer domain.
6. Click Create new application. Your application will be created and listed on the Applications page. From now on, all user actions that are monitored on this domain will be mapped onto the newly created application. Alternatively, you may want to add the domain to an existing application, in case some applications have already been created. To do this, expand the list box, select an application and click Transfer.

![Deploy](https://github.com/performgohot19/DEM/blob/master/assets/201-Create.png)

As you may want to use a more intuitive name for your application, you can easily rename it. To rename an application:
1. Select Applications from the navigation menu.
2. Click your newly created application to access the application's overview page.
3. Click the Browse button (...) and select Edit.
4. Type in the name you prefer in the text box appearing on top of the page. Note that application names must be unique.

### 2.

### 3.

---

:arrow_forward: [Next exercise: Exercise 3](/ex3)

:arrow_up_small: [Back to overview](https://github.com/performgohot19/DEM)
