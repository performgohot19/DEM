## Exercise 3
In this exercise, we will cover creating a single URL synthetic test in Dynatrace. Dynatrace offers three types of synthetic monitoring: single-URL browser monitors, browser clickpaths, and HTTP monitors.

More information can be found here: [How to use Dynatrace > Syntheic Monitoring](https://www.dynatrace.com/support/help/how-to-use-dynatrace/synthetic-monitoring)

### 1. Create two simple browser monitors for Easy Travel

1. Select Synthetic from the navigation menu.
2. Click the Create a synthetic monitor button at top right.
3. Click Create a browser monitor.
4. On the Configure a synthetic monitor page, type in the URL of your Easy Travel application and either use the default Name or provide your own.
5. For Device profile, leave it as the default (i.e. Desktop)
6. For Frequency, select 5 mins
7. Use the following 3 locations
   * Sydney
   * Singapore
   * Malaysia

### 2. (Optional) Create a browser clickpath synthetic monitor for Easy Travel

**You will need to install the Dynatrace recorder (chrome plugin)**

**Only Chrome is supported due to the requirement for a plugin**

1. Select Synthetic from the navigation menu.
2. Click Create a synthetic monitor > Create a browser monitor.
3. First-time users are asked to install the Chrome plugin. Click Install Dynatrace recorder at the bottom of the page.
4. On the extension page, click Add to Chrome > Add Extension.

Reference: https://www.dynatrace.com/support/help/how-to-use-dynatrace/synthetic-monitoring/browser-monitors/record-a-browser-clickpath/

---

:arrow_forward: [Next exercise: Exercise 4](/ex4)

:arrow_up_small: [Back to overview](https://github.com/performgohot19/DEM)
