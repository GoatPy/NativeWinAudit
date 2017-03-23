Welcome to Project Sauruon. The purpose of these project is to provide organisations without access to expenseive SEM/SIEM platforms to export event log audit data from multiple Windows machines to a central location. Also ideal for deployment in UAT/DEV/TEST environments to allow collection of events. The demonstration example which began this project was to provide a process to allow Domain Controllers to centrally store the audit events they generate for future referral and lookups.

The 3 core components can be leveraged to allow you to build your own solutions as well. 
  Custom View Creation - Create a custom view tree that allows you to easily extract specific events 
  Manifest Creation - Creates an event channel manifest file for .dll compilation to create dedicated event channels (logs) for storage of events in management .evtx files
  Subscription Creation - Creates the windows event collection subscription files to forward and store events in the appproiate log file.

Getting Started - Domain Controller Events 
A Pre-Built version of the Manifest and DLL is available and directly matches up to the provided Custom Subscriptions, Custom Views and export scripts. Refer to the following blog post for more details
http://blogs.technet.microsoft.com/russellt/2017/03/23/project-sauron-part-1

1. Create or use an existing import csv to definie the custom event channels and xPath queries
2. Compile a new or reuse an existing .manifest and .dll file to define the custom event channels
3. Load the custom events channel .manifest and .dll into your Windows Event Collector
4. Load your the correspondign WEC subscriptions into the central Windows Event Collector Server
5. Configure the machines to pull subscriptions from the WEC Subscription server
6. Refer to the event logs 

Domain Controller Event Data Sources
Account Management https://technet.microsoft.com/en-us/library/dd941622(v=ws.10).aspx
Audit Security Group Management https://technet.microsoft.com/en-us/library/dd772663(v=ws.10).aspx
Audit User Account Management https://technet.microsoft.com/en-us/library/dd772693(v=ws.10).aspx
Audit Security Group Management https://technet.microsoft.com/en-us/library/dd772663
Audit Other Account Management Events https://technet.microsoft.com/en-us/library/dd941586(v=ws.10).aspx
Audit Distribution Group Management https://technet.microsoft.com/en-us/library/dd772713(v=ws.10).aspx
Audit Computer Account Management https://technet.microsoft.com/en-us/library/dd772717(v=ws.10).aspx
Windows security audit events https://www.microsoft.com/en-us/download/details.aspx?id=50034

Contribute
Got an idea for a new Channel/Subscription/View? Leave a comment on the repository
