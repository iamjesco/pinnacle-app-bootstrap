# FEATURE

A visualizer/monitor for the Alerts API

### PROBLEM STATEMENT

A new Alerts API has been created to communicate alerts from services such as the Transaction Limit Engine and the Risk Score Provider. We need a monitor to allow operational teams to view, filter, order and search these alerts

### REQUIREMENTS

* The alerts monitor should show each alert on a separate row
* The alerts monitor should allow the customer to have a Live Mode or a Review Mode
* The alerts monitor should allow for new alerts to added to the grid in real time (via subscription to the API) if the user chooses to have Live Mode Enabled
* The alerts monitor should allow the user to choose how many hours back they can see alerts for while in Live Mode
* The alerts monitor should start up with a default of one hour of alerts visible
* The alerts monitor should display the following information on an alert:
```
- Customer ID
- Alert Category
- Alert Name (alert code description)
- Status
- Alert Priority
- Customer License ("license" field from API)
- Description (Any additional info passed with the alert - may vary depending on alert type but could include Transaction ID for payment based alerts. Could have a null value)
- Date/Time Created
- Created By
```
* The Customer ID should be a clickable link to open that customer in a new tab in the Customer Monitor
* By default, alerts should be ordered by Date/Time Created, newest to oldest so that the newest alert is at the top
* The alerts monitor content should be possible to filter in the following ways:
```
- Filter by Customer ID (complete match) - When filtering to single customer, data range should be ignored and show full history of alerts
- Filter by Date/Time Range - preset ranges of 1 hour, 6 hours, 24 hours, 7 days, one month and custom range (maximum of one year)
- Filter by Alert Category (dropdown list of available values on API) - MULTISELECT
- Filter by Alert Priority (dropdown list containing "Normal", "Important" "Attention" and "Urgent")- MULTISELECT
- Filter by License (dropdown list corresponding to our license list)
```


