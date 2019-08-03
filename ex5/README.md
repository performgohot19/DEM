## Exercise 5
This is an **optional** exercise.

Dynatrace captures detailed user session data each time a user interacts with your monitored application. This data includes all user actions and high level performance data. Using either the Dynatrace API or Dynatrace User Sessions Query Language (USQL), you can easily run powerful queries, segmentations, and aggregations on this captured data. 

User Sessions Query Language isn't SQL and Dynatrace doesn't store user session data in a relational database. User Sessions Query Language is a Dynatrace-specific query language, though it does rely on some SQL concepts and the syntax is similar, which makes it easy to get started.

A typical use case for using USQL is to build dashboards to visualize business metrics.

![USQL](https://github.com/performgohot19/DEM/blob/master/assets/500-USQL.png)

Reference: https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/how-to-use-real-user-monitoring/cross-application-user-session-analytics/custom-queries-segmentation-and-aggregation-of-session-data/

### 1. Start Easy Travel load gen

### 2. Explore USQL

1. Select User Sessions from the navigation menu
2. Use the Filter at the top bar, select your application's name 
3. Click on "User Session queries"

   ![USQL](https://github.com/performgohot19/DEM/blob/master/assets/502-USQL1.png)

4. A default USQL query is automatically created for you based on the application you selected

   ![USQL](https://github.com/performgohot19/DEM/blob/master/assets/502-USQL2.png)

Sample queries

```
SELECT DATETIME(starttime, 'MM/dd/yyyy hh:mm', '30m'),AVG(useraction.visuallyCompleteTime)
FROM usersession
WHERE country IS "United States" GROUP BY DATETIME(starttime, 'MM/dd/yyyy hh:mm', '30m’)
```

```
SELECT userId, SUM(totalErrorCount) FROM usersession
WHERE totalErrorCount IS NOT NULL
GROUP BY userId ORDER BY SUM(totalErrorCount) DESC
```

```
SELECT COUNT(*) FROM usersession WHERE useraction.name = "Loading of page /orange.jsf"
```

---
:arrow_up_small: [Back to overview](https://github.com/performgohot19/DEM)
