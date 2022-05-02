
# Option 1 - PowerBI-MessageCenter

A Power BI Report connected to the Graph API. 
Note: The data connection is set to Anonymous and the queries contains the HTTPS POST/GET request to authenicate with the TenantId/ClientId/ClientSecret 

This report contains a data query which connects to the Graph API and query the following from the API:

* Get Announcements Status: Get Incidents, Planned Maintenance, and Message Centre communications.
* Get Issues: Get current service status including any incidents.
* Get HeathOverview: Get the list of subscribed services.
* Source https://docs.microsoft.com/en-us/graph/service-communications-concept-overview
<img src="https://github.com/M365-DenzilFernandes/M365-MessageCenter-PowerBI/blob/main/PBI-MessageCenter-1.png"  style="max-width:100%;">

## How-To Use?
* Download the report and Refresh the report to download the latest messages from Microsoft 365 Admin Message Center.
* Update the Tenant ID, Client ID and Secret ID variables in the PBI Query.
* [Download the v3.0 PBIX report](https://github.com/M365-DenzilFernandes/PowerBI-MessageCenter/raw/main/Microsoft365AdminCenter-MessageCenter-Public-v3.0-Direct.pbix) 
* Right Click any Message to drill through the Message Details.
<img src="https://github.com/M365-DenzilFernandes/M365-MessageCenter-PowerBI/blob/main/PBI-MessageCenter-2.png"  style="max-width:100%;">


## Azure AD App Registration
* If you want to connect this report to your own tenant, you will need to create an app registration and grant it the following API Permissions.
* Add an Application Permission to Graph API's and Select ServiceMessage.Read.All + ServiceHealth.Read.All - Admin Consent Required.
<img src="https://github.com/M365-DenzilFernandes/PowerBI-MessageCenter/blob/main/PBI-MessageCenter-4.png"  style="max-width:100%;">

* [Download the PBIX report](https://github.com/M365-DenzilFernandes/PowerBI-MessageCenter/raw/main/Microsoft365AdminCenter-MessageCenter-Public.pbix) and update the queries (i.e. O365Token, CurrentStatus, MessageCenter, Services. Incidents).
* You only need to update the tenant id, client id and client secret where applicable.
<img src="https://github.com/M365-DenzilFernandes/M365-MessageCenter-PowerBI/blob/main/PBI-MessageCenter-3.png"  style="max-width:100%;">

# Option 2 - PowerBI-MessageCenter v3.0 
A Power BI Report to connect Service Communication API data stored in SharePoint Online. This requires the implementation of a Flow with premium connector to get data from the tenant.

## How-To Use?
* [Download the Power Automate flow](https://github.com/M365-DenzilFernandes/PowerBI-MessageCenter/raw/main/PBI-ServiceCommunicationstoTextFile%5BExport%5D-v3.0.zip) and import into your environment. 
* Update the Tenant ID, Client ID and Secret ID variables in the flow.
* Update the SharePoint Site destination to store the files.
* [Download the v3.0 PBIX report](https://github.com/M365-DenzilFernandes/PowerBI-MessageCenter/raw/main/Microsoft365AdminCenter-MessageCenter-Public-v3.0.pbix) and update the connections to use your SharePoint Online path. 
* Published the report to PBI Online/Workspace. Set Automatic Refresh

