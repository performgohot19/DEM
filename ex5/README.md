## Exercise 5
This is an **optional** exercise.

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
