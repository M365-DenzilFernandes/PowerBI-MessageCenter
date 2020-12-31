# PowerBI-MessageCenter

A Power BI Report to connect to the Office 365 Service Communications API

This report contains a data query which connects to the Office 365 Service Communications API and query the following from the API:

* Get Current Status: Get current service status including any incidents
* Get Messages: Get Incidents, Planned Maintenance, and Message Centre communications.
* Get Services: Get the list of subscribed services

<img src="https://github.com/M365-DenzilFernandes/M365-MessageCenter-PowerBI/blob/main/PBI-MessageCenter-1.png"  style="max-width:100%;">
<img src="https://github.com/M365-DenzilFernandes/M365-MessageCenter-PowerBI/blob/main/PBI-MessageCenter-2.png"  style="max-width:100%;">


# How-To Use?
* Download the report and update the queries (i.e. O365Token, CurrentStatus, MessageCenter, Services. Incidents)
* You only need to update the tenant id, client id and client secret where applicable. 
<img src="https://github.com/M365-DenzilFernandes/M365-MessageCenter-PowerBI/blob/main/PBI-MessageCenter-3.png"  style="max-width:100%;">

#Azure AD App Registration
* If you want to connect this report to your own tenant, you will need to create an app registration and grant it the following API Permissions

